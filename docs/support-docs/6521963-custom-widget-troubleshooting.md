---
title: Custom Widget Troubleshooting
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6521963-custom-widget-troubleshooting"
hide_table_of_contents: true
---

We want to make a custom widget and reproduce some common errors and issues and explain how we can fix them.

What do we want to make during this article?

![](https://downloads.intercomcdn.com/i/o/572911742/0f0826e2d8117396f19be30f/2022-09-01_15-02-15+%281%29.gif?expires=1741032900&signature=7c88811567d54b23290d3bf6b5145703a3283e27ad64ce949d36da7d1915344b&req=cSclH8h%2FmoVdFb4f3HP0gPSg6M6z1VLQg9GpS4OSSL5PoX0X1YPuJeDohHoi%0ApsU%3D%0A)

# Animated Text Widget

Project URL: https://app.flutterflow.io/project/animated-kit-widget-fyqw6j

Run mode URL: https://app.flutterflow.io/run/QP62FwanUTRs7O3HJzdo

Tips:

1: always set the left panel side

Widget name [ make sure to use a unique name ]

2: Use the boilerplate code and copy it, then start to edit, and add the code

![](https://downloads.intercomcdn.com/i/o/572934479/121f8ffc771341e8c7bd9092/2022-09-01_15-27-03+%281%29.gif?expires=1741032900&signature=466b40d5a7a61e4d40cce2734d6ea14fe8be3f832bd7e2d10899b05cd2db79cb&req=cSclH8p6mYZWFb4f3HP0gADCF2jHydZEXOQHAEKilLq%2BwZU2J0v3dF5nq78X%0AdOE%3D%0A)

Errors could happen:

​

1: The widget name is the same name as the package you used as a dependency

![](https://downloads.intercomcdn.com/i/o/572926435/e03dc9995b7c379f62e7bdea/image.png?expires=1741032900&signature=b12047cd1585efcbd7c4a720aa014fbdab5e18b0d7bc22e4016609c801a96ae5&req=cSclH8t4mYJaFb4f3HP0gMwQn4nCy09Cq3i7Gx3aLohJzgtQdkPWEkale6rA%0AMWg%3D%0A)

![](https://downloads.intercomcdn.com/i/o/572927132/84f5c1c9f8ea0724dcf16ee8/image.png?expires=1741032900&signature=acddf571d6153f9717180a3d3ba6253e522a2a26c92605d8ed912cb74f9ac45d&req=cSclH8t5nIJdFb4f3HP0gEkGuQtUWnDl3ouZo1dyBUH2zElIkSR0VkINAJgo%0AmAY%3D%0A)

Make sure the widget name you pick is not the same as the package names you import as a dependency, also don't use unique names like "main" or "widget"

Try to use unique names.

2: Forget the package import inside the code

​

![](https://downloads.intercomcdn.com/i/o/572885865/46bcce15524fc7aaadacdd93/image.png?expires=1741032900&signature=d79d87a1f658017971efccc47923910ae7ea8e2757f7b3bb85b2c5c497e6cd7f&req=cSclHsF7lYdaFb4f3HP0gImPJJggmDottS0BZgcSb7TSxBUDgUIhUQHHBX6I%0A1Ag%3D%0A)

You use an external package for your custom widget and you add it in dependency, but you forget to put the import line in the code

"The method X isn't defined ..."

Fix: Open the package URL on pub.dev, you can find the import line in the details

in our example, this is the import line

​

![](https://downloads.intercomcdn.com/i/o/572886441/bbce6fab3a65bcff6007a8da/image.png?expires=1741032900&signature=e4ba56eeb8c39cd62ea24ac252d10e2b7c52493996cb1796190467818744b781&req=cSclHsF4mYVeFb4f3HP0gA7vtJNhQweutzgD6W8PUB7g5OEIHyR%2F6pA2cwXA%0AOPY%3D%0A)![](https://downloads.intercomcdn.com/i/o/572886889/4594708c4c3bdadff5ad1d41/image.png?expires=1741032900&signature=cd802877491a13fde997da194bd53113ef3190bed08202d661044b878d031f39&req=cSclHsF4lYlWFb4f3HP0gDWh41yzYKZT1svHYcF89Fey3dE%2Bjr8cH46owU0x%0A4do%3D%0A)

3: Packages you are using also need another external package, and you need to import that as well.

Each time you want to use a package, make sure that specific packages have other needs as dependency or not.

​

![](https://downloads.intercomcdn.com/i/o/576901994/310a79f3108c6538fc936602/image.png?expires=1741032900&signature=2353f14303388b4a17694ea5184d1cb7c7087a21e0e7880c170d7894537f56c7&req=cSchH8l%2FlIhbFb4f3HP0gBr3WaTH4gLqll5CfbtpJ7vAqyRvZhRqwsg5nRrA%0A8bg%3D%0A)

In this picture, you can see our package needs another dependency name "silver_tools"

When we are making the custom widget we need to do this import as well.

​

![](https://downloads.intercomcdn.com/i/o/580724220/503370e546ca4c1f856ab3b8/image.png?expires=1741032900&signature=dbf08987dfd645a0967a977e1bcc06209d699516d7c889a0fcf3f7510ea93e1f&req=cSgnEct6n4NfFb4f3HP0gOg5AkDnVjrn4d9sk9b%2By9RS2tRYVtBsRpCzhktS%0Ai4U%3D%0A)

Notice: Always check the widget name in the code, if you forget to use the boilerplate code, then maybe the name of the widget and name in the code maybe be different, and it could cause compile failure.

​

![](https://downloads.intercomcdn.com/i/o/580750693/9799be65fc240b202d6e98ae/image.png?expires=1741032900&signature=ba824ce44a50ac645e2725426ccc7c8701471003e703133421fce1b3239f89b8&req=cSgnEcx%2Bm4hcFb4f3HP0gKo5ixHVlJApkUzHfH6EvvIcltO0Cd662wH2tH6R%0AUyM%3D%0A)

as you can see in this picture name of the widget is not the same as in the code. and this widget will fail to compile.

it should be like the picture below.

![](https://downloads.intercomcdn.com/i/o/580750337/22cc96f00ed5f5a69ccc186b/image.png?expires=1741032900&signature=9d0b271e92f00996b6b0af35ceecbf22ad19476d5f2660b8a71b66987b1c55ad&req=cSgnEcx%2BnoJYFb4f3HP0gHH320tEKLvBOM23mrBh6kNEi5RHGFNUVpsGqtW3%0A24M%3D%0A)