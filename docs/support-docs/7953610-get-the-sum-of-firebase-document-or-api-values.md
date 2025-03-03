---
title: Get the Sum of Firebase Document or API Values
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7953610-get-the-sum-of-firebase-document-or-api-values"
hide_table_of_contents: true
---

# Introduction

Sometimes, when working with databases, you might need to calculate the total of all values for a certain item or category. This is especially common when using APIs or working with Firebase. If you're looking to add up values from a database, this easy-to-follow guide is for you. We'll break down the process into simple steps.

# Getting Started

## Step 1: Identify Where You Need the Total

First, decide where in your code you need to display the total sum. This could be a text field or a variable in your code where the final sum will be shown.

![](https://downloads.intercomcdn.com/i/o/751232978/37ddb0aa6dcde0e86a1a0fb2/SCR-20230528-mncb.png?expires=1741032900&signature=6c0e6301af697a5e974c3c4e72a15fb7709d28f0aad7739de1dddfd0888112c3&req=cyUmFMp8lIZXFb4f3HP0gIrB8Mke2sc70M1UoVH%2BTld1LVUE71gWcauxcCMg%0AZK0%3D%0A)

## Step 2: Prepare Your Data Type

Next, you need to specify what kind of data you're adding up. For example, if you're working with numbers with decimal points, you'll classify your data as `double`. Make sure to indicate that you're dealing with a list of these values.

![](https://downloads.intercomcdn.com/i/o/751233395/eba44b932cb6a7789513c8ae/SCR-20230528-mnow.png?expires=1741032900&signature=1044ff39e085b367cff69d363b29e420ba4d2aa0b57b1b71955f34f1cb41582f&req=cyUmFMp9nohaFb4f3HP0gK%2FD2irA2NUCxTXiQczXf7yI6u6Xw2sCeMPY%2FsgY%0Ac%2F4%3D%0A)

## Step 3: Select Your Data

Now, choose the specific data you want to sum up. You do this by picking out the documents from your database query and then mapping out the exact data field you're interested in.

![](https://downloads.intercomcdn.com/i/o/751233801/d189156c37f242d033956652/SCR-20230528-moal.png?expires=1741032900&signature=a13db27a58668b53d36be46d10fb081e0068c96b00f600856224aefba9d0182a&req=cyUmFMp9lYFeFb4f3HP0gCUQ1GWH1%2BoxIS2t%2BHwe4eKxMJ%2FrzfTdgIHjbWVT%0ANGg%3D%0A)

## Step 4: Calculate the Sum

With your list of values ready, store them in a variable (let's call it `var1`). Then, decide on the format you want for your result. Use the `reduce` function to add up all the values in your list, `var1`, to get your total sum.

![](https://downloads.intercomcdn.com/i/o/751234340/388e35c2e70b82ef7553304b/SCR-20230528-mosb.png?expires=1741032900&signature=a4405137e610b00a8afed00bd49be734674f878f92223c2292dc5bd65d172390&req=cyUmFMp6noVfFb4f3HP0gMPa9LAkln0u2Bp7vy4syi7%2FJy8dNd%2BeMBUs1m1w%0A6N8%3D%0A)

## 

Step 5: Checking Your Results

After completing these steps, you should have the total sum displayed where you need it. If it looks right, you've successfully calculated the sum!

![](https://downloads.intercomcdn.com/i/o/751232715/6aedd4ee8ba8d5991006d2d8/SCR-20230528-mmsj.png?expires=1741032900&signature=cc4dc684968f4c756cfb6464eb12c551c580006dcc616bd3304f2335e51d4803&req=cyUmFMp8moBaFb4f3HP0gPMlqaqMVbVNEkQ3rRuH2jQw56yWGybXIKzlJS3C%0A2N0%3D%0A)

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace