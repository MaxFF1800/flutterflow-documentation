---
title: "My app colors aren't correct when running my application on a real device"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7048075-my-app-colors-aren-t-correct-when-running-my-application-on-a-real-device"
hide_table_of_contents: true
---

# Issue Overview

You are testing your application on a phone and the colors are not appearing as expected.

# Common Causes

Real devices have their own configurations in terms of theme and color. Devices typically have light mode, dark mode, or automatic (which switches between light and dark mode). For example, if your device is set to dark mode - your application will display in Dark Mode.

This issue typically arises when Dark Mode is enabled, but set up has not been completed or conflicting colors have been selected.

# Basic Troubleshooting Steps

## Step 1: Check If You Have Dark Mode Enabled In Your App

Head to Settings > Theme and check if the Dark Mode toggle is turned on. If it is, you have dark mode enabled (example below).

Turn dark mode off and redownload your application. If it works as expected, the Dark Mode Settings are the issue.

​

![](https://downloads.intercomcdn.com/i/o/683704142/97a0a53e7df57299fa4e574a/image.png?expires=1741032900&signature=8d6929488e83c214ed9eda00222f5dfa99e14dd7ea87ecc01e0a1c0d80602bca&req=cigkEcl6nIVdFb4f3HP0gIw3vKuZIUX7zVYPFuKDfVu49ZvyaehcXD3SNq4x%0ASFw%3D%0A)

To correct this issue you can:

Turn dark mode off

Update your colors so that the Dark Mode Theme is complete / visible by the user

You can preview how the colors will work by selecting the Explore Themes button in the Theme Section (example below)

![](https://downloads.intercomcdn.com/i/o/686921238/2ad962aaeb86b4d1e4dcb685/image.png?expires=1741032900&signature=11d8911a23bfc43cc6816b25075506e899ed51c2f15702e480185c6912c71aec&req=cighH8t%2Fn4JXFb4f3HP0gC%2FY%2F26SLYI2cXzCy4GCxcYMEN0KpJiVQfZXSYE8%0AYGk%3D%0A)

After you have completed these steps, your colors should appear as expected.

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace

​