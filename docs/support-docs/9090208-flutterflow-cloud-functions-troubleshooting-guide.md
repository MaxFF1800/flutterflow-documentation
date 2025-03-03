---
title: FlutterFlow Cloud Functions Troubleshooting Guide
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9090208-flutterflow-cloud-functions-troubleshooting-guide"
hide_table_of_contents: true
---

Cloud Functions enables developers to execute backend code in response to events triggered by Firebase services (callable) and HTTPS calls.

Various situations might cause cloud functions to malfunction, often stemming from setup problems or coding mistakes within the cloud function's script.

This article guides you through common challenges with Cloud Functions in FlutterFlow.

## Errors Shown In The Builder

---

Occasionally, you may encounter two specific errors: Out of Date (Error) or Not Deployed (Error).

These errors can arise from a variety of situations. If you're facing these issues, follow this troubleshooting guide designed to help you resolve them.

Out of Date Error:

![](https://downloads.intercomcdn.com/i/o/998270281/86d654faaa684e2f00e8c879/image.png?expires=1741032900&signature=308c80230029f20cd3e9956d0e564442d39bd70264194a01e0e7cf6944454eba&req=fSkvFM5%2Bn4leFb4f3HP0gAgnIEDzeQp%2FGBYEtsm2V52seklUVoeZ6Jna9gVm%0AZa8%3D%0A)

Not Deployed Error:

![](https://downloads.intercomcdn.com/i/o/998253140/c84a214e6cf7e51204a914d5/image.png?expires=1741032900&signature=74bc342f1e8cf03669da130c67c3f9ce13fd5d1eba688346cdb6133ac1c796e3&req=fSkvFMx9nIVfFb4f3HP0gFwoaDJjjAskc1pAQhGpDIJ5Jpl0%2F2EE0uWuvzBi%0AdBQ%3D%0A)

# Key Checks for Resolving Deployment Errors

---

Below are essential steps to verify your project is correctly set up for cloud function deployment.

### 1. Verify firebase@flutterflow.io has all necessary permissions

To ensure FlutterFlow works smoothly with your project, you'll need to adjust some settings in Firebase, a tool we use in the background. Here's how you can do it, 

First, we need to make sure that an email associated with FlutterFlow, which is firebase@flutterflow.io, has the right kind of access called cloud function admin permission in your Firebase project. This lets FlutterFlow do its job without any hiccups.

Besides the admin permission, we need to add a couple more types of permissions for FlutterFlow. These are called editor and Service account user. 

How to Add These Permissions:

Go to the Firebase website and log into your account.

Find your project and open Project Settings.

Inside the settings, look for a section named "Users and Permissions." That's where you can manage who has access to your project.

You'll find an option for "Advanced Settings Permissions". Click on that. This will open Google Cloud functions, locate firebase@flutterflow.io and click on the edit button to add the permissions

![](https://downloads.intercomcdn.com/i/o/998292084/ec935b62ee83fcde579da3b6/firebase.png?expires=1741032900&signature=91581562d5d87965f66e49b5d7716d41688ba693b66eeb8f295bbf54feae7d6d&req=fSkvFMB8nYlbFb4f3HP0gGBR7u7VQalsc78YvBOi0L345qe2AORW5E%2BTPQe2%0A2AA%3D%0A)

![](https://downloads.intercomcdn.com/i/o/998292533/fa799a3b3fa4a82791b5b878/gcp.png?expires=1741032900&signature=6edda8e21331a7596411576b84996c979af2cb3fe6e64e4e0a7378e35029ab6b&req=fSkvFMB8mIJcFb4f3HP0gNUZzaQoX%2BipDvr1ZA5z5cbJkEh0tyahnf7deBTu%0A4S4%3D%0A)

### 2. Make sure there are no errors in the custom code for cloud functions

Sometimes, small mistakes in your code can stop your cloud function from being deployed. To avoid this, it's a good idea to double-check your code for any errors before you move forward.

This can be done locally on an IDE of your choice

![](https://downloads.intercomcdn.com/i/o/998296080/ecadedd30b95ef6310b77786/code.png?expires=1741032900&signature=dd1ce169942ade28e049f5aa3db863a762a59ae0ef6bceec698425646bca6077&req=fSkvFMB4nYlfFb4f3HP0gHFrB74uh0gGZk8Vw%2Fz2UUmm9c8MAo6xyGcWFyEj%0Asec%3D%0A)

### 3. Make sure the project is on blaze plan on Firebase

If Cloud functions cannot be deployed, be sure to confirm if the project is in blaze plan and not spark plan,

Additionally, cross-check the logs in the console log. Sometimes, Google Cloud Platform (GCP) sends the log back to inform you that the project is in the Spark plan

In some cases, even if Firebase shows you're on the Blaze plan, there might be a billing issue on the GCP. Make sure your billing account is active and has yet to expire. 

### 4. Check if any other cloud function deployment succeeds (push notification, stripe.)

If some of your functions are already working as expected, it means your Firebase settings are properly in place. Your next steps should be to examine the settings specific to Cloud Functions and review the code itself for any mistakes or incorrect regional settings.on

### 5. Make sure the region is selected and is not left as [default] - on both advanced Firebase settings and in the cloud function deployment page

The region for the cloud function deployment should be set to the region that is set in your Firebase project setting

The region should not be left as default; this region should co-respond with all deployed cloud- functions in the project

![](https://downloads.intercomcdn.com/i/o/998298228/0ee892b8252cbe47356c17d9/cloud_function.png?expires=1741032900&signature=b05f1f014d77428e1ffb9200520878c3facd682421913e41e5f1f31405973780&req=fSkvFMB2n4NXFb4f3HP0gKb2616gaAbUX0%2Fq1wZJ2FOlthZQ5H7JgYMAdgzy%0AkW8%3D%0A)

![](https://downloads.intercomcdn.com/i/o/998298657/92cbc12bdcf55cdb4d78b604/firebase_project.png?expires=1741032900&signature=01d75b14d6db58ba319ba7a4e63653f86c53621a3833bc2892cbdf75d80453fb&req=fSkvFMB2m4RYFb4f3HP0gMeuW4rA92sdW8czI%2BAgW%2Bu9z2%2B0ZMZfrsLpR8zl%0AkgE%3D%0A)

In some cases, where you deployed some of the cloud functions in different regions, you will need to delete any that already exist but in the wrong region, modify the region, and then re-deploy again

### 6. Different Cloud function protocols (HTTP VS Callable Functions)

Suppose you had deployed the cloud function as an HTTP function. In that case, if you try to redeploy the same function as a callable function, the deployment will fail, and you will get this error [makeUserAdmin(us-central1)] Changing from an HTTPS function to a callable function is not allowed. Please delete your function and create a new one instead. 

To resolve this, you will have to delete the cloud function in the Firebase Cloud function section and then modify the Function in FlutterFlow and re-deploy the function

### 7. Verify that the package.json file is not left blank and that it doesn’t have invalid characters

Confirm that you use the generated package.json file, and don’t make any changes to the file unless you are adding the packages.

If FlutterFlow fails to generate the file details, it is recommended to use this

```json
{

 "name": "functions",

 "description": "Firebase Custom Cloud Functions", 

 "engines": { "node": "18" }, 

 "main": "index.js", 

 "dependencies": { 

 "firebase-admin": "^11.8.0", 

 "firebase-functions": "^4.3.1" 

 }, 

 "private": true 

}
```

### 8. Ensure that the packages used in the cloud functions are included in the package.json file

It's normal to forget to include third packages used in the cloud function in the package.json file. For instance, if you are using axios, please ensure that the package is already included in the package.json file

![](https://downloads.intercomcdn.com/i/o/998302686/03e2d4eb4316849f2ca0fd27/json.png?expires=1741032900&signature=5a8c1f0645c96ae5b5da644662c1720b4b4960f3fe2601de7bec0188308c8271&req=fSkvFcl8m4lZFb4f3HP0gAVn%2Fjcn7orjhaEIhlxMsuoIHrNyHpy4jBj4UeFF%0Ag7A%3D%0A)

### 9. Cross-check that the version of the third-party library used is valid

Check that the version of the third-party library used is valid, i.e., the version listed in the package.json file should be among the versions listed in the package's version archive. See https://www.npmjs.com/package/axios?activeTab=versions

![](https://downloads.intercomcdn.com/i/o/998303574/5378da9daa22532e02c19ac4/npm.png?expires=1741032900&signature=cd02a52b4a6f1a600ae971035cb5664faeff41e75934932a09921bcc6003a56a&req=fSkvFcl9mIZbFb4f3HP0gOemiH8bASsUwWVoIAcUaKcZzGU20zeSC6r03ZOf%0A94M%3D%0A)

### 10. Check for un-deployed Firebase rules

Lastly, ensure that you have deployed your Firebase configuration settings from FlutterFlow. This includes Firestore rules and Firestore indexes.

These can block cloud function function deployment when they are still not deployed

# Conclusion

---

We hope this guide provides you with the necessary steps to successfully troubleshoot and resolve any issues you encounter with Cloud Functions in FlutterFlow. Remember, careful attention to setup details and adherence to the outlined checks can prevent many common problems. 

Should you require further assistance, don't hesitate to consult the FlutterFlow documentation or reach out to our support team. Your success is our priority, and we're here to help you make the most out of FlutterFlow's capabilities. Happy coding!

# Additional Resources

---

Cloud Function CORs Null Issue

Cloud function error for generating FCM token

FlutterFlow Documentation