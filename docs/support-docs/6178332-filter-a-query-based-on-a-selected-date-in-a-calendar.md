---
title: Filter a query based on a selected date in a calendar
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6178332-filter-a-query-based-on-a-selected-date-in-a-calendar"
hide_table_of_contents: true
---

This article describes how you can filter your ListView data based on the date your user selects on a calendar.

![](https://downloads.intercomcdn.com/i/o/505403876/fddd1d74365ea98b3e9534b0/ezgif.com-gif-maker+%2845%29.gif?expires=1741032900&signature=ac6b22e5b520a69075a54ede2dde057bbae78ef73119e4a7519e273e09712bbc&req=cSAiEsl9lYZZFb4f3HP0gBjzeqHh%2Bw6sq0YQ%2FJfPvuy1nciL%2Bq3ix4ehMfoP%0AvzY%3D%0A)

# Prerequisites

Before you get started with the rest of this article, you will need to:

Complete Firebase setup

Create a Firebase collection

Add data to your Firebase collection

Have a ListView with data from Firebase

Have a Calendar Widget in your project

# Create Filters For Your ListView

In order to filter your ListView items by the date selected on the calendar, you will need to create two filters for your listview. We'll create one filter for Start Date and one filter for End Date. The result will be the date selected!

Select your ListView from the Widget Tree > Backend Query > + Filter

![](https://downloads.intercomcdn.com/i/o/505415218/f0d4ba8ff289ac9c10534b68/image.png?expires=1741032900&signature=e93c024adccc760658b78f3718e04d94b62717f24c7ae914f79c67fafe5649c6&req=cSAiEsh7n4BXFb4f3HP0gBAKTVXkAHMEzPrNd0o9NAZkKHC7j%2FMoXprfa77z%0AC1M%3D%0A)

# Create Filter To Filter For Start Date

A list of dropdowns will appear. Select the following values:

Under Field Name select the field you want to filter your data by (e.g. eventDate).

Under Relation select Greater Than

Under Value Source select From Variable

Under Source select Widget State

Under Available Options select calendarSelectedDay

Under Range Part select Start

![](https://downloads.intercomcdn.com/i/o/505413272/12ec77236818824e2f5866b0/image.png?expires=1741032900&signature=7624adeb25136eb7ed78b4d3ffdb9cfe11b6cc436482b008504b1a612b45597d&req=cSAiEsh9n4ZdFb4f3HP0gG4sWuSPdyIAS4hf%2BvCP9yqZcaOLHsqXxCJp2pwl%0A%2FOI%3D%0A)

# Create Filter To Filter For End Date

A list of dropdowns will appear. Select the following values:

Under Field Name select the field you want to filter your data by (e.g. eventDate).

Under Relation select Greater Than

Under Value Source select From Variable

Under Source select Widget State

Under Available Options select calendarSelectedDay

Under Range Part select Start

![](https://downloads.intercomcdn.com/i/o/505417361/07cb5520ed013cd649b9a356/image.png?expires=1741032900&signature=bf9055d19f158dfd83c4c2230b9e30509d1a74bfd2f82d446ce64a9bb97bd0e6&req=cSAiEsh5nodeFb4f3HP0gNh4Zt0J90BPAX4Vv2UAhwtH6H3mMud4SbpzVRvs%0Actk%3D%0A)

# Set the initial date for your calendar

The initial date is the option that will be highlighted by default. If you don't set an initial date for your calendar, you will get a gray screen in Run Mode.

Select your Calendar Widget and navigate to the right Properties Panel. Locate the Initial Date section and click the dropdown. A list of options will appear. 

In order to set the Date by current day, select:

Source: Global Properties

Available Options: Current Timestamp

![](https://downloads.intercomcdn.com/i/o/505418964/b48d0d187d3214e603b072a5/2022-04-29_15-45-34.jpg?expires=1741032900&signature=94069c168877952c436c31beec3bb99ccca6ae5aa16d0d44792d4c68f124c729&req=cSAiEsh2lIdbFb4f3HP0gHf%2F84%2BglHrnk8is57BY9HSt7HDyha1R0xZ4D3H9%0A5%2BM%3D%0A)

![](https://downloads.intercomcdn.com/i/o/505420037/e4fef7fca6a7f10e134642e9/image.png?expires=1741032900&signature=e55af96d13cce2525ebd8d969443961064456420ab827c0486ffd11a86ef3361&req=cSAiEst%2BnYJYFb4f3HP0gFmVuvjbnyPNHcgaRaDtxJQNgwZB7by%2B%2FY9asp1d%0AjSY%3D%0A)

🎉 Congrats your new feature is complete! To test your new feature, select Run and wait for your new changes to compile!

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace