---
title: How To Create An Image Carousel In FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6572448-how-to-create-an-image-carousel-in-flutterflow"
hide_table_of_contents: true
---

The following are the widgets and actions that will be required to build an image carousel in FlutterFlow:

# 

 Widgets 

Page View Widget

# Action (User Interaction)

Control Page View

Step 1: 

​

![](https://downloads.intercomcdn.com/i/o/624097002/12acd9d40e2ca2ab8cc1a619/Screenshot.png?expires=1741032900&signature=b7f304175f3bcfa83ae0ee29d21d465ace23c3bc79b695222e0c82b27e04916c&req=ciIjFsB5nYFdFb4f3HP0gOXeOtWK3hLdBsCjWgCBOuX1RcNGKxdu0yE%2F2JHu%0AyYE%3D%0A)

Add a Page View Widget to the canvas or displayed screen.

Step 2: 

Add an action to the scaffold, on 'page load'

![](https://downloads.intercomcdn.com/i/o/624097511/29a84c22822097f1f83dd090/Screenshot.png?expires=1741032900&signature=c3e897abd61142706b972b19236c9c6b94b31acb0e864c2d4dba0e8127f1207f&req=ciIjFsB5mIBeFb4f3HP0gMZtvLhhTkDxuHu2BzLiffiUvIgDRqva5NohcFjS%0Anxs%3D%0A)

Step 3: 

Under, 'define actions', select 'control page view' 

This makes it possible to set up which page view should be displayed, at the first, last, or next

![](https://downloads.intercomcdn.com/i/o/624097743/e480c043e8059c1bbd4af624/Screenshot.png?expires=1741032900&signature=864e392d9ae128a83ba0180856d10d8dcbd53c4c3fc63b203236e6cc4f735614&req=ciIjFsB5moVcFb4f3HP0gEfkTC4KpmNmwthUB2wNGijAsH6r0o%2FBpro9Y5rI%0A%2B7U%3D%0A)

Step 4: 

Select the page view control type among the options shown in the attached image. 

1. Previous: Scroll to the previous page in the pageview.

2. Next: Scroll to the next page in the pageview.

3. First: Scroll to the first page in the pageview.

4. Last: Scroll to the last page in the pageview.

​

![](https://downloads.intercomcdn.com/i/o/624099468/aefa388cf6e35892eced8cc9/Screenshot.png?expires=1741032900&signature=0241eef1e595a1fadb107e5f85a864986e44ca130d86ee98b9c67d54f2be7489&req=ciIjFsB3mYdXFb4f3HP0gL77sBOW%2FpMNUwkLwuAmZe%2BcNhr5%2F6L7CkGLFdM3%0Arso%3D%0A)

Step 5: 

For purposes of demonstration, the initial page view control was set to 'first'. 

This action should be followed by a wait action that sets the transition interval between the current page view and the next. 

​

![](https://downloads.intercomcdn.com/i/o/624099880/b5ba83d116ef45f27220f52c/Screenshot.png?expires=1741032900&signature=f08ea12f587ba14e954e1bdeac979f9a64dfeccfe35c7f16803262a14144c3fa&req=ciIjFsB3lYlfFb4f3HP0gA%2FeiF2c3feAHsYEtnqOhahiSN70hVAy2y%2Fhq5E%2B%0AKAw%3D%0A)

Step 6: 

The page view action type should be set to 'next' for displaying the subsequent page view. If a user has more page views to display, the actions setup should be extended 

![](https://downloads.intercomcdn.com/i/o/624100289/b3ad41f814ac1440b5ba0766/Screenshot.png?expires=1741032900&signature=1885a7ea4c6e6339e3e284ec624d86a8017afef322626475769c397433cc4727&req=ciIjF8l%2Bn4lWFb4f3HP0gANwsMl551dcvEXiTuI02KAXogbeQQgSRv6KOzAj%0AtyA%3D%0A)

# Demonstration 

![](https://downloads.intercomcdn.com/i/o/624100945/fa1f32a1ae23824d423489d9/Screen.gif?expires=1741032900&signature=5644bf8db0639916d3c6bed43ff0b2f042a0531d59204e831ede39dc158f9fe3&req=ciIjF8l%2BlIVaFb4f3HP0gNXZPhq%2Fy2XTyIxzwoXeumg2%2Ffoy38M5q5YKYY2l%0A3ZA%3D%0A)

#