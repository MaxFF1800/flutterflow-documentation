---
title: "Can't deploy Firestore Database rules"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7030020-can-t-deploy-firestore-database-rules"
hide_table_of_contents: true
---

This article will walk you through troubleshooting steps if you are unable to deploy your Firebase Rules.

---

1. Validate that you have created your Firestore Database

Without a database created in the Firebase project, there is no way for FlutterFlow to deploy your rules. 

​

Open the Firebase Console for your project and select Create database. 

Video:

Create a firebase firestore database in Firebase to start [ time: 1:50 to 2:05 ]

![](https://downloads.intercomcdn.com/i/o/679039105/0e5566b493122ff1f7c3c54d/image.png?expires=1741032900&signature=43255db34da14e62024850bfcd035d0c19b0f5f537551a80e1c449c72ef25c6a&req=cicuFsp3nIFaFb4f3HP0gLHmKrsuyIH%2FuwBPf8TjLSHBpIF9hq2gSD5pldYn%0Ar3o%3D%0A)---

2. Validate that the three necessary permissions are granted

In order to deploy Firebase Rules, you will need to add the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Users & Permissions.

If you don't have Cloud Functions Admin, Editor, and Service Account listed next to fireabse@flutterflow.io, you have not completed this step.

Here is a video you can watch to see how you can add the permission

![](https://downloads.intercomcdn.com/i/o/501028815/d4d5ea7c25cc3f0f78aa459a/image.png?expires=1741032900&signature=108d49a8022ae903c290a081fa5ef9b8f7c7c7060aa44794c0afb2f140fc10e9&req=cSAmFst2lYBaFb4f3HP0gN%2F1m%2Bu6JT8H1hOQeSs8p7Fnl4slsaAHCw%2Bs5eE4%0Ag%2B8%3D%0A)![](https://downloads.intercomcdn.com/i/o/678931959/f06d9b8c226f283a8361ef86/image.png?expires=1741032900&signature=4e399d5122ce2bcdb792d127e55e5633678e8fc96814b4aa84c51e1e9472a457&req=cicvH8p%2FlIRWFb4f3HP0gIiQKjVOY1gFFsBXE4%2Fuw7TE3Z9pitfd%2FIJecd2N%0AnEA%3D%0A)![](https://downloads.intercomcdn.com/i/o/679040031/e9be3cc317695a95bf576841/image.png?expires=1741032900&signature=733476a83fc2b5a4212b65243e1cdef0743ee604e59f359d06300d2b14922a36&req=cicuFs1%2BnYJeFb4f3HP0gByJdTfYgaNrVdO2%2ByJT9RpO9ExYZRa93RPeTRYP%0AWDY%3D%0A)---

3. Validate that you have selected the GCP location for your Firebase project

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > General.

If you see Not yet selected, you have not completed this step.

![](https://downloads.intercomcdn.com/i/o/679262148/de8500acaeb8d261cb83d983/image.png?expires=1741032900&signature=653c249e647520fe7151acd6903b0d2757a6066c8e01f3dc61accc0b76982810&req=cicuFM98nIVXFb4f3HP0gIfviynBCD6MstKklbEd71PWMHMt3QpiCqDij0iq%0AtLs%3D%0A)

Select the pencil and complete setup. 

Tip: Once created, this can not be changed. You can learn more about selecting locations here.

​

---

After checking these 3 steps, you should be able to successfully deploy your database rules.