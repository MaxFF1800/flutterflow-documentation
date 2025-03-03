---
title: "I get a gray (grey) screen in Run Mode"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6126050-i-get-a-gray-grey-screen-in-run-mode"
hide_table_of_contents: true
---

If you see a gray screen in the UI Builder or while using Test/Run Mode (shown below), this indicates there is likely a configuration issue within your project.

In this article, we review the most common issues and how to resolve them.

​

![](https://flutterflow.intercom-attachments-1.com/i/o/498904355/4f829f3e4b74beedb6d3c02d/assets-2F-MhFNOxEwcl8ED58MUC_-2F-Mi3IKhrVTdUFeuuTslu-2F-Mi3Pl9_1dZLUi6GawTq-2Fimage.png?expires=1741032900&signature=3d1ff66a3418c9c8d6d13b8835c6e59b2d68549e5c0818197459a8f8ec1253da&req=cCkvH8l6noRaFb4f3HP0gO2FCzKMj%2BeXXOc%2Fnb%2B7U0w33sZJbeNNZjEdC5oC%0AI0o%3D%0A)---

# Verify you have given firebase@flutterflow.io the correct access 

Run Mode and other features within FlutterFlow require that you add the have added the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account User.

To check if you have added the correct permissions, head to the Firebase Console > Select Your Project > Project Overview > Users and permissions > Advanced permission settings.

![](https://downloads.intercomcdn.com/i/o/503332971/f8747fd49b5e16c896fcb755/Firebase+Advanced+Permissions.png?expires=1741032900&signature=47cd1316921751b82967dfd33f025e622fc8304dee9e2de3f53ecfae31f3fc35&req=cSAkFcp8lIZeFb4f3HP0gNmKgXFwl2tUi8Z2lYKzaHNQTrz43ObF8BvPfFVq%0ABqQ%3D%0A)

Next to firebase@flutterflow.io you should see Cloud Functions Admin, Editor, and Service Account User.

![](https://downloads.intercomcdn.com/i/o/503336806/1d2faab7cf567740160c651a/Firebase+Permissions+Needed.png?expires=1741032900&signature=0e773ce353a573ef64f19637ab8345c71b4f57a1e4a274fa6487afbb7470e916&req=cSAkFcp4lYFZFb4f3HP0gEFvH5ms6e5ZZmDb5C7jszPTSku8NZ4mmD1DdAtN%0AdS8%3D%0A)

If you don't see these permissions, select the pencil icon and follow these instructions to add these permissions.

---

# 
Regenerate the Firebase configuration files 

Open your FlutterFlow project and select Settings & Integrations > Firebase > Regenerate Config Files. A popup will appear, select Generate Files

​

![](https://downloads.intercomcdn.com/i/o/503341987/95c80f8a95bfa245db75e31b/Regenerate+Firebase+Config+Files.png?expires=1741032900&signature=f980aeaa55efa926911ef9578bd9835bc417c8fa1fdb3eda8e19c99c51fbc9e6&req=cSAkFc1%2FlIlYFb4f3HP0gDXOGAsGYuNYg%2BEOTvCjYa2b70wEl%2FEZTInARKDr%0Alco%3D%0A)

A popup will appear, select Generate Files. After this step is complete, you will be taken back to the main Firebase page.

Tip: this step is required any time you change the name of your FlutterFlow or Firebase project.

---

# Update your Firebase rules

FlutterFlow has a built-in feature for updating your Firebase rules.

Open your FlutterFlow project and select Firestore > Settings > Scroll down to find Firestore Rules. Select Deploy.

A popup will appear. Select Deploy Now.

![](https://downloads.intercomcdn.com/i/o/503355520/f0222a5416d73bda4767cce1/Redeploy+Firestore+Rules.jpg?expires=1741032900&signature=9887b0068aeaa002fe9cd5c3bbace83f51abce4f1ac2b5c2b97eb82b8b35f141&req=cSAkFcx7mINfFb4f3HP0gInZvyF%2B9yLKuzZJwi%2BFJIgT9Ohuux77trX2Gdkj%0ANkc%3D%0A)

An orange loading icon will appear while the schema is being validated. Once deployment is complete, you will see a green checkmark.

![](https://downloads.intercomcdn.com/i/o/503356690/72c73d6674e4dad1b919830f/Deployment+Complete.jpg?expires=1741032900&signature=3ece22506d0fb13edba3cd7513f16ce6ebc7d2f4677f5175155c9ec3e0eeafb0&req=cSAkFcx4m4hfFb4f3HP0gGzz4G8UsCBSw%2FmwmyTlw6%2BhBypY8x5tZsI%2Btk5N%0ASac%3D%0A)---

# Validate your Firebase Schema

Open your FlutterFlow project and select Firestore > Settings > Scroll down to find Firebase Schema Validation. Select Validate.

![](https://downloads.intercomcdn.com/i/o/503346831/b7f1a8a916605ab311a8e90d/Validate+Firebase+Schema.jpg?expires=1741032900&signature=5760f7b93fafafa728ea3024461c24d42f40ca622a4c2cea98457c6c46c54c20&req=cSAkFc14lYJeFb4f3HP0gCl33Oku5t%2Ba7eJ2NE1Ogb82a5LkAHCuKhSJp3zA%0AX3U%3D%0A)

An orange loading icon will appear while the schema is being validated. Once validation is complete, you will see Successful next to Validation Status.

![](https://downloads.intercomcdn.com/i/o/503348314/6e566d32e95e346e97f83cb0/image.png?expires=1741032900&signature=b13ec4a2753ae51289f9d8cafc7d11396082fda655da08ec4c3480bf9cf74a5b&req=cSAkFc12noBbFb4f3HP0gDG59j%2FNFh30S8kiJZwSS2SXLbIZDDPME8kZk1Ii%0Akio%3D%0A)

Check to see if any issues were identified. If the validation found any issues, you need to troubleshoot and resolve these.

![](https://downloads.intercomcdn.com/i/o/505331104/e4a36bb3e86f04cd82163813/image.png?expires=1741032900&signature=42bf22dbea2f610cc63d59121eb985d426f0d0a778c86fd07193faad2c97dce0&req=cSAiFcp%2FnIFbFb4f3HP0gBLdECC0nMUsD9KK60cR1fqBonfyyOp1%2BuONqWNC%0AP5Q%3D%0A)---

# Make sure your Firebase collections have data in them

A query for a collection with no data in it will result in a gray screen.

To double-check that head to the Firebase Console and select Firestore Database. Here you can see your collections and the data within them.

![](https://downloads.intercomcdn.com/i/o/505343842/a8650b48b79a509b6902a695/image.png?expires=1741032900&signature=bc3c721c6e40f9df2e89daade47269e263e58869ed3967dc654c48e48cf0b96f&req=cSAiFc19lYVdFb4f3HP0gKeJSVSRM9UVoJmA9YaAAT782mU%2BRhqvXDNBVb0w%0At0E%3D%0A)---

# If you are using a custom widget, ensure that the package has Web support

Packages with web support are required for your custom widget to render properly in Run Mode.

To check if your package has web support, search for the package and check if WEB is listed under platform. 

If you don't see WEB listed, you will need to select a different package for it to work properly in Run Mode.

![](https://downloads.intercomcdn.com/i/o/502550643/96100aaeb7425c044b2d49ac/image.png?expires=1741032900&signature=a626ec5ae93d4776cc14cb11aeefd2ca4bf45cb62afe3fb977c491c93bcd96ab&req=cSAlE8x%2Bm4VcFb4f3HP0gFS5vu9Ag46fwmWG7y8dDgQ5QglCzUfyAV9dW6IM%0A3yI%3D%0A)---

# Ensure you are on the latest version of FlutterFlow

To upgrade to the latest version of FlutterFlow select Ctrl + R on Windows or Cmd + R on Mac.

After you have done this, clear your browser cache and log out/in to FlutterFlow.

Tip: Clearing the cache and restarting the browser can help if you notice FlutterFlow is running slower than usual.

---

# Retest your project

After you have completed these steps, create a new Run Mode version of your project and see if the gray screen has been resolved.

---

# Test your project locally

If the issue still persists, we recommend downloading the code and testing it locally on your machine. This will allow you to identify the exact source of your error. Here are the instructions on how to test your app locally on your machine.