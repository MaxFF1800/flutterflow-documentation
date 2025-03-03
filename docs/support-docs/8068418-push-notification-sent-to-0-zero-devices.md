---
title: "Push Notification Sent to 0 (Zero) Devices"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8068418-push-notification-sent-to-0-zero-devices"
hide_table_of_contents: true
---

# Introduction

---

Push notifications serve as a vital bridge between your FlutterFlow app and users, offering a direct channel for engagement, alerts, and updates. Despite their benefits, setting up and managing push notifications can sometimes feel like navigating a complex maze, especially when they don't work as expected. Whether you're a seasoned developer or new to FlutterFlow, encountering issues with push notifications is almost a rite of passage

​

When Push Notifications are triggered here is a flow of how the notifications ultimately reach the user.

​

![](https://downloads.intercomcdn.com/i/o/972877161/fa0a9b223bda288791415424/diagram.png?expires=1741032900&signature=208afb3411dc169a4300da857239d2236d7e7cd4ea70e518c790633c18d85ebe&req=fSclHs55nIdeFb4f3HP0gPXsRpTVyyPtVzctBMDFGvUDY7rrPsRgTwyXt4WY%0AVYQ%3D%0A)

## 

​

# Pre-Requisites

---

Please ensure that Firebase Functions are enabled in Firebase

​
![](https://downloads.intercomcdn.com/i/o/972877496/09d347a141685e2ef954ea64/diagram-2.png?expires=1741032900&signature=a09667eb6076de198f1b2ddb80e0c4e805765d5ec0f1beae7d55ca01eb07e715&req=fSclHs55mYhZFb4f3HP0gF9K17ZznaldLCfsDgb44iNgGpteeA4dcdD1qQWb%0ABJU%3D%0A)

Ensure you are on the Blaze plan in Firebase

# What the Error Message Looks Like

---

```
`Push Notification sent to 0 devices`
```

​

# ​What Does This Error Mean?

---

The "Push Notification sent to 0 devices" message in FlutterFlow refers to a situation where a push notification was attempted to be sent, but it reached 0 recipient devices. Some potential reasons for this include:

There are no registered devices to receive push notifications for that FlutterFlow app yet. No FCM tokens have been generated.

All target recipient devices were offline and unable to receive the push notification at the send time.

A configuration issue or problem is connecting to the push notification service to deliver notifications to devices.

Permissions, system settings, or other restrictions are blocking recipient devices from receiving push notifications for that app among other reasons.

​
Essentially, "sent to 0 devices" most likely means no eligible, reachable, or listening devices received that push notification - even though the system tried to send it. It could be an issue on the sender configuration side or the recipient device side. Through the instructions below, we will follow step-by-step guidelines on how to resolve this.

# How Do I Resolve This Issue?

---

### 1. Delete the Firebase Cloud Function Manually in Firebase

After successfully deploying Push Notifications or other functionalities that require Cloud Functions, the functions will be recreated.

![](https://downloads.intercomcdn.com/i/o/972879426/75d23ce7b742f8c20600d48b/Firebase_Functions+.png?expires=1741032900&signature=01fec8186677a88e3afee2bd74d9d5f0ddfb25dbfbb9062e617c2cb9387823ad&req=fSclHs53mYNZFb4f3HP0gF9jYRDRPSiLL5tiw24TeFzd1vGSkS6vGw5w2iG7%0A2Qc%3D%0A)

Then, deploy Push Notifications in FlutterFlow once more:

![](https://downloads.intercomcdn.com/i/o/972882387/c13744378d3077efece34a22/Push_Notifications+.png?expires=1741032900&signature=20db2de2da5e1592b8aa55bd1b5ba74ba580a539e8464316feb43ef024bf5901&req=fSclHsF8nolYFb4f3HP0gNRy6%2Fe%2BH5J%2FfoiKQZLE0Z9%2FxNYPpRf9lQkdTOs4%0Ank0%3D%0A)

### 2. Verify the Server Region

The other important aspect is to check the server location. If you've chosen a server in the USA (e.g., "us-central1"), ensure that FlutterFlow is configured with the same server location. Inconsistencies in server location can cause unexpected issues.

![](https://downloads.intercomcdn.com/i/o/972891328/7e1c612fc7a4c5e73f9664ac/diagram-3.png?expires=1741032900&signature=6ba743a5f139c695e00204ae5acac9b3f395dcb4c0b3ef40a8ba29f4fd437178&req=fSclHsB%2FnoNXFb4f3HP0gIDFMc3FeN%2B%2FyidcNJb472Rcxj8j0wcm22NmVgdB%0AFI0%3D%0A)

Here is how to set up the region in FlutterFlow. 

​

Navigate to Settings -> Firebase -> Advanced Settings to modify these settings. 

​

![](https://downloads.intercomcdn.com/i/o/972926057/4128a7b81428e45222f23ac1/Firebase.png?expires=1741032900&signature=e095849af05d516a8d9670ee2128a427ddd33edafc56c8ca1a7cd0519a6f7c3b&req=fSclH8t4nYRYFb4f3HP0gKvNqS%2Fgvgs7njqMtd3X75gHITQmhdwJmyiQBgY0%0A32o%3D%0A)

From the FlutterFlow, the region can be changed from [Default] to 'us-central1'

​

In Firebase Cloud Functions, the region is shown here. 

​

![](https://downloads.intercomcdn.com/i/o/972928620/d938bf6844454fb790af2a0d/Firebase_Cloud_Functions.png?expires=1741032900&signature=900e3f02225300b128e5c7637b01ef3cff2af112b28ba93e6efcec9bb110b21a&req=fSclH8t2m4NfFb4f3HP0gAbNv4Dm1ic%2BwJPK80NX0Mlm9oZGdAR1uaKaTcOi%0AX6g%3D%0A)

### 

3. Check FCM API Settings in Google Cloud Console

The third step involves checking the settings of the Firebase Cloud Messaging (FCM) API in the Google Cloud Console. It's essential to ensure that the FCM API is enabled and has a secret key displayed in the Firebase Console. If the key is not shown, you must create a new one in the Google Cloud Console.

​

In the Google Cloud console, you would have to type 'FCM API' and then enable it if not already.

![](https://downloads.intercomcdn.com/i/o/972900537/1cb0c15c2a9fdf0ba65cd3e2/FCM_Tokens.png?expires=1741032900&signature=e91e4a0109901c506c7d5b7120541c399f8c3f4a776e3efb6874c04c061ac5ab&req=fSclH8l%2BmIJYFb4f3HP0gCSGpWsSgPqAWu2ndmEcSucZnHGVt%2B3b03r2SCfa%0ADBk%3D%0A)

### 4. Ensure You Have Added The Required Cloud Permissions

To ensure that push notifications function correctly in your FlutterFlow app, you need to grant the necessary cloud permissions to the firebase@flutterflow.io service account. This article will guide you through the process of adding the required permissions in the Firebase Console.

#### Step 1: Open the Firebase Console

Go to the Firebase Console (https://console.firebase.google.com/).

Click on the project tile to open the project dashboard for your FlutterFlow app.

​

#### Step 2: Navigate to Users & Permissions

In the project dashboard, locate and click on the gear icon (⚙️) in the top-left corner to open the project settings.

From the left sidebar, select "Users & Permissions" under the "Project" section.

![](https://downloads.intercomcdn.com/i/o/1000081538/cd7d0903bee4a9284ff0b87e/Permissions.png?expires=1741032900&signature=6b3ab87c072cbc76b44c3bbdcc05199cdb3f5fad4f58a3fa1b3dbbeb7f0a3c51&req=dSAnFsl2nIRcUfMW1HO4zbUccl8E0bGBJV4VdwpHMD7ElT0X3DWawFF6Pnxk%0A3A8E%0A)

#### Step 3: Verify firebase@flutterflow.io Permissions

In the "Users" tab, look for the "firebase@flutterflow.io" service account.

Check if the following permissions are listed next to the service account:

​

Editor

Cloud Functions Admin

Service Account

![](https://downloads.intercomcdn.com/i/o/1000081713/6ba6c0f597469d04c0671749/Campus_Hub_-_Project_settings_-_Firebase_console.png?expires=1741032900&signature=ecfda165b81f5da585e2d7567b2f9b7004ea58d895d550ffb3f20bfc8014a864&req=dSAnFsl2nIZeWvMW1HO4ze7reaEYR7kUK8f8zW01gFTQX626IQDj4NjZ0%2Bka%0AoUnm%0A)

If any of these permissions are missing, proceed to the next step to add them.

Step 4: Add Missing Permissions (if necessary)

Click on the "Add Member" button in the top-right corner of the "Users" tab.

In the "Add members" dialog, enter "firebase@flutterflow.io" in the "Members" field.

Click on the "Select a role" dropdown and choose the missing permission(s) from the list:

Editor

Cloud Functions Admin

Service Account

![](https://downloads.intercomcdn.com/i/o/1000081947/e753c530143a0144fae7617c/IAM_%E2%80%93_IAM___Admin_%E2%80%93_Campus_Hub_%E2%80%93_Google_Cloud_console.png?expires=1741032900&signature=58f0e9d3ac17e26595672770b2db8b23ebe16dbbd7e355a0d8234702deaf1b8c&req=dSAnFsl2nIhbXvMW1HO4zeSHHE0ynbK88aipy9SKxPm8kwTQgCs2zL6qaQRp%0A6Dke%0A)

Click the "Add" button to grant the selected permissions to the firebase@flutterflow.io service account.

​

Step 5: Verify the Added Permissions

After adding the missing permissions, verify that "Editor," "Cloud Functions Admin," and "Service Account" are now listed next to the firebase@flutterflow.io service account in the "Users" tab.

# Additional Resources

---

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help