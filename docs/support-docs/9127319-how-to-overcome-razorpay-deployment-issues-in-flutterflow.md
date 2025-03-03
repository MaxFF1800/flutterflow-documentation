---
title: How to Overcome Razorpay Deployment Issues in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9127319-how-to-overcome-razorpay-deployment-issues-in-flutterflow"
hide_table_of_contents: true
---

Razorpay is a major payment processor in India. Integrating Razorpay can allow users to make payments using their app. This article outlines some common scenarios and troubleshooting instructions for Razorpay deployment issues.

## 1. Firebase Integration and Auth

FlutterFlow uses Firebase integration and cloud functions to facilitate Razorpay payments. Ensure you have Firebase configured in your FlutterFlow project and that Firebase Auth is enabled. 

![](https://downloads.intercomcdn.com/i/o/1004961385/7775e131260350d6c8330946/image.png?expires=1741032900&signature=89d7c15ad73f0cfc8e9dc738bda6da1191eb4358788500ca2650d9794d79980b&req=dSAnEsB4nIJXXPMW1HO4ze3G%2FQxEENnmu5KSGuLw3Y%2FiTH3h%2Frx%2F1c60Di5r%0AGMiy%0A)

![](https://downloads.intercomcdn.com/i/o/1004961763/954730e61ef075d44c711564/image.png?expires=1741032900&signature=a6b33dbd0090f15fe428dc129eb18f76c198056935ab525f84feade62be6a3f5&req=dSAnEsB4nIZZWvMW1HO4zXjWeTWsyfUoDozjVhP0jppXQqzBgWRBnAWkh1cS%0A3W5p%0A)

## 2. Firebase Blaze Plan

Razorpay uses cloud functions behind the scenes to facilitate payments. Cloud functions are a part of Firebase's "Blaze" plan. You must upgrade from the Firebase Spark plan to the Blaze plan to avoid disruptions. Learn how to upgrade here. On the bottom left side of your Firebase console, you will see which plan you are on

![](https://downloads.intercomcdn.com/i/o/1004966718/9ae7f9080ab7fbbbbb1fa3d9/image.png?expires=1741032900&signature=e873c66c45c209f99f9e12f7de716f2dffa87c759c8d65af5a59b7b6840cbfff&req=dSAnEsB4m4ZeUfMW1HO4zUhoBwPciAa7535yp%2FuJL%2BhxSIAFsgHiDIFOiBve%0AEVuT%0A)

## 3. Set Google Cloud Location

Ensuring your Firebase project is pinned to a specific Google Cloud Platform (GCP) location is key for optimal service functionality across regions. Skipping this step could result in errors.

​

![](https://downloads.intercomcdn.com/i/o/982079571/6cbe4958b54aebbb6598752c/image.png?expires=1741032900&signature=94287023ff2a2a7deceef313948b6b876417e3077ba1ef721b7415ba210335c2&req=fSglFs53mIZeFb4f3HP0gCwkM654We530qgUouj3jQK4RQzwRVE9Ec0KUkMP%0AWHI%3D%0A)

## 4. Firebase Project Permissions

Make sure your Firebase project has the required permissions activated. Access management and service configuration are two essential permissions to focus on. For guidance on setting these up, look at the instructions in the FlutterFlow Documentation.

## 5. Razorpay Keys Check

Make sure to copy and paste the correct Key ID and Key Secret from Razorpay for testing and production, respectively. For testing, make sure "Is Production" is turned off.

![](https://downloads.intercomcdn.com/i/o/1004972818/4ae7a81861d0881bc0b3426a/image.png?expires=1741032900&signature=6c19d48bf02c25b6f985d18ceabbb4000da870170244a285995937d8c1c08ab9&req=dSAnEsB5n4leUfMW1HO4zQBxbENr07ljaGyALBBFVyENYA4UfzvJmxZOIOx%2B%0AskcG%0A)

![](https://downloads.intercomcdn.com/i/o/1004976455/756d9289363b0249aaf3b25b/image.png?expires=1741032900&signature=7f73d5e2f01b2de56a51982e54768e00070bfbd5b8a4b4376f734e7d2440cdd8&req=dSAnEsB5m4VaXPMW1HO4zfw8RBD8sgoAtKdpVRfroOi40XNtdWW%2BQ%2FrxFZqd%0At0%2BE%0A)

![](https://downloads.intercomcdn.com/i/o/1004977867/d04bd8895d557f77a27d70b2/image.png?expires=1741032900&signature=7247c8b97ca5b584f7a9fd754432174662abfd3bd8a4882cb6efbcfc821a472c&req=dSAnEsB5molZXvMW1HO4zUIsvu3LgPKbpBJwxXfr9cn4ue6va94vAssUoFP6%0A2Fzi%0A)

## 6. Razorpay Business Name

Finally, ensure you have entered the proper "Business Name" in the Razorpay additional settings in FlutterFlow. Make sure this business name matches your business name in Razorpay records. 

![](https://downloads.intercomcdn.com/i/o/1004974660/43a66560b609cc9c4ac13a1b/image.png?expires=1741032900&signature=5ae3733192a5bd7ead9dd360e83a8ba321a9fd46900dd402ec2422b67d611bff&req=dSAnEsB5mYdZWfMW1HO4zahR6yVdm2rCz%2F4bHcJSQNU8d9g6dX%2F50FQYrqKS%0Ac1I4%0A)

## Other Considerations

Razorpay currently works only on mobile (Android and iOS). This is due to a limitation from Razorpay's Flutter Package. If you are planning to collect payments on a web app - consider using Stripe.

![](https://downloads.intercomcdn.com/i/o/1004979225/c2d60dc401d0e60864a34f63/image.png?expires=1741032900&signature=2d5736996767b6808706e5405047720d283fd214c15469a0003d073471319346&req=dSAnEsB5lINdXPMW1HO4zbG6T2EUh0MsdrZPjrvQviXqsTKtu61v2NanJoLI%0A60K7%0A)

If you are still facing issue with deploying Razorpay on Flutterflow, please feel free to reach out to support@flutterflow.io