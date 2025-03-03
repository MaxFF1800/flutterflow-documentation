---
title: "Google Play failed to upload artefacts. Package not found."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6500652-google-play-failed-to-upload-artefacts-package-not-found"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

This issue can result from two scenarios: when it is the first time you are deploying your application to the Play Store, or when you update your app's package name but don't update the config files.

## Full Error Message

```
`Google Play failed to upload artefacts. Package not found: com.flutterflow.appname.: {

 "error": {

 "code": 404,

 "message": "Package not found: com.flutterflow.appname.",

 "status": "NOT_FOUND"

 }

}

`
```

# How to resolve this issue?

### First time project deployment

To resolve this issue for first time project deployme to play sore, you will need to download the AAB that was generated and manually upload it to paystore.This is required for teh initial first time deployment, after that the subsiquest deployment should go on without any disruption or the same error being through 

Click on the button marked "AAB" to download the build.

Open your Play Store account under the registered project, and upload it as a release depending on the track you are uploading the build to.

![](https://downloads.intercomcdn.com/i/o/1151804561/cc7704115428f77a4dc40f3f/image.png?expires=1741032900&signature=f735a41cf9532ed21a7c2dad5f67fd10e72efb7f4e6ff0f2ef1972f140527b21&req=dSEiF8F%2BmYRZWPMW1HO4zVPIAu7ZBaHlFk5gFvunc46cNrDY3APt8Df2HEnP%0AsZO2%0A)

### Package Id update 

To resolve this issue, please follow the following steps.

You'll need to Regenerate the config files from FlutterFlow. To do this, open your app in FlutterFlow and then click on Settings > Firebase.

​
![](https://downloads.intercomcdn.com/i/o/526141349/f8652b819ab7d9c3f098bb0d/image.png?expires=1741032900&signature=7e68a7bfbafe90deeafe6347c8fec7d76df2a1dd77e1cb9ce5641bc207835292&req=cSIhF81%2FnoVWFb4f3HP0gC2q6qSyAd8Qk4Nxmd9UI4kbFnBSD6k%2FqoLGcg%2FK%0A0DQ%3D%0A)

Here, Click on the Regenerate Config Files button, Enter the new package name and then Click on Generate File.

​
![](https://downloads.intercomcdn.com/i/o/526142048/f54acfd365e0c6a943552098/image.png?expires=1741032900&signature=198f1665b9a69833e93802fdce3d2d3c408ce2d75b26a9c89c0024d1a6a94c9a&req=cSIhF818nYVXFb4f3HP0gHEstd0eiQI0DTOCAB7R4qWrIrhX8LFWlmxEXQrr%0AZqU%3D%0A)

This issue should now be resolved. You can now re-deploy to confirm that the issue has been fixed.

# Issue was not resolved after following the given steps

If you are deploying from FlutterFlow and still getting this error after following all the steps outlined above, then please report this issue to support via Chat or Email at support@flutterflow.io.

​