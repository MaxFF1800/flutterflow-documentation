---
title: Backend Issues
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6126049-backend-issues"
hide_table_of_contents: true
---

These common steps are recommended to perform for any issue faced with the backend.

Ensure you have added the following cloud permissions for firebase@flutterflow.io: 

Editor 

Cloud Functions Admin 

Service Account User (Here are instructions on how to do this)

---

Update your Firebase rules. Here are instructions on how to do this.

---

Delete firebase@flutterfow.io from your authenticated users and then deploy the firestore rules again and validate the schema. 

​
![](https://downloads.intercomcdn.com/i/o/568617529/b45db5f32a09864d9a97a28e/image.png?expires=1741032900&signature=695936da2e1cfd6ae8ebe6cf0f3bbc4280839344fb070ab1e6a48dbb08eb1059&req=cSYvEMh5mINWFb4f3HP0gP3U%2Fk6O0knA7kaU2OrzUCHezfBq%2FTqCfRHHyHBe%0AxqU%3D%0A)

---

Make sure all the data field types and field names should match in Firestore and FlutterFlow. Here are instructions on how to do this.

---

Validate the Firestore schema by clicking on the blue Validate button in Firestore -> Settings in FlutterFlow. This ensures that everything is configured correctly and the Firestore collection schema matches with the Collection schema configured in FlutterFlow.

![](https://downloads.intercomcdn.com/i/o/504125945/de5b6bd01585ec3c356241a2/Screenshot+2022-04-28+at+1.32.09+AM.png?expires=1741032900&signature=9a5e0e34001eba58c26338f3ce68be98afa5e1fd43a4818466e7b1f6fa341435&req=cSAjF8t7lIVaFb4f3HP0gOXez74INPfDlhVa0EXnsx7AJD1mJ2sJ5IldRlkf%0AfF0%3D%0A)

---

If you have already completed the Firebase setup, remove the existing permissions and complete a new setup from scratch. Here are instructions on how to do this.

---

Make sure you've added app.flutterflow.io to Authorized Domains under the authentication tab in Firebase.

---

Ensure you are on the latest version of FlutterFlow by selecting (ctrl/cmd + shift + R). After you have done this, clear your browser cache and log out/in to FlutterFlow.

---

In order to use Cloud Functions like Push Notifications, Payments, etc. Please make sure your Firebase project is on a Blaze Plan.