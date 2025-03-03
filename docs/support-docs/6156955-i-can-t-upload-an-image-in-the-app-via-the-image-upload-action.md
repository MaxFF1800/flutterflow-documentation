---
title: "I can't upload an image in the app via the image upload action."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6156955-i-can-t-upload-an-image-in-the-app-via-the-image-upload-action"
hide_table_of_contents: true
---

This is a common issue that may arise due to the misconfiguration in Firebase Storage. This can be fixed by updating the Firebase Storage rules. 

Here are the instructions on how to do this.

Head over to the Storage section in your Firebase project and click on the Rules tab.

![](https://flutterflow.intercom-attachments-1.com/i/o/500359052/d12a36595db25ca568c55345/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FyN3xeSPb6dOpVkmzceDp-2FAnimation.gif?expires=1741032900&signature=7546788e7670bb46a28f61a717ef84c89a793a2a67339d953185aa3c3928f873&req=cSAnFcx3nYRdFb4f3HP0gN3MkWzK6Z7l2rgvaM1gNEnzExf7wBGwncxdf7TU%0AIkw%3D%0A)

Here you would need to replace the current rules with the rules given below.

```
`rules_version = '2';

service firebase.storage{

	match /b/{bucket}/o{

 	match /{allPaths=**}{

 	allow read, write: if request.auth != null;

 }

 }

}`
```

![](https://flutterflow.intercom-attachments-1.com/i/o/500359072/1359c0ef972d65f0573d992e/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FrHsa05RPyNDabl761lAA-2Fstorage-20rules.gif?expires=1741032900&signature=ff068c543b82b609b697c132229120a0641bc745176b2f7b5e934d1730f68359&req=cSAnFcx3nYZdFb4f3HP0gPNLeaSJdJU6SdV62sKo5%2B5FE3v546tOBs4Eydt0%0AR8k%3D%0A)

This should fix the issue with uploading media in the application. If you still face this issue then please make sure to re-upload all the previously uploaded images from the application.