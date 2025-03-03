---
title: Troubleshooting Push Notification Issues in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9127377-troubleshooting-push-notification-issues-in-flutterflow"
hide_table_of_contents: true
---

Push notifications play a vital role in mobile apps, enabling you to connect with your audience and update them on key developments. Yet, there are instances when push notifications fail to deliver. In this guide, we will explore the typical problems that hinder push notifications in FlutterFlow and offer detailed instructions on how to fix them.

![](https://downloads.intercomcdn.com/i/o/1004946547/bf9634e91470264a633a3c0b/pushNotifcationError.JPG?expires=1741032900&signature=dd1a9a44c29c0403c541cbe4284e7e9f01b66cf3bd9e93be17fa93a735aefe0c&req=dSAnEsB6m4RbXvMW1HO4zcIhl%2F%2BMNrqv2kpKuo%2BCP83Wso4VHOnHAaSt2ZnY%0A9Zv2%0A)

​

# Without CodeMagic Deployment In FlutterFlow

If you are using CodeMagic deployment, please see the section With CodeMagic Deployment.
---

Ensure your subscription status hasn't changed.

Head to the Firebase Console and select Project Settings > Usage & Billing > Details & Settings. 

![](https://downloads.intercomcdn.com/i/o/500855770/5e647556893ffab9d036ec25/image.png?expires=1741032900&signature=afd844c02f717cb96cc88117b626ff8ed3afa277db03889cee5d953d7a3bf25c&req=cSAnHsx7moZfFb4f3HP0gISU9wGOMRor01jq9Jagpltv32t5GUuDKLgAX7lu%0AjSU%3D%0A)

If you see Spark listed, you will need to select Modify Plan and upgrade to a Blaze Plan. 

Click here for more information on Firebase pricing plans.

# 1. Ensure you have added the required cloud permissions

---

For push notifications to work, you will need to add the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Users & Permissions. 

If you don't have Cloud Functions Admin, Editor, and Service Account listed next to fireabse@flutterflow.io, you have not completed this step.

![](https://downloads.intercomcdn.com/i/o/501028815/d4d5ea7c25cc3f0f78aa459a/image.png?expires=1741032900&signature=108d49a8022ae903c290a081fa5ef9b8f7c7c7060aa44794c0afb2f140fc10e9&req=cSAmFst2lYBaFb4f3HP0gN%2F1m%2Bu6JT8H1hOQeSs8p7Fnl4slsaAHCw%2Bs5eE4%0Ag%2B8%3D%0A)

Here are the instructions on how to add the required cloud permissions to your project.

---

### If you encounter an error in FlutterFlow related to insufficient permissions for the firebase@flutterflow.io account, follow these steps to resolve the issue:

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

If you continue to face issues after following these steps, please reach out to the FlutterFlow support team for further assistance.

Note: Ensuring that the firebase@flutterflow.io account has the necessary permissions is crucial for FlutterFlow to interact with your Firebase project correctly

![](https://downloads.intercomcdn.com/i/o/1000078371/412bc4d95b87358a1652469a/IAM_%E2%80%93_IAM___Admin_%E2%80%93_Campus_Hub_%E2%80%93_Google_Cloud_console.png?expires=1741032900&signature=9ba21076f7267bae5a3f4296b3bcb9e16c8d14ab58205d81f4eccc31b23f8da1&req=dSAnFsl5lYJYWPMW1HO4zWqcUPVb8i1s2ZgF%2FFZm95bxnzxX%2Fb5eO9nBW5xU%0AlGnY%0A)

Ensure that all these permissions have been added and saved. 

# 2. Ensure you have created a push notification key for Apple

---

Apple requires developers to create a key for the push notifications inside the Apple Developer Console to verify the push notification's sender.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles > Keys.

![](https://downloads.intercomcdn.com/i/o/500867400/c4e2a7314b415f9a82cb4c72/image.png?expires=1741032900&signature=3e9a2107f2fc13970951b89edaa44b1ab5f5f07d0d2341d35837ff883207218c&req=cSAnHs95mYFfFb4f3HP0gHt%2BathP3Aoj0ZfTfytqdBXaLzVVB62h5%2B8Bxeus%0AejU%3D%0A)

If you haven't added a push notification key, you will need to add this.

Here are instructions on how to add a push notification key.

​

# 3. Ensure you have added the APN key to Firebase

---

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Project Settings > Cloud Messaging.

Scroll down to the iOS section. If you have no files listed under APNs Authentication Key (like the photo below), you need to upload the APN Key.

![](https://downloads.intercomcdn.com/i/o/500871590/fdf5e9298a8c9bca3588606b/image.png?expires=1741032900&signature=8a0d06031326651833b294beb9abd345cded40ead075fab52a986fb0ecc3e962&req=cSAnHs5%2FmIhfFb4f3HP0gCSJJOSRvrG94eVk5%2FGBHZdqSzqn3Ql0lt7u91o%2B%0AqFw%3D%0A)

Here are the instructions on how to upload the APN key to Firebase.

​

# 4. Ensure you have added a push notification identifier for Apple

---

You must add an Identifier to be able to send the push notifications to the iOS devices after you deploy your app to the app store.

Head to your Apple Developer account and select Certificates, Identifiers & Profiles.

![](https://downloads.intercomcdn.com/i/o/500861775/438eecc997ce015b2d565c1a/image.png?expires=1741032900&signature=27da22a294cbe0e0756ac7002439fd73e04886a576ec9ae815bdf4eda26de458&req=cSAnHs9%2FmoZaFb4f3HP0gOnz3GAOTcrwxnTp3BeKsLhrYA7RjAjjYY4LQOCt%0A34M%3D%0A)

If you haven't created a push notification identifier, you will need to add this.

Here are instructions on how to create your push notification identifier.

​

# With CodeMagic Deployment

If you are not using CodeMagic deployment, please see the section Without CodeMagic Deployment.
---

### Error 1: Signing for "ImageNotification" requires a development team - Flutterflow and Local builds

​Error (Xcode): Signing for "ImageNotification" requires a development team. Select a development team in the Signing & Capabilities editor.

## Method 1 - FlutterFlow Deployment

These are the steps to follow if you are building from FlutterFlow instead of GitHub in this case. 

Having reviewed the guidelines on how to add an identifier in the Apple Developer console. 

In the Apple Developer console, under the Identifiers section:

![](https://downloads.intercomcdn.com/i/o/980061123/c233809c68653d180a2fb7f3/Account_-_Apple_Developer.png?expires=1741032900&signature=45ac6b27acb7372afcff2408d31eaf448afe55612685a7f22ada5d3074246b83&req=fSgnFs9%2FnINcFb4f3HP0gE9o4wYlH4X9aUMrpb2jVUx8d%2F2u%2FSP9ZWVnM6zI%0AstI%3D%0A)

Please verify that an identifier is created with the name 'ImageNotification' and the Identifier set to be the package name of your app + plus the extension .ImageNotification appended to it.

![](https://downloads.intercomcdn.com/i/o/980061486/c8f51958a984eeb302015118/Naming+Identifier_.png?expires=1741032900&signature=0fa459e5c309a374a0a5acaf10c19f4eb2b5d33e8ba2f8e705ea6c9d81971be1&req=fSgnFs9%2FmYlZFb4f3HP0gA%2F6AoMnzd%2FnO%2F6klZ6YDr6tJG2s97j9sSflgFLi%0AwZc%3D%0A)

## Verification Of Identifier And Capabilities

Register an Identifier of type App IDs

![](https://downloads.intercomcdn.com/i/o/980068857/733cc72335d99b2acaa3256d/App_IDs.png?expires=1741032900&signature=d62e4fc71f153f020953ad268dc8f7aa1ab9ceffaa4ec8951ab729ee775fc8ec&req=fSgnFs92lYRYFb4f3HP0gB9bgDb6UQ8YouYm%2BAODzatbI8aWXpHOpZB00v8B%0AztE%3D%0A)

Select the type 'App' then click 'Continue'

![](https://downloads.intercomcdn.com/i/o/980069091/cd1d68db1632648745f9d8bd/Type+of+App.png?expires=1741032900&signature=1885e20b9e34927a3efaa4dae30409c67ffc9f040bf4076c0978d2fac03ba794&req=fSgnFs93nYheFb4f3HP0gDH9skLcjgfZfmVgS1uf33xguzUI82s0vMttSObF%0AiRo%3D%0A)

Set the description to 'ImageNotifcation' and the bundle ID to the package name of your application + the extension '.ImageNotification' appended at the end. 

![](https://downloads.intercomcdn.com/i/o/980069263/220063a13fb96063961107f2/ImageD.png?expires=1741032900&signature=cb471919e43062a32bb62daf15bd0656cc23aa773fba4bbe979ba35c6617b87e&req=fSgnFs93n4dcFb4f3HP0gPZ8OtH7vOizz84eHMVHAsIHzyDjY9TcgXjsWVSi%0A1PI%3D%0A)

Enable the Push Notification capability and continue from there. 

​

![](https://downloads.intercomcdn.com/i/o/980069824/c8bbf562534c4c82c24a9f73/PN.png?expires=1741032900&signature=bfaeb4420828e8f25b372353c3db23bcab95fc4c9ef8a5ef1b9feba564d02e22&req=fSgnFs93lYNbFb4f3HP0gAS5%2BWDBiBGklrII2r0UfGOryF0qfseKTftI4lN4%0AIlc%3D%0A)

The Identifier should be created from there and it will take up the form shown in the image below. 

![](https://downloads.intercomcdn.com/i/o/980070091/32229935a858af30603eb1d1/P.png?expires=1741032900&signature=6e97536c50c9c6e4182a5b9ee1f6b221990c4286c8dd7e9c49f205f63f301d1b&req=fSgnFs5%2BnYheFb4f3HP0gGk2KD%2BktBbXeQg9UXrKC85bEfoOMjiFzE0XTZt%2B%0AanQ%3D%0A)

You should be set to deploy to your application once more! 

## 

Method 2: GitHub Deployment 

---

These are the steps to follow if you are deployment from GitHub in your FlutterFlow. 

​

To fix this error you need to add an Apple Developer Team Profile to your Xcode project. 

​

1. First, you'll need to open the iOS folder inside the project file in Xcode.

​

![](https://downloads.intercomcdn.com/i/o/792691938/a939833ff69659fca9068765/SCR-20230725-oyii.png?expires=1741032900&signature=6973c91947d1ddc02a2bbc9a9eac1030b8ccd83a1143d7d974c15c9aebaaa407&req=cyklEMB%2FlIJXFb4f3HP0gIGeh0V6TNoyqsLNCOf74K2SOZpGAn1nwHmkZn%2BX%0Au7E%3D%0A)

2. After that, you will need to click on the runner folder of the project and select the sign-in and Capabilities option

​

![](https://downloads.intercomcdn.com/i/o/792692984/72f7f76704b223bc213a1738/SCR-20230725-oyru.png?expires=1741032900&signature=af787a84a6692008ba43a638beba471f1714cc696d1eec308f04ee2c5e3ec4fc&req=cyklEMB8lIlbFb4f3HP0gN6Bw2QGC2jS38px3zMTroVZ6Auu5SmEpFuwrKFT%0Acww%3D%0A)

3. You should be able to see the tab shown in the screenshot. Click on add account, Once you add the profile, you should see the list of teams appear at the top of the signing and capabilities panel. You can select the one that matches the team you would like to use, save the settings, and then try to build the project again.

​

# Additional Resources

---

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help