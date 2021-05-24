---
title: GsoC 2020 Work Report for Android Client app
date:   2020-09-02 18:01:35 +0300 
tags:   [GSoC, Android Developement, Java, Kotlin]
image: assets/img/nn_part_2.jpeg
style: fill
color: danger
description: Open source contributor to the client application for the field officers. I introduced new features related to GIS support, notification integration, KYC/on-boarding feature, and other minor features which made it to upgrade to its version 7.
---

<div align="center"><img src="https://user-images.githubusercontent.com/20596763/91049695-2ff0f180-e63b-11ea-858e-166706eac223.png" width=600/>
<h1> GSoC2020 work summary</h1>
</div>

**Organisation:** The Mifos Initiative

**Project Name:** Android Field Operations App Version 7

**Project GitHub repository link:** [master branch](https://github.com/openMF/android-client/tree/master)

**Commits made during GSoC:** [Pull Requests](https://github.com/openMF/android-client/pulls/robustTechie)

## Contents
- [Overview of project](#overview-of-project)
- [Project Implementations](#project-implementations)
- [Future Improvements](#future-improvements)
- [GSoC expierence with The Mifos Initiative](#gsoc-expierence-with-the-mifos-initiative)

## Overview of Project:
<p align="justify"> 
Android Field operation application based on Mifos X is a robust core banking platform that is developed for field officers using which they process transactions, keep track of their client’s data, center records, group details, different types of accounts (loan, savings and recurring) of the client, run reports of clients, etc. Its sole purpose is to make field operations easier and effortless. This application also provides an offline feature that allows officers to connect with clients and provide them financial support in remote areas as well.

During this GSoC, I will work on extending support of Kotlin in the app, improving offline availability, extending testing coverage, integrating with external systems via Payment Hub EE, tighter integration with our notifications framework, improved client data collection via forms, and enhanced GIS tracking features. 
</p>

## Project Implementations
**1. Added Bottom Navigation and Floating Action Button(FAB) in Dashboard** [PR link](https://github.com/openMF/android-client/pull/1521)

<p align="justify"> 
For increasing user experience, using bottom navigation will be more
preferred over side navigation to reach the top-level destinations. Also, the tab bar fairly easily communicates the current location in the app and properly uses visual cues (icons, labels, and colors) to enable the user to understand their current location at a glance. So, it will contain 4 frequent destinations i.e. dashboard, client, center, and group lists. 

FAB is a good way to prioritize the most important actions the user should take. Here in our app, it will provide quick access to create a new client, center, and group on just one click.
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/85178442-1e3a4900-b29c-11ea-90f2-02b8405ea78b.gif">
</p>

**2. Language support through Locale** [PR link](https://github.com/openMF/android-client/pull/1522)
<p align="justify"> 
Added the multi-language support in the application which will allow the user to access the application in various languages like Spanish, Hindi, English, Chinese, French, etc. Localization support is very useful for increasing user engagement in the app. 
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/85862930-0e60be80-b7e0-11ea-948f-056542225e59.gif">
</p>

**3. UI enhancement** [PR link](https://github.com/openMF/android-client/pull/1523)
<p align="justify"> 
An excellent User Interface will create an instant attraction to the app while a superb User Experience will put a lasting impact on the users’ minds. The basic UI of this application can be modified by providing thecorrect padding, color formatting, proper alignment (of buttons, spinner, text
view, edit view, etc), optimizing some predefined UI, elimination of unnecessary functionalities, enhancing toast notifications, etc.
</p>
<table>
     <tr>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85418612-9c456b00-b58e-11ea-9240-0fb36cf281f5.jpg" /><br /><center><b>Login Page</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85418604-9b143e00-b58e-11ea-9068-a2c4244eea5b.jpg" /><br /><center><b>Dashboard Page</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85418613-9cde0180-b58e-11ea-83dd-1525eb5144c6.jpg" /><br /><center><b>Client Details</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85418615-9d769800-b58e-11ea-8993-f1f200bd43aa.jpg" /><br /><center><b>Individual Col. sheet</b></center></td>
     </tr>
  </table>
 
**4. Instant Search feature in search fragment** [PR link](https://github.com/openMF/android-client/pull/1524)
<p align="justify"> 
It will allow the user to get the search results at the instant he types the client's name. 
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/85458507-d464a200-b5be-11ea-9c04-0e9404743dbc.gif">
</p>

**5.  Dark Mode support** [PR link](https://github.com/openMF/android-client/pull/1525)
<p align="justify"> 
Dark Mode design reduces the light emitted by device screens while maintaining the minimum color contrast ratios required for readability. It saves energy, mainly if the device uses an OLED or AMOLED screen. With the majority of the screen dark, the screen glare will be reduced. While the dark text on a white background is the best in terms of readability, Dark Mode (which has light text on a dark background) is better for reducing eye strain in low light conditions.
</p>
<table>
     <tr>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85792302-e2e2c300-b750-11ea-805d-26e5d384dfba.jpg" /><br /><center><b>Dashboard Page</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85792314-e5ddb380-b750-11ea-86d4-f426e8ee0812.jpg" /><br /><center><b>Checker Inbox</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85792313-e5451d00-b750-11ea-9ba8-d28fc20f3ebe.jpg" /><br /><center><b>Settings</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/85792428-1aea0600-b751-11ea-8dde-b4b4994575ef.gif" /><br /><center><b></b></center></td>
     </tr>
  </table>
  
**6.  Notifications support** PR link- [path tracker](https://github.com/openMF/android-client/pull/1526) and [offline mode](https://github.com/openMF/android-client/pull/1527)
<p align="justify"> 
From 8.0 and above a new concept of Notification Channels came into action for notifications framework. Notification Channels provide us with the ability to group the notifications that our application sends into manageable groups. The notification feature can be used to further enhance the UX, for example if the user is offline and they create new clients, groups or centers, they shall receive a notification when they are back online after the offline sync is done.
</p>
<table>
     <tr>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/86897179-b487bf00-c124-11ea-961e-17618965f7f5.gif" /><br /><center><b>Path tracking</b></center></td>
          <td><img height="400" width = "200" src="https://user-images.githubusercontent.com/52889867/86948759-40bcd500-c16b-11ea-9c7d-15dcef18c197.gif" /><br /><center><b>Offline mode</b></center></td>
     </tr>
  </table>
  
**7.  Change Passcode feature** [PR link](https://github.com/openMF/android-client/pull/1528)
<p align="justify"> 
It will allow the user to change or reset the passcode without logging in again. As previously if the user had set he passcode once so he needs to log in once again to change it which will decrease the UX and also make the login workflow long.  
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/88366595-290a6100-cda7-11ea-85c7-0a6f21068ba2.gif">
</p>

**8.  About App feature** [PR link](https://github.com/openMF/android-client/pull/1530)
<p align="justify"> 
This section was previously missing in the application. It allows to user to know more about the application and it also contains a few links related to the contributors, GitHub, license, and their Twitter account.   
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/89718149-680cf900-d9da-11ea-929c-38d6dd6fc17e.gif">
</p>


**9.  Identifier status type** [PR link](https://github.com/openMF/android-client/pull/1536)
<p align="justify"> 
As client identifiers are classified into two types: "Active" and "Inactive", but previously these details are not visible on the identifier list which made two same identifiers with different status type difficult to classify. So I added a new row to show the status as "Active or Inactive" in the identifier details section. 
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/90064566-96efdb80-dd08-11ea-9255-076d5c23b80d.jpg">
</p>


**10.  KYC/client onboarding feature** [PR link](https://github.com/openMF/android-client/pull/1541)

<p align="justify"> 
KYC-Know Your Customer is a process by which financial institutions obtain information about the identity and address of the customers. This process helps to ensure that the services of the financial institutions are not misused. The KYC procedure is to be completed by the institutions while opening accounts and also it should be periodically updated. So now it contains a three-level KYC system to store the information based on the levels.
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/52889867/90796136-910f8100-e32c-11ea-88e0-ed875e7934aa.gif">
</p>

**11.  Extending support of Kotlin:** 
<p align="justify"> 
Migrated the prexisiting Java code to Kotlin and also tested the new codes so that this migration doesn't affect the exising functionalities. So why Kotlin? Because Kotlin is a new language that has adapted and corrected mistakes over the time, it generates the same bytecode as what Java does. So Kotlin can seamlessly call Java code and vice-versa. Also, null type is integrated into the language's type system itself. So it is not necessary to keep wrapping codes with null checks around it to avoid NPE. Kotlin is not limited just for android development. Kotlin Native opens possibilities for Kotlin to support almost any platform.
</p>

**PR links -** 

1. Create new client ([#1533](https://github.com/openMF/android-client/pull/1533))
2. Groups related fragment ([#1535](https://github.com/openMF/android-client/pull/1535))
3. Surveys related fragments and activities ([#1539](https://github.com/openMF/android-client/pull/1539))
4. Centers feature ([#1540](https://github.com/openMF/android-client/pull/1540))
5. Savings account-related fragment([#1542](https://github.com/openMF/android-client/pull/1542))
6. Loan Account related fragment([#1543](https://github.com/openMF/android-client/pull/1543))
7. Client signature, data tables, notes, and documents related fragment ([#1544](https://github.com/openMF/android-client/pull/1544))
8. Collection and Individual Collection Sheet ([#1545](https://github.com/openMF/android-client/pull/1545))
9. Client related fragment ([#1550](https://github.com/openMF/android-client/pull/1550))

### Future Improvements

1. **SMS push notifications** 
<p align="justify"> 
As of now Fineract 1.x doesn't support Firebase Cloud Messaging service for sending push notifications( Triggered, Scheduled, and Direct), so this feature can be easily implemented once the FCM integration is done. 
</p>

2. **GIS support** 
<p align="justify"> 
There is no proper workflow of GIS that is developed yet, as of now it is used for tracking the path of the client which can be improved. The field officer can easily access the nearby client's location and track the path based on that. And it can also be integrated with a notification framework so that whenever he is near to any client then he will get a notification for that. 
</p>

### GSoC expierence with The Mifos Initiative
<p align="justify"> 
I had a great experience throughout this three-month-long program. The community(<a href = "https://mifos.org/"> The Mifos Initiative </a>) and my mentors (<a href = "https://www.linkedin.com/in/abhilash-g-55160a139/"> Abhilash Gunasegaran </a> and <a href = "https://www.linkedin.com/in/tarunmudgal/"> Tarun Mudgal</a>) were very supportive in this three-month-long journey.  I also want to thanks Ed Cable for his great support. The weekly check-ins were awesome, it provided me a good community bonding chance and also helped me to solve some problems which I faced in between. GSoC helped me a lot to learn and grow in a lot of aspects. I am looking forward to contributing to this organization in the future and would also like to help the new contributors to start their contributions in the community.
</p>


