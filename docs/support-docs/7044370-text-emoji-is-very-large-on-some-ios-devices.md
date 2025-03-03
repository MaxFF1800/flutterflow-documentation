---
title: Text emoji is very large on some iOS devices
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7044370-text-emoji-is-very-large-on-some-ios-devices"
hide_table_of_contents: true
---

### Issue 

The text emoji is rendering much larger then expected on some (or all) iOS devices.

![](https://downloads.intercomcdn.com/i/o/682764107/c62573d97d1f429dee017a9a/image.png?expires=1741032900&signature=b945b3245b0a51801acf569e0392c922597f907b243cc39e73565832d68a11ca&req=ciglEc96nIFYFb4f3HP0gEGq4WMojx2rpxyHZglp7%2FXTuCsTqUeUoRtPihVk%0AhMA%3D%0A)---

### Troubleshooting Steps

If encountering an issue with text emojis, it is possible that their size will be affected by certain device configurations. Unfortunately, there is no straightforward solution to this issue, but there are some workarounds that can be tested.

One recommended approach is to enable auto-sizing on the text widget, and then wrap the widget within a container that has a fixed width. The aim is to restrict the text size from exceeding the fixed width of the container. Therefore, if the issue arises again, the emoji will not be larger than the container, even when auto-sizing is enabled.

​

![](https://downloads.intercomcdn.com/i/o/682764672/c317584761562668f0d41b8d/image.png?expires=1741032900&signature=cb0ab17f2f6ad9b59a12dc299fa0da463b940f1faaaa34a0ee29f2fdbe9c4490&req=ciglEc96m4ZdFb4f3HP0gJykjHeo2ay5pL4OamTTqWHsR6P14zMe3TFL6NdS%0A0XU%3D%0A)---

### Example 

Suppose you create a container with a fixed size of 32x32 pixels and insert a text widget with an emoji and font size. Enabling auto-sizing would result in the font size being adjusted based on the widget's dimensions. However, since the container has a fixed size, the font size cannot exceed the container size. Therefore, the text widget's size is restricted to the dimensions of its container, thereby limiting the maximum font size that can be applied.

​