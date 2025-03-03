---
title: Understanding Firebase Storage Limits in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8115288-understanding-firebase-storage-limits-in-flutterflow"
hide_table_of_contents: true
---

# Introduction

In the development journey with FlutterFlow, you might find yourself asking about the limits of Firebase storage. Whether you're working with images, videos, or other types of files, understanding how much space you have available is crucial. In this article, we aim to shed light on this topic.

​

# Firebase Storage Limits

Firebase indeed imposes limits on storage, and these limits depend on the plan you are using. Firebase offers two types of plans: the Spark plan (free) and the Blaze plan (pay as you go). Below is our summary of their plans as they relate to usage in FlutterFlow. For the most updated pricing and plan information, please visit the Firebase Pricing page.

​

## Spark Plan

The Spark plan is a free tier that provides up to 5 GB of storage. This means you can store data up to this limit without any cost. Once you reach this limit, you will need to consider upgrading to a paid plan to continue using Firebase Storage.

​

## Blaze Plan

The Blaze plan is a pay-as-you-go plan that charges you based on the amount of storage you use. The price per TB decreases as the amount of data stored increases, providing better rates for high storage usage. You can find the most current details on the Firebase Pricing page.

​

# Firebase Operations Limit

Apart from storage space, Firebase also sets limits on the number of operations (upload, download, delete) that can be performed on the storage each day, particularly on the Spark plan. It's crucial to consider these limitations when planning your app's functionality and user experience.

​

# Managing Firebase Storage Wisely

Remember, managing your Firebase storage effectively is vital to avoid unnecessary costs. For example, deleting unneeded files or compressing files where feasible can help keep your storage usage in check. This practice is especially useful for apps dealing with high volumes of data or larger file types, such as images or video content.

​

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace