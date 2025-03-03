---
title: "Tutorial: Search Implementation for Supabase"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8171759-tutorial-search-implementation-for-supabase"
hide_table_of_contents: true
---

### Background:

FlutterFlow does not yet officially support Supabase search functionality, but we do have a workaround to implement a simple search function. Please note that this will not be a full-fledged search solution, but rather makes use of the equal filter by using the Supabase Realtime feature.

​

### Steps for Implementation:

1. First you need to enable Realtime from the Supabase table settings.

![](https://downloads.intercomcdn.com/i/o/756034317/d8407bfa7b00e1c01e1e12c3/SCR-20230604-ngja.png?expires=1741032900&signature=1bc98bb739372bf093efc259e856aafde9304e1a7ed0a31bf2edc9bfcc49737b&req=cyUhFsp6noBYFb4f3HP0gKEO0M99NOeiuUjOWj%2BKE6t4h18W0ATxAELtfuD5%0A2mY%3D%0A)![](https://downloads.intercomcdn.com/i/o/756034316/d402c915cb929a096b7807d3/SCR-20230604-ngky.png?expires=1741032900&signature=0e60ef54553a982383541fec4f18d0ba68edab845a375ef91c2e9f8cf5c5fb67&req=cyUhFsp6noBZFb4f3HP0gBJC4aVaO3P4Kg%2FkHT9yuQ9FxUiJb5CXX5CHsvZH%0AF44%3D%0A)

2. After enabling this you will then need to filter the query data with the input text field and set the filter to is equal.

​

![](https://downloads.intercomcdn.com/i/o/756034814/1fe081c74c2bf4a2bfe637a0/SCR-20230604-nhgb.png?expires=1741032900&signature=d5d31bd36067d6c7042ef7eeebecaf0828a71a5153a1b9477d17b98e668f96de&req=cyUhFsp6lYBbFb4f3HP0gFJoLrziA2YoLx%2B455jigBYzszGQbTwRnLvO6EK2%0AoEE%3D%0A)

3. Now there are two options, first is to automatically search the data as soon as its typed. To do so, you need to enable the update page on change and set the frequency accordingly.

![](https://downloads.intercomcdn.com/i/o/756035492/e2115e3603e1f91516e94116/SCR-20230604-nhqr.png?expires=1741032900&signature=8f5d5bf0a9bb038af2c039a16746a4d285afa080bfc0d887c4946f60c3c008bb&req=cyUhFsp7mYhdFb4f3HP0gO84io%2FIqYR4uCTOgJ74CZdsvbQr5Lj2r6auGTJE%0AtfY%3D%0A)

4. The second option is to refresh the database when the text is submitted.

![](https://downloads.intercomcdn.com/i/o/756036199/c3c7ff927748c4fe95622307/SCR-20230604-nioe.png?expires=1741032900&signature=b3791f0710c35cdbe0ec9a02fc06c92d414b8ba0d783c14497cceccaef394966&req=cyUhFsp4nIhWFb4f3HP0gIGNYyljK7YMOjidwI5IabICMm8tEn4xitbVLXah%0Asn8%3D%0A)

Please note that real-time updates will be more costly compared to searching after submission.

The issue was not resolved

---

If the error persists after following the outlined steps, please report this issue to support via Chat or Email at support@flutterflow.io.