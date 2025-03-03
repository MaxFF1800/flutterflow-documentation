---
title: "Failed Step: Generate Launch Icon Could not find package \"flutter_launcher_icons\""
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6517947-failed-step-generate-launch-icon-could-not-find-package-flutter_launcher_icons"
hide_table_of_contents: true
---

## Full Error Message

```
`Codemagic Deploy Output 

Failed Step: Generate Launch Icon Could not find package "flutter_launcher_icons". Did you forget to add a dependency? pub finished with exit code 65. Build failed: Step 5 script 'Generate Launch Icon' exited with status code 65. `
```

What does this error mean?

The flutter icon launcher dependency was not recognized in the source code. 

How do I resolve this issue?

When deploying directly from FlutterFlow. 

![](https://downloads.intercomcdn.com/i/o/572673164/5c16e148c39e12a5e6a137ce/App_Launcher_Icon.gif?expires=1741032900&signature=344666330dd24ba9c50d2a0fab985aa0fb3288b919c96df3e68cf672d48fbca7&req=cSclEM59nIdbFb4f3HP0gAwfizOtQgiECsBRl12IHqVDLhcgrzo9nulVVYKC%0AFnQ%3D%0A)

Navigate to the settings and integrations > App Assets. 

If the Splash Screen and Launcher Icon are already set, clear them and re-upload once more. 

2. Deploying from GitHub 

Requirements

Package flutter_launcher_icons 0.10.0 or higher

android.png (App icon for Android)

ios.png (App icon for iOS)

1. Add the flutter_launcher_icon package to the pubspec.yaml

 
dev_dependencies:

 flutter_launcher_icons: "^0.10.0"

flutter_icons:

 android: true

 ios: true

 image_path_ios: "assets/images/launcher/ios.png"

 image_path_android: "assets/images/launcher/android.png"

 

Whereby, 

1. dev_dependencies: flutter_launcher_icons: “0.10.0”: Refers to the package version that will be installed

2. image_path_ios: This is the location where the application launcher image for ios is found.

3. image_path_android: Just like image_path_ios, image_path_android refers to the location where the app launcher image for android is stored.

​

2. Build and run the application

To run and build the application, run the following source code in your integrated development environment 

​

```
`flutter pub get

flutter pub run flutter_launcher_icons:main

flutter run`
```

This was not resolved. 

If the issue still persists, contact support@flutterflow.io for further assistance.