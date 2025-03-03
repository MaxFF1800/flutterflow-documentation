---
title: "Google Sign-In Troubleshooting"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6283519-google-sign-in-troubleshooting"
hide_table_of_contents: true
---

If you face any issues while using the Google Sign-in feature from the exported app, then follow the given instructions to resolve them:

# If App is Pushed to Play Store from FlutterFlow by using CodeMagic deployment:

Deploy the application to Google Play Store by using the CodeMagic Integration in FlutterFlow.
![](https://downloads.intercomcdn.com/i/o/526126119/eded7301112637e150b6e920/image.png?expires=1741032900&signature=8a0ab1f6f356cff1bde5e5c79cf081ce8f36862b61e4f0be4bbfad0afb54827c&req=cSIhF8t4nIBWFb4f3HP0gI9FreS%2BcqC6fQrOjIugVfKX65BpHjiNttwxeGEk%0A9dM%3D%0A)

After this step, head over to the Google Play Console. Here open the app from the All apps list.
![](https://downloads.intercomcdn.com/i/o/526126974/dd9e6753d277eaf99ff2330c/image.png?expires=1741032900&signature=b3b053e956bb14cc8a6e3b7288f2a31aae0c5ea32030bea5a7f25a94482102ae&req=cSIhF8t4lIZbFb4f3HP0gE8Y8JSKmxAFuN36ZFsLMvvsQD8aQ4lH7k1clpB6%0AVGc%3D%0A)

After opening the app dashboard, click on the App Integrity option under the Setup menu present on the left side of the screen.
![](https://downloads.intercomcdn.com/i/o/526127837/bed86fa31d04eb8d87cdc936/image.png?expires=1741032900&signature=9b360e8d7de6b713a3b1541a3dd53ba7ca30b96162d715d14e3c97a8e61f538c&req=cSIhF8t5lYJYFb4f3HP0gGH8o2sXy7hohcCgSDM%2F5cPRz%2Bq%2BXDaqKcciL9sY%0AXEY%3D%0A)

After opening the App Integrity section, click on the App Signing tab. Here you'll find the SHA-1 certificate fingerprint. Copy this key by clicking on the Copy Icon. 
![](https://downloads.intercomcdn.com/i/o/526131470/408d1bae9162bcb3e3d6403a/image.png?expires=1741032900&signature=ace72985ab83950d87fd2fdf5a1dcb901adcaddb38cec54a9f4e7d35a5c79726&req=cSIhF8p%2FmYZfFb4f3HP0gLxG4DggPSWFqf0h1%2BIAZdum9PTfp5%2FGwjXlglMu%0AH9U%3D%0A)

After completing the above steps, head over to the Firebase console and open the project settings of the same project.

![](https://downloads.intercomcdn.com/i/o/526135027/805de41de20a399b9c51e951/image.png?expires=1741032900&signature=ef9be9a893e51c9e070dc75d79460b96e166f4ff7f3ab9d37c5390aa8344a84b&req=cSIhF8p7nYNYFb4f3HP0gPlPd898ExMF2oJDzGNNG46dhF%2FQhAyHL5Dx4E9w%0AmwQ%3D%0A)

Here, scroll down to the find Your Apps section. Select the Android app and click on Add fingerprint. You'll need to paste the copied SHA-1 Fingerprint here and then hit Save.
![](https://downloads.intercomcdn.com/i/o/526139746/0c0d57ff6c3a7d62eadaa14e/image.png?expires=1741032900&signature=59c0d18fd8b878777ed43813f4a3442ae3caaefcfb4ebce75b99d6988c23337e&req=cSIhF8p3moVZFb4f3HP0gAD1BoeIhPsE%2FVg%2FHdhKyK5buUX9honOrDoyUFj%2F%0A4Hs%3D%0A)

After this, you'll need to Regenerate the config files from FlutterFlow. To do this, open your app in FlutterFlow and then click on Settings > Firebase.
![](https://downloads.intercomcdn.com/i/o/526141349/f8652b819ab7d9c3f098bb0d/image.png?expires=1741032900&signature=7e68a7bfbafe90deeafe6347c8fec7d76df2a1dd77e1cb9ce5641bc207835292&req=cSIhF81%2FnoVWFb4f3HP0gC2q6qSyAd8Qk4Nxmd9UI4kbFnBSD6k%2FqoLGcg%2FK%0A0DQ%3D%0A)

Here, Click on the Regenerate Config Files button and then Click on Generate Files.
![](https://downloads.intercomcdn.com/i/o/526142048/f54acfd365e0c6a943552098/image.png?expires=1741032900&signature=198f1665b9a69833e93802fdce3d2d3c408ce2d75b26a9c89c0024d1a6a94c9a&req=cSIhF818nYVXFb4f3HP0gHEstd0eiQI0DTOCAB7R4qWrIrhX8LFWlmxEXQrr%0AZqU%3D%0A)

This issue should now be resolved. You can now re-test to confirm that the issue has been fixed.

---

# If you have not yet pushed to the play store or are self-signing your app

If you're not using Play Store App Signing or have not deployed yet, follow the instructions in our documentation to use Keytool or Gradle's Signing Report to get your SHA-1.

After manually generating the SHA-1 please make sure to update it in Firebase and then regenerate the config files in FlutterFlow using these instructions:

Head over to the Firebase console and open the project settings of your project.

![](https://downloads.intercomcdn.com/i/o/526135027/805de41de20a399b9c51e951/image.png?expires=1741032900&signature=ef9be9a893e51c9e070dc75d79460b96e166f4ff7f3ab9d37c5390aa8344a84b&req=cSIhF8p7nYNYFb4f3HP0gPlPd898ExMF2oJDzGNNG46dhF%2FQhAyHL5Dx4E9w%0AmwQ%3D%0A)

Here, scroll down to the find Your Apps section. Select the Android app and click on Add fingerprint. You'll need to paste the copied SHA-1 Fingerprint here and then hit Save.
![](https://downloads.intercomcdn.com/i/o/526139746/0c0d57ff6c3a7d62eadaa14e/image.png?expires=1741032900&signature=59c0d18fd8b878777ed43813f4a3442ae3caaefcfb4ebce75b99d6988c23337e&req=cSIhF8p3moVZFb4f3HP0gAD1BoeIhPsE%2FVg%2FHdhKyK5buUX9honOrDoyUFj%2F%0A4Hs%3D%0A)

After this, you'll need to Regenerate the config files from FlutterFlow. To do this, open your app in FlutterFlow and then click on Settings > Firebase.
![](https://downloads.intercomcdn.com/i/o/526141349/f8652b819ab7d9c3f098bb0d/image.png?expires=1741032900&signature=7e68a7bfbafe90deeafe6347c8fec7d76df2a1dd77e1cb9ce5641bc207835292&req=cSIhF81%2FnoVWFb4f3HP0gC2q6qSyAd8Qk4Nxmd9UI4kbFnBSD6k%2FqoLGcg%2FK%0A0DQ%3D%0A)

Here, Click on the Regenerate Config Files button and then Click on Generate Files.
![](https://downloads.intercomcdn.com/i/o/526142048/f54acfd365e0c6a943552098/image.png?expires=1741032900&signature=198f1665b9a69833e93802fdce3d2d3c408ce2d75b26a9c89c0024d1a6a94c9a&req=cSIhF818nYVXFb4f3HP0gHEstd0eiQI0DTOCAB7R4qWrIrhX8LFWlmxEXQrr%0AZqU%3D%0A)
 
This issue should now be resolved. You can now re-test to confirm that the issue has been fixed.

​
---

You can also refer to the Google Play Services documentation for more information.