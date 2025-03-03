---
title: "Have an issue saving my work in my project. my changes not save."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7034395-have-an-issue-saving-my-work-in-my-project-my-changes-not-save"
hide_table_of_contents: true
---

If you have reached the size limit for your FlutterFlow project, it's important to check the browser developer console to confirm this. Here's how you can do that in Google Chrome:

​

![](https://downloads.intercomcdn.com/i/o/680236330/3875cb959e6e651ccc9966db/image.png?expires=1741032900&signature=da305e541e15bbe2b6715c2024633f8d4c0249b9cc0f1f5fc9352c8b4c79031a&req=cignFMp4noJfFb4f3HP0gHN3rL3i3ONp6AAXvOM48nIO9kAHJA2FhSKUQaK9%0AZ9g%3D%0A)

Press F12 to open the developer console.

Click on the console tab.

Wait for any errors to appear while you work on your project.

​
![](https://downloads.intercomcdn.com/i/o/680234843/f6afadfbb26251925be3c841/image.png?expires=1741032900&signature=b80c7c203347332423c0558e04fd1ee558baa69e3eaa4eb3b430f01784448634&req=cignFMp6lYVcFb4f3HP0gAoeRrJWA1nj0CACC0IVe8aHrZVSRZR47DUIXQNq%0ArjA%3D%0A)

For instance, if you receive an error message when trying to work on a project that has reached its limit, unfortunately, there is no way to increase the project size limit. However, you can reduce the project size by optimizing it. Here are some steps you can take:

Remove any unnecessary assets from the asset folder and try to use their URLs instead. You can upload your assets to Firebase Storage, grab the URL, and use them in your project. Only use assets if you need them offline and have no other choice.

Remove any temporary pages or components from the project.

If you keep some UI elements in the project just in case you need them later, put them in a clone version of the project instead of keeping them in the current one.

Save a version of your project and remove any unused or unnecessary UI elements. If you need something later, you can retrieve it from an older version or snapshot and paste it into your current project.

Convert any UI element you use more than once into a reusable component to reduce the project size.

If you are creating a page repeatedly, make it more dynamic or convert it into a modal and use it in different places.

By following these steps, you can optimize your FlutterFlow project and reduce its size to avoid hitting the size limit.

​