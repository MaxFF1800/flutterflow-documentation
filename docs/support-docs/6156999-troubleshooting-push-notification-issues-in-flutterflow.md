---
title: Troubleshooting Push Notification Issues in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6156999-troubleshooting-push-notification-issues-in-flutterflow"
hide_table_of_contents: true
---

Push notifications are a crucial feature in mobile applications, allowing you to engage with your users and keep them informed about important updates. However, sometimes push notifications may not send as expected, leaving you and your users frustrated. In this article, we'll guide you through the most common issues that can cause push notification failures in FlutterFlow and provide you with step-by-step solutions to resolve them.

![](https://downloads.intercomcdn.com/i/o/1004946547/bf9634e91470264a633a3c0b/pushNotifcationError.JPG?expires=1741032900&signature=dd1a9a44c29c0403c541cbe4284e7e9f01b66cf3bd9e93be17fa93a735aefe0c&req=dSAnEsB6m4RbXvMW1HO4zcIhl%2F%2BMNrqv2kpKuo%2BCP83Wso4VHOnHAaSt2ZnY%0A9Zv2%0A)

Please note the following situations where push notifications do not work by design:

Push notifications will not work on an iOS simulator. To test you will need to use a real device. Here are instructions on how to do this.

Push notifications will not work if the user is not logged in to your app.

Push notifications will not work if you have the app open on your device.

## 

# With Codemagic Deployment

---

## Ensure your Blaze Plan is active for Firebase.

Even if you've previously subscribed, it's always good to double-check this and make sure your subscription status hasn't changed.

Head to the Firebase Console and select Project Settings > Usage & Billing > Details & Settings. 

![](https://downloads.intercomcdn.com/i/o/500855770/5e647556893ffab9d036ec25/image.png?expires=1741032900&signature=afd844c02f717cb96cc88117b626ff8ed3afa277db03889cee5d953d7a3bf25c&req=cSAnHsx7moZfFb4f3HP0gISU9wGOMRor01jq9Jagpltv32t5GUuDKLgAX7lu%0AjSU%3D%0A)

If you see Spark listed, you will need to select Modify Plan and upgrade to a Blaze Plan. 

Click here for more information on Firebase pricing plans.

---

## Ensure you have created a push notification key for Apple.

Apple requires developers to create a key for the push notifications inside the Apple Developer Console to verify the push notification's sender.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles > Keys.

![](https://downloads.intercomcdn.com/i/o/500867400/c4e2a7314b415f9a82cb4c72/image.png?expires=1741032900&signature=3e9a2107f2fc13970951b89edaa44b1ab5f5f07d0d2341d35837ff883207218c&req=cSAnHs95mYFfFb4f3HP0gHt%2BathP3Aoj0ZfTfytqdBXaLzVVB62h5%2B8Bxeus%0AejU%3D%0A)

If you haven't added a push notification key, you will need to add this.

Here are instructions on how to add a push notification key.

​

---

## Ensure you have added the APN key to Firebase.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Project Settings > Cloud Messaging.

Scroll down to the iOS section. If you have no files listed under APNs Authentication Key (like the photo below), you need to upload the APN Key.

![](https://downloads.intercomcdn.com/i/o/500871590/fdf5e9298a8c9bca3588606b/image.png?expires=1741032900&signature=8a0d06031326651833b294beb9abd345cded40ead075fab52a986fb0ecc3e962&req=cSAnHs5%2FmIhfFb4f3HP0gCSJJOSRvrG94eVk5%2FGBHZdqSzqn3Ql0lt7u91o%2B%0AqFw%3D%0A)

Here are the instructions on how to upload the APN key to Firebase.

​

---

## Ensure you have added a push notification identifier for Apple.

You must add an Identifier to be able to send the push notifications to the iOS devices after you deploy your app to the app store.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles.

![](https://downloads.intercomcdn.com/i/o/500861775/438eecc997ce015b2d565c1a/image.png?expires=1741032900&signature=27da22a294cbe0e0756ac7002439fd73e04886a576ec9ae815bdf4eda26de458&req=cSAnHs9%2FmoZaFb4f3HP0gOnz3GAOTcrwxnTp3BeKsLhrYA7RjAjjYY4LQOCt%0A34M%3D%0A)

If you haven't created a push notification identifier, you will need to add this.

Here are instructions on how to create your push notification identifier.

---

## Ensure you have added the required cloud permissions

For push notifications to work, you will need to add the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Users & Permissions. 

If you don't have Cloud Functions Admin, Editor, and Service Account listed next to fireabse@flutterflow.io, you have not completed this step.

![](https://downloads.intercomcdn.com/i/o/501028815/d4d5ea7c25cc3f0f78aa459a/image.png?expires=1741032900&signature=108d49a8022ae903c290a081fa5ef9b8f7c7c7060aa44794c0afb2f140fc10e9&req=cSAmFst2lYBaFb4f3HP0gN%2F1m%2Bu6JT8H1hOQeSs8p7Fnl4slsaAHCw%2Bs5eE4%0Ag%2B8%3D%0A)

Here are the instructions on how to add the required cloud permissions to your project.

---

## Ensure your cloud function region is the same in FlutterFlow and Firebase 

We have an option in setting/firebase/advance you can change your data center region. In case you change this, it may be the cause of the notification deployment issue you are facing

​

Check your GCP location in your firebase project/setting.

​

![](https://downloads.intercomcdn.com/i/o/712004352/47a828c18cdd550aa45797dd/image.png?expires=1741032900&signature=89efcaacf8d4d5f5f185b091a95f194ccf6c917190951cdf6a78e435f9835062&req=cyElFsl6noRdFb4f3HP0gF0QyUPuXDJ4okesWQqpDwLzLjMvaapbKh29BWMh%0A%2F4c%3D%0A)

Make sure in FlutterFlow project / Setting / Firebase / Advance the cloud functions region is set to default, or the same region you have in your setting.

In my case, it is set by default and it is good.

​

![](https://downloads.intercomcdn.com/i/o/712006151/d76e53981d0ba98e4b053a25/image.png?expires=1741032900&signature=249797dc65db42568d956bd7f2959ae047375dd222c766d3e9762f426b6aa507&req=cyElFsl4nIReFb4f3HP0gNU69Qng3xSnPchcH7ixaOIjUgEgUq014KJZONl%2F%0AgNo%3D%0A)

---

## Ensure you are using the latest version of FlutterFlow

To have access to the latest features, bug fixes, and performance improvements, it's important to keep your FlutterFlow version up to date. In this article, we'll guide you through the process of upgrading to the latest version of FlutterFlow.

#### Step 1: Refresh FlutterFlow

The first step in upgrading to the latest version of FlutterFlow is to refresh the application. To do this, follow these steps:

If you're using Windows, press the "Ctrl" and "R" keys simultaneously (Ctrl + R).

If you're using a Mac, press the "Command" and "R" keys simultaneously (Cmd + R).

This action will trigger FlutterFlow to check for any available updates and download the latest version.

#### Step 2: Clear Your Browser Cache

After refreshing FlutterFlow, it's crucial to clear your browser cache. This ensures that any outdated files or data are removed, allowing the latest version of FlutterFlow to run smoothly. The process of clearing your browser cache may vary depending on the browser you're using

---

## 

# FlutterFlow has insufficient permissions for Push Notifications

If you encounter an error in FlutterFlow related to insufficient permissions for the firebase@flutterflow.io account, follow these steps to resolve the issue:

Step 1: Open Firebase Console

Go to the Firebase Console 

Click on the project tile to open the project dashboard for your FlutterFlow project.

​

Step 2: Navigate to Users & Permissions

In the project dashboard, click on the gear icon (⚙️) in the top-left corner to open the project settings.

From the left sidebar, select "Users & Permissions" under the "Project" section.

![](https://downloads.intercomcdn.com/i/o/1000081304/56b180f20a04fbde82e9a468/Permissions.png?expires=1741032900&signature=e6b84f554eeb2b386ab5c5a0afa522d5eb6401f28347369bf740e95be9758644&req=dSAnFsl2nIJfXfMW1HO4zWvb63XB64b%2F%2FzTzVf2VJtRmdy9Z%2FPHb2mqSyXRH%0AJ3Ga%0A)

Step 3: Locate the firebase@flutterflow.io Account

In the "Users" tab, look for the firebase@flutterflow.io account in the list of users.

If the account is not present, you may need to add it by clicking on the "Add User" button and entering firebase@flutterflow.io as the email address.

Step 4: Assign Necessary Permissions

Click on the firebase@flutterflow.io account to open the user details page.

In the "Permissions" section, ensure that the following permissions are assigned to the account:

Editor

Cloud Functions Admin

Service Account User

![](https://downloads.intercomcdn.com/i/o/1000080364/cc612661682c8b679411484d/Campus_Hub_-_Project_settings_-_Firebase_console.png?expires=1741032900&signature=922e170846b88c0d0d852776dafff55cfee95ecf9fca02c3c8eb15b516933fa7&req=dSAnFsl2nYJZXfMW1HO4zVszh9sspHwmpkF3S7tclsWpxfYfoBYeME%2BhxoaW%0AllF9%0A)

If any of these permissions are missing, click on the "Add Permissions" button and select the required permissions from the dropdown menu.

Step 5: Save the Changes

After adding the necessary permissions, click on the "Save" button to apply the changes.

Double-check that all the permissions have been successfully added and saved.

Step 6: Retry the Operation in FlutterFlow

Go back to your FlutterFlow project and retry the operation that previously caused the permission error.

The error should now be resolved, and FlutterFlow should be able to access the required Firebase resources.

I

f you continue to face issues after following these steps, please reach out to the FlutterFlow support team for further assistance.

Note: Ensuring that the firebase@flutterflow.io account has the necessary permissions is crucial for FlutterFlow to interact with your Firebase project correctly

![](https://downloads.intercomcdn.com/i/o/1000078371/412bc4d95b87358a1652469a/IAM_%E2%80%93_IAM___Admin_%E2%80%93_Campus_Hub_%E2%80%93_Google_Cloud_console.png?expires=1741032900&signature=9ba21076f7267bae5a3f4296b3bcb9e16c8d14ab58205d81f4eccc31b23f8da1&req=dSAnFsl5lYJYWPMW1HO4zWqcUPVb8i1s2ZgF%2FFZm95bxnzxX%2Fb5eO9nBW5xU%0AlGnY%0A)

Ensure that all these permissions have been added and saved. 

# Additional Resources

---

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help