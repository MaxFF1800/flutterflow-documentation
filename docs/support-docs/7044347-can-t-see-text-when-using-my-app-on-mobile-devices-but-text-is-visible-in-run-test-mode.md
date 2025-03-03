---
title: "Can't see Text when using my app on mobile devices, but Text is visible in RUN/TEST mode."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7044347-can-t-see-text-when-using-my-app-on-mobile-devices-but-text-is-visible-in-run-test-mode"
hide_table_of_contents: true
---

### Issue

Text widget is not showing when I am testing on a real device, but this text is visible in Run/Test Mode (example below).

![](https://downloads.intercomcdn.com/i/o/682752122/2a30d9b574e9e3e3141dc467/image.png?expires=1741032900&signature=80dd749cae6a050624fdc366072da460ab8fd62a8477fc7e3fe4ef9068bfbc61&req=ciglEcx8nINdFb4f3HP0gHTFHGbVVFD6qu8uqTBTl6duUsHvqQFZV%2FfrGk2t%0AK%2FY%3D%0A)---

### Troubleshooting This Issue

If you encounter this issue, there are two specific areas to investigate:

​

#### Check Light/Dark Mode Text Colors

It's possible that the color scheme for the dark mode is leading to poor visibility of text against the background colors. This issue can be resolved by either disabling dark mode if it is unnecessary or adjusting the color scheme for the dark mode to a suitable setting.

Navigate to Settings > Theme > colors to check the color settings.

​

![](https://downloads.intercomcdn.com/i/o/682753288/7a51650040be82cfccbdcd68/image.png?expires=1741032900&signature=7a82f543869603563da5fb637ecc824a8f08add80aa9ae629f79f14e5c47f843&req=ciglEcx9n4lXFb4f3HP0gN0zwATpY%2BlIs8Br0SZpu%2FOD4Ui9istIHClIlZEt%0AtLU%3D%0A)---

#### Ensure No Translations Have Been Missed

If a translation has been missed, then the text will appear as an empty string when the application is run in a non-default language setting. To address this issue, you can use the FlutterFlow automatic translator to ensure all pages are translated when a new language is added. 

#### 

![](https://downloads.intercomcdn.com/i/o/682758309/fc92aa397ffc7583c8d2e962/image.png?expires=1741032900&signature=a8e15eeb51d625415e6b0e82f38417f9afe4b2075597a37dbbcedb14821a9fdf&req=ciglEcx2noFWFb4f3HP0gFeiqMMMP8rWCBrcr%2FKpTVcbRdKIaVa0Giv85O%2Bc%0ADO0%3D%0A)

Alternatively, you can open the translations and look for any empty cells (example below)

![](https://downloads.intercomcdn.com/i/o/686292827/dbbd2b88df252f3e2be85c2f/image.png?expires=1741032900&signature=7621d71a45d329ea24e6fcd4913268ca5384d27b2edf9f626c0a12a57c42f808&req=cighFMB8lYNYFb4f3HP0gMYheiMK%2FZl00RStC6WOC6zpRlOGSP7W9GpfaB1K%0A1QA%3D%0A)