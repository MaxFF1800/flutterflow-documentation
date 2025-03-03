---
title: "Run mode-only notification: Firestore Security Rules: Missing or insufficient permissions"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6395544-run-mode-only-notification-firestore-security-rules-missing-or-insufficient-permissions"
hide_table_of_contents: true
---

If you are seeing this error in Run Mode, there is a mismatch between your Firestore Rules and the permissions required for your query.

Tip: the error will indicate which item has the issue. For example, in this project there is a permissions issue with Container on this page. Giving your widgets descriptive names will make it easier to identify the source of the permissions issue.

​

![](https://downloads.intercomcdn.com/i/o/548270105/8b422c089627d5da7cb27655/image.png?expires=1741032900&signature=921474b0433ec60572e4dba433c78a0ac0d8270788183b024e1b1e8c8526254e&req=cSQvFM5%2BnIFaFb4f3HP0gFBqIFiTYn%2FGfr5XSdsofRcgNdhUk7e8I2ppo596%0A%2FLo%3D%0A)

Here a couple of examples that would cause you to see this error:

If Firestore rules are set to “No one can read from this database” then you would see this notification on every query. 

If your Firestore rules are set to “only logged in users” and you put a query collection on the sign-in page (before a user signs in), that query would fail and you would see this error message.