---
title: What To Do When FlutterFlow has Insufficient Permissions for Push Notifications
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7159783-what-to-do-when-flutterflow-has-insufficient-permissions-for-push-notifications"
hide_table_of_contents: true
---

# Background

When deploying push notifications to Firebase using FlutterFlow, you may encounter an error message indicating that FlutterFlow has insufficient permissions. This error occurs when FlutterFlow doesn't have the necessary access rights to deploy the push notification settings to your Firebase project. In this article, we'll explore the cause of this error and provide a step-by-step solution to resolve it.

![](https://downloads.intercomcdn.com/i/o/694744237/2cca6382d87ba3e19fc2370c/SCR-20230320-mnpk.png?expires=1741032900&signature=c1a7276f2c8a51fd7ad966805ab9f4cbf75b4b0374d98dfe3ced3f8802bf2aa5&req=cikjEc16n4JYFb4f3HP0gJD64Kmor7c1nHc6r8517dqogoAgGEBtWuHYb9pR%0AYKE%3D%0A)

# How To Resolve 

---

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

If you continue to face issues after following these steps, please reach out to the FlutterFlow support team for further assistance.

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