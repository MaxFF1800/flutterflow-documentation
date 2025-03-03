---
title: "Can't upload photo to Content Manager"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6369337-can-t-upload-photo-to-content-manager"
hide_table_of_contents: true
---

Our default rules don't allow for upload in CMS. In order to do this, you will need to update your Firestore Rules. 

Open your FlutterFlow project and click Settings & Integrations > Firebase > Open Firebase Console 

![](https://downloads.intercomcdn.com/i/o/542854442/a848ea328c634a544ac6a618/image.png?expires=1741032900&signature=37e77b08b0d6e888330898fe1433501f4e6206f21aa74cd42e262e750669634b&req=cSQlHsx6mYVdFb4f3HP0gH%2B8y3dLHosMaLWLwstSOoWm7m%2FH5OOhlZdlN0bh%0Apb0%3D%0A)

Next click Storage > Rules

![](https://downloads.intercomcdn.com/i/o/554302220/3d7ca83d858ee58a13badf96/image.png?expires=1741032900&signature=57578fb1a2e34e9fc9ffedaaec2915e3aeb2e82365d6bb3c178ff1148304a43c&req=cSUjFcl8n4NfFb4f3HP0gDmX2PIAnHLVP7H5qAkE5Nrb5%2BpcYuRLtMfnnsGq%0AD8k%3D%0A)

Replace the code with the following and then click publish

```text
rules_version = '2';

service firebase.storage{

match /b/{bucket}/o {

match /{allPaths=**} {

allow read, write: if request.auth != null;

}}

}
```

Important: We recommend reviewing your Firebase rules before deploying your app. Please see this link for additional information on Firestore security rules.