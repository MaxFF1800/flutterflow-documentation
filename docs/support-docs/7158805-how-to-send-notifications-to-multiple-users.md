---
title: "How To: Send Notifications to Multiple Users"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7158805-how-to-send-notifications-to-multiple-users"
hide_table_of_contents: true
---

# Use Case

FlutterFlow enables users to schedule and trigger notifications. You may want to automatically send notifications to multiple users from the user's collection when a document is created. This article details a step by step instructions on how to achieve this.

---

# Sample Project

We've created a sample project to demonstrate how to build this in FlutterFlow:

https://app.flutterflow.io/project/auto-notification-2bm5hz

Keep reading for step-by-step instructions to learn how you can build what we have created in our sample project.

---

# Automate Notifications Upon Creation Of A Document

### Project Configuration

Ensure your project is set up correctly with Firebase.
- Here are detailed instructions on how to set up Firebase in Flutterflow

Ensure firebase@flutterflow.io account has all the necessary permissions.
- Here are detailed instructions on how to enable access to your project 

To send notifications, your project must be in the Blaze plan. 

Enable Push notifications in your projects and deploy them.

### Send Notifications

Send notifications to multiple users from the user's collection once a post is added;

In submit button, add a backend query
- Set Query type to Query Collection
- Collection to your data source collection, i.e users
- Query type to List of Documents click save

Add create document action to the button

Set the value to the parameters sent to firebase

add another action, trigger notification action

Set notification parameters with the necessary data i.e (title, message, initial page)

In the recipient section, select multiple recipients

Click on the unset section, a pop will show

Select user document as the source of data

In the available options, select filter list items

Click unset under filter conditions, a pop will show

Select Items in list , under document properties, select Document Exists

Click Confirm , this will pop you back to the previous dialog

In this pop, under available options, select Map List Items

Click unset a pop will show, and under Document Properties select Reference

Click Confirm` in all pop-ups

Close the action chain

The notification will be triggered automatically once a new post has been sent successfully.