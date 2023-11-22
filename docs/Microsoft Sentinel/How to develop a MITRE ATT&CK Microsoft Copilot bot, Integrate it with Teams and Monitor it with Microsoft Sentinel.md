# How to develop a MITRE ATT&CK Microsoft Copilot bot, Integrate it with Teams and Monitor it with Microsoft Sentinel.

## Introduction 

Hi defenders, At Microsoft Ignite 2023, Microsoft introduced Microsoft Copilot for Microsoft 365 that uses Large Language Models (LLMs) and your enterprise data to provide powerful intelligent assistance capabilities. In this blog we are going to explore how to use Microsoft Copilot Studio to develop your first Copilot, integrate it with Microsoft Teams and Monitor it with Microsoft Sentinel. 


1- Create the MITRE ATT&CK Copilot



https://lh7-us.googleusercontent.com/oFGm_05v0hycXRqGKLNv2A_6NzgnUcbj87bwmfQ5W6pY5IyXDy2U9FUT-V-Jmrp-TlTwDg37mLtF4WQ1HnHTAGLGM8BxPtkX2321nxB_MFGdu8HhAk-GqNLRyI8C5zgvOsa2O-6EFB5pslJ77UpGo44

To create an account, use your Work or School email address:

https://lh7-us.googleusercontent.com/71PDthk6kkqpGBUQCTtuLvpamgrmQKkG6D4IieCn07w7ELLWMs6VX1fQpFSdP8sPfBTLHrAc8Is6bg71tW258-J8g7Djm3ljLwgjXhP_mKU5IsfKdmykN3ndNwbRP5hhCwOpOFSgdY04GDpsuYLyjPI

Now you are ready to create your first Copilot.

https://lh7-us.googleusercontent.com/Zpuw_O_pUkvfH8Ufy5Cgd8DdlJA5IMoVdw_zswiyp7cZ_c7UCrJH0a3Vm3PORUshQkltD2J6fPdq3x4C4DFn0o19sgDo2IbmIJPzcX944CwHcEuExYz1ZqmUugrdVDkQYmq0fjTm8UFLQg9nOgDaCAQ

Click on ***+ Create a copilot**. *****We are going to build a copilot that uses the MITRE ATT&CK website information to answer all your questions about the framework. Enter the following pieces of information and click on “Create”

https://lh7-us.googleusercontent.com/lQ_n-yPbqpwWdDR9HYhToDuN5e72NUpRDM82P81yJUnxs785zYuMko4s-0QXHFi8kXCeJdbBBaGSDWEOk4Va4ErZvr4FkyXBfE40AF7NXTeW0Se6haC2Bha5kn74oyWko70DNbEjU2iRjs0xbTwiwC8

You can edit advanced options such as the Copilot icon etc

https://lh7-us.googleusercontent.com/AQCccemQDrvBNZVZXyaRwVVGKLC6BRsSnBSsiRo5tGvtBm6_Gp3NnIy_djtAbJvoFmDZcScuchkFnw_REpRpCs-CEvMAesIPxRLIUN2Ssqomw9UuFJc0QpWByPq4xPWXgxh8CRrH_MWFjXtQ_sksKBQ

Congratulations, your first Copilot is ready.

https://lh7-us.googleusercontent.com/Vo4hIoBgyVIDRxPxn23rSBzzKm8Ok_PVDnDC2u7jl01Z-IE5ig5TOcpXDo8XsGofzIvCW7RuD01jiixVgElG5La0NGJMIB0b4j9lwwETBsooZiOmRrLqRvscPhQB9KuvlpNp3SWDZxDMjcNNmwDiYX4

You can start testing it right away. Select MITRE ATT&CK Copilot and try to ask some questions about it.

https://lh7-us.googleusercontent.com/sZlSYvdr5pVcVVwpRFFOzH7LuIWOX3v0kikIzYhMeO9HRbbPB-xKgI2nWfY7Q_KFDwO27YC9xyY2hQ_4Ys8eQ922PfZOuKMKfMOoWz_aw0SdgD9EPJeE7gndrMCQHsF1DqhBLjrGGhy36DA7WEIS6pg

Now publish the Copilot

https://lh7-us.googleusercontent.com/uxNgmh5fenrpX3kKkhJG0NXVlUBx_5Xzhekwkv3wGMTY0RoUYaL1ZKmlo5lC-Z_YWRi6KNgQwIYSxeLMItRQj-ZpPxxaOg59szqp9IBgHy18M5QDo9JgHRYK_J756-tzcSVtjIFtX0ohrLJqpT62rOQ

You can explore the copilot web demo directly by clicking on “**demo website**”

https://lh7-us.googleusercontent.com/B4r_Hq5LddN3QoI5ap-3_rY7s8N1IRAMjeoeWS0Zy8ZuUVegFb9xOy4tfNC4NDPb1RQroQNEa5Pl7fO1FBuIHTfpLNiGZE_8LrtIln95Ud2RGKBtMTSqjHK9-tkTtl3Er_wmgAcjR0KyRrn6Hx0AnbE

**2- Integrate MITRE ATT&CK Copilot with Microsoft Teams**

Once the copilot is published now, it is time to integrate it with Teams. Click on “Go to channel” and select Microsoft Teams

https://lh7-us.googleusercontent.com/-gfV13ejYsnVorsJjLXe47pCO_vlfbLv146ZaoWreBYzbhCwwRpnf4s6frjMtXrSBTweekX4hntfvqMLxXtLeMsWyqogsnmenNXrlinVpjZVx-ulCiqBZWcGOIC36DQLNIYpBb8u_D9O7aaut8Jkfjk

Click on “Open bot”

https://lh7-us.googleusercontent.com/APqhcmQgThu3UMHpuYp4l3BiPJQQn42lzUcyke1wkl5KAv-lX9wLnFl5ZiPYw2S4ku768NgIPhvXtx-ETnhQ9TNUYUspob53B1-4xRxuOMJpPhn6M9azipS0NK484hzFOVj9_idkTWdva01DO8DcHkY

Or you can download it from “**Availability options**” and upload it to Teams. Click on “**Download zip**”

https://lh7-us.googleusercontent.com/iNiAJGG7yNXHrDdcZZbI3sKBmmbyA87yqSNn_T1stS2qjGxTyuL7Xsu9EqD6wqCoT_yuofNar7dZfBu59cq2I1wfXeWP6oI44iwUA9uUVvJMv8BZtYe_qUvQVbZ5l1HOcItT6vcQMjqMRPN3PQ8m8B4

Then open Microsoft Teams, select “Apps” and click on “**Upload an app**”. Upload the copilot app.

https://lh7-us.googleusercontent.com/c23xrSPxJ15Y8i6OJomtOqwSV3yQlBJHIe8s-1JCousNZMg_34OcfKz8GX2kPkPhnwql_1eKKqCKq-0dsnon0pIL7dVPRkvfvHKw9mcP-sjr-k14ucW70z3_ywrMtzb8WVJNo3iC8d1z9d4G3W0gPmI

Click on the first option:

https://lh7-us.googleusercontent.com/kzx68JkuIG6AeUZoREdcp7Pbnng0_xT9T27h6l-dIQGLy76jmoz2n9FlfeWBEDfTkSn5X6F49rZFcvGTNgzEhBtBNXlDMK-PKMvxsOeRXPjzScfgUK4upEIY5MrVAD5LVm9xZP1fyMr65D-iBC6gwXU

Then add the application

https://lh7-us.googleusercontent.com/HwLtnrO3Xnj-jUpeLPvoFJFiM6bfYMdqodgN187l0xCvrBMQbzVuHgh1B6mkOBlru-zjBiSoYjCX6ifc479bdmq6vOGDSxcfkYpcQienK9OmAG6JzyTVZWv2ZbPLjlnlF3swLqdCV4Bi0LK5MDz-jv0

https://lh7-us.googleusercontent.com/onZuL1mMZkcEUAFw9c6rpmeDHynl9ZlcRSSpKYB3q6OYB928GVRHm7SVWpqHT9uKyggCzWgRA7xiOHCI-vkBj-BViU6YltdWtkhwSR3W08RUvAFGmlE5TIRAOkBDPl013p7dnllrs0PcOazDG633NWc

Once the app is uploaded and added you can interact with it directly in Teams.

https://lh7-us.googleusercontent.com/Ehs8aD56ZL1uyPrw9StR2QuI0y_9V5gTBC9BGnPMGhbQgQzYubInL7CYV0RjnKDYHUzRzBuw1530v9d5eyzMkigRCGT8M20TAm-hh8GOJcCoeYtt-CXv1nCB8uDPeQxOgNeQ17iIAcSBcDSVE6PoprU

**3- Monitor the copilot with Microsoft Sentinel**

Once the copilot is active within Teams, we are going to monitor its activities with Microsoft Sentinel. First, create a new azure Application Insight

https://lh7-us.googleusercontent.com/q71PO0cJcSqieF4q4TsYq2-HboW_x9cVOq_gMHQeCIO_1GcfVBfLZ3yjlQPoDbW8a_ipi8v5OisQaFFqaQ96IU1o0gRAfDzdyGqDA7kEtu6fjHAhqYOj-M3hQMzRwu1tObArCaZwE1zmkBv5i75O9Hg

Click on the newly created Application Insights

https://lh7-us.googleusercontent.com/BDxcM9OF31TuNwT9S4peok2-3amFxDSpMeQgXGQAbhPC99_jZlgbx2BiWhYI23fKTPtFZc9V5PB1ys_J9PjoI88u6c8l4FABb46xN7p-0C6EBNYPm_116nDJOCGlVSBkJ-vMx8BeQ6LBwjXNkKipV4s

Copy the connection string

https://lh7-us.googleusercontent.com/4IE5DvtHXIiYKgT8gNkdJc6jy3qFobHl15oZfu2NFNa1Lmly3Spi3llQBWMPoDfwlkXn9HbsrMrUwoffHhjfYbENn1tvIt50PLw1cQ9CKHz-2HOSiOEVySmMauImRiUciLaIfd-Royt2TneNphEDPBQ

Go back to **Microsoft Copilot Studio** and click on “**Copilot Details**” in Settings and paste the connection string in Advanced bot details

https://lh7-us.googleusercontent.com/8NWs445jHNt_9fZTHWok3x4cIdHEvyI0pcIf6lQv-fNxnYwBtGSz4FO29ih5o0Isf5zQufgYrnqVHTBN9_6xZbALyWgCPLnwv39gb8hq8APnETSZTxDL4WW30YlX1svaQVmyDiNG0prpeZEWiqhPSGs

After a few minutes you will start receiving the bot events. Events will be stored in a table “customEvents”. You can explore it by going to **Logs**

https://lh7-us.googleusercontent.com/cSfwIhJ5k0t1s4N0gnZxYio6-nfp5KyiWDYhG378DAqEjjrr9yunkj0VnOe3INlcc-dCjC8C3xsLzY_zEOMz0k1izZsB0kNrU8DD-pKkniAOsU5Q27WnC3vCiiKxXonpB6N-eGDJHJreWMvsbCxh2N8

Once we have events, it is time to develop a Microsoft Sentinel Workbook. Go to Microsoft Sentinel and create a new Workbook

https://lh7-us.googleusercontent.com/3IOklF9CsBv5_DSm9Ikkn6b_obC59iatnIYEvEWaHC7-K-UcAuFQyF0gzILpzdiGueyNZQtsve7-2O0s20Wvh7wZkwo2n9DetIkAemXvA9xk5HJhAS1eeZR_sViZKAQRhxtQaill9aqcFw4O4LuhxnQ

You can name it for example, **Microsoft Copilots Workbook**

https://lh7-us.googleusercontent.com/uwBf8bildT-yruTqrgVW78c3v9BY2rFuy2OrKCSApz-BN4Q3BOWvKIrctR-gVmJY09aFhOi-PCMts5vjgk9pL5hnK1xU8aCD2M4sJSkJ4QJPmob2Eu9bocHZleP1E5OumjWDf_GlcQs_JLOBVghylSE

Click on code icon and paste the following workbook code: https://github.com/chihebchebbi/MITRE-ATTACK-Microsoft-Copilot-Workbook/blob/main/MITRE_ATT%26CK_Copilot_Workboook.json

And save the workbook. Now you can monitor the copilot events in Microsoft Sentinel.

https://lh7-us.googleusercontent.com/KuxeUJCbBDSE3z8RFO_jXiLu6Tk7izjx9kesmbEDYmsNSjFk0hzmojjb6oQFpKFaGo3qHX9lCejL3ll8Jm8Pk4XmO54OHKRH1pnTTVV_ouUGnVty3M-ZM1LHhVvPoyDy3Ksv6yFt8TMZUQZXi9eV8dw
