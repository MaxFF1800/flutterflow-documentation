---
title: "This release includes the com.google.android.gms.permission.AD_ID permission but your declaration on Play Console says your app doesn't use advertising ID. You must update your advertising ID declaration."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7170290-this-release-includes-the-com-google-android-gms-permission-ad_id-permission-but-your-declaration-on-play-console-says-your-app-doesn-t-use-advertising-id-you-must-update-your-advertising-id-declaration"
hide_table_of_contents: true
---

If you are trying to deploy through the Play Store but have received this error message. This article will walk you through how to troubleshoot this issue.

# Full Error Message

```
`This release includes the com.google.android.gms.permission.AD_ID permission but your declaration on Play Console says your app doesn't use advertising ID. You must update your advertising ID declaration. I get this error when i deploy my app to play store. But in my app there is no app related content.`
```

---

# What does this error mean?

This error can happen when you do not have advertisements in your project, but you use Google Analytics in your Flutterflow project. 

Advertising Id is usually set when your app uses AdMob; however, your application may import other services/libraries that have advertising ID SDK, in this case, you will also have to declare that your application uses Advertings Id similar to Admob, but you have the option to select where specifically it is used. 

---

# How to resolve this issue?

### Enable The Advertising ID In Your Google Play Console 

In your Google Developer Console, open your project (app), this setting is specific to a project you have 
- Open your project 
- From the left tool panel
- Scroll to App content, this should be under Policy and programs
- Click App content, and select Advertising Id
- Click start to set the configuration

![](https://downloads.intercomcdn.com/i/o/693853035/c6400a5c80a1cc06072fe9a5/Snip20230318_6.png?expires=1741032900&signature=20828329d8577fa70a2d4c1475e93e72856297e9f493fbb8e297140070458ba4&req=cikkHsx9nYJaFb4f3HP0gDnJh%2FhSrpQj63CdNYesRy6Zj7qyq3hNCGKUULvB%0AnMc%3D%0A)

2. Under Advertising ID choose YES even if the app is not using Ads. 

If you use analytics, we need to choose YES on The AD_ID permission for an analytics use case in the Advertising ID section.

3. Scroll until you see Analytics and check it

![](https://downloads.intercomcdn.com/i/o/695785802/1d3a8e4da78ddd106d341055/image.png?expires=1741032900&signature=e8e9abee4c45a6b61965bd25e4cd7509af5dcd142bfbfe28e17516034ea460dd&req=cikiEcF7lYFdFb4f3HP0gA6162basBco9Fa3MSTYGVNSNsmU0jZwjYb3m0Nt%0A83I%3D%0A)

4. Remember to Save all the changes.

 

# The issue was not resolved

---

If the error persists after following the outlined steps, please report this issue to support via Chat or Email at support@flutterflow.io.