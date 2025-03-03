---
title: "APK specifies a version code that has already been used."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

## Full Error Message

---

```
`Publishing failed :|

Google Play failed to upload artefacts. APK specifies a version code that has already been used.: {

"error": {

"code": 403,

"message": "APK specifies a version code that has already been used.",

"status": "PERMISSION_DENIED"

}

}`
```

​What Does This Error Mean?

---

The version of the application published conflicts with an earlier version that was already published and will need to be updated

​

​How do I Resolve This Issue?

---

When Deploying Directly From FlutterFlow. 

Navigate to the Settings And Integrations > Mobile deployment. 

​

![](https://downloads.intercomcdn.com/i/o/793281793/615016fa064c8c3140042bc4/Snip20230726_1.png?expires=1741032900&signature=0d68c20a539463cf6dab4b1351b7239fe94fdd48a70f4a80082c62f466f79f67&req=cykkFMF%2FmohcFb4f3HP0gAEl4p89dikJfoYyyJ04AaTLO6UzoMXCCtWgMCyy%0A7jQ%3D%0A)

App Version: This refers to the version that the application will be set to. Setting a version number is optional, but may be required for specified cases. 

​Build Number: The build number is used for deployment. Each time it is successfully deployed this should increase by 1 until a new version is set (at which point it will be reset to 1)

If left empty, it will automatically increment the build number each time it is deployed. 

​

​After incrementing the app version and build number from the previous one, you can deploy it once more.

​

​2. Deploying From GitHub 

Step 1: Open the pubspec.yaml file.

Step 2: Locate the version tag.

Step 3: Update the build name and number such as version: ^1.0.2+2.

NB: Use the latest Flutter version package

Step 4: Open the terminal and hit the flutter clean command.

Step 5: Build the app.

![update app version in flutter](https://flutterflow.intercom-attachments-1.com/i/o/793287693/bb7b5ca0fbed31517d0419f7/update-app-version-flutter-1024x831.png?expires=1741032900&signature=67cfdc94df7282a13a84a52a027f632467d4bda57f784ca649aeea26f230cd72&req=cykkFMF5m4hcFb4f3HP0gMSJRQV63Zlx3IGkrny%2BZs78p9%2Bx%2BFV4hPDChXii%0ARQ4%3D%0A)

The Issue Is Not Resolved

---

If this issue is not resolved, please contact support@flutterflow.io

## 

​