---
title: "How To: Resolve 400 API Call Errors"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6366398-how-to-resolve-400-api-call-errors"
hide_table_of_contents: true
---

Standard API status codes are returned when unsuccessful API calls are made in FlutterFlow. Outlined below are some of the common responses for 400 HTTP API calls and how to solve them. 

# 400 (Bad Request) 

The server could not understand the request due to malformed syntax. The API endpoint should be modified before attempting an API call again. 

Some of the likely causes are:

1. For POST API calls, the uploaded file might be too large.

2. The accessed URL is invalid

3. Expired or invalid cookies in the browser. 

An example of the returned API call is shown in the attached image below.

![](https://flutterflow.intercom-attachments-7.com/i/o/542543282/96af81d173e3357a49054a37/VFsVUM0QssVnsgSt13hfRuBYNwHhs_60OwV2ui7gdggiAFCFr9o-d6Bfe0dxZ8fQ5d_k0uUfNMlo5FI5GjIS7GxoPbuYNGqfmStdpL1lihrnDyLeH2mJFktzfJ3PJTun2T7J2ekpsZun0FoOY-k?expires=1741032900&signature=27c4498d0f07188c214a43b2914f60b78451c4e42556aa2a3ba38a534447aa22&req=cSQlE819n4ldFb4f3HP0gEWuqXpJx%2Fq3SL1ZCWYmwXCWB2u7C2mFF6MdIMN7%0AsKw%3D%0A)

Troubleshooting Steps:

1. Clear the browser cache. 

The browser cache can be cleared by going to More tools -> Clear Browsing Data

![](https://downloads.intercomcdn.com/i/o/542540977/67259995ecc5402ebde85486/Duplicate_Ticket.gif?expires=1741032900&signature=11aa774b37f8e2d34c414171b2d87197b3d0732989ea447b2d65af13ef81a685&req=cSQlE81%2BlIZYFb4f3HP0gE4NQZBgyH3h0J2XZCuseWDCQ5e6%2FItfrFfXf5Uj%0AwG0%3D%0A)

2. Clear the browser cookies.

![](https://downloads.intercomcdn.com/i/o/542543132/4b9546bac852868b94eb1c32/Duplicate_Ticket_20.gif?expires=1741032900&signature=3dfa266598fb13f8ddccaecf98e13c066c55e4c369e837c229ac183fec5d98b1&req=cSQlE819nIJdFb4f3HP0gIyTyflwcIeXTbfJBYbz6pGpo1daccmmvE0DvQrU%0AIeg%3D%0A)

3. Check the requested URL or endpoint. (Domain names are case-sensitive). 

4. Upload smaller files