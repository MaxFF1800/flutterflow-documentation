---
title: Scroll To Action Is Not Working When Used On Page Load
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7047006-scroll-to-action-is-not-working-when-used-on-page-load"
hide_table_of_contents: true
---

### Issue

I am using on Scroll To Action for an On Page Load action chain. It is not working as expected.

​

![](https://downloads.intercomcdn.com/i/o/683574637/6dcd4cd994891f748ee84ea7/image.png?expires=1741032900&signature=32d960aa4f4d47b3d7bb3a3e3cb509b0fec05f0f68775488705a767a76520d97&req=cigkE856m4JYFb4f3HP0gMuK3wvzHU6evVSHuqeC9HU0WS%2BgzXAnKL52231y%0A%2FMs%3D%0A)---

### Background

When you add an action to a page load, it executes before everything else. So you may be trying to scroll a widget that doesn't exist yet.

---

### Solution

The solution is to wait until the page is fully loaded before executing the scroll action.

For this, we could use a delay action before the scroll to action for just 500 to 700 milliseconds (example below).

Now the page has time to build and the moment you execute the scroll action the scrollable widget exists.

![](https://downloads.intercomcdn.com/i/o/683576484/8eea5c4328b3d78052bf0a7f/image.png?expires=1741032900&signature=d8b229a46caf3376857f2a1ef00f9e44940904bae58d6c391cf82b8201db9836&req=cigkE854mYlbFb4f3HP0gNAycYMHTd2gZCHVrUk6s4eIJCIblgFPilorwr9M%0AHhk%3D%0A)

You can also add an animation to the scrollable widget, on load animation. So this way widget will be animated and then scroll to action will execute and the user doesn't see a break or jump on the UI.

For example: if you have a fade animation for 1200 milliseconds on your listView, also a delay for 700 milliseconds after that doing the scroll, users don't feel anything.

​