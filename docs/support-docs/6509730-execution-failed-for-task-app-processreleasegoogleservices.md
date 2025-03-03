---
title: "Execution failed for task ':app:processReleaseGoogleServices'."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6509730-execution-failed-for-task-app-processreleasegoogleservices"
hide_table_of_contents: true
---

Tip: Not sure which type of error your project has? Check out this article on how to identify your Codemagic error.

# What does this error mean?

This error usually means that there is some mismatch with the package name and that it needs to be checked.

# 
Full error message 

```
`FAILURE: Build failed with an exception.

* What went wrong:

Execution failed for task ':app:processReleaseGoogleServices'.

> No matching client found for package name '[app.app.app]'`
```

# How to resolve this issue?

To resolve this issue, please follow the following steps.

You'll need to Regenerate the config files from FlutterFlow. To do this, open your app in FlutterFlow and then click on Settings > Firebase.

​
![](https://downloads.intercomcdn.com/i/o/526141349/f8652b819ab7d9c3f098bb0d/image.png?expires=1741032900&signature=7e68a7bfbafe90deeafe6347c8fec7d76df2a1dd77e1cb9ce5641bc207835292&req=cSIhF81%2FnoVWFb4f3HP0gC2q6qSyAd8Qk4Nxmd9UI4kbFnBSD6k%2FqoLGcg%2FK%0A0DQ%3D%0A)

Here, Click on the Regenerate Config Files button, Enter the new package name and then Click on Generate File.

​
![](https://downloads.intercomcdn.com/i/o/526142048/f54acfd365e0c6a943552098/image.png?expires=1741032900&signature=198f1665b9a69833e93802fdce3d2d3c408ce2d75b26a9c89c0024d1a6a94c9a&req=cSIhF818nYVXFb4f3HP0gHEstd0eiQI0DTOCAB7R4qWrIrhX8LFWlmxEXQrr%0AZqU%3D%0A)

This issue should now be resolved. You can now re-deploy to confirm that the issue has been fixed.

# Issue was not resolved after following the given steps

If you are deploying from FlutterFlow and still getting this error after following all the steps outlined above, then please report this issue to support via Chat or Email at support@flutterflow.io.