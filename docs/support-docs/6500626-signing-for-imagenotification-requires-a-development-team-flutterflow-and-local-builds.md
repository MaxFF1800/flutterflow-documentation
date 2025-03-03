---
title: "Signing for \"ImageNotification\" requires a development team - Flutterflow and Local builds"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6500626-signing-for-imagenotification-requires-a-development-team-flutterflow-and-local-builds"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

---

# Introduction

---

Builders often encounter issues when attempting to sign the "ImageNotification" feature within their applications, especially when configuring their projects in IDEs (Integrated Development Environments) and also directly from the Apple Store developer console. This process is crucial for ensuring the application's integrity and security, as it involves selecting the appropriate development team and configuring the signing certificates correctly.

The mindmap below shows how the 'ImageNotification' works and how it is utilized.

![](https://downloads.intercomcdn.com/i/o/980031533/a2e2edc56a6e1a46fe5802b6/diagram+%281%29.png?expires=1741032900&signature=563e99157effa35edd47c6a991307a645e18505138ee8e745cf90788f8c95fa1&req=fSgnFsp%2FmIJcFb4f3HP0gFO9GQnadSkvb0PXxfhqk4h%2FzcSvxqRA77YZ%2BMyt%0ATwU%3D%0A)

# What Does This Error Mean?

You have received this error because the Identifier required by Apple to send push notifications was not added to your Apple Developer Account.

## 

​Full error message

​Error (Xcode): Signing for "ImageNotification" requires a development team. Select a development team in the Signing & Capabilities editor.

---

## Make sure you have completed the Apple Developer setup

Please ensure that the required configurations are set up in the Apple Developer Console: iOS Push Notifications Configurations 

---

# 

​How To Resolve This Issue?

---

## Deploying Through FlutterFlow Mobile Deployment

These are the steps to follow if you are building from FlutterFlow instead of GitHub in this case. 

Having reviewed the guidelines on how to add an identifier in the Apple Developer console. 

In the Apple Developer console, under the Identifiers section:

![](https://downloads.intercomcdn.com/i/o/980061123/c233809c68653d180a2fb7f3/Account_-_Apple_Developer.png?expires=1741032900&signature=45ac6b27acb7372afcff2408d31eaf448afe55612685a7f22ada5d3074246b83&req=fSgnFs9%2FnINcFb4f3HP0gE9o4wYlH4X9aUMrpb2jVUx8d%2F2u%2FSP9ZWVnM6zI%0AstI%3D%0A)

Please verify that an identifier is created with the name 'ImageNotification' and the Identifier set to be the package name of your app + plus the extension .ImageNotification appended to it.

![](https://downloads.intercomcdn.com/i/o/980061486/c8f51958a984eeb302015118/Naming+Identifier_.png?expires=1741032900&signature=0fa459e5c309a374a0a5acaf10c19f4eb2b5d33e8ba2f8e705ea6c9d81971be1&req=fSgnFs9%2FmYlZFb4f3HP0gA%2F6AoMnzd%2FnO%2F6klZ6YDr6tJG2s97j9sSflgFLi%0AwZc%3D%0A)

## Verification Of Identifier And Capabilities

Register an Identifier of type App IDs

![](https://downloads.intercomcdn.com/i/o/980068857/733cc72335d99b2acaa3256d/App_IDs.png?expires=1741032900&signature=d62e4fc71f153f020953ad268dc8f7aa1ab9ceffaa4ec8951ab729ee775fc8ec&req=fSgnFs92lYRYFb4f3HP0gB9bgDb6UQ8YouYm%2BAODzatbI8aWXpHOpZB00v8B%0AztE%3D%0A)

Select the type 'App' then click 'Continue'

![](https://downloads.intercomcdn.com/i/o/980069091/cd1d68db1632648745f9d8bd/Type+of+App.png?expires=1741032900&signature=1885e20b9e34927a3efaa4dae30409c67ffc9f040bf4076c0978d2fac03ba794&req=fSgnFs93nYheFb4f3HP0gDH9skLcjgfZfmVgS1uf33xguzUI82s0vMttSObF%0AiRo%3D%0A)

Set the description to 'ImageNotifcation' and the bundle ID to the package name of your application + the extension '.ImageNotification' appended at the end. 

![](https://downloads.intercomcdn.com/i/o/980069263/220063a13fb96063961107f2/ImageD.png?expires=1741032900&signature=cb471919e43062a32bb62daf15bd0656cc23aa773fba4bbe979ba35c6617b87e&req=fSgnFs93n4dcFb4f3HP0gPZ8OtH7vOizz84eHMVHAsIHzyDjY9TcgXjsWVSi%0A1PI%3D%0A)

Enable the Push Notification capability and continue from there. 

​

![](https://downloads.intercomcdn.com/i/o/980069824/c8bbf562534c4c82c24a9f73/PN.png?expires=1741032900&signature=bfaeb4420828e8f25b372353c3db23bcab95fc4c9ef8a5ef1b9feba564d02e22&req=fSgnFs93lYNbFb4f3HP0gAS5%2BWDBiBGklrII2r0UfGOryF0qfseKTftI4lN4%0AIlc%3D%0A)

The Identifier should be created from there and it will take up the form shown in the image below. 

![](https://downloads.intercomcdn.com/i/o/980070091/32229935a858af30603eb1d1/P.png?expires=1741032900&signature=6e97536c50c9c6e4182a5b9ee1f6b221990c4286c8dd7e9c49f205f63f301d1b&req=fSgnFs5%2BnYheFb4f3HP0gGk2KD%2BktBbXeQg9UXrKC85bEfoOMjiFzE0XTZt%2B%0AanQ%3D%0A)

You should be set to deploy to your application once more! 

## 

Deploying Through GitHub

---

These are the steps to follow if you are deploying from GitHub inside of FlutterFlow. 

​

To fix this error you need to add an Apple Developer Team Profile to your Xcode project. 

​

1. First, you'll need to open the iOS folder inside the project file in Xcode.

​

![](https://downloads.intercomcdn.com/i/o/792691938/a939833ff69659fca9068765/SCR-20230725-oyii.png?expires=1741032900&signature=6973c91947d1ddc02a2bbc9a9eac1030b8ccd83a1143d7d974c15c9aebaaa407&req=cyklEMB%2FlIJXFb4f3HP0gIGeh0V6TNoyqsLNCOf74K2SOZpGAn1nwHmkZn%2BX%0Au7E%3D%0A)

2. After that, you will need to click on the runner folder of the project and select the sign-in and Capabilities option

​

![](https://downloads.intercomcdn.com/i/o/792692984/72f7f76704b223bc213a1738/SCR-20230725-oyru.png?expires=1741032900&signature=af787a84a6692008ba43a638beba471f1714cc696d1eec308f04ee2c5e3ec4fc&req=cyklEMB8lIlbFb4f3HP0gN6Bw2QGC2jS38px3zMTroVZ6Auu5SmEpFuwrKFT%0Acww%3D%0A)

3. You should be able to see the tab shown in the screenshot. Click on add account, Once you add the profile, you should see the list of teams appear at the top of the signing and capabilities panel. You can select the one that matches the team you would like to use, save the settings, and then try to build the project again.

​

![](https://downloads.intercomcdn.com/i/o/792694059/e7e34f562f486af909052699/SCR-20230725-oyuq.png?expires=1741032900&signature=10922c05d69e2eb055785d2ddf3da89783305b8248ccdb992dcdce52d337b29f&req=cyklEMB6nYRWFb4f3HP0gGUkXfTaG6hbv09DY%2Bs%2BNwm%2FXtOx5SSMj4KGEP%2Bw%0A%2BVU%3D%0A)

## 

​The issue Was Not Resolved

---

You must use these instructions to add this identifier to your Apple Developer Account.

If this does not resolve the issue once more, contact FlutterFlow Support at support@flutterflow.io

# Additional Relevant Resources

---

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help