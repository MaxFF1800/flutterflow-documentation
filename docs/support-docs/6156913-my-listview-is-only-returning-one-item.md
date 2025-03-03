---
title: My listview is only returning one item
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6156913-my-listview-is-only-returning-one-item"
hide_table_of_contents: true
---

Here are the things to check if you are facing this issue:

Make sure you are using a Listview/Gridview/Row/Column to dynamically generate the children.

Make sure your query is for a list of documents and not a single record.

If you are using a filter then make sure the data present in Firestore has more than 1 record that can pass through the filter.

Make sure that your Firestore collection has enough records.

If you are querying a single field then make sure it’s a ListType field in FlutterFlow and in Firebase.