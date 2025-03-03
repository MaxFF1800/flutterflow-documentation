---
title: "Backend query don't return any results even though I have data in my database"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7058101-backend-query-don-t-return-any-results-even-though-i-have-data-in-my-database"
hide_table_of_contents: true
---

### Issue

You have data in your Firestore database, but your backend query is not returning any results.

---

There are a number of issues that may cause this issue. Here are some of the most common issues to check for:

​

### You've not deployed the correct rules for that particular collection that is not returning the data

In some cases, when you create a new collection in the project, the user forgets to setup and deploy the rules for that collection. Please take a look at the firebase section and deploy the correct rules

​

![](https://downloads.intercomcdn.com/i/o/787415317/aa029b395d3ca3541a19162e/SCR-20230718-myon.png?expires=1741032900&signature=077b59a55411c85f349f6b5d0cecd99c09031253d534c1899daaa2b0b7a2ee18&req=cyggEsh7noBYFb4f3HP0gK8cY%2Bfle9TjBq%2F4KPDFBhW1fJfR9QD70BSOsySv%0A4cY%3D%0A)---

### 

You've enabled the Ignore Empty Filter Values Option and have missing or Null Data

In the example below, we have a filter on created_time and have enabled the Ignore Empty Filter Values Option. This means the query will ignore all the documents that:

Don't have the created_time field 

Have the created_time field, but it is null

![](https://downloads.intercomcdn.com/i/o/685933971/acdf5f7083ff212311390021/image.png?expires=1741032900&signature=64965ee80fd7779bf38ba93c720e2b758f9b33b81b715d78dc1952063340d90e&req=cigiH8p9lIZeFb4f3HP0gFKd4TLfyXyxmCwh8%2BlhQU%2FWTv%2Fc4zciIGs29A7L%0AG7Q%3D%0A)

To troubleshoot this:

Check to see if your query has the Ignore Empty Filter Value Option enabled

Review your database or CMS to make sure that your documents have the field you are using on your filters.

---

### You have Ordering on your query and the field you selected as order doesn't exist or is null

If you use a field for order, and that is null or does not exist in the document, FlutterFlow will ignore that document and not load it.

In the example below, signinDate is set to be order by Increasing. 

If my list returns no documents, this means none of my documents doesn't have the signinDate field or it is null

If my list only returns 99/100 documents, this means that one document doesn't have the signinDate or it is null

![](https://downloads.intercomcdn.com/i/o/685937386/1e8cb5256019f74dc2a15305/image.png?expires=1741032900&signature=39c0094202aec2d9733d2558b1092c5ad33805abfda2920bf3be32e279a430ba&req=cigiH8p5nolZFb4f3HP0gKYhsdebsefbOFY2SlpHykUkxs%2F0BB97smbdxRS8%0ATeU%3D%0A)---

### In case of APIs returning empty results

If the APIs are working fine in test mode but do not return any data in the deployed app, mostly it is due to the CORS issue, please take a look at the browser's console to see if it shows any errors regarding CORS (check the screenshot for reference). If yes, please take a look at this article to understand and resolve the problem.

​

![](https://downloads.intercomcdn.com/i/o/787428305/ab56a319ecb98238f68194f2/SCR-20230718-ncwa.png?expires=1741032900&signature=283e5361ea510c03f5ed8f385107f1b04d32361f6fc926dfee2c4ffdc2a1acde&req=cyggEst2noFaFb4f3HP0gGTh7ovM5y87so0CuG2x0GQVrBgX6b2FaMYW%2B9Xb%0AbiQ%3D%0A)---

The issue was not resolved.

If the error still persists after following the outlined steps, please contact support via Chat or Email at support@flutterflow.io.

---