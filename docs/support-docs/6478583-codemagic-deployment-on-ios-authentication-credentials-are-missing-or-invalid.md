---
title: "Codemagic Deployment on iOS: Authentication Credentials Are Missing or Invalid"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6478583-codemagic-deployment-on-ios-authentication-credentials-are-missing-or-invalid"
hide_table_of_contents: true
---

Need help identifying your Codemagic deployment error? Check out this article. 

## Invalid Authentication Credentials Error

This means that there was a misconfiguration issue while setting up deployment for App Store. The token used is likely expired or is invalid. 

Learn more about Generating Tokens for API Requests https://developer.apple.com/go/?id=api-generating-tokens

Full error message

```
`Failed Step: Fetch signing files

GET https://api.appstoreconnect.apple.com/v1/bundleIds?limit=100&sort=name&filter%5Bidentifier%5D=appname.com&filter%5Bplatform%5D=IOS returned 401: Authentication credentials are missing or invalid.

Provide a properly configured and signed bearer token, and make sure that it has not expired. Learn more about Generating Tokens for API Requests https://developer.apple.com/go/?id=api-generating-tokens `
```

## How To Resolve the Issue

To resolve this issue, you'll need to generate a new API key for your app and then replace it with the one present inside FlutterFlow. 

Please follow these steps to generate your API Key:

Navigate to App Store Connect, select Users and Access, and then select Keys (blue text).

If you see the Request Access button, click on it.

Click on the Generate API Key. Otherwise, select the Add button (+).

A popup will appear. Enter your API Key Information:

Name: Enter a name for the key. This is a reference and is not part of the key itself.

Access: Select the access type. This link has additional information on roles.

When you are done, select Generate.

Find the row for the API Key you just generated and select Download API Key. A popup will appear, select Download. 

​
Note: If you don't see the Download API Key link immediately, refresh your page.

Return to FlutterFlow and navigate to Settings & Integrations --> Deployment.

Under Private Key, select Upload Private Key. Select the API Key File and then select Open.

After this please try deploying the app again. 

![](https://flutterflow.intercom-attachments-1.com/i/o/570550109/16c23b7d8deb5aa5d86c29e0/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FJPrxRZ2AgTqDCXc7DTyR-2Fezgif.com-gif-maker-20%283%29.gif?expires=1741032900&signature=5dfa39a2b43c1fc8e3a7ec9d964fcdceb3a156efca5df0f2d26ce151ee3f8cd3&req=cScnE8x%2BnIFWFb4f3HP0gNHqLoL5sJXxEwvoYlGCewXGPTFWpJjE5%2FRzlyW9%0Aq%2FI%3D%0A)

# 

---

Still need help? If you are deploying from FlutterFlow and still getting this error after following all the steps outlined above, then please report this issue to support via messengar or email at support@flutterflow.io.

​