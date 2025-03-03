---
title: "Provisioning Profile Doesn't Support Push Notifications"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7126543-provisioning-profile-doesn-t-support-push-notifications"
hide_table_of_contents: true
---

This article runs through troubleshooting steps when you face issues after setting up push notifications. For a step-by-step guide on how to enable push notifications in your app identifier via Apple Connect, check our documentation here.

# 

Issue Overview

When deploying an app through FlutterFlow to the Apple App Store, developers may encounter a specific error related to the "Push Notifications" capability. This article aims to illuminate this issue, explain its cause, and guiding you through the process of enabling this capability within your Apple Developer account's key identifier.

# Full Error Message

```
`Provisioning profile doesn't support the Push Notifications capability.​`
```

# Common Causes

The error message Provisioning profile doesn't support the Push Notifications capability is presented when an app that includes push notification functionality is submitted to the Apple App Store without first completing the necessary configurations. This setup is essential because the push notifications feature requires explicit permission within your Apple Developer account to function properly.

​

# Resolution Steps

## Enable the Push Notifications capability in your Apple Developer Account

To resolve this issue, follow these steps to enable the "Push Notifications" capability for your existing app:

Visit Your Apple Developer Account: Log into your Apple Developer account and navigate to the "Identifiers" section under the "Certificates, Identifiers & Profiles" area.

​
![](https://downloads.intercomcdn.com/i/o/987872016/bf4ab8d12cebd5646c1938ba/image.png?expires=1741032900&signature=64cb0165fd4189ab0841311e844635d2d52222b5cc5c63536e54c5ed30231f1b&req=fSggHs58nYBZFb4f3HP0gKokSIX5dZCAuJaQ664XqgclawqanWObFhlBl9WY%0A4IY%3D%0A)

​

Select Your App's Identifier: Identify the App ID associated with the app you are deploying. This step is critical as the adjustments you're about to make are specific to the app's identifier.

​

Enable the Capability: Within your app's identifier details, find the section for enabling capabilities. Check the option for "Push Notifications." Unlike some capabilities, there's no need to alter the primary App ID or create a new key if it's your first time enabling this capability for an App ID.

​
![](https://downloads.intercomcdn.com/i/o/987884094/4855eb7efabaa6a8df6b79af/image.png?expires=1741032900&signature=7b0a4acd6dda42e29175056a434f3d4dd72f48b86f142939e2d74dcf60132671&req=fSggHsF6nYhbFb4f3HP0gNZqReC3i5Oasu1su3C4QGDNUB%2BDgmC91L4uhcJu%0ATG0%3D%0A)

​

Save Changes: Make sure to save the changes. Even if you see UI elements suggesting further edits, enabling this feature and saving changes is enough for the initial configuration.

​

Deploy Through FlutterFlow: With the "Push Notifications" capability now enabled for your App ID, you can deploy your app through FlutterFlow without encountering the previous error.

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace