---
title: Securing Your API Keys in Private API Calls
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8516352-securing-your-api-keys-in-private-api-calls"
hide_table_of_contents: true
---

## Introduction

Ensuring the security of API keys is a critical aspect of building and maintaining a safe and reliable application. In the realm of private API calls, it's especially important to make sure your API keys are not exposed. This article aims to provide a best-practices guide on where to place your API keys to increase security in a FlutterFlow environment.

​

## The Misconception: Private API Calls Secure Everything

Many users assume that simply marking an API call as 'private' is enough to protect all associated data. However, this is not the case. Private API calls run in a Cloud Function, which means any keys or sensitive data in the body will be secure—as long as they're not passed in from the frontend. Even in private API calls, if you're loading an API key from the frontend (like from Firebase remote configs), then you're still exposing it.

​

## Where to Put Your API Keys

The ideal way to secure an API key is to include it in a request header or directly within the API endpoint URL. This ensures that it is never passed in from the client, thereby maintaining its confidentiality.

​

For example, you can hard-code the key directly into your API call header like this:

​

```
`{ "Authorization": "Bearer YOUR_API_KEY_HERE" }`
```

Or directly within the API endpoint URL:

​

```
`https://api.example.com/resource?api_key=YOUR_API_KEY_HERE`
```

The key should never be a variable that gets passed in from the frontend, as that would make it accessible via the client-side code, defeating the purpose of using private API calls for secure operations.

## 

Verification

After implementing these changes, a straightforward way to verify that your key is secured is by downloading your application code and checking to make sure the API key doesn’t appear in any frontend files.

​

## Example: Not Secure

## 

![](https://downloads.intercomcdn.com/i/o/862308234/0c45685f81e5c605e38402d4/image.png?expires=1741032900&signature=0dc64129a5ff37e6d4d63614c9864b7bc419f47b008bbfa62a6fd0c99a1c0de7&req=fCYlFcl2n4JbFb4f3HP0gKIv0DE8tleUc1hxpRno30yUpY0PR%2BY2mdQbPVFy%0AdCY%3D%0A)

## Example: More Secure

![](https://downloads.intercomcdn.com/i/o/862308652/19d1fbaa7426e7dec7ef163c/image.png?expires=1741032900&signature=32658599397bc4e86f730c447a25b64d8b1b7857761c9a02073207a1b048b4d0&req=fCYlFcl2m4RdFb4f3HP0gI8y4jHgTZ28I3tJzYYNFo7PfXDdbSCXa0aekP7o%0Ah64%3D%0A)

## 

Conclusion

By adhering to these best practices, you can increase the safety of your API keys even while making private API calls. Remember, the goal is to keep all sensitive data, including API keys, away from the client side of the application to ensure optimal security.

## 

Further Reading and Help

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help

​