---
title: Custom routing when a user logs in
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6300011-custom-routing-when-a-user-logs-in"
hide_table_of_contents: true
---

Why do we need a mission control page?

In this article we'll show you how to use a Mission Control page to:

Show a page to a user for the first time they log in and then route the user to the home page.

If a user is an admin, route them to the admin dashboard instead of the home page.

You don't have to both of these together (e.g. you could just build the admin routing). However, many users have asked to include these together - so we thought it would be helpful to show them together.

Prerequisites:

In order to get started, you will need:

A FlutterFlow project with Firebase set up (instructions)

Authentication setup in your FlutterFlow project (instructions)

---

# The Pages You Will Need In Your App

We will need five pages in our app to accomplish this:

Login page: this is our initial page and the page that let users log in to the app

Onboarding page: we want to show this page one time, to new users only

Admin home page: we want to route admins to this page after login

User home page: we want to route users (non-admins) to this page after login

Checkup page: this is our mission control page. we route all logged users to this page and after checking conditions again route them to other pages.

We've create a cloneable project so that you can see what the final project should look like.

Note: we've added a 1 second delay to improve user experience. 

---

# Create a Local State variable:

Local State allows you to store values that you can use on different pages of your app. Tip: You can learn more about Local State here.

## Create a Local State Variable called firstTime

This Local State variable will check to see if this is the first time a user has logged in.

Complete these steps to create this variable:

Select Local State from the left navigation menu and then select + Add State Variable.

Create a State Variable called firstTime. Select Boolean from the dropdown and turn Persist on. 

Tip: Persist means this will remain on the device until the user uninstalls the application.

Important Tip: The Persist option works only on device. If you are testing on the web, each time you refresh the page the local state value will be set to true again [ back to default ]. 

![](https://downloads.intercomcdn.com/i/o/529723187/6956e94c24f1bca9940f536e/image.png?expires=1741032900&signature=0d97566e68317753d295a4d79ae1af6ea7a8f419db436c671d0af195f8c306c4&req=cSIuEct9nIlYFb4f3HP0gM%2BjPsT7FkpXUB9BOBhICydzCFKWPuENxzZq464d%0Anog%3D%0A)

![](https://downloads.intercomcdn.com/i/o/529723518/4e2b65f0e188af12b9263390/image.png?expires=1741032900&signature=5df27b83b85118a523e9e41541d2cbcbb5d65683e34aac7ade9b5dddafb6c9a5&req=cSIuEct9mIBXFb4f3HP0gCqr2tiMJbPQKpa5U3wBcb4BHYwhtUDdDyyTwf5P%0Ad2Y%3D%0A)

# Create a User Field called isAdmin 

Next, we'll need to add a field to the users table called isAdmin. This will allow us to route an Admin to a different page than other users:

Select Firebase from the left navigation menu and then select + Add Field.

Create a State Variable called isAdmin. Select Boolean from the dropdown.

If a user is an an admin, you should set this value to True for this user. 

![](https://downloads.intercomcdn.com/i/o/529729645/2c0b5c3c6019e50a27fbf814/image.png?expires=1741032900&signature=e8890de48c1f0a315e4a91cc64fc7caba3c0ec06ecc0a51be3aa11cb8fef490c&req=cSIuEct3m4VaFb4f3HP0gBszsXjQXDHElZcvSbEcxFBNR4TDhJYqFlWtv5Rf%0AdjI%3D%0A)![](https://downloads.intercomcdn.com/i/o/529730301/decbf5fc57fbe56a1c4ef0ca/image.png?expires=1741032900&signature=e5e855f1fd04529f338a67b56c327cbe16ab7f7f87071791da7eb3d205a17cd3&req=cSIuEcp%2BnoFeFb4f3HP0gAsGlyin05xg49qfnoyF7f1SZqK2lySsV8Yl3hDj%0AwmI%3D%0A)---

## Define the Initial Pages

Next you need to define your initial pages. Head to Settings & Integrations > App Details > Initial Page and define:

the login page as our entry page 

the checkup page [ mission control ] as our logged in page

Tip: Entry Page is the page will be shown if the user is not logged in. Logged In Page is the page will be loaded if the user is already logged in to your app. 

![](https://downloads.intercomcdn.com/i/o/529736783/8a059925219d2ecf98e40152/image.png?expires=1741032900&signature=ffc2d35d9fc8f952bd86933a542c1aeadd1ce7047465ef4a8a7faf1c6b279ea3&req=cSIuEcp4molcFb4f3HP0gPv4xAptFYt1g38%2BfL%2FNFLgM0n5D2HymicsZmdxa%0AuHc%3D%0A)---

## Define Actions On The Check-Up Page

Next, we'll need to define a series of actions that will help us identify user role, whether a user has seen the onboarding, etc.

Tip: If you're new to actions, you may want to read our Actions Introduction.

On your mission control page, select Open in the Action Flow Editor

![](https://downloads.intercomcdn.com/i/o/529757687/b4d32aee1e2175b6eda385bd/image.png?expires=1741032900&signature=7ddee37d545334a331aba7dd1760d9caa0a8ed58da27a4e115d6827680b75c2b&req=cSIuEcx5m4lYFb4f3HP0gHDxHdrQXtJrAAc4rMrWKuTGoxM5eTVoVFDGl5Um%0Ab1E%3D%0A)

Make sure On Page Load is selected at the top and then select + Add Conditional Action from the bottom of the screen

![](https://downloads.intercomcdn.com/i/o/529738954/9cc55163abf38d08b90e06d7/image.png?expires=1741032900&signature=01eee859b676f8528cea26826232abcfb11a346d50c09328a16524a5b85f1193&req=cSIuEcp2lIRbFb4f3HP0gA2Qnhwk9Nyh7UTUTNkNV3U4FVtmduSQvkmVHXnn%0AIKo%3D%0A)

## 

Add a [ conditional ] Action To Check If User Is Logged In 

This action will check if a user is logged in. If they aren't it will route the user to the Login page.

Complete these steps to define this action:

Under Source select Global Properties.

Under Available Options select Is User Logged In

![](https://downloads.intercomcdn.com/i/o/530634739/5c12f06c7557a7d88836123c/image.png?expires=1741032900&signature=fce5775247a32d41ff8b0b0097a97d00d66b9b461c23ac895497e4e52e731595&req=cSMnEMp6moJWFb4f3HP0gHJMx05%2FnUAdMiilUEmRlIoDaE%2B7lD5Qn4SNY4kN%0Ans0%3D%0A)

In the FALSE branch, select the + icon and then select Add Action. 

![](https://downloads.intercomcdn.com/i/o/530636579/1248136439a74409761d63ae/image.png?expires=1741032900&signature=d1c0a45d6b96e17dca0ee70faef1fe06e92b047c1a5efc67e0c93aedf193b2ea&req=cSMnEMp4mIZWFb4f3HP0gINcxJi1dywK5eemaGnb%2FapHR%2FwVkv5z25nwTv2x%0AAMw%3D%0A)

Define the action as Navigate To > Login.

Change the Allow Back Navigation Toggle to Off.

![](https://downloads.intercomcdn.com/i/o/530637626/fa752c8c61ec98026518e08c/image.png?expires=1741032900&signature=5db3644802afd1d43bf6ef685add0166ff7fdbddd4439d1706f6b4cf9c91e51e&req=cSMnEMp5m4NZFb4f3HP0gEqCFx5%2BqRgcqHUpkTpJ99H%2BmM7ItDJfX0t%2BQalq%0ADtM%3D%0A)

Now select the small + icon on this action and select Add Terminate.

![](https://downloads.intercomcdn.com/i/o/530638377/57b4d130abca0953f488aa16/image.png?expires=1741032900&signature=2bcf3eda73ca5f9b9f4e1a7f9632d17e728cccf02d01f8adb5ec5cd9f69fb0ea&req=cSMnEMp2noZYFb4f3HP0gCWN8yGC7Q0UqxatjkuuJgK6fW2Bn7%2BgoIh%2F1wbz%0Akvc%3D%0A)

Your action flow should now look like this:

​

![](https://downloads.intercomcdn.com/i/o/530639227/c1f01ae90cc11f0b7a96da9c/image.png?expires=1741032900&signature=c46de41089cfc051b66988713bf9dbdcda95f43937d6cf8bde04279e54a7898f&req=cSMnEMp3n4NYFb4f3HP0gMWsk8l2iaUs61Nu2rjdSa2FToU%2Bizn5IVjRVI4E%0APxE%3D%0A)---

## Add a [ conditional ] Action To Check If User Has Seen The Onboarding Page Already

This action will check to see if this is the first time a user has logged in. If TRUE they will be shown the onboarding page.

Complete these steps to define this action:

In the TRUE branch, select the + icon and then select Add Conditional. 

In the Set Condition For Action (right side of screen) select Source > Local State and Available Options > firstTime.

Under the TRUE branch of the firstTime conditional, select the + icon and then select Add Action. 

Define the action as Navigate To > Onboarding. Change the Allow Back Navigation Toggle to Off.

Now select the small + icon on this action and select Add Terminate.

![](https://downloads.intercomcdn.com/i/o/529743721/8f85fdc68de83e073a57a0e9/image.png?expires=1741032900&signature=f76ecd25b15d3a7253bf0bd35258c6fbbac5f683e4ee59cdeb4a49b63286ac53&req=cSIuEc19moNeFb4f3HP0gApz5vVgWgbpR1lIGfBFOQTlDU5BTZAcrh0XmMrB%0AeT8%3D%0A)

on the onboarding page, we need to turn the firstTime local state variable to False. it means the user checks this page one time.

---

## 
Add a [ conditional ] Action To Check If User Is An Admin 

This action will check if a user is an Admin. If they are, they will be sent to an Admin page. All other users will be sent to a different page.

Complete these steps to define this action:

In the FALSE branch of the firstTime Condition, select the + icon and then select Add Conditional. 

In the Set Condition For Action (right side of screen) select Source > Authenticated User and Available Options > isAdmin.

Under the TRUE branch of the firstTime conditional, select the + icon and then select Add Action. 

Define the action as Navigate To > AdminPage. Change the Allow Back Navigation Toggle to Off.

Now select the small + icon on this action and select Add Terminate.

Under the FALSE branch of the firstTime conditional, select the + icon and then select Add Action. 

Define the action as Navigate To > UserPage. Change the Allow Back Navigation Toggle to Off.

Now select the small + icon on this action and select Add Terminate. 

![](https://downloads.intercomcdn.com/i/o/529747942/fc4f07dcb1fb099b5c9d1d33/image.png?expires=1741032900&signature=08f6642d8ec239446f785fbbd2de1f8bc0599eeeaacf81e5561488411839aa96&req=cSIuEc15lIVdFb4f3HP0gPrCtgvuY70T31vKcwznXLEDhEr8UqqKgWZlZyhM%0AQcQ%3D%0A)---

Set firstTime to FALSE after user sees the Onboarding Screen 

​

To prevent users from seeing the onboarding screens multiple times, we'll set the firstTime variable to FALSE after they have viewed the onboarding screen.

Go to the Onboarding Page, select the Start Button and then open the Action Flow Editor.

Complete these steps to define this action:

Select On Tap > Add Action > Update Local State (under Database/Backend).

Select Select field to Update > firstTime and Select Update Type > set value.

Set Value Source to Specific Value and Value to False.

![](https://downloads.intercomcdn.com/i/o/530652315/cb890dab7d48c05571435f7e/image.png?expires=1741032900&signature=022923eeaed18ab1bb4e6f2706004c49f06b6d2f414fe229555baf8f05f5cefa&req=cSMnEMx8noBaFb4f3HP0gLNLjC2ApIL%2B%2FMBMbzcboQ00941fRhEOf2uRuW6D%0ADfQ%3D%0A)

Under the Update Local State Action, select the + icon and then select Add Action. 

Define the action as Navigate To > Checkup. Change the Allow Back Navigation Toggle to Off. 

![](https://downloads.intercomcdn.com/i/o/530653377/6d6f38b41417d88652b5f80a/image.png?expires=1741032900&signature=5dc7eec8454325eaa4a21efe78185d3bdcc511da62d105b1b5c7b5be279c3b63&req=cSMnEMx9noZYFb4f3HP0gDKF8wx8lX%2FlnoeUZOf1X1nPv2qdTEtNlbFWjgZQ%0AEiU%3D%0A)

Congrats! You've completed these steps.

Bonus Tips:

You can reuse this "Mission Control" page for other advanced routing options.

For example, if you want the user to complete their profile. You can route the user to the checkup page and have another conditional if profileIsCompleted==false then go to the complete profile page.

What if I don't want to show onboarding page to admins as well? You can accomplish this using this logic:

![](https://downloads.intercomcdn.com/i/o/529753629/0af77d97e971a57b366f735a/image.png?expires=1741032900&signature=c377c73d20121ab8beb8c5c2796d8dbeda68c0ae113fb863110a0dbc327bf893&req=cSIuEcx9m4NWFb4f3HP0gPTbhKyU3bZHykr3bI58lfijuklIDILhOyE7EOip%0ApKE%3D%0A)

​