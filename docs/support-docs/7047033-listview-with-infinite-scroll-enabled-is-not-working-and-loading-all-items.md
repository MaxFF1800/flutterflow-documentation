---
title: ListView with infinite scroll enabled is not working and loading all items
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7047033-listview-with-infinite-scroll-enabled-is-not-working-and-loading-all-items"
hide_table_of_contents: true
---

### Issue

You have infinite scroll enabled for a ListView, but the ListView is loading all items instead of loading a certain number of items per page. 

Infinite scroll is a popular feature in mobile applications that allows users to continuously load more content as they scroll through a list. However, implementing infinite scroll in a ListView can lead to unexpected behavior if not done correctly. In this article, we will discuss best practices for implementing infinite scroll in ListView and how to avoid common pitfalls.

---

## What Can Cause This Issue

This issue typically arises when the ListView expands indefinitely because there is no limit on its height. As a result, the query loads all the items as there is no indication of where the end of the available height is.

---

## Solution

To fix this issue, the ListView needs to be "aware" of the available space in order to calculate the number of items to load on each page. For example, if the ListView has 800px space, and each item is 100px in height, it should load 10 items, displaying 8 in the view and 2 out of view. As the user scrolls, the next set of 10 items should be loaded.

​

---

## Implementation In FlutterFlow

This project includes examples of the implementations below

#### Best Practice Implementations

Turn off the scroll on the column and let the ListView itself do the scroll with the primary option turned on and expanded options. With this configuration, the ListView knows the page height and adjusts the items accordingly.

​

![](https://downloads.intercomcdn.com/i/o/683646947/0bb68858ed31df6eb3aa38b5/image.png?expires=1741032900&signature=5b3759ec1d299368cbb66b5eb02a629886366c040fc29390eb876855f30378a3&req=cigkEM14lIVYFb4f3HP0gF0%2FQdmEkvz%2FfY9f77CYpK2ekVxP70nscKw%2BPxH0%0AOjg%3D%0A)

If you want to put the listView inside a scrollable widget and want to implement infinite scroll, wrap the ListView inside a container with a fixed height or max-height.

For example, in the project example provided, the main scrollable is the column, and the ListView is wrapped inside a container with a fixed height of 500px. The ListView scrolls until it reaches the end, and then the page starts to scroll.

​

---

#### Configurations That Can Cause Issues

In this example, the ListView widget is not expanded, and the red box at the bottom of the page indicates empty space, indicating that the ListView cannot determine the height. 

The column, as the parent of the ListView, has the scrollable option, making it impossible for the ListView to determine the height and adjust the items based on a fixed height. 

![](https://downloads.intercomcdn.com/i/o/683642835/2aa9f017e47e7d9530ae6853/image.png?expires=1741032900&signature=1d3ea43c1e37438fcb65495d42b282b4a538373a317fe55c159fa99da21174fe&req=cigkEM18lYJaFb4f3HP0gG43xjuWvaHnAp0SM4FFLPLt0%2FzTlIMu3twmmVoi%0Afhc%3D%0A)---

### Conclusion

Implementing infinite scroll in ListView can improve user experience by allowing users to continuously load content as they scroll. However, it is essential to configure the ListView correctly to avoid unexpected behavior.

By following best practices, such as calculating the number of items to load and wrapping the ListView in a container with a fixed height or max-height, developers can ensure a seamless and enjoyable user experience.

​

![](https://downloads.intercomcdn.com/i/o/683692629/eba8eb7d838f3e0b49e3c49f/2023-03-03_17-35-46+%281%29.gif?expires=1741032900&signature=91feaaefd455133b2c4864376db8eeb28ce231d5fb37c8f6936ae2bb00e6c99c&req=cigkEMB8m4NWFb4f3HP0gDOXghFGhS8p266BCIDrI0kYNc2LMXL%2Bu8GFgTm2%0APKk%3D%0A)

You can check the project example here to see them all in action in Flutterflow

https://app.flutterflow.io/project/list-view-scroll-example-wdv076

​