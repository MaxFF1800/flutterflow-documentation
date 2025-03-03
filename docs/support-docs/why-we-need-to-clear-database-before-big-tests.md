---
title: "Why we need to clear database before big tests?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

sometimes you add items during the test, then during development, you add more fields to a collection and you use those fields, now the problem is you do not erase your old data. and you are testing the app

the new ones are ok, but the old items, because they do not have the data for a new field, do not load properly.