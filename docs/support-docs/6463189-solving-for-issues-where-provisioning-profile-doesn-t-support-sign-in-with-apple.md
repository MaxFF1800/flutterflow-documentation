---
title: "Solving for Issues Where Provisioning Profile Doesn't Support 'Sign in with Apple'"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6463189-solving-for-issues-where-provisioning-profile-doesn-t-support-sign-in-with-apple"
hide_table_of_contents: true
---

## Understanding the 'Sign in with Apple' Capability Issue

When deploying an app through FlutterFlow to the Apple App Store, developers might encounter a specific error regarding the "Sign in with Apple" capability. This article aims to shed light on this issue, explaining its cause and guiding you through the process of enabling this capability within your Apple Developer account's key identifier.

​

## Root of the Problem

The error message "Provisioning profile doesn't support the Sign in with Apple capability" occurs when an app that includes the Apple Sign In method is submitted to the App Store without the proper configuration steps being completed. This configuration is crucial because the "Sign in with Apple" feature requires explicit permission set within your Apple Developer account to work seamlessly with your app.

​

## Enabling "Sign in with Apple" Capability

To resolve this issue, follow these steps to enable the "Sign In with Apple" capability for your existing app:

Visit Your Apple Developer Account: Log into your Apple Developer account and navigate to the "Identifiers" section under the "Certificates, Identifiers & Profiles" area.

​
![](https://downloads.intercomcdn.com/i/o/987872016/bf4ab8d12cebd5646c1938ba/image.png?expires=1741032900&signature=64cb0165fd4189ab0841311e844635d2d52222b5cc5c63536e54c5ed30231f1b&req=fSggHs58nYBZFb4f3HP0gKokSIX5dZCAuJaQ664XqgclawqanWObFhlBl9WY%0A4IY%3D%0A)

​

Select Your App's Identifier: Find the App ID associated with the app you're deploying. This is crucial as the configuration you're about to adjust is tied specifically to the app's identifier.

​

Enable the Capability: Within your app's identifier details, locate the section for enabling capabilities. Check the option for "Sign in with Apple." There's no need to alter the primary App ID or create a new key for this step if it's your first time enabling this capability for an App ID.

​
![](https://downloads.intercomcdn.com/i/o/987855647/57c1fddd187641a2fb79c299/image.png?expires=1741032900&signature=1f02e4047abd6f50cd27848cf8604c6cd5757eae09255c09a1db244e0661198e&req=fSggHsx7m4VYFb4f3HP0gJHc21q3lKVINBkn34FjYGvb6gggZmnRfN9rr%2FcV%0Axkk%3D%0A)

​

Save Changes: Ensure you save the changes made. Contrary to some UI elements that might suggest editing further, simply enabling the feature and saving suffices for the initial setup.

​

Deploy Through FlutterFlow: With the "Sign in with Apple" capability now enabled for your App ID, proceed to deploy your app through FlutterFlow.

​

​

Contact Support if Necessary: If you encounter any issues or your app does not utilize the "Sign in with Apple" method, it's advisable to contact FlutterFlow support for tailored assistance. You can reach out via live chat or email at support@flutterflow.io.

​

​

For more information on deploying apps with FlutterFlow and other app development topics, visit Apple Sign-in Documentation, FlutterFlow's documentation and community resources.

​