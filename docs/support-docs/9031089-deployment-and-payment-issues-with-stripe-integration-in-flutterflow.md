---
title: Deployment and Payment Issues with Stripe Integration in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9031089-deployment-and-payment-issues-with-stripe-integration-in-flutterflow"
hide_table_of_contents: true
---

Integrating Stripe for payment processing in FlutterFlow projects can streamline the monetization process for app developers. However, developers often face hurdles during the deployment phase and while handling payment transactions. This article outlines solutions to common deployment and payment issues associated with Stripe integration, ensuring a smooth user experience in FlutterFlow applications.

​

# Deployment Checklist for Stripe Integration

## 1. Firebase Connection

Stripe integration requires a connected Firebase project. Before running through this checklist, it's important to ensure your FlutterFlow project is linked to Firebase, a crucial step for successful payment processing. Detailed guidance can be found at FlutterFlow's Firebase Setup.

## 

2. Upgrade to Firebase Blaze Plan

Stripe functionality requires a Firebase Blaze Plan for operational capabilities. To avoid disruptions, you will need to upgrade from the Firebase Spark plan to the Blaze plan. Learn more about Google's process for upgrading here.

## 

3. Set the Google Cloud Platform (GCP) Location

A defined Google Cloud Platform (GCP) location for your Firebase project ensures the correct regional operation of services. The absence of a set location can hinder the deployment process.

​

![](https://downloads.intercomcdn.com/i/o/982079571/6cbe4958b54aebbb6598752c/image.png?expires=1741032900&signature=94287023ff2a2a7deceef313948b6b876417e3077ba1ef721b7415ba210335c2&req=fSglFs53mIZeFb4f3HP0gCwkM654We530qgUouj3jQK4RQzwRVE9Ec0KUkMP%0AWHI%3D%0A)

## 

4. Firebase Project Permissions

Ensure you have the necessary permissions enabled for your Firebase project. Two critical permissions involve access management and service configuration. You can reference the setup guide on FlutterFlow Documentation.

​

![](https://downloads.intercomcdn.com/i/o/982079760/8fc2809d05a3c44bfa1a8ad3/image.png?expires=1741032900&signature=ec4e40eececfa6c6bae01156f4096f3c5cc2f01eeb3af0cf64322f2f84c6adaa&req=fSglFs53modfFb4f3HP0gLD3YuZBcYrSlEHwHpnL9rWljtb5s7lM9RrVCi7M%0AW2I%3D%0A)

## 

5. Correct Merchant Code

Use the correct 3-letter merchant country code (e.g., "GBR" for the United Kingdom vs. "UK"). Incorrect codes can lead to failed transactions. For accurate codes, refer to IBAN Country Codes.

​

![](https://downloads.intercomcdn.com/i/o/982080233/fa9f74d02bf02aaa1c2ea6b6/image.png?expires=1741032900&signature=1f40104c9942cd5a9a5fbde2b1f27d13ee7a52aa1e54a665dc08b5ad2898b555&req=fSglFsF%2Bn4JcFb4f3HP0gLi4GmoOHja%2Fiu3CeeJDS2LMKFPc22VBD73NU3Ad%0AZMQ%3D%0A)![](https://downloads.intercomcdn.com/i/o/982080404/3a1bfd625d54e37a8ea1aa37/image.png?expires=1741032900&signature=26b530a67ec942e565878b2854567e60b99acbb4e323c7969190f5ed305f49cd&req=fSglFsF%2BmYFbFb4f3HP0gDkUE2uB2pCoEN8oU05vfIsUAkNt3UVhO%2F097bAE%0A%2FSI%3D%0A)

## 

6. Test and Live Keys

For deployment, both Test and Live Stripe keys must be configured in your project settings, regardless of the development stage. This ensures Stripe's API can properly interact with your application.

​

![](https://downloads.intercomcdn.com/i/o/982080736/8e1e1fba73df4c35a6722517/image.png?expires=1741032900&signature=c127c9ef713fcd8ca6d7d7b3c803a0f0f6a3f8040fe280e96b647c5039431566&req=fSglFsF%2BmoJZFb4f3HP0gCPZCwDLKx%2BLgenqzjCOFbjeE2vUd7N8QoRKazpR%0AYz0%3D%0A)

## 

7. Consistent Region Settings

Align your Firebase project's region with that of your FlutterFlow settings to prevent deployment failures. Inconsistencies can cause function deployment issues.

​

![](https://downloads.intercomcdn.com/i/o/982081014/2472250daa21a455ec34b243/image.png?expires=1741032900&signature=ac69e66fe8686f2ff9a0ca4f0787b2cfa2a7a66aa7082527781a25c0430ad906&req=fSglFsF%2FnYBbFb4f3HP0gD4sTbwUghxRFAWKePYfxOgO%2BzkWMbGSW9F3o4Fc%0ABU0%3D%0A)![](https://downloads.intercomcdn.com/i/o/982081195/c9f6f2be8baea50f5bfb196c/image.png?expires=1741032900&signature=040676cb3f9252554506bef524033ce5a6df77092b79ed1e3c76977735278854&req=fSglFsF%2FnIhaFb4f3HP0gC%2Fz9Uj6A45MkymdxlFxYneDgALxl0QnXFWJa2M2%0AwYw%3D%0A)

# 

Addressing Payment Transaction Issues

## 1. Authentication Requirement

Stripe payments require an authenticated user session. Before initiating payment processes, ensure your application logic includes user login or account creation.

## 

2. Payment Modal Variations

It's important to note that web and mobile platforms present different payment modal presentations. These UI differences are out-of-the-box fro Stripe and cannot currently be customized within FlutterFlow.

## 

3. Price Format

Prices should be submitted to Stripe in cents, not dollars. Utilize a custom function to convert dollar values to cents for accurate transaction processing.

​

To set a price in cents to Stripe, you can simply use a custom function that takes the price in dollars and returns it as cents.

​

Here is custom code you can use to make this calculation in a custom function: 

```
`int dollarToCent(double amount) { String st = amount.toString(); st = st.replaceAll(".", ""); st = st.replaceAll(",", "");return int.parse(st); } ﻿

Input: 14,99$

Output: 1499 cents`
```

## 

4. CORS Error Resolution

A CORS error during payment initiation often indicates a permissions issue with your Firebase function. Verify and adjust the allUsers permission for your Stripe function in the Firebase console to resolve this error.

​

![](https://downloads.intercomcdn.com/i/o/982083120/0c297e5fd3d81fe6425eb2d9/image.png?expires=1741032900&signature=c8f3a8234c6b729ccba86b08bcc1cc8d2b3841c9d0a9ac02dfd56f34f5027709&req=fSglFsF9nINfFb4f3HP0gEa5JK0sBK%2BeRA7ridjqB4jWZimFRwBlkfPbxnYA%0Ak3E%3D%0A)![](https://downloads.intercomcdn.com/i/o/982083308/67d2f92f64ef09379c601117/image.png?expires=1741032900&signature=ac2ecb8464a13b854f76e58ef30890a13837d173f4aef0bd859bf8d22f84a69f&req=fSglFsF9noFXFb4f3HP0gDMolvAheDsM6SUuPvli9sIEq4JC28HBZ2GTnHBq%0ASjU%3D%0A)

## 

5. Subscriptions

Currently, Apple and Google restrict Stripe subscriptions on mobile platforms. To expand your subscription capabilities, you can use alternative solutions like RevenueCat for mobile apps and direct API calls for web applications.

​

For further information and troubleshooting:

​Stripe Documentation 

​Stripe Payments: FlutterFlow University

Payments - Intro FlutterFlow University