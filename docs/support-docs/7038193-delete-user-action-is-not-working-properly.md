---
title: "Delete user action is not working properly!"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7038193-delete-user-action-is-not-working-properly"
hide_table_of_contents: true
---

![](https://downloads.intercomcdn.com/i/o/681118867/6e7548b766d9bcd56b1deb58/image.png?expires=1741032900&signature=2441cf9958f8d5c3118ee79f87ca0b228df70d8e03b958721c0e7a109cc79c5f&req=cigmF8h2lYdYFb4f3HP0gGEcLWUy0Hq4iCGOU5ha3y%2Fz4f2sRWnEq5LKQ%2BNx%0ADLs%3D%0A)

When a user attempts to delete their account, they may find that the delete action doesn't work as expected. Here are some tips for troubleshooting this issue:

Understand that the delete action in Firebase is designed to delete the user from the auth table only. This means that the user's document in the database will not be affected. If you want to delete the user's document from the database as well, you'll need to create a custom action with some custom code.

After you've completed the delete action, it's important to log out the user. This is because there is no longer a user connected to the authenticated user in the app. Logging out will ensure that the user is routed back to the login page, which is the initial page of your project.

Keep in mind that if the same user uses the same signup method to log in again, Firebase will create a new document in the database for them. This is because Firebase will connect the new login information to the old user document. 

![](https://downloads.intercomcdn.com/i/o/681119827/0e0697d1abd7190af31b4827/image.png?expires=1741032900&signature=4204c4330d0c3f7702f8b3e553463adb8fb0db0abf90751ae4ff56d1a5948086&req=cigmF8h3lYNYFb4f3HP0gD0qzxB9j%2FmuVRer1uVaiS5qbHse7JDiqZVkNvu8%0Akb4%3D%0A)

Note: the action we do in Flutterflow is exactly the same action we can do manually to delete a user from the authentication table in Firebase.

​