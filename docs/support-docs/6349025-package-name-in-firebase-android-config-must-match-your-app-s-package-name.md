---
title: "Package name in firebase android config must match your app's package name"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6349025-package-name-in-firebase-android-config-must-match-your-app-s-package-name"
hide_table_of_contents: true
---

This is a common issue which arises when the package name defined in FlutterFlow is changed recently and when it doesn't matches with the Firebase config files.

Tip: Make sure that your package name matches exactly in FlutterFlow and Firebase (this includes capitalization, spacing, etc.)

In order to resolve this issue please follow the following steps.

You'll need to Regenerate the config files from FlutterFlow. To do this, open your app in FlutterFlow and then click on Settings > Firebase.

![](https://downloads.intercomcdn.com/i/o/526141349/f8652b819ab7d9c3f098bb0d/image.png?expires=1741032900&signature=7e68a7bfbafe90deeafe6347c8fec7d76df2a1dd77e1cb9ce5641bc207835292&req=cSIhF81%2FnoVWFb4f3HP0gC2q6qSyAd8Qk4Nxmd9UI4kbFnBSD6k%2FqoLGcg%2FK%0A0DQ%3D%0A)

Here, Click on the Regenerate Config Files button, Enter the new package name and then Click on Generate File.

![](https://downloads.intercomcdn.com/i/o/526142048/f54acfd365e0c6a943552098/image.png?expires=1741032900&signature=198f1665b9a69833e93802fdce3d2d3c408ce2d75b26a9c89c0024d1a6a94c9a&req=cSIhF818nYVXFb4f3HP0gHEstd0eiQI0DTOCAB7R4qWrIrhX8LFWlmxEXQrr%0AZqU%3D%0A)

This issue should now be resolved. You can now re-test to confirm that the issue has been fixed.