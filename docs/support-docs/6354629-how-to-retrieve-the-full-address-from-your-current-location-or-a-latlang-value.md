---
title: "How to: Retrieve the full address from your current location or a latlang value."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6354629-how-to-retrieve-the-full-address-from-your-current-location-or-a-latlang-value"
hide_table_of_contents: true
---

In Flutterflow we have access to the current device location from Global properties. the retrieved data is in the Latlang data type.

we can use that data to set the location on a map, but what if we want to show a marker there?

First: if you just simply want to show a marker on the map and no need to retrieve the full address, you can save the latlang value on a document, and set that document as a single marker of the map.

But if: you want to have the full address and full data about the location. like country, city, state, street, etc

then follow the instructions.

![](https://downloads.intercomcdn.com/i/o/539486170/be4c1d7314d0576671e3f824/image.png?expires=1741032900&signature=c27475278a9d21418623ebfb12c918d073a52bad9fce24fcd1256adac4c1a083&req=cSMuEsF4nIZfFb4f3HP0gNFjp9ZXQfYejqBi%2BNNB0pTDBWFGImPWlHTcZf1w%0AWX0%3D%0A)

Project Link

Run Link

What do we need?

1- Google map API key [based on the device you need different API keys ] if you already use Google Maps in your project and set your google map API keys, you can use the same key here.

​

![](https://downloads.intercomcdn.com/i/o/539492983/dffba8c4df6376149feac7c0/image.png?expires=1741032900&signature=ac830e970c2d9dc9d10ad27f3b66d68f44f6b6ffbc87e33c75dcacd0d02b782a&req=cSMuEsB8lIlcFb4f3HP0gEAbCqRWPPPCWyT5fDDbFBxUYXMqrWOfIRNqwWiX%0AdSk%3D%0A)

If you do not know how to get your keys, follow the video or documentation in the Flutterflow/Settings/Google Maps

2- A Flutterflow project

# What do we want to do?

We want to use global properties current device location and get the user's live location, then use google geocoding API and retrieve the full information about the location, such as the full address, country, state, etc

# API call:

![](https://downloads.intercomcdn.com/i/o/539498661/356df6b0428e643f4a7716b7/image.png?expires=1741032900&signature=5abb0e071767b805088461c0f2f25f2c4375df3419792d3380d87fc15231a36e&req=cSMuEsB2m4deFb4f3HP0gJ%2FeMGaUv1tzmFlTzX6HMDDvT3xdAaLWcv23boHu%0AsWk%3D%0A)

We need to make an API call as you can see in the picture.

1: the URL of the Google geocoding service.

https://maps.googleapis.com/maps/api/geocode/json?

this URL is static and you simply can use it

at the end of the URL we have 2 parameter

 2- the location as a latlang value

 3- key, your google map API key

We provide both as string.

​

*Notice: you can use the parameters you have in your call inside brackets 

[param name] like what you can see in the picture

name the API call [ GeoCoding ] and save the call.

# Call the API:

![](https://downloads.intercomcdn.com/i/o/539510268/fed1e5486ded80ae6bd9dfb5/image.png?expires=1741032900&signature=cf1530e3b07541f8e10b538dfe35fca9fc9906282dd4a3feda9a855d7c97d2c0&req=cSMuE8h%2Bn4dXFb4f3HP0gEkzLt9UHiZIA8Aofj2fnakAZPB2vQM4VZAjO0Vc%0A9EI%3D%0A)

I want to show the full address on this page, so I do an API call on the page

Now I need to pass the parameters

1- latlang: as you remember we have a latlang parameter in our API call, but it is String, so here we need a custom function to convert our current device location from a latlang to a string and pass it to the API call.

![](https://downloads.intercomcdn.com/i/o/539512031/28562572839c666a7f0da37a/image.png?expires=1741032900&signature=6b00db134b0844197f5781a65bdd25867fbbf1867f0ebcaadea40483052c6bc5&req=cSMuE8h8nYJeFb4f3HP0gHdp79p9Z6D3LEXki72EKBtKb3SHpgJ64Js9RO5q%0AyS8%3D%0A)

This function simply takes the global properties current device location and convert it to string and will return it as a string value.

![](https://downloads.intercomcdn.com/i/o/539512767/a06bb233732a50f2cbccfc57/image.png?expires=1741032900&signature=d51e5ffd108a5b874ebf2653d7a977a9898379829d94d299cf4da65e747787c1&req=cSMuE8h8modYFb4f3HP0gJjrKrzlgwp0IijeMXyDQNPQ3tHtBEna%2B964SfVw%0Ab7E%3D%0A)

![](https://downloads.intercomcdn.com/i/o/539513017/9aa097d38a312b71dade02cf/image.png?expires=1741032900&signature=3dd37a6e0727f78013f57b3871ebbb7a820a3bf5c1899103d65eee157d009263&req=cSMuE8h9nYBYFb4f3HP0gAyGR7jarW1iErgb5Ar9J%2FTc17PQYmqRahMnJ5Il%0AMyA%3D%0A)
```
`return (latlang.latitude.toString() + ',' + latlang.longitude.toString());`
```

2- Key: your google API key, in my case I save the key on my user table, you can put it directly or do the same for security.

Now when the page loads I do the API call, and now I have access to the API call response. now what I am doing is just showing the response on the page.

you can do other things, for example, you can do the API call in an action, and then after that save the response on the database. it is up to you and your use case.

# Access to each node in the API response:

for more info about using API call responses, you can see this video

Here I want to show the full address in a text widget, you can use the same principle and retrieve any kind of data the API response provide to you

![](https://downloads.intercomcdn.com/i/o/539516308/fcc871902090c084034e5719/image.png?expires=1741032900&signature=01aebf0b9e72ce5cd68c16f1a2044f448b28f1cf56bfd548b1e3259b290bd297&req=cSMuE8h4noFXFb4f3HP0gPQT51hZpmqOroObu13bp3fPK%2FRH8Wo7hMfbcORS%0AV0s%3D%0A)

You can continue this principle to show all the data, or save them in database.

Now everywhere in your project, you can do an API call, use the current device location and retrieve the full information about the user device location.

and use the data where ever you need it.

Enjoy!