---
title: How to make a custom NavBar
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6268677-how-to-make-a-custom-navbar"
hide_table_of_contents: true
---

Why do you need a custom NavBar?

If you want to have control over the NavBar base on conditions: for example, you want to hide the navbar on the page if another widget is shown on the page.

​

If you want conditional views and conditional items: for example, You want to show two different views and items when a user is an admin, so the admin will see a totally different view of the NavBar, or maybe you want to hide an item for the admin and show him something else.

​

If you want to have more than icons and text for the item of a navBar: for example, You want to show a cart widget for an item, in case you have an e-commerce app.

And maybe some more reasons.

Things you need to know [ principles ] :

A custom navBar should be floating on the page, it should be on a Stack, and on top of all other widgets. So the page should be like this:

Page > Stack [ inf, inf ] > Container [ inf, 100px or height of navBar you need ] > NavBar component.

then in the alignment of the container, you need to put 1 for the vertical.

​
![](https://downloads.intercomcdn.com/i/o/523364917/5d8e031aa90039332ddca0be/image.png?expires=1741032900&signature=b46c12238468ac35e2718e0829d8bf1f1561bfcd60aed4eacbeddc3c4fa65184&req=cSIkFc96lIBYFb4f3HP0gDCbYIxU7TZJL1qzbOmgK8iPucbHCjoVsBZtR%2BFr%0A5L0%3D%0A)

If you have an item in the navBar [ a page ] that page should not have any back navigation, this means if a page is an item in a navBar it is the main page.

you do not put navBar in a subpage. Pop actions [ back action ] can cause confusing navigation in the app routing.

You need to control the navBar dynamic field on each page, it can be set by static values, or it can be set from the localState or database.

You need to make sure your contents on the page have bottom padding, same as navBar height, 

![](https://downloads.intercomcdn.com/i/o/523367804/ad8ba6acf4e428c31936407e/image.png?expires=1741032900&signature=4345315ee09fb6f34375c50a7755130c44a60979b229347f0e890cd6b34da7bc&req=cSIkFc95lYFbFb4f3HP0gEDszxPMqRmoqPunHOi2HiAtHkC%2FNOZY4IncNvCM%0Ah4s%3D%0A)

Here is the example of a custom navBar we made for you, so you can investigate and replicate it.

​

## Project Link

Run Mode LInk

How to use the sample project:

When you run the app, just tap on the login button, we made a test user ready so everyone can log in to the app freely.

​

![](https://downloads.intercomcdn.com/i/o/523371386/1679ebf86fd2edcbef24fec7/image.png?expires=1741032900&signature=3ffdc9eb9c366044b51518b2e909e34a588bbe07105232bfe8b915eadfd1ec89&req=cSIkFc5%2FnolZFb4f3HP0gHsk4xniMYwjjBpkZOWois1VdM8HFBmP2CG1d4hp%0ArQs%3D%0A)

On the home page:

![](https://downloads.intercomcdn.com/i/o/523373090/d1216dc8c5972155a24e59b8/image.png?expires=1741032900&signature=9a8e79ab3b4ca0008c02cabb4ddaebec3b8ae05136e18d7271d653481b983f5e&req=cSIkFc59nYhfFb4f3HP0gJU6CNNb8ly3jFTVjWFY1qcl1%2BBZ3l0Vnl5kvtdr%0AsIo%3D%0A)

You can select Custom navBar/AppBar: in the page, you will see a custom App bar and a simple custom navBar

​

You can select Conditional NavBar: on the page, you can see a conditional navBar, with admin and normal user view. there is a toggle you can use to turn is_admin in the user table ON/OFF

![](https://downloads.intercomcdn.com/i/o/523373714/9774cd0b19a29230eb895c4b/image.png?expires=1741032900&signature=93b092974e86c24d806e50d4bdc34d17806f6db747b6c05cf9be4c524e86be03&req=cSIkFc59moBbFb4f3HP0gPt46VjbLX3fOw%2FQEwOXi75eWYaVcqzxOLgTlebG%0AjkE%3D%0A)