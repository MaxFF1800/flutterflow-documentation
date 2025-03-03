---
title: Compilation Fails Despite the Compiler Not Showing Any Errors
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8076318-compilation-fails-despite-the-compiler-not-showing-any-errors"
hide_table_of_contents: true
---

# Issue Overview

In certain scenarios, your code may fail to compile, but the compiler might not show you any errors. 

![](https://downloads.intercomcdn.com/i/o/776896385/46aa686677e20aa75eb69aa0/image+%2828%29.png?expires=1741032900&signature=42a28b3f703aab97583bf2995250f276f27bb6d3c4fed8fa377ceecf11f67dab&req=cychHsB4nolaFb4f3HP0gHnaJQ1bB5VBNDfHNvJYWne%2BBoe1NA0xksCNVbDp%0AFfU%3D%0A)

In this article, we'll discuss some of the common reasons that might cause this problem. Our team is continuously improving error detection, but in the meantime, you can check for these problems in your project:

# 

Scenario 1: Different Package Versions​

​You might be using some packages with a different version compared to the already existing packages in your project found in Pubspec.yaml file.

​

![](https://downloads.intercomcdn.com/i/o/776896205/26fc14ac19243ffc146ec104/Screenshot+2023-06-20+at+4.11.09+PM.png?expires=1741032900&signature=f2301dacc291540399420ee99f07fa4175b11c3722c305d64c645cbfc272ba30&req=cychHsB4n4FaFb4f3HP0gP0UAp5mJw%2BetmuXuXq5agKEIoh2d1XsFBAGhAMF%0AWK0%3D%0A)

![](https://downloads.intercomcdn.com/i/o/776894614/b9c8ab6ba468a1eb88368e49/SCR-20230704-bpqp.png?expires=1741032900&signature=f23e9ec6ebc5e9cd2e3628f726d7573a6f2482a44bff4833f7684c89c8468d6e&req=cychHsB6m4BbFb4f3HP0gPMS2yGkrPhG%2F2hApouXCQBE4J6dPknxc6lU%2Ffz0%0ASls%3D%0A)

In order to resolve this problem, remove the existing pubspec dependencies.

# Scenario 2: Differences in Code​

The custom code defined in the project is different compared to the code, which might have different parameter names, null safety, return types, etc.

​

![](https://downloads.intercomcdn.com/i/o/776899384/d87068414af5619e1d909f2f/SCR-20230704-bstz.png?expires=1741032900&signature=089714075b112271699787253e5f7d84251b6bf6d141c5d655d103afe38c4247&req=cychHsB3nolbFb4f3HP0gMOH38SpJxFvQS7S7WQBlFyIzXTeKyU1cn1JJjsl%0ApLU%3D%0A)

![](https://downloads.intercomcdn.com/i/o/776899440/cc135d01aafa0dcb6af1bf56/SCR-20230704-bswd.png?expires=1741032900&signature=dd944cdc0a18c03665e7d5108f28896af6c229989b3f34ae0d1c93198877a2ca&req=cychHsB3mYVfFb4f3HP0gKL2ouwt%2BbJ2I%2FsJZyPtn%2B3ybBJULABNVgEvqiic%0Az8E%3D%0A)

You'll need to confirm that the code matches the defined custom code. You can also compare your code structure with the boilerplate code.

​

# Scenario 3: Forgetting to Press Save

It happens to everyone eventually: you forgot to press save. After modifying the code, if you didn't hit save, this might result in the same error.

​

To resolve this, please click the save button before compiling the code.

---

# Additional Resources

Need additional information? Check out these other helpful sources:

FlutterFlow Documentation

Community Tutorials: FlutterFlow Community

FlutterFlow on YouTube

FlutterFlow Blog

FlutterFlow Marketplace