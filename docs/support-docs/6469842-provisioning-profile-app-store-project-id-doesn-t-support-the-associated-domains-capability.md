---
title: "Provisioning profile [app store project ID] doesn't support the Associated Domains capability."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6469842-provisioning-profile-app-store-project-id-doesn-t-support-the-associated-domains-capability"
hide_table_of_contents: true
---

When deploying an app through FlutterFlow to the Apple App Store, developers might encounter a specific error regarding the 'Associated Domains' capability. This article aims to clarify this issue, explaining its cause and guiding you through the process of enabling this capability within your Apple Developer account to ensure smooth app functionality.

​

The Root of the Problem

The error message 'Provisioning profile [app store project ID] doesn't support the Associated Domains capability' occurs when an app submitted to the App Store lacks the proper configuration for the Associated Domains. This capability is essential for apps that need to verify domain ownership and set up app-to-site associations, which are critical for features like Universal Links, App Clips, and website authentication.

Enabling 'Associated Domains' Capability

​

​Example: You will face this error when you use dynamic links in your projects.

​

To resolve this issue and enable the 'Associated Domains' capability for your app, follow these steps:

Visit Your Apple Developer Account: Sign in to your Apple Developer account and navigate to the 'Identifiers' section found under 'Certificates, Identifiers & Profiles'.

​
![](https://downloads.intercomcdn.com/i/o/987872016/bf4ab8d12cebd5646c1938ba/image.png?expires=1741032900&signature=64cb0165fd4189ab0841311e844635d2d52222b5cc5c63536e54c5ed30231f1b&req=fSggHs58nYBZFb4f3HP0gKokSIX5dZCAuJaQ664XqgclawqanWObFhlBl9WY%0A4IY%3D%0A)

​

Select Your App's Identifier: Locate the App ID for the app you're deploying. It's essential since the capability adjustments are specific to your app's identifier.

Enable the Capability: In your app's identifier details, find the section for enabling capabilities. Select the option for 'Associated Domains'. This step does not require altering the primary App ID or creating a new key if it's the first time you're enabling this capability for an App ID.

​
![](https://downloads.intercomcdn.com/i/o/994627005/2db0fc9de128d91746f2d5c1/image.png?expires=1741032900&signature=f5a4431c1215e7b73bc4286e06a28dbf0d3b7c9c4e859a343d2bd7e3ab33d43c&req=fSkjEMt5nYFaFb4f3HP0gFr4sVW2YG2Nf3CafyDhc%2Fc3nufo8JgxMmrpYpa6%0AVRI%3D%0A)

​

Save Changes: After enabling the 'Associated Domains' capability, ensure you save the changes. Unlike some UI elements that might suggest further editing, enabling the feature and saving should be sufficient for the initial setup.

​

Deploy Through FlutterFlow: With the 'Associated Domains' capability now enabled for your App ID, you can proceed to deploy your app via FlutterFlow.

​

## 

Understanding Your Developer Account's Capabilities

​What does this error mean?

The provisioning profile error indicates that the domain linked to the developer account is unsupported due to the user's subscription status. This often occurs when the user is not subscribed to a paid Apple Developer account plan.

​Full error message

'Provisioning profile [app store project ID] doesn't support the Associated Domains capability.'

​

How can I resolve this issue?

Verify Your Apple Developer Account Subscription Status: Ensure that your account type supports the 'Associated Domains' capability, which requires a paid plan.

![](https://downloads.intercomcdn.com/i/o/675262491/a98989f5f575b049c9d20c1b/Snip20230219_22.png?expires=1741032900&signature=b9c9697b83c3fa26a46574a087eeaa7fc0431613e2b1e56e1e4bfda1e17d352b&req=ciciFM98mYheFb4f3HP0gI7kje3GXy%2BOCjsiNsLeAk4f6aZ6SU7VrWzeXJCG%0AeRE%3D%0A)

​How can I view my subscription status?

To check your Apple Developer subscription status, log into your Apple Developer account. Your account information, including subscription status, will be displayed on the dashboard, with active subscriptions marked as 'Current'. If your subscription is nearing its expiration, the 'Expiration Date' will be visible, allowing you to plan for renewal. For further assistance, contact Apple Developer support at devsupport@apple.com.

​