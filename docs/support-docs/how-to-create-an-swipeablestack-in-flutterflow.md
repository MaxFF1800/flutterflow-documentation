---
title: How To Create An SwipeableStack In FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

WHEN TO USE A SWIPEABLESTACK WIDGET 

A swipeable stack widget is typically used when you want to create a user interface where multiple cards or elements are stacked on top of each other, and the user can swipe horizontally to navigate through them. This pattern is commonly seen in apps that display a series of cards or pages that users can easily navigate through by swiping left or right. Some common scenarios where you might use a swipeable stack widget include:

Tinder-like card swiping: When you want to implement a UI similar to the popular dating app Tinder, where users can swipe left or right to like or dislike cards, a swipeable stack widget can be used.

Image carousel or gallery: If you have a set of images or content that you want to display one at a time and allow users to swipe through them horizontally, a swipeable stack widget can be a great choice.

Onboarding screens: In apps with onboarding processes that introduce the app's features or functionality, a swipeable stack can be used to present different screens to the user, one at a time, with the ability to swipe through them sequentially.

Content exploration: If your app has content items, such as articles or products, that users can explore, a swipeable stack can provide an engaging and intuitive way for users to navigate through the content.

NB: Keep in mind that while a swipeable stack can offer an appealing and interactive user experience, it's essential to consider the context of your app and ensure that this navigation style aligns with your overall design and usability goals. Additionally, be mindful of performance implications, especially if you have a large number of elements in the stack, as rendering multiple widgets with animations can impact performance on lower-end devices.

Widgets

SwipeableStack Widget

# Action (User Interaction)

Control SwipeableStack View

Step 1: 

​

![](https://downloads.intercomcdn.com/i/o/775241007/0fdbf0ca716fbb16f163263a/Snip20230630_1.png?expires=1741032900&signature=4bad8b68b39db26d8ac092bba08e2675a6f9cd1fbcf4b6f0d6ba0d153c003579&req=cyciFM1%2FnYFYFb4f3HP0gEcJj8UIySxHTAxJt7rxmqZMJ7MqzZUOoMmSd46E%0AZlk%3D%0A)

Add a Swipeable Widget to the canvas or displayed screen.

Step 2: 

Add an action to the scaffold, on 'page load'

![](https://downloads.intercomcdn.com/i/o/775243501/fd15181295c5054e1fbc9fb8/Snip20230630_3.png?expires=1741032900&signature=5c71c8daee53ad97bf1073d2598c98438b220a2d007fc9511a8c2e4e8b47cf82&req=cyciFM19mIFeFb4f3HP0gGa%2B8NDy8ER5RlDinwQthsaDiE2sH%2F7U%2BuSTa8br%0AD4Q%3D%0A)

Step 3: 

Under, 'define actions', select 'Control Swipeable Stack' 

​

![](https://downloads.intercomcdn.com/i/o/775243779/b2d6a229fe7f49d61e060664/Snip20230630_2.png?expires=1741032900&signature=b6a6c7eca369f77bb0399be30f10935b8d73922a052e474eaf58186a27e2752b&req=cyciFM19moZWFb4f3HP0gPzTftaBhymHFrXclzmQ%2F1ll50G%2BEbfjR4aabami%0AhG4%3D%0A)

Step 4: 

Select the Swipeable Stack type among the options shown in the attached image.

1. Trigger Left Swipe: This will initiate a swipe to the left

2. Trigger Right Swipe: This will initiate a swipe to the right

3. Trigger Up Swipe: This will initiate a swipe upwards

4. Trigger Down Swipe: This will initiate a swipe downwards. 

​

![](https://downloads.intercomcdn.com/i/o/775244670/d2a5bc9d6d56d11c840d5267/Snip20230630_4.png?expires=1741032900&signature=d472c74b6314bceded36bc2e9e4a49562224e923ccf230254ad5b8a6d4ca738d&req=cyciFM16m4ZfFb4f3HP0gHHreljF%2FfipPI6dPpY8AY72QK5J1ZOdjq9nLE6W%0AI5A%3D%0A)

That way it will proceed to use the selected trigger type. 

Do You Have Questions?

---

If you have any questions, please reach out to support via Chat or Email at support@flutterflow.io.