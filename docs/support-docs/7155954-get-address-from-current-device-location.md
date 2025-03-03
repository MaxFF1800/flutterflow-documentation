---
title: Get Address From Current Device Location
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7155954-get-address-from-current-device-location"
hide_table_of_contents: true
---

# Use Case

FlutterFlow enables users to get the current device location or make calls to google maps API were you can get location meta data and details. You may want to get the location name to display in your FlutterFlow project , from the current device location or from an API call. This articles details a step by step instructions on how to achieve this.

---

# Background

You can get formatted addresses from latitude and longitude in a few ways.

Using the google maps API https://maps.googleapis.com/maps/api/geocode/json?latlng=[latlang]&key=insertAPIkeyhere

Using dart package Geocoding

We'll show you step-by-step how to set this up in FlutterFlow.

---

# Sample Project

We've created a sample project to demonstrate how to build this in FlutterFlow:

https://app.flutterflow.io/project/geo-track-rvndye

Keep reading for step-by-step instructions to learn how you can build what we have created in our sample project.

---

# Using Google Maps API

To use the Google Maps API to get a user's current device location:

Visit google cloud platforms and enable Maps for your project application 
Here are detailed instructions on how to do this. Enabling the map's API
![](https://downloads.intercomcdn.com/i/o/693925422/5a00bcc7b34a71fd78d0ecbe/Untitled+design+%283%29.gif?expires=1741032900&signature=ea923441355bd95a2e52d1240d0775c3e71f225c074c877fb92ed496d1f72410&req=cikkH8t7mYNdFb4f3HP0gPHOEHO22EeW9sXu3ooDIkDZb4dhc61LyKwhs2ok%0AN40%3D%0A)

2. Add the API key to the local App State

![](https://downloads.intercomcdn.com/i/o/693931063/0558c58249fffd4764dbf272/Screenshot+2023-03-18+at+13.26.55.png?expires=1741032900&signature=b9fbfc8da1999f77ba9f76134834cceadacb872821c0cecf01a1ec8462f0afaa&req=cikkH8p%2FnYdcFb4f3HP0gP%2FoGmo3A3DQiNKHemXRUugRVwG%2BFOYWfk%2Bbv1He%0ACg4%3D%0A)

3. Set up and configure your APIs

- Navigate to API calls

- Create an API call 

- Ensure you add the base URL and set the request method to Get

- Under the variables section, create 

- create a variable name that latlng, set the data type to a string

- create another variable name it apiKey, and set the data type to string

![](https://downloads.intercomcdn.com/i/o/693930392/edb1794091a10de62752567e/Screenshot+2023-03-18+at+13.24.45.png?expires=1741032900&signature=b0bcf30ee9cdb506f6fbf2813b6aeb99ef7951d5d91ecdd83a3319e1fdb471f5&req=cikkH8p%2BnohdFb4f3HP0gGl23RsinDZgHY6ZXu%2Fmju1wgodpTjI%2F6uOetjdp%0AS7o%3D%0A)

Here are detailed instructions on how to do this.

- Creating API Call

- Adding API call query 

4. Create A Custom Function To Convert The Device Location To A String

To convert the current device location from global properties to string, create a custom function that will return a string.

The custom functions take one parameter of type LatLng which is the type of the current device location.

This Custom function will return a string of latitude and longitude to be passed to our API variables.

![](https://downloads.intercomcdn.com/i/o/693435342/c2d81cec2d28ccf4ad6e82ee/Screenshot+2023-03-17+at+16.30.58.png?expires=1741032900&signature=da55d5315ce8e96cf4fc546df3c3194297651bb6dfdb4cae5fee90c22e5933ac&req=cikkEsp7noVdFb4f3HP0gNMzk7AiVRMUaJR4gTEBnuF4Zq1ME3bl3ILFDBBQ%0Ak24%3D%0A)

In the UI builder create a button and set an action the performs a backend call

5. Head back to API's run and test if the API is working well.

From the result create a JSON path.JSON path makes it possible to retrieve specific data out of the whole JSON response.

![](https://downloads.intercomcdn.com/i/o/693943421/70a837524a1c29e1bdab7188/Untitled+design+%282%29.gif?expires=1741032900&signature=87c48ba5e25b6389fcb70626eae98e94725525902bc159a9e80594551ae3dd76&req=cikkH819mYNeFb4f3HP0gD%2Fx2lyR2T9nRpNfoDhWrrgyQyUijobVzMaNZUhH%0Ak0E%3D%0A)

5. You can now show the City name in the UI builder by passing the JSON Path as a variable to the text. 

To target a specific data we will pass array index of the long name to the json path

$.results[0].address_components[1].long_name

Head to JSON paths to get more detailed instructions on how to create JSON paths.

![](https://downloads.intercomcdn.com/i/o/693422179/143ea74c50a5799b7c6eb91d/Screenshot+2023-03-17+at+16.14.58.png?expires=1741032900&signature=6fd97b75f0035320c68ecfc18f5ba5ea555b1639313950db8572c9391aa4683f&req=cikkEst8nIZWFb4f3HP0gAq%2F4%2BWbWCIgJz0GDmEOT1CeK2ucar7CiaC4koVS%0A6Xw%3D%0A)

You should have such results.

![](https://downloads.intercomcdn.com/i/o/693425889/e5d09c88452a22e3bf61a0e8/Screenshot+2023-03-17+at+16.19.42.png?expires=1741032900&signature=f640257cf0336f8cc8f1ab55acc938021d62ddea853d7cd858535c33df01b1e6&req=cikkEst7lYlWFb4f3HP0gLbntkt%2FDpMOls3AWPYi6ryQ002f3GbCvrRfJHuO%0AQOM%3D%0A)

# Using the Geocoding package

You also can use a custom action that receives the user's current device location from the global properties as parameters and relies on a dart plugin like (geocoding) to convert the coordinates to the city name. 

Here is a sample of the custom action. 

![](https://downloads.intercomcdn.com/i/o/693210386/04e1cb5af77768f991908bbe/Screenshot+2023-03-17+at+10.59.01.png?expires=1741032900&signature=f2a0467d07ea7e4f64176126a057e62ffaa6c272b18e68c0f242dddd913aa23f&req=cikkFMh%2BnolZFb4f3HP0gCFkxqrCJVAGFi6o5mHj7sugJXdBXD%2F4RXKVJQ0p%0AI5I%3D%0A)

Set the text variable from the custom action and pass the current device location.

​

![](https://downloads.intercomcdn.com/i/o/693444311/a8b3f55e0ba159b99f9dcc0d/Screenshot+2023-03-17+at+16.40.58.png?expires=1741032900&signature=f898e160c82074dea2e0a425bb747b0188c252ad3e243609e6189ac18f2bf14f&req=cikkEs16noBeFb4f3HP0gDVyl1RKG2D5EaWYLOxklJLmRfOjvdHtq59z6%2B5d%0A4K8%3D%0A)

To learn more about adding dependencies to your FlutterFlow project, read this article https://intercom.help/flutterflow/en/articles/7152626-adding-dependencies-in-pubspec-yaml-file-for-entire-project .