**Introduction to Ethical Hacking and Penetration Testing**

In this article, we are going to explore many important terminologies in information security and especially in penetration testing. Later we are going to explore how to setup a penetration testing laboratory with kali Linux .I am planning to create a new series. Most articles of this series will start by discussing the fundamentals of the subject and later dive deep into the practical details using Kali Linux distribution tools.

# Introduction to Information security

Before learning how to setup a penetration testing lab and exploring the realms of ETHICAL HACKING, it is vital to discover the fundamentals of information security. Information security refers to the processes, tools, policies and systems that defend against cyber threats. The core of information security is modeled as a triad called  "CIA" (don't confuse it with the agency). The CIA is the abbreviated form of  **C** onfidentiality,  **I** ntegrity and  **A** vailability. In other words, the aim of information security is assuring the confidentiality, the integrity and availability of data in its different states. Let's explore the three terms one by one.

- **Confidentiality**  refers to protecting data by granting access to data (for example Personal identifiable information PII of clients) only to authorized persons and groups.
- **Integrity**  refers to the fact that data should be protected during every process. Simply is ensuring the trustworthiness, consistency and accuracy of data
- **Availability**  refers to ensuring that the data is available by authorized users when it needed.

The CIA Triad is represented as the following:
![](https://lh5.googleusercontent.com/CyMANiwMh7-MTWMdRW7JBPF24ldZPgqQr5k6aEG19RI3701XiDyBeMeASCzT-jBP1sRqUaSq5xKFEbrvy-bIKG3pQPdQ8SI2ugGtq_Wo8RkauaapTN8LfHZJIr9A1O4fRHaQenvJyieY63tc8hFpcw)

# Hacking  phases

**San tsu**  in his famous book the "Art of war" said

"_If you know the enemy and know yourself, you need not fear the result of a hundred battles. If you know yourself but not the enemy, for every victory gained you will also suffer a defeat" . _

![](https://lh4.googleusercontent.com/R3PVWzaN8WYFbGxSUazX6hC0dwPWRox8CKHBDS6PHJMEB01xcQYR4QL_DWJdOuN4c2Slnv4Y00GIAbggxwD2PQhM9ITjPVR9Q8gJLXmh4mcHiSmN0J49Ai0IMl29EOwNpXd0MOTl0DA0byibaHeuuQ)

[source: [https://images.gr-assets.com/authors/1185211202p4/1771.jpg](https://images.gr-assets.com/authors/1185211202p4/1771.jpg)  ]

To defend against criminals and cyber attackers you need to think like one of them. Online criminals are intelligent individuals (in some cases Groups). That is why cyber attacks are respecting usually methodological processes.Generally to perform cyber attacks, black hat hackers follow these steps:

- Information Gathering and Enumeration: the first steps is gathering information, sometimes called "Reconnaissance". Before attacking a target it is necessary to search and collect information about it. To attack an organization black hat hackers should collect information about it and by information i mean not only technical information(domain name,IP ranges,TCP/UDP services). Organization location, employees, physical environment, management stuff also are some very important pieces of information that are needed to perform a successful attack.
- Scanning: After collecting juicy information about the target, criminals start the scanning phase, where they use their tools to reveal information about the systems and the services. This phase includes Port scanning, network scanning and vulnerability scanning
- Gaining Access:  by now the attacker gained information about the target. In this phase, he will use them to gain unauthorized access to the systems
- Maintaining access: usually, the main goal of a cyber attack is not only gaining access to the systems but also ensuring persistence and stay as much as possible.
- Clearing Tracks: finally attackers should clear their tracks to avoid detection and being caught.

![](https://lh6.googleusercontent.com/WRlpZQkZMymEwt8QMvsUmmBKy6EaYJpcqJ6UgTdhmnRniH2AAHS-KaRHLspA_2_DluB77z1YEBT2AkJKlMsdYvWUr5xqTPvre6ZBIP9KYZ0Llie8-hia3DHgbJlNuzq7GLb3eiP0H9WrlpWYVcMraA)

[source: [http://varutra.com/blog/wp-content/uploads/2016/01/diagram\_steps.gif](http://varutra.com/blog/wp-content/uploads/2016/01/diagram_steps.gif)   ]

# Introduction to Penetration testing

The definition of "Hacking" and "Hackers" is a misused term nowadays. It is usually connected with cybercriminals. The terms were mishandled especially by modern media. In the wild, there are many categories of Hackers:

- Black hat hackers:  are the ones who use computers to steal and harm systems. They are cybercriminals.
- White hat hackers: are usually information security professionals. Their main goal is deploying safeguards to defend against Black hat hackers. They are the good ones who work in a legal way. They are sometimes called "Ethical Hackers"
- Grey hat hackers: This category is the combination of the two previously discussed categories

One of the most known activities of Ethical Hackers is performing Penetration testing. The are many other tasks and sub-fields within information security but in this series we are going to deal mostly with ethical hacking and penetration testing. Penetration testing is simulating a black hat attack to evaluate the security posture of a given organization. Also, penetration testing can be categorized into three main categories:

- White box pentesting: the pentester knows everything about the target
- Black box pentesting: Before the pentesting mission, the pentester has no idea about the target.
- Gray box pentesting : the pentester knows only few information like normal user credentials.

**Information-tip:**  Don't confuse penetration testing with Red Teaming.

## Pentesting standards

To ensure a successful penetration testing mission, pentesters could follow penetration testing standards. These standards are the result of seasoned pentesters and information experts to give others documents that can follow to succeed a pentest based on years of experience in the field. The following are some of the most used pentesting standards:

- The Open Source Security Testing Methodology Manual (OSSTMM)
- The Information Systems Security Assessment Framework (ISSAF)
- The Penetration Testing Execution Standard (PTES)
- The Payment Card Industry Data Security Standard (PCI DSS)
- The Open Web Application Security Project (OWASP)

![](https://lh5.googleusercontent.com/oQU5uVqCAC8VNbiw_yhJzJCJVrRrEaJQwmDihSSEg4F6uFwP4qwhY7BRcSYxetBuOqhScAL1xwBpFKICsM_OHgw1VrWLnEzzwrW9tXAQRBRLMQ8M6TNqoA9vKtxuruVwtP96LWwKdcfSi6CqwvJQwg)

[source: [https://www.owasp.org/images/b/b1/Logo3.jpg](https://www.owasp.org/images/b/b1/Logo3.jpg)   ]

## Penetration testing phases

For example, if you decide to use The Penetration Testing Execution Standard (PTES), you need to follow these important steps in your pentesting mission:

- Pre-engagement interactions: This step is really important in penetration testing, before starting the mission you need to discuss very important points with the client (organization). As discussed before, don't forget that we are working legally. So everything should be discussed before the pentest. Some of the points are:
  - The objective and the scope of the mission (Physically and technically)
  - The " **get out of jail free card**"
  - Emergency contact information
  - A non-disclosure agreement (NDA)
  - Schedule and Payment information

As you can see pentesting requires good managerial skills too.

- Intelligence gathering: After agreeing with the client about the scope and the details of the pentest, you need to start collecting information about your target depending on the agreed pentest type (Black, white or Grey). It refers to collecting every available information about the target from different sources.  It includes:
  - Human intelligence (HUMINT)
  - Signal intelligence (SIGINT)
  - Open source intelligence (OSINT)
  - Imagery intelligence (IMINT)
  - Geospatial intelligence (GEOINT)

![](https://lh5.googleusercontent.com/0wGtmSyCcW4JsF8-vMo45hCdLyfoMu8P1OKQ4hE8glZykEzHZPl4NBN9ssjB9Tm7IsYNPEs5C8glbcIK8we-KgCbJjy8rS4cEPC0A0dn_SVp-DJe6FBc4FIDfjLeT5UCjrf9QXGuHuS3CjXY4Rga2g)

[source: [https://automaticballpoint.files.wordpress.com/2013/02/intel-collection-methods.png](https://automaticballpoint.files.wordpress.com/2013/02/intel-collection-methods.png) ]

- Threat modeling: refers to identifying threats against the infrastructure of an organization. Threat modeling goes through 5 steps:
  - Business asset analysis
  - Business process analysis
  - Threat agents analysis
  - Threat capability analysis
  - Motivation modeling
- Vulnerability analysis: goes through these 6 steps:
  - Identification and discovery
  - Prioritizing and classification
  - Assessment
  - Report
  - Remediate
  - Verification
- Exploitation: in this phase the pentester lunch his attack and try to gain access to the systems
- Post-exploitation: in this phase, the pentester try to maintain access and gain root access instead of a normal user. It goes through the following steps:
  - Infrastructure analysis
  - Pillaging
  - High-profile targets
  - Data exfiltration
  - Persistence
- Cleanup
- Reporting: it is the final step of pentesting, it is also really important. Sometimes it is called "The Art of Reporting" because delivering a badly written report will fail the mission.

## How to install Kali Linux

By now, we acquired a fair understanding of information security and especially penetration testing and ethical hacking. This series is a delivering a practical and a hands-on experience. Thus, we are going to prepare a penetration lab with the famous distribution Kali Linux.

Kali Linux is a Debian-derived Linux distribution designed for digital forensics and penetration testing. It was developed and maintained by offensive security ( [https://www.offensive-security.com](https://www.offensive-security.com/) ).

![](https://lh3.googleusercontent.com/mCotQNbe0uWihMNpUpdC4-k8aOU9ugyZL5v8AGXgWMASNp87dZmReNXdPa5uKbzpCf9ZCXxZPLMEHtAeqc10seDkR8iTiyvmpR6KGd3oIhVfG98IaBBKrBC2HfwnO_DuWK4J1jBdebuMwcqZ2YtC_Q)

According to Kali linux official documentation,To install it you can use one of many methods:

- Kali Linux Hard Disk Install
- Dual Boot Kali with Windows
- Dual Boot Kali on Mac Hardware
- Single Boot Kali on Mac Hardware
- Kali Linux Encrypted Disk Install
- Kali Linux Network PXE Install
- Kali Linux Mini ISO Install

For example, if we want to install kali Linux on our computer (Hard Disk Install):

1 - Go to [https://www.kali.org/downloads/](https://www.kali.org/downloads/)  and download your ISO file and then burn it on a CD-DVD or a USB stick.

2- Boot your DVD or USB

3- Select "Graphical install"

![](https://lh5.googleusercontent.com/_tUu0veuOHmibOAsxC7_UEewHm8yfbOXt4AGtwdBOG9NC1sZ7E-fAtDUL8JkAlhGDLLaUsx0z3__BQZ8Ev5B7lPJkn6WwquEsxdMvwPGL6xBCZr4Uuv-VDVM173M8RiS58FJ-7IULXNbpcUQfwcpPA)

[source: [http://docs.kali.org/wp-content/uploads/2015/02/01-install-select.png](http://docs.kali.org/wp-content/uploads/2015/02/01-install-select.png)  ]

**4- ** Select your options (Timezone, keyboard, language and so on )

![](https://lh6.googleusercontent.com/efWETXfCu5kIlFXWYD7Lk9tmL_6gefRmS4dsoL8BWwYsf7QtR233JOo_IKymhE0awhZZ6o1fngNJqZU0dvrx9UQfEBhQzdb2dXUMQdalmaFB1j1vZCrPJ9LwMd-1ZcsP1iM8HSDEjd_Pentknhjx2w)

[source:[http://docs.kali.org/wp-content/uploads/2015/02/02-language-select.png](http://docs.kali.org/wp-content/uploads/2015/02/02-language-select.png)   ]

5- Select the partitioned Disk  ![](https://lh3.googleusercontent.com/tVgJEhMEMTP7sTXyowfhz8EAt6EVP-wYzXkc0TxedA5zzYVDUFvLPR8OtaxCMVDayNWMi3Y1x3KpdxXW3f-A-ZCJeZYtQ2K8nubM307A_12HAFrbK9Lrka4st93Loh3A8qhloQc0JFNllrZ7IdzjGw)

[source:[http://docs.kali.org/wp-content/uploads/2015/02/10-partitionmethod.png](http://docs.kali.org/wp-content/uploads/2015/02/10-partitionmethod.png)    ]

6- Install GRUB

![](https://lh3.googleusercontent.com/Q7EaVqZzMbYvy95pEnAeXH8XKcv4JYXKf7P1RCfa6NFvUBgQTwJWOFBWMC8sZ_gqm0GIxXz3CB43ihsnh7xP-k1yKlwLZEBmP6AtkSuQVpS4r6i6zc16ewUVUtDH-9F7v2SeZJwW69sfv4yKcQ9z1g)

[source:[http://docs.kali.org/wp-content/uploads/2015/02/15-install-grub.png](http://docs.kali.org/wp-content/uploads/2015/02/15-install-grub.png)     ]

Voila! We installed Kali Linux Successfully

![](https://lh3.googleusercontent.com/jhXzgJyKNeeyxG54EvdhlGshS2L2dvINZgj7cup_JuNVpusNn6zJR3SKHJnNOGoPHsS6D-OTvufr--OFGWPK_gqgP3c20rM6HuHsfYQFpCefebZ-rp3Trvgn1HHMm2ZIo7gxvUU69flCZOcvsXdIAA)

[source: [http://docs.kali.org/wp-content/uploads/2015/02/16-install-complete.png](http://docs.kali.org/wp-content/uploads/2015/02/16-install-complete.png)  ]

## Summary  

In this post, we learned some fundamentals of information security and penetration testing. Then, we explored the required steps to perform a successful penetration testing. Finally, we build a penetration testing lab with Kali Linux so we can use in the further postschapters. In the next article, we are going to learn how to perform Information gathering and Enumeration using many built-in kali Linux tools, scripts and online sources.

## References and Further readings:  

1. [http://www.pentest-standard.org/index.php/Main\_Page](http://www.pentest-standard.org/index.php/Main_Page)
2. [https://www.kali.org](https://www.kali.org/)
3. [https://www.debian.org](https://www.debian.org/)
4. [https://docs.kali.org/category/installation](https://docs.kali.org/category/installation)
