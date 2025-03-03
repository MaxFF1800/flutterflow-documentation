---
title: "How to: Take an email from textField [ user input ] and update the same user record?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6220372-how-to-take-an-email-from-textfield-user-input-and-update-the-same-user-record"
hide_table_of_contents: true
---

Sometimes you need to update/delete a record and the record related to the user choice. for example, you want the user to type an email address and if a user exists with that email address you want to update that user or maybe put the user reference on a document.

But how? as we do not have any action that does a query.

![](https://downloads.intercomcdn.com/i/o/513718732/1628d6c403638346864c588a/2022-05-16_13-02-52+%284%29.gif?expires=1741032900&signature=361abac0167e10f89543a0e8f98296120f993771d03dcfc10190e26de86d5259&req=cSEkEch2moJdFb4f3HP0gDzb1WQ5gbrYCTEYkqyuerzBsQ6CcMot3Qk8eEEX%0A65E%3D%0A)

Trick: we need to load the document before any action, so how?

As a pre-requisite you will need to:

Complete Firebase setup

Create a Firebase collection

Have some users documents in your database

1: We need a textField widget to take the email from the user

we need to turn on the Update page on change functionality so this way every time users type a character the page will be refreshed and we can access the value.

​

![](https://downloads.intercomcdn.com/i/o/513697006/69be6b720ec76bfb723b8d14/image.png?expires=1741032900&signature=8ac1ca0b96e850603e6c10225f6f0b95bbbc1f96cee6166588fe7abe6c4cebf6&req=cSEkEMB5nYFZFb4f3HP0gL7jIE3ueJyWultS4arPXqOysIqw%2B%2BpMugIaEu3Q%0A9%2BE%3D%0A)

2: now we need another widget to show the result and the button that we want to use to raise the action.

this widget should be hidden when we do not have any results. the query will take care of that.

so we do a single query on the widget and make sure to turn on the Hide widget if no match. simply here we are hiding the entire widget when we do not find any user with that email.

so if this widget is shown it means we find the user and we have a result on our query. now let's go for the action on the button

![](https://downloads.intercomcdn.com/i/o/513700284/f30dcfb2818fba611a4cbf06/image.png?expires=1741032900&signature=7c9dd7ea14a98c9bff90ef925f9a069faef513e3da81f4801b1de39e092a1512&req=cSEkEcl%2Bn4lbFb4f3HP0gIfEWTCI0RIiOBiHYAVr0ZmeQ1Jvm3PPB7cswxF1%0A0ww%3D%0A)

3: in the action panel, we just do an update on the query result that is a user document. and after that, we show a snack bar

![](https://downloads.intercomcdn.com/i/o/513701239/38aa3fd94becf288dc8d6fdf/image.png?expires=1741032900&signature=0ef1c65b30ac1b3bb1f6f2bc2183dc1dce560c1898134ffa8153fbb31ba0b2ac&req=cSEkEcl%2Fn4JWFb4f3HP0gNrP6e2N8A8B8ZNAPash0vnwpPzSgsP6Lu8GOCe6%0AWjY%3D%0A)

That's it.

* You can instead turn on the Update page on change for the text field. use localState and a button to set the localState value from textField. and use the localState value to filter your query.

You can open this project [ https://app.flutterflow.io/project/flutterflow-adcdi2 ] page "UpdateUser" and see how we did this. replicate the process then.

.

​