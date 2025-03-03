---
title: "Can't deploy firestore database indexes."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7034528-can-t-deploy-firestore-database-indexes"
hide_table_of_contents: true
---

Whenever you add or edit a query with different filters, FlutterFlow will prompt you to deploy your indexes. By deploying indexes, FlutterFlow creates your database indexes on your behalf in the Firebase project's Firestore database indexes.

Before deploying indexes, it is important to read this documentation about indexes provided by FlutterFlow.

​

![](https://downloads.intercomcdn.com/i/o/680278724/54923a85ed5341bef38f2b88/image.png?expires=1741032900&signature=761df433844c7f4628aefee519cf117aac1dc650db91dea91ecde8508678f98d&req=cignFM52moNbFb4f3HP0gG0U7kgLkJLpmF7Sy%2BoBY6hJ%2BJjn4quDYAlTcV%2Bc%0AKDA%3D%0A)

​

If you are unable to deploy indexes, please complete these troubleshooting steps:

Ensure you have email sign-in enabled. Here are instructions on how to do this.

Ensure you have added the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account User. Here are instructions on how to do this.

Update your Firebase rules. Here are instructions on how to do this.

Ensure you are on the latest version of FlutterFlow by selecting (ctrl/cmd + R). After you have done this, clear your browser cache and log out/in to FlutterFlow.

​

---

In the event that the troubleshooting guide does not help you solve the issue, it is possible that you have reached the limit for the number of indexes allowed.

To confirm this, go to your Firebase project, navigate to Firestore database, and select Indexes. If you see any notifications or error messages regarding the limitation of indexes, you will need to delete some indexes. In most projects, the maximum number of allowed indexes is 200, although this can vary depending on the plan and project.

​

Note: When you modify, add, or remove queries in the FlutterFlow project, FlutterFlow will once again prompt you to deploy the necessary indexes. This ensures that your application continues to function efficiently.

​