---
title: "Your app targets Android 13 (API 33) or above. You must declare the use of advertising ID in the Play Console"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7158384-your-app-targets-android-13-api-33-or-above-you-must-declare-the-use-of-advertising-id-in-the-play-console"
hide_table_of_contents: true
---

# Full Error Message 

---

```
`Google Play failed to upload artefacts. Your app targets Android 13 (API 33) or above. You must declare the use of advertising ID in Play Console.: {

 "error": {

 "code": 400,

 "message": "Your app targets Android 13 (API 33) or above. You must declare the use of advertising ID in Play Console.",

 "status": "INVALID_ARGUMENT"

 }

}`
```

---

# What does this error mean?

# What Is Advertisement ID Error?

While submitting application to the Google Play Store, sometimes you may get an error that reads "Advertisement ID Error". This error can happen when you do not have advertisements in your project but it was declared that your project has advertisement IDs or if your application has advertisement IDs, they were not correctly declared and insufficient information was provided in the Google Play Store.

## What Happens When You See the Error?

When you see this error, you will have to submit a completely new release for the application with advertisement ID already included, properly declared and sufficient information provided in the store listing.

## What Should I Do To Avoid This Error?

To avoid this error, you should always make sure that you are providing valid and sufficient information about advertising IDs in the store listing. You must provide complete details about the advertisement that includes - if there are ads appearing, if it is an in-app purchase or if it is some other type of ad. If the application does not have any advertisement, then this should also be declared properly in the store listing.

We hope this article has helped you understand more about the Advertisement ID Error. If you have any further queries, please reach out to our team.

---

# How to resolve this issue?

#### STEP 1

---

In your Google Developer Console, you have to access, the App Content section

​

![](https://downloads.intercomcdn.com/i/o/693853035/c6400a5c80a1cc06072fe9a5/Snip20230318_6.png?expires=1741032900&signature=20828329d8577fa70a2d4c1475e93e72856297e9f493fbb8e297140070458ba4&req=cikkHsx9nYJaFb4f3HP0gDnJh%2FhSrpQj63CdNYesRy6Zj7qyq3hNCGKUULvB%0AnMc%3D%0A)

#### STEP 2

---

If your application does not contain any advertisements, you would only have to select 'No' 

​

![](https://downloads.intercomcdn.com/i/o/693853720/6affb63adc73948679dff5b4/Snip20230318_7.png?expires=1741032900&signature=5103b4aa351a9c2e80832dc764b8a05d1e98c6cdfaf12e3ccc040aa6a9cabf95&req=cikkHsx9moNfFb4f3HP0gIIqBN%2BQkHfBwWlN6A5pC2FbelmXOtBn5SXYoiB6%0AK64%3D%0A)

And if your application contains advertisements, you would have to select 'Yes' in that case.

# The issue was not resolved

---

If the codemagic error still persists after following the outlined steps, please report this issue to support via Chat or Email at support@flutterflow.io.