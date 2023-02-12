# A Detailed Guide on Nmap  
![](https://lh4.googleusercontent.com/5RUsrhZcIKE3Opau3EeXah4s86grFXZcTVw2FiG0kqoKTl--gbXwff6uehQSAGEoBvoT8pi1sK1F75u2CvjK-xb93CbYOhcLdvBHSZiC6ZmapTAps76PcD_FCXBq9EcpGhqSToqmJsWZ0idNI9Wfow)

Image source:[Cover](https://www.belden.com/hs-fs/hubfs/cyber-security-microsite-4.jpg?width=978&height=450&name=cyber-security-microsite-4.jpg)

In information security, "Information changes situations". In other words, collecting information and reconnaissanceis an important step in cybersecurity. It doesn't matter if you are sponsored state black hat hackers or pentesters and red teamersyou need to collect heavily every publicly or privately available information about the target organization. Once you have useful pieces of information you need to move on to the next step which is scanning. It is one of the most important operations in information security. It is gathering information about the connected devices in a specific network. In this guide, i want to take the opportunity to help you acquire a fair understanding of one of the most well-known network mapping and scanning tool. It is the famous "Nmap" weapon. This detailed guide is going to discuss the following points:

- What is network scanning
- Nmap Project
- How to install Nmap
- Targets
- Ports
- Service and version detection
- OS Detection
- Timing
- Nmap scripts
- Outputs

## What is Network Scanning?  

If you are familiar with my articles you will notice that before diving deep into the technical details i always try to start from the required basics and fundamental terms. First, let's explore where do you need "network scanning". Hacking (Black or white) goes through a methodological flow. Mostly, you need to follow these steps:

- Reconnaissance and information gathering
- Scanning
- Gaining access
- Maintaining access
- Clearing tracks

Network scanning can be found in the Scanning step. It is important to learn the difference between scanning and enumeration.

**Nmap Project**

![](https://lh5.googleusercontent.com/LVCMHgKFOdnvr1sQkXP1viqzQ3XiXg_OUr1Tv3ssp9uEvW1RtcDBcDz8h7OgvAYkP2aT7fQgPOGQjkeNVjbMfBKFPSzBDytsh2nQf4TNwA1BQlHuPo8W9we1-wcoRHHhWkvmPbjWG5w2dh5j-6_JQg#logo)

Image source: [Nmap logo](https://i0.wp.com/gbhackers.com/wp-content/uploads/2017/06/top.ten_.tools_.nmap_-768x432.png?fit=768%2C432&ssl=1)

As a real-world demonstration to learn how to scan networks we are going to discover Nmap. The project's [founders](https://nmap.org/) describe it as the following:

"Nmap ("Network Mapper") is a free and open source utility for network discovery and security auditing. Many systems and network administrators also find it useful for tasks such as network inventory, managing service upgrade schedules, and monitoring host or service uptime. Nmap uses raw IP packets in novel ways to determine what hosts are available on the network, what services (application name and version) those hosts are offering, what operating systems (and OS versions) they are running, what type of packet filters/firewalls are in use, and dozens of other characteristics. It was designed to rapidly scan large networks, but works fine against single hosts. Nmap runs on all major computer operating systems, and official binary packages are available for Linux, Windows, and Mac OS X."

**How to install Nmap?**

For the hands-on explanation, i am using a Debian machine. Thus, the installation will be easy. You just need to run (after updating the system):

apt-get install nmap

![](https://lh3.googleusercontent.com/-OSvBng1vLOWhfv7-d-b-EGTdlySfeFWQApv7D7EuB3VFP_ao7yof_nIC4ZipUZvDtV98GjiUxSxr51vtkwxhZ6JEA-fJD8agdmATTgl1FuL7NAYOT7GEu6JiUnerCTfJ_xtEJEG5BGwIQdx8VYvxw)

Voila! You installed nmap easily. To run it just type:

Nmap \<options\> \<target\>

![](https://lh6.googleusercontent.com/it3dU-Dpr3_YUGfqXeUIvlC-GYiJd9Bil1Z62JtE59gpM1vDC1-XJsJPG3XW8LnCYAfdPMmdUv0A7nQGWoNnevG6V-nbPkujbU_CprUNLDBUlglMgAap1O2l5iiJj4xXs9b2hoTWctJf1d-4Azx86Q)

You can install it for sure on many other different operating systems such as Windows.

Now, let's explore the power of Nmap. The first thing we are going to try is of course "Host Discovery"

As a target i am going to attack/scan an online vulnerable machine called "[Metasploitable 2](https://information.rapid7.com/download-metasploitable-2017.html)" developed by Rapid 7 and hosted on an amazing platform called "[root-me.org](https://www.root-me.org/)"

Usually, we use an ICMP echo request to discover if a host is up or down (ping command as an utility for example). To discover live hosts with nmap type:

nmap -sn -PE -Pn 212.129.29.185

![](https://lh5.googleusercontent.com/Dmxb4DMTkU4rVQvmNSZ9-v0jsUOBICpw8QBFTzBXPfqfpuZckY7l-Ytz_rPyw4dB2RNOJNYTXz1HtMhNexg-T-pJ8Xe3FRV6hOgEAehvPbdCV5Ts0RxBs_HKws86n9szIQpwn9YjWdneqqmXD1DzQg)

Our target is up!

**Targets**

In your network scanning missions, you are not going to scan only one host (IP address) but usually you need to scan ranges and many IP addresses. Nmap gives you the ability to do so by offering many easy options and techniques. For example to scan a range you can use the following trick

nmap 10.0.0.2-254

It scans 10.0.0.2 to 10.0.0.254

You can also use wildcards (\*)

Nmap 10.0.0.\*

Or even subnets:

Nmap \<IP\> /24

If you want to scan a list of IP addresses from a text file for example this file:

![](https://lh6.googleusercontent.com/yM9U1ENn0FnhF1BCauKZC54_LhktRTZmGxSJ3eEedKf0k08qlVaLs6s3kgW8WS7McBCi01KYRs-WZBOC1aEpQxQlVllj4uy59VnR3_084Xvjv3osCzcu-QoM6UVk1Xlz81PF8EOIdIpzCu-X9ZKQ3g)
You need to use the 'iL' option

nmap -iL targets.txt

![](https://lh5.googleusercontent.com/FaCjk1NrasDHWQrcFHqXNncIBHULPA7vmza9x44EAcptF9mY9IBhx9kziB3-45A2_-sak1sPumR2Ej5_pFJxEnEOa3GTQ0F31bTvcuefhvp0dKq_8z3wk3whlxypyf_CgZyJanuB1wTccwiaFdXbOg)

To select random targets you can use the -iR option

Nmap -iR \<num hosts\>

To exclude a host you can type

nmap --exclude \<host1\>

To scan a target with a specific network scanning technique (discussed in the previously discussed article) you need to use these commands:

- Ping: nmap -sP IP Address Here\>
- Full scan : nmap -sS \<Target IP Address Here\>
- FIN scan: nmap -sF
- XMAS scan: nmap -sP \<Target IP Address Here\>
- NULL scan: nmap -sN \<Target IP Address Here\>
- UDP scan: nmap -sU

**Port status**

By now, i bet you are wondering, "_emm i am scanning networks but what information i need to perform an attack?_"

You are right!

When performing network scanning in most cases we are looking for open ports. According to Wikipedia:

"In computer networking, a port or port number is a number assigned to uniquely identify a connection endpoint and to direct data to a specific service. At the software level, within an operating system, a port is a logical construct that identifies a specific process or a type of network service."
Usually, port numbers are connected (logically) with specific services. Many ports are already reserved for some [specific services](https://www.utilizewindows.com/list-of-common-network-port-numbers/).
There are many port status that are described in details on the official [documentation](https://nmap.org/book/man-port-scanning-basics.html):

- Open
- Close
- Filtered
- Unfiltered
- Closed/filtered
- Open/filtered

**Service or version detection**

Let's find out what are the open ports on our target metasploitable. BTW, you can download the "[Metasploitable 2](https://metasploit.help.rapid7.com/docs/metasploitable-2)" on a VM and practice with it directly on your computer.

Let's run a service detection command with "sV" option

nmap -sV 192.168.1.108

The following screenshot illustrates all the open ports including the running services on the target

![](https://lh4.googleusercontent.com/8KqmhIEdKR10Tl4Y-Cb7BOXBInYBU4t2YkJ8N1w6Mv3WxGpYLdqtdCWYCqUNaFeHqfQmi8B473oK2lF6yQ0qAGa_YF2WfUBDZCuBUmSZSMLfWg6lHaaXoFUX6NZHcK_qHbA8Yl6Z2OSY4g73-pLIvg)

To collect more and detailed information about the services add "-v" option.

![](https://lh5.googleusercontent.com/5myoCdbUdKKAEE_-cyvtJf8fU5VMtF0WUCV4nVu7_3rzmQyIeVjKW-Dpe59kAGYsby8BAss6g5E9Eu9RZlYIfgLIXkkL7eG-WktOMrOJWEOVsM82PYo6Ozkb6LKBXIatQLtzXw-RlJCeWaHWecxYmw)

**OS detection**

Now let's try to detect the running operating system. The trick is easy just run

Nmap -O 192.168.1.108

![](https://lh6.googleusercontent.com/OeDw1qKdYljH8uy4D2p3Z28SzsBGAsoWK14Xg9o4CG4reiiutRckhwpp2gBzBJgzsOoH91zMKG88n0GVYHW5_SbStmmJhzu3tjhcyeZRDLTe9YaxDWZP8rRCvWKXsZfjDdamuEo9E1nLHE0uc1RPYA)

**Timing**

Nmap delivers what we call "[Timing templates](https://nmap.org/book/performance-timing-templates.html)". There are 6 templates; paranoid (0), sneaky (1), polite (2), normal (3), aggressive (4), and insane (5). Timing templates are specifying how aggressive a scan is for many purposes including intrusion detection evasion.

For example, this time is used the "T4" template and "-A" (operating system detection) to perform a scan

Nmap -T4 -A 192.168.1.108

![](https://lh5.googleusercontent.com/gGLCukk0CAl_yXU2YuSuECuZtpbkHt8YOrn_KNg2qTCSAXeGk9ib5wQxG7cfmsmiNgGm_0-2QcLY_1Jm-gBMsg2ffPVqxa1yuJp2VUOQ5ldapz5mvtwsT5CawVtAz0fn-LvixTH0_BGSFvmZK4nolA)

**Nmap Scripts**

Nmap is so powerful. It gives you the ability to write your own scripts thanks to its engine. It is called "Nmap scripting Engine" (nse). To write NSE scripts you need to explore the Lua Programming language.

The are many premade scripts when you install nmap. Let's explore some of them:

Find MySQL info:

nmap --script=mysql-info.nse 192.168.1.108

![](https://lh3.googleusercontent.com/8yzpWhwz38kYKSgExk-XX6GnbEP80l-aMx7j8w5yoKkFUPp9ve8eq8EWUO1lNHws-gGEOWoyltA5_LXNBcNEeo-DfzDaU7QJtRC3dD5wwn7tuUXDQYDf6A5ymzE0FCDM9jJ12IEoHqD_Dj7BKI6uVw)

To check if the target is vulnerable to ssl-poodle use this command

nmap --script=ssl-poodle.nse 192.168.1.108

![](https://lh6.googleusercontent.com/2KxUJZJRvJg2EZU0segbqP2mP7rorN7k-7T-9pQQLcGeQg81EmsdTbunFw2t7kx2LrzwyBp3cdN4smDvrEoCTG5gA2OEGqTxjWUVRzSFrte7i6OMA0WR8spwIwvFV2PmLnRVbgaQZr9dSF8LF0gohA)

There are many other nse scripts you can try like:

- Http-enum
- Http-wordpress-brute
- Http-title
- http-waf-detect

You can find all namp scripts under:  **/usr/share/nmap/scripts/**  (on linux)

**Outputs**

To get the most of your scanning efforts you need to save the collected information. You can save the results easily with Nmap. To save the results as a text file type:

nmap -A -T4 -v 192.168.1.108 \>\> result1.txt

![]([RackMultipart20230211-1-qup5ag_html_86ae1371b1bb8ba2.png](https://lh5.googleusercontent.com/rPpdTyPYuqPDTjkrCzjSA9pLDuQ_2YlZRDrmNGJ43_Ge207EQrNqMzTZ_QPaSZep87ezb0IL6wJc01awLEocIHNcuqZr3FY_VZM_vL9CYywjyZARn0NGIR3GB2SoiGZa9LV2VSH8k-uo2JzWRFrPeQ))

Or you can use "-oN"

nmap -A -T4 -v 192.168.1.108 -oN result2.txt

To save the report as an XML file type:

nmap -A -T4 -v 192.168.1.108 -oX result3.xml

![](https://lh5.googleusercontent.com/rPpdTyPYuqPDTjkrCzjSA9pLDuQ_2YlZRDrmNGJ43_Ge207EQrNqMzTZ_QPaSZep87ezb0IL6wJc01awLEocIHNcuqZr3FY_VZM_vL9CYywjyZARn0NGIR3GB2SoiGZa9LV2VSH8k-uo2JzWRFrPeQ)

There are other reporting options like:

- -oS
- -oA
- -oG

By now you acquired a good understanding of network scanning with nmap. If you need me to correct or modify something please leave a comment below.

I am going to add more techniques to this guide in the next days.

 Thank you and i hope you found it helpful.
