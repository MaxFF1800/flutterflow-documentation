---
title: "How To: Make a custom Loading Indicator Animation With Bottom sheet"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6332011-how-to-make-a-custom-loading-indicator-animation-with-bottom-sheet"
hide_table_of_contents: true
---

![](https://downloads.intercomcdn.com/i/o/535545360/3d0bfba22c88ee3cb3b4b8ad/2022-06-24_14-28-20+%281%29.gif?expires=1741032900&signature=295a30cfbc3f1b348146e17270c18b498e8f9e84e882bff9705a7fe15c508451&req=cSMiE817nodfFb4f3HP0gCN0Kani4PlpIZwjQN4yjH6wOa%2Bw278sfmDHmASp%0ATH0%3D%0A)

Why do we need this? Sometimes we have actions that need time to finish, like calling an API and waiting for the response.

Now we want to show a nice custom loading animation with help of bottom sheets.

1: Create the loading modal

![](https://downloads.intercomcdn.com/i/o/535548069/93819b5191060d9a413add26/image.png?expires=1741032900&signature=32e7d3e3cd11d163e621758ded6b34a4e6a91cb54d0964dac688eebf63528ff8&req=cSMiE812nYdWFb4f3HP0gJ0pPUWTPv%2FfKebnnzi8bkznQzbamyxpChn%2B4OWH%0AjS4%3D%0A)

Make a new component, the bottom sheet, we putLottiee animation inside the modal.

You can simply make any kind of UI for this bottom sheet, show film, Gif images or animations, text etc.

2: Create our chain of actions:

![](https://downloads.intercomcdn.com/i/o/535549913/a53e4089190b87d2224bdccb/image.png?expires=1741032900&signature=170b1aa0b8e2f5243a52db648ae24cf31473a77c0f10a482f75cebdb7db328e0&req=cSMiE813lIBcFb4f3HP0gJvAvtVSndtO8T0tiAaDQefiGfrpVCZggluCp4Cw%0AakE%3D%0A)

1- a fake delay action, can be the API call or a simple action, even you can ignore this one.

2- show the loading animation, and open a bottom sheet. here we start to show the loading.

![](https://downloads.intercomcdn.com/i/o/535550876/cf766b569576307f89c1ebcc/image.png?expires=1741032900&signature=c2890cbfba2be4a92bbddb926cae3a258ef833be25b66d88e01f4beaf017f922&req=cSMiE8x%2BlYZZFb4f3HP0gPMbRL7PIqtbtf%2Fe4Lp3w6cEWgpL1dPil%2FI2yTgj%0Af0I%3D%0A)

IMPORTANT: in the open bottom sheet action, you can see the option "Non Blocking"

We need to turn this option on.

it means: open the bottom sheet and do not block the next actions. any action after the open bottom sheet action will be executed immediately.

3- our main actions, I just put a delay for 5 seconds here to simulate some actions that need time to be finished. this could be a chain of actions. anything you need to do and meanwhile you are showing the loading.

4- Close the loading, Here all our actions are finished and we just need to dismiss the bottom sheet.

![](https://downloads.intercomcdn.com/i/o/535552641/d96dc36ef9de51eddda6ce32/image.png?expires=1741032900&signature=9deba2a353562b46709dcebe54e515b826206321e5f86fd70ff629e93bb7d8fa&req=cSMiE8x8m4VeFb4f3HP0gF6UBXtRGiEArc7MEU2WPFUpee4SMH%2BhYsRrWxo0%0ADGo%3D%0A)

5- Show a finished message, this is a snack bar we show, a message that says the actions are done! if you need to give a message to the user after all.

Project URL [ Public ]

​

page name "CustomLoading"

when you run the project, just hit login on the login page [login with our test user] in the home page click on the item "Custom Loading"

Run Mode Link

![](https://downloads.intercomcdn.com/i/o/535555435/7b975e8c08ff4d59532833a2/2022-06-24_14-48-44+%281%29.gif?expires=1741032900&signature=dc93d659dcd121cef9c3c2fdf3357f5f93af7847452a56d07e65b4ba244c30f9&req=cSMiE8x7mYJaFb4f3HP0gKFDoggNX4LbHFtVbHdTWb3fVE%2BzY42R1hk0UA%2FC%0AhzU%3D%0A)