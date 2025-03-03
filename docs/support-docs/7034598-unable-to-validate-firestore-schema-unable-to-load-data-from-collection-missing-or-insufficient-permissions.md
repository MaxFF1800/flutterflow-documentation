---
title: "Unable to validate Firestore Schema: Unable to load data from collection. Missing or insufficient permissions"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7034598-unable-to-validate-firestore-schema-unable-to-load-data-from-collection-missing-or-insufficient-permissions"
hide_table_of_contents: true
---

Issue: You see an error like this when trying to validate your Firestore Schema:

Unable to load data from collection. Error: [cloud_firestore/permission-denied] Missing or insufficient permissions.

​

![](https://downloads.intercomcdn.com/i/o/683953518/e585151a5fc17d4bb6e6a360/image.png?expires=1741032900&signature=dfb47e50f5c7f1fc4a34238bfd09a6d6e9ee23d7262ba395c28d479f0ab64c29&req=cigkH8x9mIBXFb4f3HP0gH%2FnLwh8aooZpZ1GubwEpQltxneHs%2BmmCUnKca3T%0AV3k%3D%0A)---

Troubleshooting Steps:

#### 
1. Make sure you already created a database in firebase

![](https://downloads.intercomcdn.com/i/o/680316319/51fba815ec2865cd7a8dffc2/image.png?expires=1741032900&signature=4aff8f287f2f5192984d3543b581c70c4ad9fb3975f88b33c2427e95bf0bd0c9&req=cignFch4noBWFb4f3HP0gNPOp2VsWrM%2BkPnyPm8AGHhdas2Jx0Wg%2FcnnEzPX%0Aa14%3D%0A)---

#### 

2. Make sure your database is not on TEST MODE. 

Important: A Database in Test Mode may not work properly

Note: after creating the database on test mode there is no visual way to set it on production mode, instead, you need to change the firebase rules. and if you deploy your rules from Flutterflow it will be done. and no need to do this manually and you can skip this part.

1) Go to your firebase project.

2) Select Cloud Firestore.

3) Select Rules.

You will see something like below.

​

![](https://downloads.intercomcdn.com/i/o/680322864/4209c19b06e38bbd3b66b5ba/image.png?expires=1741032900&signature=2813cdc5fa70347a94548194ea10f91aca7085edd29a74fb5d56b5efc0d556c2&req=cignFct8lYdbFb4f3HP0gHRjQVjPOcsMRkPm3ewjQSudSDFTRI3zFANNd9Oe%0AgHc%3D%0A)

Change it as follows, Note: mind the rules_version and ensure you are reflecting the correct rules_version.

![](https://downloads.intercomcdn.com/i/o/680323054/f55c38f9a451a6e03728a2e7/image.png?expires=1741032900&signature=729462320290d97cbe94df0334c3fd19d45be77020699477be455edd9e62f744&req=cignFct9nYRbFb4f3HP0gPIjjFISfK83lPkByRQRH6dUxngBE8cky5mOo%2F2P%0Aing%3D%0A)

4) Publish.

That's it, you are now switched to Production mode. Thanks.

Tags: Firebase Cloud Firestore project

---

#### 3. Make sure you give the necessary permissions to firebase@flutterflow.io editor account in your firebase project

You will need to add the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Users & Permissions.

If you don't have Cloud Functions Admin, Editor, and Service Account listed next to firebase@flutterflow.io, you have not completed this step.

Here are the instructions on how to add the required cloud permissions to your project.

![](https://downloads.intercomcdn.com/i/o/680326189/9ad76299af0ce1b98d86ca48/image.png?expires=1741032900&signature=5bfae3fe19b1906bf8349b4ad34bdd56f7829e7b408f532b5c5bbe8a7015c101&req=cignFct4nIlWFb4f3HP0gPR3s6ThFQ5v25csW6t3HFY9d1JgXQ8x8wiBs%2Fmg%0APg4%3D%0A)

---

#### 4. Make sure you at least one collection created in FlutterFlow

Select the Firestore tab from the left menu. If you have no collections listed, you will need to create one.

This article will walk you through step-by-step on how to create a collection.

​

![](https://downloads.intercomcdn.com/i/o/680328089/b103b6602010021011856bc3/image.png?expires=1741032900&signature=a7c8a4a54c104cff5ddb64a3e026f528b473acbabacf64510e7fbcd44e8f30d7&req=cignFct2nYlWFb4f3HP0gPGT%2F6S0721bLD8T5eYK%2FtpmahiHENeDJchgo%2FVz%0AML0%3D%0A)---

#### 

5. Make sure that at least one of your collections has at least one document. 

You can use the CMS in FlutterFlow to confirm that you have at least one document. Select Manage Content and view your collections.

If you don't see any data listed, you will need to add this data.

This article will walk you through step-by-step on how to use the FlutterFlow CMS to add data to your collection.

​

![](https://downloads.intercomcdn.com/i/o/680328666/3c734a412968c1b3b4b14fb7/image.png?expires=1741032900&signature=e19f8f0e7fde26ae2094037c23ffb66bd34ee14c656ae3f84558adc58066eae8&req=cignFct2m4dZFb4f3HP0gJetCUdvEnqD%2BGDGvRAw5JabsR4gEyVrlfUqd5II%0AZEc%3D%0A)![](https://downloads.intercomcdn.com/i/o/680329585/a05dbf42e0ed5b434593413a/image.png?expires=1741032900&signature=82f4515b8be8e0dccfd51203f886f0991e9bb9374f31c8ef6b0434168c341b2a&req=cignFct3mIlaFb4f3HP0gASay6zLdZFcOkKECr1AFh%2BYRKRdtxINKIfsdgu4%0AwGQ%3D%0A)---

#### 

6. Make sure you deployed your database rules with the proper permissions

From within your FlutterFlow project, select Firestore > Settings > Scroll down to Firestore Rules > select Deploy/Redploy.

![](https://downloads.intercomcdn.com/i/o/680315400/9223585271b4a728ab31e373/image.png?expires=1741032900&signature=5d7ba3988308f9493263a9512be540b81a16220992b9f7375dda03415dab223c&req=cignFch7mYFfFb4f3HP0gIt0Y7ErsFZ2lZcYRAMVHdNMQSiGBhavgIVcbWEq%0AiaY%3D%0A)