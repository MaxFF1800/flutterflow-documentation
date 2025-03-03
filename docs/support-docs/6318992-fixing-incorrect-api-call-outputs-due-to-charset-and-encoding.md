---
title: Fixing Incorrect API Call Outputs Due to Charset and Encoding
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6318992-fixing-incorrect-api-call-outputs-due-to-charset-and-encoding"
hide_table_of_contents: true
---

## Overview

API responses can vary based on factors like charset and encoding, occasionally leading to what may seem like incorrect outputs. This brief guide offers a solution to address and correct such issues.

## 

Solution for Accurate API Responses

Ensure the API header is correctly set up by including the following elements:

Content-Type: application/json

Charset: utf-8

​

![](https://downloads.intercomcdn.com/i/o/996384321/4cabbc546ffb79ef48375a03/SCR-20240319-uqyt.png?expires=1741032900&signature=da1b99de11519d79ecca667e8a982f088e31c19b2ca3eb4e85ba8fa9efc14471&req=fSkhFcF6noNeFb4f3HP0gEwZCtIPOn8AZ8amSGdUMI%2B2ZKe%2F1xVC%2BvmNYWo6%0Apgk%3D%0A)

You can also set up an API advanced settings whether to force the response to be decoded as UTF-8:

​

![](https://downloads.intercomcdn.com/i/o/996382329/3728fe98e839c564c15bac70/SCR-20240319-upsl.png?expires=1741032900&signature=ae4914b6fea09aba303b53f1e870f84550408df8cd774d1f97910872f2e9d4e1&req=fSkhFcF8noNWFb4f3HP0gEN%2B%2BDdiYjIJFtlIZyYUFw7ze%2Fv%2BKtfoEBjFn2To%0AMKI%3D%0A)

By verifying these settings, you can get more consistent and accurate outputs from your API calls.

---

 Additional Resources:

YouTube Tutorial: API's

FlutterFlow Documentation: API Calls 101

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help