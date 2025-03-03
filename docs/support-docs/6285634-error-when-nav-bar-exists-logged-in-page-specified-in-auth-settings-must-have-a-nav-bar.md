---
title: "Error: When nav bar exists, Logged In Page specified in Auth settings must have a nav bar"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6285634-error-when-nav-bar-exists-logged-in-page-specified-in-auth-settings-must-have-a-nav-bar"
hide_table_of_contents: true
---

If your project has this issue, here are the steps to fix it

![](https://downloads.intercomcdn.com/i/o/526334428/de1e6e62be926932f68dc154/image.png?expires=1741032900&signature=2a6722ef7c17be30718e4b6cc6fafca3ad75237314af5367392600576f82db80&req=cSIhFcp6mYNXFb4f3HP0gOywDIzPj71yiGqWvNrxEAujqx%2FZpC%2FPHlNP9rWq%0ABh4%3D%0A)

Why does this happen? This issue can happen when you turn ON/OFF authentication and the editor does not properly save whether you are using authentication.

What is the solution? We need to reset the process so the editor understands that you are not using authentication.

You can use these steps to fix this issue: 

1: We need to enable authentication temporary:

Please go to setting/Authentication and enable authentication

![](https://downloads.intercomcdn.com/i/o/526334826/5f12b4b64b60c65985a7926e/image.png?expires=1741032900&signature=a05e45d476f9e0beb3d4c5748769bd481703b714063acd761e84c4b1eccd1a42&req=cSIhFcp6lYNZFb4f3HP0gKW%2FzoUdLMT3oCr5eOsIPMsYzDfmMWXOUk1Fugu%2B%0A7IM%3D%0A)

2: Set entry page and logged in page: No matter whether you have firebase connected or not, here we just want to reset this setting.

you need to just select 2 pages that have a nav bar on them.

![](https://downloads.intercomcdn.com/i/o/526335393/c9ba7de6f7920b4fb066ee40/image.png?expires=1741032900&signature=8ab2c87ecd6b10d5f27008ea9bd583d8ec8a7942dab2f92eb5c99370f616154b&req=cSIhFcp7nohcFb4f3HP0gMDDyklG4A4DohlElw%2FOPFpj6EaEh926uTBdiP0j%0AbPA%3D%0A)

3: Now you need to turn OFF the enable authentication.

This way we backward the process and now the editor knows that we turn the authentication OFF.

![](https://downloads.intercomcdn.com/i/o/526335874/3106ad69d76240d9d1ca55d8/image.png?expires=1741032900&signature=d9cffb291f36f1dec7e1baf43e791d4956598d89a9f52f9c46fa9b5c7c543654&req=cSIhFcp7lYZbFb4f3HP0gAlLllaD0OYDz9GwWnsparQv0e9SwfuqekKUCVry%0AEmw%3D%0A)