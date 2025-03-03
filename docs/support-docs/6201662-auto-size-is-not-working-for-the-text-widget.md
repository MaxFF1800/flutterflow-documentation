---
title: "Auto Size is not working for the text widget?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6201662-auto-size-is-not-working-for-the-text-widget"
hide_table_of_contents: true
---

Have you enabled Auto Size on your text widget, but the text is not autosizing as expected?

![](https://downloads.intercomcdn.com/i/o/513964125/ac3a2914286af48a4c1adeda/image.png?expires=1741032900&signature=d742d96b62f25dd0d101bd20de305382c672cc185b7fd25caf24d8fbcbc346d5&req=cSEkH896nINaFb4f3HP0gCjPZqarCZsZtnLp8w3r37mRS65%2BVp7PUwOR%2FxGc%0AOoU%3D%0A)---

# Check That Your Text Widget Is Placed Inside Of A Widget With A Defined Height And Width

In order to work correctly, the Text widget needs to be placed in a widget with a defined height and width (e.g. Stack or Container). This way the Text widget "knows" how much it should reduce the font size to fit the frame.

Click on your Text widget and then locate the parent widget it is placed inside. Check to see if the parent widget has a defined width and height. If not, you will need to add this.

Below are some examples of how Auto Sizing will impact how Text looks in your app. Each of these examples uses the same Container and Text Widget. The only difference is the properties that are enabled.

A container with width inf, and height 100px, autosize not enabled on the Text widget.

A container with width inf, and height 100px, autosize enabled on the Text widget. You can see the text widget font size has been reduced.

A container with a width of 30% and no height defined, autosize enabled. Auto size is enabled, but is not working because the container has no height defined.

A container with a width of 70% and height of 50px, autosize enabled. In this case the space is not enough for the text, so the text size is reduced to its limit.

![](https://downloads.intercomcdn.com/i/o/514660194/1dc1080e0810190885aa4f10/AutoSize.png?expires=1741032900&signature=21ff51efc0078bf2a10cb09da28f6c9a58dfc10407dab186854668ee51c9e796&req=cSEjEM9%2BnIhbFb4f3HP0gGyvG6jWEJL5uZFV6DHgFoi2%2FBLT7JjPLP%2FF5SP3%0AlzU%3D%0A)

Tip: Auto Size can be very useful when you are using % width and % height for responsive UIs. You can simply set your container width to 30% and auto size text inside it. This way if the width of the page grows in bigger screen sizes the text will "grow" with the larger screen size.

​

Tip: Font size reduction has limits and can only be reduced so far. You may face issues if you try to use extremly tiny text.

So next time you want to ask a text widget auto size, don't forget to tell it how much 😀

​