---
title: "Email: Client access to your Cloud Firestore database expired"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7171578-email-client-access-to-your-cloud-firestore-database-expired"
hide_table_of_contents: true
---

## Background

You've received an email from the Firebase that "Client access to your Cloud Firestore database expired"

​

---

## Why Am I Seeing This Message?

When the user enables the cloud firestore, there are two rules to select in order to get started. 

![](https://downloads.intercomcdn.com/i/o/695431435/23020ae47384cc33b47346f8/Screenshot+2023-03-21+at+11.26.35+AM.png?expires=1741032900&signature=f526e0a76b38bda8285da5ada94f75c08c7648c174d6ec0fdd0024f0e0120a0d&req=cikiEsp%2FmYJaFb4f3HP0gGj1lmF2xQGVSnIu27yluZd3W%2B2x3teM4BxSNmz%2B%0ACGk%3D%0A)

1. Test Mode (Time bounded)

2. Production Mode (Not Time bounded but secured at the start)

Usually, the user selects the Test Mode and the Firestore works fine. but after the time has been completed the client access get expired. To keep using Firestore user must update the rules.

​

---

Solution 1: Manage the Firestore Rules directly from FlutterFlow

Head over to this article to see step by steps instructions about how to Manage the Firestore Rules directly from FlutterFlow.

Solution 2: Manually update the Firestore Rules from Firebase

In order to keep using Firestore, User should head over to the Firebase Firestore section and select Rules.

Here we can see our previously defined rules, We have two options here, any of these options will solve the problem.

Update the timestamp date to a future date if you still want to keep it in test mode.

​
![](https://downloads.intercomcdn.com/i/o/695432192/6c868d68de4080297d265f87/Screenshot+2023-03-21+at+11.28.13+AM.png?expires=1741032900&signature=7ed245615a6f4c4be4af5cab60ad1c75259a6e931bee8151df84307b4844dc94&req=cikiEsp8nIhdFb4f3HP0gHnppBGV4V6fGpXt5EP0je5X3uKd4001qwhFwuJ3%0AE%2BM%3D%0A)

Update the rules with some conditions in your database to make it secure.

![](https://downloads.intercomcdn.com/i/o/695432384/c8995dccb5576136098751ce/Screenshot+2023-03-21+at+11.28.46+AM.png?expires=1741032900&signature=4b14bf1c55c9b80fddbd94af0b53da248839577d8274d6daae2b25aa12b14700&req=cikiEsp8nolbFb4f3HP0gBV8Hg88yuKguTHMsTWJSyby3aFZITtli1XCwY9d%0AqpY%3D%0A)

After applying this solution, your problem should be resolved, it the problem still persists, feel free to contact us at support@flutterflow.io

​