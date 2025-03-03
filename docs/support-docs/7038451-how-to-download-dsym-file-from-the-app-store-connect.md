---
title: "How to download dSYM file from the app store connect?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7038451-how-to-download-dsym-file-from-the-app-store-connect"
hide_table_of_contents: true
---

![Downloading dSYM from the App Store Connect is no longer possible.](https://flutterflow.intercom-attachments-1.com/i/o/681189977/76b34c61f62af3047baff1c5/missing-dsym-past.png?expires=1741032900&signature=a240022f9d3c1744a28027c41c37091e8dadec834b0601f61b75f5937d4666c3&req=cigmF8F3lIZYFb4f3HP0gOFIcf7wS4OLS4XKnLHzm8lZIjKtcxBV9cKeEfj1%0AN8g%3D%0A)

To download the dSYM file from the App Store Connect Developer Console, follow these steps:

Sign in to the App Store Connect Developer Console (https://appstoreconnect.apple.com/) with your Apple Developer account.

Open your app

Select a build from the test flight tab on your project page

Open the Build Metadata tab

Now you should be able to see the Include symbols part and download your dSYM file

​

![](https://downloads.intercomcdn.com/i/o/681194478/040901e2adfcbfa41a32efb2/image.png?expires=1741032900&signature=826f62170252379bd724568f8b5b8da16736903347144fd83d936236edaa643b&req=cigmF8B6mYZXFb4f3HP0gPli8TO3P7a4Huktr7wI6PjdQgDqCT9yu77X%2BHgN%0AG7Q%3D%0A)

Note: You will only be able to download the dSYM file for builds that have been successfully uploaded to App Store Connect and are in a "processing" or "ready for submission" state.

If you can't see the Download dSYM file link. then seems there was an issue during the deployment to the app store.

You need to deploy again. After the submission proceeds, you can again try to download the file.

​

![](https://downloads.intercomcdn.com/i/o/681195076/cf864a2f7153de9b70edfcf0/image.png?expires=1741032900&signature=321a4cf3df554e83afc954fa26814cfa7216e2f1bbc12ce0db48ffb6752c2fa2&req=cigmF8B7nYZZFb4f3HP0gHmNPOqo19RJiiy93150PdNuUeuhfSwAt%2F7nHbIX%0AIms%3D%0A)