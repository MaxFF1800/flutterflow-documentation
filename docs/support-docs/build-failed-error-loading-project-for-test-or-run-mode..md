---
title: "Build Failed: Error loading project for test or run mode."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

### Issue

You receive this error when you try to create a new build in Run or Test mode, but you don't have any identified issues in your FlutterFlow project.

​

![](https://downloads.intercomcdn.com/i/o/684871630/8bcf3fffffa968febf9469ec/image.png?expires=1741032900&signature=64ae1631cac6ccd84bb8692ea7acdb3ecaff61efb0202a1b2b2536dd00110221&req=cigjHs5%2Fm4JfFb4f3HP0gFxcuaFFcgx8bNsIyKDUDJmEqFIOw3aSjFkvLaOR%0APqQ%3D%0A)---

### What does this error mean?

There is an issue in your FlutterFlow project that is stopping your code from compiling. 

We typically try to notify you of potential project issues using the debug menu (example below). However, sometimes there are new error types that our system does not catch.

![Debug Menu](https://downloads.intercomcdn.com/i/o/684852344/3789bec88e632c06739287a4/image.png?expires=1741032900&signature=748f9e769c397233234a3430ad722709aa4a28668ce8059053ad48d413f5ac1e&req=cigjHsx8noVbFb4f3HP0gCcqjHDzdWVGCqJCmjS6I5UnFr%2BxQFkDoQyLGJy1%0A2ZU%3D%0A)

---

Example Issues That Can Cause A Build Failure

copy/paste a widget with lots of actions and visibility rules on it

copy/paste a widget with animations and animation actions on it

copy/paste a whole page or component

select a wrong data source that doesn't exist at the time of build, for example, you do a condition on a periodic action on a page load when the periodic is not exist yet.

Flutterflow Bug, It may be a bug and you need to report it in our github issue tracker if you find it.

---

### Troubleshooting This Error Type

If you have the ability to download your code, run the code in your local machine. You can check the last code and see the error in the code. With this information, you can return to the FlutterFlow editor and fix the issue.

You can also review your previous snapshots to identify the changes made that caused the error. 

For example, if the last thing you did was duplicate the page bookings and change some of it.

Go to that page, check all the actions, Visibility rules, and open them one by one to find a red noticed item there.

Example of how an error could be hidden:

![](https://downloads.intercomcdn.com/i/o/684868572/d1b15c6debcced66b72ab7ce/image.png?expires=1741032900&signature=086fd1cbc82abd155cea6de9b806c4376e7014c38469c8aaa8ecb90988f3e0bf&req=cigjHs92mIZdFb4f3HP0gPMl5Vrqa5yFHXRFaf3Kt%2Fk6RHjTwDUgRDhauIsC%0AcB0%3D%0A)

Here in this visibility rule, you can't see any error. but let's see after opening the condition what we could see

![](https://downloads.intercomcdn.com/i/o/684868407/2ee580dc9da21b21d9bff023/image.png?expires=1741032900&signature=fd629e8a6f6eaba0bcbe54de128fab704c27b128d1d08a4920bf4e7ca9b8cd9e&req=cigjHs92mYFYFb4f3HP0gMA7e1A21uVYBVspH3H%2BrU2unTDbtCeNxsDO%2Fbsw%0AKy8%3D%0A)

You could see after opening the second value, we could see it's unset and red. Simply it could cause a build failure when we run the project.

​

If with all above attempts the issue persists, Then please reach to the support@flutterflow.io.