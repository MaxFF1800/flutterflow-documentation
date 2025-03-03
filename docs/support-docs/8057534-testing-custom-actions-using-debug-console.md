---
title: Testing Custom Actions using Debug Console
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8057534-testing-custom-actions-using-debug-console"
hide_table_of_contents: true
---

Background:

Sometimes, the compiler does not show any errors in the custom action, but the custom action still won't work as expected. This might be due to the code logic or the implementation. In order to test the implementation and the flow, you can use the debug console to test the custom action in different scenarios.

Steps for Implementation:

The core function that you can use to test the custom actions on the console is the debugPrint function in Flutter. To use that in the custom actions, follow these steps:

Step 1

Use debugPrint to print some error on the debug console in case of a specific result. You can use if-else statements or try-catch statements in order to test the success of the scenario:

​

![](https://downloads.intercomcdn.com/i/o/772498969/3c60bfd5e7ea8058cfe47f70/SCR-20230627-oqrf.png?expires=1741032900&signature=1b7eafc15c950189bb7972b91192f1a028ba0cd1a30d64e81cef37f47d60ee74&req=cyclEsB2lIdWFb4f3HP0gC2%2BIJgznCtIMvJOZh1GM5%2FZq8VQPHdBZy%2FIUlaF%0AB3w%3D%0A)

Step 2

After the correct implementation in the code, use the action inside the app. On the run mode, open the console. Now you should be able to see the errors in the console upon performing the action.

![](https://downloads.intercomcdn.com/i/o/772502046/500cf23ebd5b5053465a802a/SCR-20230627-osal.png?expires=1741032900&signature=79b66af5f5dffeeb134cf56a425dceb6fdc91b7c883cd3c2df4a25d988660efb&req=cyclE8l8nYVZFb4f3HP0gGR5RyyglQeBZlJ604Wc1bVIjMGRkjuCFSL9LYvP%0ALes%3D%0A)

Still having issues?

---

If you are still running into issues in your implementation after following the outlined steps, please contact support via chat in-app or email at support@flutterflow.io.

​