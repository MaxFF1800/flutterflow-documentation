---
title: "Share media/files in storage, 1 user upload all users see"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

chat;https://app.intercom.com/a/apps/w66h9try/inbox/inbox/5495770/conversations/1152

solve the issue related to: when a user upload an image to firestore other users can not see the image with same params

we need to run the command to google cloud

https://cloud.google.com/storage/docs/gsutil_install

gsutil cors set cors.json gs://exampleproject.appspot.com

save file core.json in project directory

```json
[ { "origin": ["*"], "method": ["GET"], "maxAgeSeconds": 3600 } ]