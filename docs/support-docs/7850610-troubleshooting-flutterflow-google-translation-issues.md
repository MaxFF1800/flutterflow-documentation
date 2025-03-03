---
title: Troubleshooting FlutterFlow Google Translation Issues
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7850610-troubleshooting-flutterflow-google-translation-issues"
hide_table_of_contents: true
---

FlutterFlow offers integration with Google Translation to provide your app in multiple languages. However, you might encounter issues when trying to translate elements of your app. Follow these troubleshooting steps to resolve common problems.

## Issue: Long Text Forms

---

Problem: You're trying to translate long forms of text within your project.

Solution: Remove these long text elements and translate them outside of FlutterFlow. Then, manually insert the translated text back into your project. Ensure the input field is empty when attempting to translate again.

## Issue: Special Characters

---

Problem: Your app includes special characters that are not supported by the Google Translate API.

Solution: Identify and remove or replace these special characters within your app. After making adjustments, try the translation process again.

# 

## Issue: More Than 10 Language Options

---

Solution: Limit your translation feature to 10 languages, as Google Translate currently supports only a select group of 10 languages for integration within your application.

​

# 

Solving Translation Issues

---

#### Step 1: Narrow Down the Issue

Start by identifying where the problem lies within your app. This could be a specific page, component, or even a particular text field. Pinpointing the exact location makes it easier to tackle the issue effectively.

#### Step 2: Check Chrome Developer Console

Look for any translation-related errors in the Chrome Developer Console. These errors can give you insights into what might be going wrong.

#### Step 3: Use the 'Translate All' Feature

Try out the 'Translate All' button to see at what point the translation process fails. This can help you identify any elements that may be causing translation issues.

#### Step 4: Remove and Test Text Elements

Temporarily eliminate text elements and then attempt to rerun the translation. This step is crucial for figuring out if specific texts are causing the problem. If the issue disappears upon removing the text, you might need to adjust or manually translate these elements before re-incorporating them into your project.

​

​

# Still Having Issues?

---

If the problem persists despite trying the above steps, please contact FlutterFlow Support for additional assistance. Our team is dedicated to helping you ensure that your translation process is efficient and issue-free.

​

## 

​

​