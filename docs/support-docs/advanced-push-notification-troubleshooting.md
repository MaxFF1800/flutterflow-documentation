---
title: Advanced Push Notification Troubleshooting
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

If push notifications are not sending as expected, this article will help you identify and correct the most common issues.

Please note that push notifications will not work in these situations:

Push notifications will not work on an iOS simulator. To test you will need to use a real device. Here are instructions on how to do this.

Push notifications will not work if the user is not logged in to your app.

Push notifications will not work if you have the app open on your device. 

---

# Ensure you have created a push notification key for Apple.

Apple requires developers to create a key for the push notifications inside the Apple Developer Console to verify the push notification's sender.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles > Keys.

![](https://downloads.intercomcdn.com/i/o/500867400/c4e2a7314b415f9a82cb4c72/image.png?expires=1741032900&signature=3e9a2107f2fc13970951b89edaa44b1ab5f5f07d0d2341d35837ff883207218c&req=cSAnHs95mYFfFb4f3HP0gHt%2BathP3Aoj0ZfTfytqdBXaLzVVB62h5%2B8Bxeus%0AejU%3D%0A)

If you haven't added a push notification key, you will need to add this.

Here are instructions on how to add a push notification key.

​

---

# Ensure you have added the APN key to Firebase.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Project Settings > Cloud Messaging.

Scroll down to the iOS section. If you have no files listed under APNs Authentication Key (like the photo below), you need to upload the APN Key.

![](https://downloads.intercomcdn.com/i/o/500871590/fdf5e9298a8c9bca3588606b/image.png?expires=1741032900&signature=8a0d06031326651833b294beb9abd345cded40ead075fab52a986fb0ecc3e962&req=cSAnHs5%2FmIhfFb4f3HP0gCSJJOSRvrG94eVk5%2FGBHZdqSzqn3Ql0lt7u91o%2B%0AqFw%3D%0A)

Here are the instructions on how to upload the APN key to Firebase.

​

---

# Ensure you have added a push notification identifier for Apple.

You must add an Identifier to be able to send the push notifications to the iOS devices after you deploy your app to the app store.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles.

![](https://downloads.intercomcdn.com/i/o/500861775/438eecc997ce015b2d565c1a/image.png?expires=1741032900&signature=27da22a294cbe0e0756ac7002439fd73e04886a576ec9ae815bdf4eda26de458&req=cSAnHs9%2FmoZaFb4f3HP0gOnz3GAOTcrwxnTp3BeKsLhrYA7RjAjjYY4LQOCt%0A34M%3D%0A)

If you haven't created a push notification identifier, you will need to add this.

Here are instructions on how to create your push notification identifier.

---

# Ensure you are using the latest version of FlutterFlow

To upgrade to the latest version of FlutterFlow select Ctrl + R on Windows or Cmd + R on Mac. 

After you have done this, clear your browser cache and log out/in to FlutterFlow.

---