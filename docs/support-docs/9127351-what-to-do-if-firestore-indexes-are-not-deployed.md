---
title: What To Do If Firestore Indexes Are Not Deployed
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9127351-what-to-do-if-firestore-indexes-are-not-deployed"
hide_table_of_contents: true
---

When working with Firebase, ensuring that your indexes are properly deployed is crucial for the functionality and performance of your app. If you're encountering issues with Firebase indexes not being deployed, follow this step-by-step guide to troubleshoot and resolve the problem.

# Problem Overview

---

Issue: Firebase indexes are not being deployed as expected.

Expected Outcome: Indexes should be successfully deployed to Firebase to ensure optimal app performance and functionality.

![](https://downloads.intercomcdn.com/i/o/1004958863/830c10f0246f14cb77cd827c/deployedIndex.png?expires=1741032900&signature=c52dae226511e4a4a7a6d0f0e66cfa46cbfa6ab673dc67a0dfa8a964159a0cda&req=dSAnEsB7lYlZWvMW1HO4zeaZWkF6AaTc8t1DpYfrPwAnG%2FOZL8XM9L09pyd4%0AcV9i%0A)

# Troubleshooting the Issue: 

---

## Step 1: Enable Email Sign-In

The first step in ensuring that your Firebase project can properly deploy indexes is to make sure that email sign-in is activated.

Action: Navigate to your Firebase project's authentication section and ensure that the email/password sign-in method is enabled.

Reference: For detailed instructions, visit the FlutterFlow documentation on email sign-in: https://docs.flutterflow.io/data-and-backend/firebase/authentication/email-sign-in

## Step 2: Grant Proper Permissions

Next, it's essential to ensure that the firebase@flutterflow.io email address has the necessary permissions within your project. This email address needs appropriate access to manage and deploy Firebase indexes.

Action: Add firebase@flutterflow.io as a member of your Firebase project with the correct permissions.

Reference: For a step-by-step guide on adding this email and setting up permissions, consult the Firebase setup documentation: https://docs.flutterflow.io/data-and-backend/firebase/firestore-database-cloud-firestore/firestore-rules

![](https://downloads.intercomcdn.com/i/o/1004971382/8e50d9324c0089844b53e7a4/firebaseEmail.png?expires=1741032900&signature=db745c03791215d2579c7456acd3c09667455d829bb8b1c956f5e3145e862b27&req=dSAnEsB5nIJXW%2FMW1HO4zec665IcblWLx%2BsMQOT2%2FCu7X1Hz9d7kadmEgm5K%0AozBv%0A)

## Step 3: Update Firebase Rules

Having the current and correctly configured Firebase rules is vital for the security and functionality of your app. These rules determine how data can be accessed and manipulated within your Firebase project.

Action: Review and update your Firestore security rules in both the Firebase console and FlutterFlow to ensure they're correctly set up for your app's needs.

Reference: For more information on checking and updating Firestore rules, see the Firestore rules documentation: https://docs.flutterflow.io/data-and-backend/firebase/firestore-database-cloud-firestore/firestore-rules

## Step 4: Verify the Indexes are Deployed

After ensuring the above steps are correctly implemented, it's crucial to verify that your Firebase indexes are indeed deployed.

Action: Check the Indexes section in your Firebase console to confirm that your indexes have been successfully deployed.

Note: The deployment might take a few minutes, so consider waiting a bit and then refreshing the console to check the status.

![](https://downloads.intercomcdn.com/i/o/1004975421/d24dfe0020988d8d02be95fc/image.png?expires=1741032900&signature=54d2b29460c5c4cca0e89625ca34c404a88599f76248679319b384b5d1cb3a79&req=dSAnEsB5mIVdWPMW1HO4zVnG4TPLyv2rkGEq4y9rykDd3GZpD%2FWQFpFhnVzB%0A9%2Fgi%0A)