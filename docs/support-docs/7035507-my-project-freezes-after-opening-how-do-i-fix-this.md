---
title: "My project freezes after opening, how do I fix this?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7035507-my-project-freezes-after-opening-how-do-i-fix-this"
hide_table_of_contents: true
---

### Issue

When I try to open my project it freezes. I'm unable to access my project or make changes. How do I fix this?

---

### Background

The most frequent cause of a project freezing is a rendering issue in one of your pages

---

### How To Use Safe Mode To Identify And Resolve The Issue

The best practice to fix a project that is freezing is to open the project in safe mode, go to the place you were working before the crash happened, and undo the changes (e.g. update properties, delete the widget, etc.)

---

#### Add ?SAFE_MODE to the URL

Simply add ?SAFE_MODE to the end of the URL (e.g. https://app.flutterflow.io/project/sample-app-social-app-tx2kqp?SAFE_MODE) which will open it without rendering the UI Builder.

Tip: Don't forget to add the ?

​

![](https://downloads.intercomcdn.com/i/o/680517369/9d26bdcb49e3e67a88fcb5b3/image.png?expires=1741032900&signature=7a1806806c2c5b21df90c03905275222e43b851ad4373be586b34ab52182a378&req=cignE8h5nodWFb4f3HP0gEKcRKfwUbwDCUiVyt9aPGZ2Djt4VvljrZSmX6jC%0Afy4%3D%0A)

Example project when the UI is not rendered in the Builder:

![](https://downloads.intercomcdn.com/i/o/680518351/e8a4bebb2a1513e759748113/image.png?expires=1741032900&signature=71dbc34cc9d66e7d371fcb484daddee7222c1a37bef8b6c2cbd2d18dbfbd3353&req=cignE8h2noReFb4f3HP0gEPAR8qTCGW0WQhZ7TO5D7eLH2rXIbg1%2F25WuUNi%0AuTA%3D%0A)---

#### Undo The Changes You Made Before The Crash Happened

Enter the project in Safe Mode and go to the place you were working last time before the crash happens.

​

Undo the changes you made (e.g. delete the widget, change the height back to 50px, etc.)

​

After doing the first edit, the editor will exit from the SAFE_MODE. If your project successfully renders, you can return to building. 

Otherwise continue to enter make safe mode and make changes until you find what was breaking your project. 

---

#### If you are unable to identify the widget causing the issue, please reach out to support at support@flutterflow.io or via chat.