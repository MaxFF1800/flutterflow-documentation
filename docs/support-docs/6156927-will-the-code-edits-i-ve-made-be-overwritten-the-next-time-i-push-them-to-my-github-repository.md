---
title: "Will the code edits I've made be overwritten the next time I push them to my GitHub repository?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6156927-will-the-code-edits-i-ve-made-be-overwritten-the-next-time-i-push-them-to-my-github-repository"
hide_table_of_contents: true
---

FlutterFlow pushes any changes to a branch called "flutterflow". You should not make any direct changes to the flutterflow branch. Instead, you should create a separate branch for local modifications.

Here's an example of how to do this:

Push from FlutterFlow to Github - this places the code in the flutterflow branch.

Bring the FlutterFlow project into your main branch.

Make any local modifications there in the main branch.

Next time you push from FlutterFlow, it will overwrite the flutterflow branch.

Now, you can merge the flutterflow branch onto the main branch, and choose what changes to keep and what to discard.