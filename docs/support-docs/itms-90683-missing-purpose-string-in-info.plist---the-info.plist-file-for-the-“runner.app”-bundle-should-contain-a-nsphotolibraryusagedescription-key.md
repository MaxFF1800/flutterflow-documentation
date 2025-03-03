---
title: "ITMS-90683: Missing purpose string in Info.plist - The Info.plist file for the “Runner.app” bundle should contain a NSPhotoLibraryUsageDescription key"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

Full Error Message

Dear Developer,

We identified one or more issues with a recent delivery for your app, "Gral Wind Orchestra App" 1.0.1 (1). Please correct the following issues, then upload again.

ITMS-90683: Missing purpose string in Info.plist - Your app’s code references one or more APIs that access sensitive user data, or the app has one or more entitlements that permit such access. The Info.plist file for the “Runner.app” bundle should contain a NSPhotoLibraryUsageDescription key with a user-facing purpose string explaining clearly and completely why your app needs the data. If your app supports multiple locales, you’re now required to provide a purpose string value in the Info.plist file in addition to a valid localized string across each of your app’s localization folders. If you’re using external libraries or SDKs, they may reference APIs that require a purpose string. While your app might not use these APIs, a purpose string is still required. For details, visit: https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources.

---

### Background

This error occurs when you have not provided a permission usage description for the requested permission.

### 

How To Resolve This Issue?

Navigate to Settings and Intergrations

Scroll to Project setup and click Permissions

Locate the permission requested without a usage description and add the description.

![](https://downloads.intercomcdn.com/i/o/694592699/314f3b3129a51a36815245bf/SCR-20230320-jmvs.png?expires=1741032900&signature=6a92d25b1071ed9a1798c32e63dfad29dcef9831c2b8fdabae43ec503188aa61&req=cikjE8B8m4hWFb4f3HP0gBikkX1Om28bEZUrF%2FIv5OSAUI6RWymF6PRf9lBF%0A4Qs%3D%0A)

![](https://downloads.intercomcdn.com/i/o/694593494/93019deee508313aabf27faf/image.png?expires=1741032900&signature=d45061857d99ec31d83b2548a3fbdf7b6ee8957e2abf8a64acade5e397f2c427&req=cikjE8B9mYhbFb4f3HP0gBN9mo6lRBWA43BYdcxVtBn3v0LuyTwqm2tJclzH%0AFJU%3D%0A)

The issue was not resolved.
---

If the error persists after following the outlined steps, please report this issue to support via Chat or Email at support@flutterflow.io.

​