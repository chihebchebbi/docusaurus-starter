![](https://lh6.googleusercontent.com/SYRC6jwuYiAzYR1fMO1rqy1kdIf-sWnNh8eeAbM0RSn8nvdXaKtKf27lELOzl7kqQfh6absOzaTAwTnizodN3-adLxJQAZHN05NS5ilUZANUPNmP9-mfJ5RILTPD1FbB17z0_mTfvsishEtiUXddaA)

Linux is one of the most known and used Operating systems. In this post, I am going to explain the required steps to develop a Linux Kernel Module (LKM)
For the demonstration, I am going to use a Ubuntu 14.04 server hosted on Microsoft Azure.

![](https://lh4.googleusercontent.com/YaTL4ttWOUG0sCzg4k_8OK8G1iD7X-lF-G16seeZ3Akoi6ZbcURShY7gApeTN5NTFBuoXyVr7DvD56DcOZMD13e7AU1aRnI5tf824EgSI0GV8YIE--T5VN1IFB9ehIamo07q1lVnucwGjlOxLAqg_Q#logo)

First you need to prepare the environment and make sure that you installed "build-essential" 
sudo apt-get install build-essential

![](https://lh5.googleusercontent.com/4DyftfDAvns11ckIltpXqN00B-6pq3dtxaBmDJ4UDXRpOd0G3uVtBdj11ZLcJzQLWMg3Fa_ScRG69lD-8UdiJJUXj2GR-asI2FQTZriT1IRi4LISt6k3106NylYyy-Te8LwJ0wzPtkI4mSU9Y_3PcA)

![](https://lh6.googleusercontent.com/T2GuuG-U06IUe0Na2J9O5gUIMlNLh2opGCMoJQPuC7IU-r2Np2oh-w0pkdBJPwfJ8YK8_iu70CEFgIdiC2PCReSf5wMZpuBm-G8exIL4Jtgw-FsJfUbbnuK7pjYWVdr8vd1u9REfUloESVCqbTriyA)
Install the "Linux headers"
sudo apt-get install linux-headers-'uname -r'

![](https://lh3.googleusercontent.com/nw13ByzBI8UMHNEAEtOEe_XxVICj9nJ-l2PcdHoaM34br9pAfPv2kgHER4uFMs7DJ8XVPvaEpe72oAwsVFWGcrYoiuDOPaKN8yyh9XHX4_Mb6mNs9qQ73IARrzQIjISPG8wkifofzgOGwSDr5zrWEg)

Enter /usr/src and create a c file and insert the following code:

![](https://lh3.googleusercontent.com/0Dig5I41xlslbXKQLsfVW_18qNF6gyMqVVVfFbdSkGE56C4bCewI3yLSA_JrVMt7booOeE2Z4hupvQblV0RjyolZin17bUxi3jygveLHYUzZqLZTNV8iGAgkgjS7ggJZ9sy7BVYntclG7fl7PtR_Ow)

Name it linux_module.c
#include <linux/init.h>
#include <linux/module.h>
#include <linux/kernel.h>
MODULE_LICENSE("GPL");
MODULE_AUTHOR("Chiheb Chebbi");
MODULE_DESCRIPTION("This is a Demo for a Linux module.");
MODULE_VERSION("0.01");
static int __init linux_module_init(void) {
 printk(KERN_INFO "Hello, Peerlysters!\n");
 return 0;
}
static void __exit linux_module_exit(void) {
 printk(KERN_INFO "Goodbye, Peerlysters!\n");
}
module_init(linux_module_init);
module_exit(linux_module_exit);
for the demo, I used "vi" . As you can see from the c program, Linux kernel modules usually include 2 elements: init(constructor)and exit(destructor). In addition of the Module information (LICENSE, DESCRIPTION and so on) we simply used a print command to result "Hello Peerlysters!" when the module is deployed into kernel address space.

![](https://lh6.googleusercontent.com/-nJrOj1vKpkX5VSIuNjHllBSYbnRedoze5raNtAg_AawVyiZnBiAo0W2CjkfYEQAn7qzbJCbTptr-7VCrXltWac8AibTx1WOd2c6GUSDhbzqXeGUrbZYZfhJQRfKlsO8IZFmZ7b6HPFH1M1TK2T8mA)

Create a makefile (use Tabs before make instead of spaces): 
obj-m += linux_module.o
all:
 make -C /lib/modules/4.15.0-1031-azure/build M=/usr/src/ modules
clean:
 make -C /lib/modules/4.15.0-1031-azure/build M=/usr/src/ clean
 
 ![](https://lh4.googleusercontent.com/aTWaQhyTzKxWbt6335nZFZUparaTe-5HKeZJd9rBQFBMSvbpwHoqwz0AKJt-EbJ3LJsUcN1D0kgaJlpwieq80P7NkNekdROkDrmAG1TAfoNUu3XsEhwTYHCAxXddJqcmzbngz6BrPRl9VV4Wnra7Pg)
 

Your module will be compiled successfully

![](https://lh4.googleusercontent.com/6kXWgUN6iLCCdSr1y5M9Wpti0UxGIOJn7GyHCb-SF5XfGMm3uv_sjFH-j20oFZ7N11i83Pv2dfHnP5EDR1UTkMnepxqTGW2ovNxeZbxfucCiycK8vxTQxChPFeXUpjGYL2rWxwzAUe97Qy58allgvg)

To add it you just need to use insmod


sudo insmod linux_module.ko

![](https://lh3.googleusercontent.com/pL12DGRJSNSIHX7Nfn-N4vvOH6E2LHYcu7sJfSEx4k4RYxgklvF4M3h-hMWy0TPlMyRn619DByMcjxho4qaQUI9IYQ2VFxqyGX4c_t5rQdQWkSa5Zc-FPE86w8X305Fq7U4h6SyxWDyJnEvaAFSdYA)

To check the message "Hello Peerlysters!" run dmesg

sudo dmesg

![](https://lh5.googleusercontent.com/dla__bc4pkIJomgjh2T9J9sdohtdH0UjBIo1gZfXBpqJsxdKZCVee9I4eXkqUS8hDC7taVH0BLU-Op-jYpxzQeqaKQ6IAONwzKxmHitDRQhfV1YCOZ_--k2IiSHQt300jipUOInYA0LsLHBTV8aVfQ)

By now you learned the required steps to build a simple Linux Kernel Module (LKM)
Further readings:
https://blog.sourcerer.io/writing-a-simple-linux-kernel-module-d9dc3762c234
http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction/
Mastering Linux Kernel Development

