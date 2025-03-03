---
title: "Invalid Pre-Release Train. The train version 'X.X.X' is closed for new build submissions"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6398258-invalid-pre-release-train-the-train-version-x-x-x-is-closed-for-new-build-submissions"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

This error means that the app that you're trying to submit to the App Store is closed for new build submissions. You can't submit it again with the same app version, even if the build number has changed.

# How to resolve this issue?

You'll need to increment the app version in the FlutterFlow deployment settings.

In order to do this, please follow these steps:

Press Cmd/Ctrl + k, type "deployment" and hit enter. It will take you to the deployment page.

![](https://downloads.intercomcdn.com/i/o/550342644/e11d9dbb7afdfcd7b5ef6564/Screenshot+2022-07-21+at+11.05.25+PM.png?expires=1741032900&signature=3798b8c2f04cf9d2460256b9f10275b2c2f67ccfec70595d758f975c1271fb29&req=cSUnFc18m4VbFb4f3HP0gE718v8zY9Q0U22IriEYqfASbEjFY2UC0L7UzXaI%0AJZs%3D%0A)

You can also navigate to the Deployment section by clicking Project Settings > Deployment (under App Settings).

​
![](https://downloads.intercomcdn.com/i/o/550384963/47f46a67591c372bbddb5acd/image.png?expires=1741032900&signature=7d99e3a0eda456b53a6716cfe93bffb76798bd0584bb634d0dcdc883b9a90928&req=cSUnFcF6lIdcFb4f3HP0gC08UOSSc7fQxqJ0p2vp8RFxDaxzg8fycz44%2FEQe%0AR88%3D%0A)

Click on the Expand icon in front of the Version.

![](https://downloads.intercomcdn.com/i/o/550343682/b44686c1d50020697829179e/image.png?expires=1741032900&signature=7ab1c8a8941773364d2fa8d577e638893b9f0e04516ebf49605bb6a042fcab95&req=cSUnFc19m4ldFb4f3HP0gGW6hk8iDpE6CEZGsIcVTfD2MDQQNUZFehbge0hv%0ArFI%3D%0A)

Here you'll need to update the version number to the next increment version number. For example, if you have 1.2.0, you will need to upgrade to 1.2.1
Learn more about when to increment version numbers after the 4th step.

![](https://downloads.intercomcdn.com/i/o/550353020/a9af6837550d8dd9d2d0337e/version+increment.gif?expires=1741032900&signature=c3edab67da0a47af5ab51e2a34098d5594b19332827809b9930aac98a9bbfb70&req=cSUnFcx9nYNfFb4f3HP0gDOs7%2BMD7eAied3Tf8Jg8VFtq6kolSmTdYSCZmPu%0A5Gg%3D%0A)

After this, you can try deploying your app once again, and it will succeed.

---

# When to increment the app version number?

The best versioning scheme is to choose what makes sense to you or your team. But here's a common versioning method called Semantic Versioning (Major.Minor.Build)

## Major Version

The first number in the sequence (1.x.x) is the major version and this semantically means that the software has a breaking change that could affect any other software that depends on it. For example, you could have an API that completely changes the URI path in an upgraded version from 1.x.x to 2.x.x.

## Minor Version

Minor versions are changes to the code that do not reflect breaking changes but are significant enough to warrant a version increase. More often than not, this includes additions to the code that add functionality and does not break it. So if you added a new endpoint to an existing API and kept all other endpoints the same, then the API's version could be increased from x.1.x to x.2.x.

## Bug/Build Version

The last number in the scheme stands for the bug/build version depending on how you want to look at it. This could be used for bug fixes and hotfixes that come up in the lifecycle of your application. For example, x.x.1 to x.x.2.