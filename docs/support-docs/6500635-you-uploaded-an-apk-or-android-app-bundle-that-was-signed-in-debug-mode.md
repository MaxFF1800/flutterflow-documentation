---
title: "You uploaded an APK or Android App Bundle that was signed in debug mode."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6500635-you-uploaded-an-apk-or-android-app-bundle-that-was-signed-in-debug-mode"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

You need to sign your APK or Android App Bundle in release mode instead of debug mode.

# Full error message

```
`You uploaded an APK or Android App Bundle that was signed in debug mode. You need to sign your APK or Android App Bundle in release mode

`
```

# How to resolve this issue?

You'll need to modify your android/app level build.gradle file and replace debug with release.

​

Step 1: Find the debug keyword under buildTypes in android/app/builld.gradle in your project folder

![](https://flutterflow.intercom-attachments-1.com/i/o/568786373/5904db08ea7e3f4ac6320c2f/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FgE7XKijedwD802kR4wWn-2Fimage.png?expires=1741032900&signature=4b460d9dd34856376af1cd8474de6dac3f0b4d058fc90dc81cc1f9106d4d886b&req=cSYvEcF4noZcFb4f3HP0gFS6CK8KXXuDsV9VFpJ7u7rT2udYyL%2FCc%2FfgtF5g%0Aemg%3D%0A)

Step 2: Replace the debug keyword with release and then save the file

![](https://flutterflow.intercom-attachments-1.com/i/o/568786375/e2582bf6f64ffd80b36df6b6/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FLkCDXDCpP9iRSrS7NHil-2Fimage.png?expires=1741032900&signature=a85edba791b40e07e9d53114a035183e710fefc26eb43dd4826744fd70b583a8&req=cSYvEcF4noZaFb4f3HP0gJasQIufbeJ0Fi79EyEmMH%2FAaa8LvXj2wAFa%2BCQY%0Ah3I%3D%0A)

Step 2: Replace the debug keyword with release and then save the file

The issue was not resolved

If this does not resolve the issue, contact FlutterFlow Support at support@flutterflow.io