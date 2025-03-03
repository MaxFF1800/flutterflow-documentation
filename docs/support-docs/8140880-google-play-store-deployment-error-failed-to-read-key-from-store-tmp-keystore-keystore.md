---
title: "Google Play Store deployment error: Failed to read key ******** from store \"/tmp/keystore.keystore\""
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8140880-google-play-store-deployment-error-failed-to-read-key-from-store-tmp-keystore-keystore"
hide_table_of_contents: true
---

## Background:

The Google Play Store deployment is unsuccessful and displays the error below:

​

```
`Execution failed for task ':app:signReleaseBundle'.

A failure occurred while executing com.android.build.gradle.internal.tasks.FinalizeBundleTask$BundleToolRunnable

Failed to read key ******** from store "/tmp/keystore.keystore": toDerInputStream rejects tag type 123 `
```

### Reason:

This error usually means that the alias or the password of the uploaded keystore is incorrect.

### 

Solution:

Ensure that you are uploading the correct keystore file for your application. You can learn more about keystore files on this page.

​

The issue was not resolved

---

If the error persists after following the outlined steps, please report this issue to support via Chat or Email at support@flutterflow.io.