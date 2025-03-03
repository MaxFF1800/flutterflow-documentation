---
title: "Google Play failed to upload artefacts. The Android App Bundle was signed with the wrong key. Found: SHA1: XX:XX:XX:XX. Expected YY:YY:YY:YY"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6454854-google-play-failed-to-upload-artefacts-the-android-app-bundle-was-signed-with-the-wrong-key-found-sha1-xx-xx-xx-xx-expected-yy-yy-yy-yy"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

One of the most common causes of a publishing error when deploying to the Google Play Store is attempting to deploy using the wrong Keystore file.

# Full error message

```
`Google Play failed to upload artefacts. The Android App Bundle was signed with the wrong key. Found: SHA1: XX:XX:XX:XX. Expected YY:YY:YY:YY 

`
```

# How to resolve this issue?

If you are not using GitHub, contact support@flutterflow.io

​

# Verify That The Correct Keystore File Was Submitted For Signing

To create a new keystore, please run the following commands in your Integrated Development Environment

keytool -genkey -v -keystore ~/upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload

If the application was already deployed and the previous keystore was misplaced, contact Google Support for further assistance.

# Verify That Build.Grade File Was Correctly Modified

It is helpful to check the build.gradle file was modified to include the changes illustrated in the Google Play deployment documentation.

# Verify your application was submitted in Release Mode

Debug mode is when the application is still in development. In debug mode, the source code is not optimized for production, and the performance of the application might not be optimal. The application should be signed in Release Mode when it is ready to be published to the app stores. Signing the application in Release Mode will result in code optimization and much better application performance. To check:

Check whether the application is signed in Release Mode instead of Debug Mode
If you see debug mode, you need to use these steps to fix it 
![](https://downloads.intercomcdn.com/i/o/560054841/179a49a5ad1687f96b48773f/DebugMode.png?expires=1741032900&signature=3cbb46f71b2b993ef9329b99f8cf76b9bfaa19f5eea1784b0099e57920801713&req=cSYnFsx6lYVeFb4f3HP0gI8r3FbBfSECwN01YB8ODweRz9Qcvtt8wVF5peG%2B%0A7bo%3D%0A)

The issue was not resolved
If you are deploying from FlutterFlow and still getting this error after following all the steps outlined in our documentation, then please report this issue to support via Chat or Email at support@flutterflow.io.

​