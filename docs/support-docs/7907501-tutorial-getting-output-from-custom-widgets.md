---
title: "Tutorial: Getting output from Custom Widgets"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7907501-tutorial-getting-output-from-custom-widgets"
hide_table_of_contents: true
---

# Use Case

There might be scenarios when you might need to get some output from the custom widgets, but because it is no direct way to do that in FlutterFlow, I will be sharing an alternative way to do that.

​

# 

Tutorial:

In order to get the value out of the custom widgets, we'll be using app state variables to do that. The strategy would be to store the value from the custom widget inside the app state variables and then use them outside the custom widget on the screen.

Step 1: Create a new app state variable.

​

![](https://downloads.intercomcdn.com/i/o/742014834/7d2763fc8c73ec0c31579878/SCR-20230515-puuv.png?expires=1741032900&signature=e1658477d2122dfa0b2875a1556da0a2c2ad2d2a2ab150ebf6ed5d25a5605c96&req=cyQlFsh6lYJbFb4f3HP0gOAUMWN10NPlMSfZ5zHYDtMGLx0pNq%2FjzCpcl5yC%0A0KU%3D%0A)

Step 2: Update the app state variable inside the code using FFAppState() as shown in the image

​

![](https://downloads.intercomcdn.com/i/o/742014977/7ef75c1a6ef9c78c092fbe8f/SCR-20230515-puwk.png?expires=1741032900&signature=cd11010d65a804f04969466b5298bdffbb1b4aab0f32a4e99782674e9c162c30&req=cyQlFsh6lIZYFb4f3HP0gOyEFQhbvhLxaFRf39AXRwVYYqq4H%2BnEgUHODAsH%0Am0k%3D%0A)

Here is the code to update:

```dart
FFAppState().update(() {
  FFAppState().localvalue = 'setvalue';
});
```

Still facing any problems?

---

If you still face any problems after following the outlined steps, please reach out to support via Chat or Email at support@flutterflow.io.

​