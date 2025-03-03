---
title: Google Play Store Deployment Issues
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6157034-google-play-store-deployment-issues"
hide_table_of_contents: true
---

# You uploaded an APK or Android App Bundle that was signed in debug mode. You need to sign your APK or Android App Bundle in release mode

You'll need to modify your android/app-level build.gradle file and replace debug with release. You'll need to replace the debug keyword with the release.

Here are the instructions on how to do this:

Find the debug keyword under buildTypes in android/app/builld.gradle in your project folder.

![](https://flutterflow.intercom-attachments-1.com/i/o/500371940/80e55cb9c4eb1c8f3e6262e5/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FgE7XKijedwD802kR4wWn-2Fimage.png?expires=1741032900&signature=5043f6f5e7c185fee3f179093b855c9f335a0be68f47c7ee37e8ab6f15a60f9d&req=cSAnFc5%2FlIVfFb4f3HP0gJ%2FMWmoo7FKn9tmeu5h2%2FgHd5AEJx6EEKQi7i1wM%0AebY%3D%0A)

Replace the debug keyword with release and then save the file.

![](https://flutterflow.intercom-attachments-1.com/i/o/500371945/f53840878e0f78c40cb752ba/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FLkCDXDCpP9iRSrS7NHil-2Fimage.png?expires=1741032900&signature=4a7699e856e614f06016dfe3c457d9358cf825862782dd9bc9652544368920ef&req=cSAnFc5%2FlIVaFb4f3HP0gBltbOoJy5CwnixhWmFVLk3NfWQF0aay3QvLh1t5%0AXds%3D%0A)

​
---

​
Publishing app-release.aab to Google Play Published app-release.aab to track internal Google Play failed to upload artifacts. Only releases with status draft may be created on draft app.
Please make sure that you fill out all the information in the play store including the store listing information and the setup information.

---

# Common Issues with PlayStore Deployment with Code Magic

Here are some common issues that you might face while deploying your app to the Google Play Store.

## 

​