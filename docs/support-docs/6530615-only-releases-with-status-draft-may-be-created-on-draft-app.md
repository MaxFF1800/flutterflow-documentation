---
title: Only releases with status draft may be created on draft app
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6530615-only-releases-with-status-draft-may-be-created-on-draft-app"
hide_table_of_contents: true
---

Not sure which type of Codemagic error you're running into? Check out this article on how to identify your Codemagic error.

# Full Error Message

```
`Google Play failed to upload artifacts. Only releases with status draft may be created on draft app.: 

{ 

 "error": { 

 "code": 400, 

 "message": "Only releases with status draft may be created on draft app.", 

 "status": "INVALID_ARGUMENT" 

 } 

}`
```

# Most Common Error

One of the most common causes of a publishing error when deploying to the Google Play Store is when you haven't filled out all the necessary information in the Play Store before deploying the application.

# How To Resolve This Issue

Please make sure that you fill out all the information in the Play Store including the store listing information and the setup information. Then, please follow the steps outlined below:

## 

Step 1

On the projects dashboard, navigate to the settings and integrations section.

​

![](https://downloads.intercomcdn.com/i/o/792418784/18974fbcf654710c6a8bbab4/Snip20230725_1.png?expires=1741032900&signature=0a7733b8cf8424801458ac9e3f27ac1068f5ffa526e19080c3e6dd5ef3105163&req=cyklEsh2molbFb4f3HP0gD9bcEUz8LhYkVqSM5WgNNbpmmuaG84sAlG%2FX4Ys%0AUZM%3D%0A)

## Step 2

Navigate to the Mobile Deployment section.

​

![](https://downloads.intercomcdn.com/i/o/792419447/1deb20dd44df8be6c7246b83/Snip20230725_2.png?expires=1741032900&signature=73a26f42812923a079eb868c619d4ea6344228dbd0ee86b662b3df9fd667e53b&req=cyklEsh3mYVYFb4f3HP0gOO83B4V4mvTOmWWw3SBBChfStRrVc1ag2f%2BGMl7%0A9FQ%3D%0A)

## Step 3

Under the Google Play Store Deployment section, toggle on submit as draft.

![](https://downloads.intercomcdn.com/i/o/792419980/add510b2c8debac70f915923/Snip20230725_3.png?expires=1741032900&signature=dfff0cbc0b55b196036adef3d05415bf4422ec0da048ccba84505bbaf1153cd4&req=cyklEsh3lIlfFb4f3HP0gDKI85f7x%2FS5huX8ASmrLWpKBUXzvqAQ1O2%2BSfxe%0ALwo%3D%0A)

# 

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace