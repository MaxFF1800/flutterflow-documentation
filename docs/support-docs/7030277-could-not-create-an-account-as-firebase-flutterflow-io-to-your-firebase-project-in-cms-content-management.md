---
title: "Could not create an account as firebase@flutterflow.io to your firebase project, in CMS - content management"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7030277-could-not-create-an-account-as-firebase-flutterflow-io-to-your-firebase-project-in-cms-content-management"
hide_table_of_contents: true
---

If you believe all your configurations are correct, Or it was working before and you see this error now.

![](https://downloads.intercomcdn.com/i/o/679012922/0081332dede77c6ab7ce4b11/image.png?expires=1741032900&signature=edd779268dccffa43109024a38b89387f7f4b2c260aaafc8d97562c61f84f015&req=cicuFsh8lINdFb4f3HP0gLi7f4UrpWZMD%2F%2FMsA%2B%2Fci%2BW0kEBVGQBjPZ6KUMW%0A8sI%3D%0A)

1- Please go to firebase project > Authentication and search for firebase@flutterflow.io user

​

![](https://downloads.intercomcdn.com/i/o/679015967/5549e3971d3af5dd41cec0ae/image.png?expires=1741032900&signature=b183ceb84cba94562a206d846f77346ec2016ad43da00847e6c3c6f5a1d334d4&req=cicuFsh7lIdYFb4f3HP0gNAY6MY8ycok%2BB4HmWYdXGNsOdQspfKip7yuyGh4%0ABn4%3D%0A)

2- Load the user by typing the firebase@flutterflow.io email and hit reload, After that you need to remove it from the authentication table

3- Please back to CMS. and refresh the page, now you should be able to see your database content

Why this is happening?

When you connect more than 1 Flutterflow project to a firestore database and manage the data in more than one place. sometimes permissions got conflicted and when you open the CMS from project one, it works, but when you open CMS from the inside project two it does not work. so you need to remove the email and let it be created again.