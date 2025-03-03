---
title: "Test mode is not loading or is very slow, it takes a long time to load the app"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7052737-test-mode-is-not-loading-or-is-very-slow-it-takes-a-long-time-to-load-the-app"
hide_table_of_contents: true
---

### Issue

Test mode is taking a very long time to load (e.g. 5 minutes).

---

### Background

When you start a new testing session, we are compiling a new version of your app - so this can typically take 2-3 minutes to load (but is sometimes a bit longer for big projects).

Each time a build is initiated in RUN or TEST mode, the compiler will require time to compile the custom codes, import assets, compile all the code within the project, and create the final build. 

The speed of building the project can be impacted by different aspects, such as the number of pages, components, custom codes, assets, custom fonts, and icons used in the project. 

---

## Troubleshooting This Issue

Here are a few tips we recommend:

Check your internet connection: Poor connectivity can affect the loading speed of a page. Ensure that your internet connection is stable and strong.

​

Clear your browser's cache: Your browser may have stored a large number of temporary files, which can cause the page to load slowly. Clearing your browser's cache can help to speed up the loading process.

​

Try a different browser: If the problem persists, try loading the test mode page on a different browser. This can help you determine if the issue is with your browser or the website itself.

​

Disable browser extensions: Some browser extensions can cause conflicts and slow down the loading of web pages. Try disabling any extensions that you have installed and see if this helps to speed up the loading of the test mode page.