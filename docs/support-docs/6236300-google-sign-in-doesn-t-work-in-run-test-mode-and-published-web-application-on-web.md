---
title: "Google Sign-In Doesn't Work In Run/Test Mode And Published Web application on web"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6236300-google-sign-in-doesn-t-work-in-run-test-mode-and-published-web-application-on-web"
hide_table_of_contents: true
---

​If you want to use social login features such as Google sign-in, Facebook, Microsoft, etc. on RUN or TEST mode or for your published web application, you need to add your domain to Firebase Authentication/Authorized Domain.

![](https://downloads.intercomcdn.com/i/o/681147766/2ad3e03dfa6ffa43cb787bed/image.png?expires=1741032900&signature=9864fbde7e9bfc058105ec1eff8ce2d090519eff21a4d52ca7bbff84db7bf540&req=cigmF815modZFb4f3HP0gJlKnPaM9AEpsMk0%2BvoQGu6pTmWPuYCjz9kNWJL%2B%0AKuw%3D%0A)

By doing this, you will whitelist your domain for Firebase authentication and give permission to the social login performed from the domain as an origin.

Here are the steps to follow:

Open your Firebase project.

Go to Authentication > Settings.

Select Authorized Domains.

You should now see a list of domains that are already authorized. To add your domain, click on the Add Domain button.

​

For instance, if you want to use social login in RUN mode in Flutterflow builds, you can whitelist this domain: app.flutterflow.io. If you published your app to yourapp.flutterflow.app, you need to add the same URL to your Authorized domains.

Side note: Specifically for the Test mode, you need to add our debug session URL to your authorized domains as well, as we explained here in test mode in the known issues panel.

You can copy the URL from the known issues menu.

![](https://downloads.intercomcdn.com/i/o/1000753205/66a23e5a91a07753dab51510/image.png?expires=1741032900&signature=d02069812daf0281bd6a661aebd53b6f090cd9b20cdd99e01deaf6046e562ff1&req=dSAnFs57noNfXPMW1HO4zW5i8e7cLZbssFw0ZAbq1WI3g3qwNgYAp2zGXZoU%0Ajg%2FL%0A)