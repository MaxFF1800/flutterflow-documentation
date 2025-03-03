---
title: "Don't see Cloud Functions Admin in the Firebase Console"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7038084-don-t-see-cloud-functions-admin-in-the-firebase-console"
hide_table_of_contents: true
---

Issue: I am trying to add firebase@flutterflow.io as a Cloud Functions Admin, but I can't find the option to add this.

#### Background

Cloud Functions Admin permissions are required for several FlutterFlow features (e.g. Push Notifications). Adding this Cloud Functions Admin is optional, but not doing so will prevent you from using any functions that require Cloud Functions

​

Adding the Cloud Functions Admin role requires that you have a Firebase Blaze plan. 

#### How To Add A Blaze Plan To Your Firebase Account

![](https://downloads.intercomcdn.com/i/o/681081582/090b9bc801b545c329a530ec/image.png?expires=1741032900&signature=3216b4851e29baf52c661e71a1f93c93716395876f980bc6baf21992f83d7f36&req=cigmFsF%2FmIldFb4f3HP0gNVh9xaJXsyVRx7Lr1plOg%2FQIyC9jSzTz3zGMrd9%0AVe4%3D%0A)

To activate the Blaze plan on your Firebase project and enable this permission, follow the steps below:

Open your Firebase project and navigate to the settings menu.

Select the Usage and Billing option from the settings menu.

In the Usage and Billing page, open the Details and Settings tab.

Confirm that an active Blaze plan is associated with your project and that your billing account is properly connected.

​
![](https://downloads.intercomcdn.com/i/o/681082986/052723216b69eaeff6493ddd/image.png?expires=1741032900&signature=a5a05847eadb81365699c97a0f866bc0f77abb77759c4d662fc237c8adced6a8&req=cigmFsF8lIlZFb4f3HP0gJezx9cWsBfzXvJNDEYgHxB2ozC7sdLM3XAs3wLe%0AwTI%3D%0A)

Once these steps have been completed, you will be able to grant FlutterFlow permission to access and manage backend functions, allowing you to take full advantage of the platform's features.

![](https://downloads.intercomcdn.com/i/o/681084044/7b02284209c679b3389fae98/image.png?expires=1741032900&signature=f798eb1ca24f58814e7b2a58dcbfe1dd0886284e453f81edcaf87f0e49fe83db&req=cigmFsF6nYVbFb4f3HP0gP8Qs59f%2Bc5wTzmfkqwIY5I8Gd5PLtR2UaoVJus8%0AiEw%3D%0A)

​