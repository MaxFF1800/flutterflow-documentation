---
title: "Code: 403, The caller does not have permission. status: PERMISSION_DENIED"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6509670-code-403-the-caller-does-not-have-permission-status-permission_denied"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

One of the most common causes of a publishing error when deploying to the Google Play Store is attempting to deploy without configuring the permissions correctly. 

# Full error message

```
`Google Play failed to upload artifacts. The caller does not have permission: {

 "error": {

 "code": 403,

 "message": "The caller does not have permission",

 "status": "PERMISSION_DENIED"

 }

}

`
```

# How to resolve this issue?

This could be due to an invalid JSON file or permission issues with the service account. Please make sure you have done the following:

Created a service account in the Google Play console

Set the service account access to “Editor”

Created a JSON private key

Added the JSON key to FlutterFlow.

Navigated to your Google Play Console API access and granted access to the service account

Given the service account access to your application

Invited users to the service account

Check out this guide for detailed explanation.

# Issue was not resolved after following the given steps

If you are deploying from FlutterFlow and still getting this error after following all the steps outlined in our documentation, then please report this issue to support via Chat or Email at support@flutterflow.io.