---
title: Appstore deploy button not working
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

Background

When trying to deploy your application on App Store, you might face an unresponsive deployment button, during that if you check the browser's console you should be able to see this error:

​

```
`POST https://api.flutterflow.io/v1/codemagicBuildRequest 503`
```

Reason:

This error occurs when the project contains too large assets, which has increased the size of the project resulting in unacceptance from the code magic.

Solution:

In order to resolve this problem, The user should remove some of the larger assets (like videos) and access them via the network instead of assets, the recommended size of the project is 50 Mb, So ensure to keep the project within the recommended size in order to avoid errors.

The issue was not resolved.

---

If the error still persists after following the outlined steps, please contact support via Chat or Email at support@flutterflow.io.