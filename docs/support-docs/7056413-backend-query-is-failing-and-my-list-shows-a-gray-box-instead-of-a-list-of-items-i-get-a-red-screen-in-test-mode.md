---
title: "Backend query is failing and my list shows a gray box instead of a list of items. I get a red screen in test mode."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7056413-backend-query-is-failing-and-my-list-shows-a-gray-box-instead-of-a-list-of-items-i-get-a-red-screen-in-test-mode"
hide_table_of_contents: true
---

### Issue

You are trying to load a list of items from database and it doesn't work and shows a gray box.

​

---

### What Is The Cause Of This Issue?

The gray box means the back-end query failed and can't return any result.

​

---

### How Do I Tell If My Query Is Working?

If a query is working you should see the items generated. Or if there is no result in database and query was successful - you should see the empty state of the list you generated the item on.

![](https://downloads.intercomcdn.com/i/o/685785071/cbfb0d540269dec78e670fd6/image.png?expires=1741032900&signature=135d964d52292dc8e14158515e1aeed1f5401b7c035bc8e7040c826ed9cc4058&req=cigiEcF7nYZeFb4f3HP0gKax2hcXtL2P3DNC1h3lwEREdBvmtBrZEdLP1VVt%0AaJc%3D%0A)

Tip: always make sure if you have a query on a list, set the empty state. This way when the list is empty and there wasn't any result you can see the empty state, you can be sure that query was working fine.

---

### How To Identify This Issue

If you query is failing you will see different results in Run vs. Test mode:

RUN Mode: A gray box in the real device 

TEST mode: A red screen with an error message.

Below you can see two examples:

Working query with no results

Failed query with a gray box that will result in red screen error

​

![](https://downloads.intercomcdn.com/i/o/685801720/97593abbebb1d3b621ac1497/image.png?expires=1741032900&signature=df7a6dd6b5904f1946d249121b2caa31642d4af36b076db507b770c924b257ea&req=cigiHsl%2FmoNfFb4f3HP0gPMsVUEFZS7Ty3mwOpobXrjNKRVP8WDTy2CZGrsF%0AD1U%3D%0A)![](https://downloads.intercomcdn.com/i/o/685897866/4b7e6b9a9fcc80f944a9f03f/image.png?expires=1741032900&signature=4d68c9394a92ee5262ceb20b3abb70aca7b27ec7b6676906b7f47dd89636d380&req=cigiHsB5lYdZFb4f3HP0gBtA%2BdXXSOQHJZ6Hvp5KpWOvfhSm6HacARcx1Wj%2F%0A7fY%3D%0A)---

### Troubleshooting This Issue

If you have a query without any filter or order applied to it and you are experiencing the gray box, the data itself is likely the issue.

 Null values in your database will cause issues in your FlutterFlow project. 

​

![](https://downloads.intercomcdn.com/i/o/685805216/75e9a2cb324565b4b9ad4668/image.png?expires=1741032900&signature=612f97fa41f429acc7903234e2dd3f1083672c6d81ec9c1ea59e50940a7be393&req=cigiHsl7n4BZFb4f3HP0gNllJd%2FXA5I%2By3894d7oXOhqOOjkru1%2BhTABjiQL%0Ax78%3D%0A)

### How To Identify Null Values In Your Database

You will need to check your data in firebase and search for any null value on your fields. 

If your dataset is on the smaller side, you can also use the FlutterFlow CMS to identify null values.

For example in this picture you can see the created_time is null. If you were to use the created_time in your items, you query would fail and you would see the red error message.

We would be setting the formatting on a value that is null, which would cause an issue.

​

![](https://downloads.intercomcdn.com/i/o/685824229/45afbce92897276ea60d68e7/image.png?expires=1741032900&signature=0359ea724558966db610401d8c7838b363ffb295479abfe9478522c28357d02f&req=cigiHst6n4NWFb4f3HP0gB9f06hqJNK2FBK%2FGW8YUUzmPpHhJScf5IT2SL6w%0Apes%3D%0A)

​

![](https://downloads.intercomcdn.com/i/o/685827835/f7c6a5c57a479b17aa9de654/image.png?expires=1741032900&signature=775afe0c5fb8d91a8cbb2e5e3b9c33c35bfdaa9f8a61a49b31e8789a748a8c57&req=cigiHst5lYJaFb4f3HP0gHj%2FbRucldw0RtA7rv%2Bfr%2BZbmkQcegFcJRpfct1h%0ACAo%3D%0A)---

### Tip

If you are not sure you have a null value in your database or not you can use visibility rules to hide the widget you are trying to show data in.

​

![](https://downloads.intercomcdn.com/i/o/685902656/e628bd24cf2ef25d5d3a1359/image.png?expires=1741032900&signature=671ef3cdbe6007f730d5b5de617f50a15d362e4da5fa55e5a99664f65eabe5a6&req=cigiH8l8m4RZFb4f3HP0gOaW9Y6VZS%2BKuMFqMqIefOThu36v18ZN6lj5YZCi%0ADUo%3D%0A)

Note: If you are doing a document from reference query again in your item widget on the reference loaded from your item - make sure to put a visibility rule on the widget you are performing the query on. In case the field was empty and the query is not executed, it won't cause the whole list to fail.

​