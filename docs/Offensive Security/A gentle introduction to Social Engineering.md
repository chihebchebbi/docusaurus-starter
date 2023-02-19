

![](https://lh3.googleusercontent.com/5lM0k9acvszbq7UDVpXivhBSU9dbdKRkNMCx0ZTSU_ZkLE7vbcx4_GmH3hoTQdCQpz2Og5YzfUwqNkYfzllfueQI9fj-XYlbjMivYvViVgEde1eqI0uSZGF20xd0-zl5jNhJTnhOfcExbmlYzzcFjg)

You probably heard this mantra "Social Engineering !  because there is no patch for human stupidity". Social engineering is the art of hacking humans. In other words, it is a set of techniques (technical and nontechnical) used to get useful and sensitive information from others using psychological manipulation. In this article, we are going to learn Social engineering fundamentals, Why people and organizations are vulnerable to it and finally, how to perform social engineering attacks using Kali Linux.

## Social Engineering Overview   

There are many books like "The art of inception", "The art of deception", "Ghost in the wire", "The art of hacking the human mind" and so that discussed Social engineering and presented many techniques to teach how to manipulate people to get them to disclose sensitive information and useful information so you can use them later in your attacks. All the works proved that human is the weakest link when it comes to information security. It is not just about hacking tools and techniques. Studying human weaknesses could be very useful to succeed in an attack. Before learning how to perform Social engineering attacks let's explore why People and organizations are vulnerable to Social engineering attacks.

![](https://lh6.googleusercontent.com/RoQyauKHyzcG9tD9iENrlyrNlhXRvnG88xFysGAnZiNE0SgvWvrjY5Iy0kJpc4ymSalUAO0sUp5KzTDsQd7ZZ8D4rcjH5_yd8HKCZfGUwhwTN1WsiznbDGm39W3SOsLWonATm3DMNZb0IxFzUjDGHw)

[Image Courtesy: [https://wraysec.com/wp-content/uploads/2015/10/Social-engineering-security.png](https://wraysec.com/wp-content/uploads/2015/10/Social-engineering-security.png) ]

**What makes Organizations vulnerable to Social engineering?  **

We discovered previously that social engineering uses psychological manipulation to trick targets. Thus, many human weaknesses could be exploited when performing SE. These are some causes why people and organizations are vulnerable to Social engineering attacks:

- Trust
- Fear
- Greed
- Wanting to help others
- Lack of knowledge

Other causes were discussed and named " **Cialdini's 6 Principles of Influence"**

### Cialdini's 6 Principles of Influence 

The Cialdini's 6 principles of influence were developed by Dr Robert Cialdini. These principles can be exploited while performing social engineering engagement. The principles are:

1. **Reciprocity:**  we pay back what we received from others.
2. **Commitment & Consistency:**  We tend to stick with whatever we've already chosen
3. **Social Proof:**  We tend to have more trust in things that are popular or endorsed by people that we trust
4. **Liking**  We are more likely to comply with requests made by people we like
5. **Authority** : We follow people who look like they know what they're doing
6. **Scarcity:**  We are always drawn to things that are exclusive and hard to come by

### Maslow's hierarchy of needs (Maslow)

Everyone knows the Maslow's hierarchy of needs. It is very implemented in the framework while attack vectors can be based on it. By having a fair understanding of its needs attackers can exploit them to perform social engineering attacks

![](https://lh4.googleusercontent.com/bKWlhIy-NvZmEnB9vbiYwIGi_XPUSEf7AUf8Fu7q4UWz_xGbZxVS365-Lo4iqp9eCtlkNrRPgw3-FyStN1CBPP-iu8qcWpPfFs5aV5wsyw0Ok94O8dHgBOb6mXc0Qp1cqW9FR_WJhPpWRosM20iUEw)

## Social Engineering  Techniques  

There are a lot of Social engineering attacks. Generally, they can be divided into two major categories:

- _Person-based social engineering attacks_
- _Computer-based social engineering attacks_

The following are some of the most used engineering attacks:

- **Baiting:**  is in many ways similar to phishing attacks. However, what distinguishes them from other types of social engineering is the promise of an item or good that hackers use to entice victims
- **Impersonation:**  is an act of pretending to be another person for the purpose of entertainment or fraud.
- **Tailgating:**  a common type of _tailgating attack_, a person impersonates a delivery driver and waits outside a building. When an employee gains security's approval and opens their door,
- **Dumpster Diving** : is searching through the trash for obvious treasures like access codes or passwords written down on sticky notes.
- **Phishing** : Phishing scams might be the most common types of social engineering attacks used today
- **Shoulder surfing** : is the practice of spying on the user of a cash-dispensing machine or another electronic device in order to obtain their personal identification number, password, etc.

## Phases of Social Engineering  

To perform Social engineering you need to follow well-defined steps:

1. Information gathering about the target
2. Victim Selection
3. Engagement with the selected victim
4. Collecting information from the victim

## Social Engineering with Kali Linux

By now,  we acquired a fair understanding of Social engineering and theoretically how to perform it. It is time to put what we learned into the test and practice what we learn using many open source scripts and Kali Linux tools. As discussed before information gathering is a required step in social engineering. We already explored information gathering in many Peerlyst posts so, I think we need to dive in directly into how to perform social engineering.

### Social-Engineering Toolkit  

Social engineering Toolkit is an amazing open source project developed by  **Trustedsec ** to help penetration testers and ethical hackers perform social engineering attacks. To check the project official GitHub repository you can visit this link: [https://github.com/trustedsec/social-engineer-toolkit](https://github.com/trustedsec/social-engineer-toolkit)

In this article we are using Kali Linux as a distribution, so there is no need to install while it is already installed in Kali Linux.

To run the toolkit just open the terminal and run  **setoolkit**

![](https://lh5.googleusercontent.com/sFb-FA8BYPEo7SYjMoJqlSQiVHQk0gOKucwXQp904y1idn0xJYzacAnC_VIdl2wIKljDZT-i_zRyQO0L6Y-F36SzljSYtKd6kd-mq96MApAPbNIk-e6G7o0xc6hQeE3d_5h0ykVoWFkiUkzxhTwUfA)

To start using the social engineering toolkit you can select one of the following options.

![](https://lh6.googleusercontent.com/W-Y-rd-fMPuN7y-lsFEAmoD26f2ySvzf2PZ7-zYb8INMmm6lS2372dAIqiPyRbjBn81y8qJu2ZyseEjt_TrV3icJtbrCQa2i-qfn2EcmWlr67vthfmhgmlCjrh0c6M3akm5OLMbP5rg_XlxsuvnkCQ)

If we want to perform a social engineering attack type 1

![](https://lh4.googleusercontent.com/_7g5cI0qDQGGbasxDMuCySp26cVLrFyYIv7VKatWQXWfY98wL0EA6IiL7_l8_HbYoyS3VP4lVySvxW7SV4vkIzdQ8cVs4SpCLihRqvUdkh4X60C9hP9FZTe-O7xuM6MbeV4k_AXRpgET7VPW4YlF-A)

You will find many Computer-based Social engineering techniques you can choose from.  Let's suppose that we want to create a Facebook phishing website.  Select  **Credential Harvester Attack Method **

![](https://lh5.googleusercontent.com/mgfKY_jnvpKELbf8PIZH8vRY4fzkpEH7EUlcdrF3Gm06gdB7FTjN0gI2QcPS3Td_Gh4UGfsu6fI3NSfqDbNr_Af-kANx1kWPyq2xA6bbUbZ-Xi7ZvolkDGPGGYN6p09xkgLoH87n1JWAQs9sZ_u0Sg)

and then  **Site Cloner.**   Enter all the required info and options (The URL to clone and so on)

![](https://lh5.googleusercontent.com/nbqeDbd6KptxV0G9weGjw-Wer-EyvyfjMhlPAu3NVit7b3G3e-m5T4qK0b7NspcnT4BjxCqxkN2boSb8LgT0lhc9zRste5Mw66jpdO6QoPUMBqClGVEEOQ15nzoHMBHOySW5tEz85w1U3hifNN_Vbw)

## Summary  

In this post, we explored the fundamentals of Social Engineering and some of its techniques (Human and computer-based). Later we practice what we learned using many useful scripts and Kali Linux tools.

## References and Further Readings:**

- SEEF definition of Social Engineering:"The elicitation of information from systems, networks or human beings through methods and tools" :[ https://seef.reputelligence.com/](https://seef.reputelligence.com/)
- Dr. Robert Cialdini's 6 Principles of Persuasion (Over 60+ Examples Inside!):[https://www.referralcandy.com/blog/persuasion-marketing-examples/](https://www.referralcandy.com/blog/persuasion-marketing-examples/)
- 5 Social Engineering Attacks to Watch Out For: [https://www.tripwire.com/state-of-security/security-awareness/5-social-engineering-attacks-to-watch-out-for/](https://www.tripwire.com/state-of-security/security-awareness/5-social-engineering-attacks-to-watch-out-for/)
