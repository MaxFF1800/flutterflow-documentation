---
title: "Backend call: Update Document action is not working!"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7053492-backend-call-update-document-action-is-not-working"
hide_table_of_contents: true
---

![](https://downloads.intercomcdn.com/i/o/685868394/c3878910c4b74177c99c7696/image.png?expires=1741032900&signature=8f34653978605251fc8c4736c2928993227e5a5a9a91e2c2766e5b57cdaed712&req=cigiHs92nohbFb4f3HP0gJ%2BWh9kTNpkTWaZOvoJkvz0SZxH8YVXk88dPm22p%0A4Vw%3D%0A)

Note: Make sure after performing the update action you check the data in the database. sometimes when you don't have a stream on the document you edited, you can't see the updated data in real-time in the app.

So it's important you check the data in CMS or Firebase/Database before moving forward.

​

![](https://downloads.intercomcdn.com/i/o/685873268/882b768f202139e73a567257/2023-03-07_16-49-06+%281%29.gif?expires=1741032900&signature=5cb582109d45c63778ff964346ccacf797f0906224ce1717a8d03bc8d7d5a063&req=cigiHs59n4dXFb4f3HP0gBxwLrY9xm%2F%2B%2FAPmmtECrBea0izY8ttp1psYrNpZ%0ACK4%3D%0A)

When you perform the update action, the loading indicator will be displayed and shortly after will stop. it means the update wasn't successful. 

If it was based on my action flow I should see an alert dialog.

​

![](https://downloads.intercomcdn.com/i/o/685877372/92f6f65dd4a3eac168d1b0aa/image.png?expires=1741032900&signature=d2fb53d91662de0936819822c21cec93b711ce0fd0f508a4f8c45df1f89ffcbc&req=cigiHs55noZdFb4f3HP0gHdSaua%2BwJaNIES47mntvNxQggGGUtSaIsqEqV6S%0AVrw%3D%0A)

Why is this happening?

When the upload action fails, the action flow will break and cause the next actions to not be executed.

Why does the Update action fail?

There could be 2 major reasons

1- the user doesn't have permission to perform the writing on the document. it is a firestore database permission issue

​

![](https://downloads.intercomcdn.com/i/o/685880803/a40c63fed0b51ce69f6dd2c3/image.png?expires=1741032900&signature=99cb233453768f5d4756984b9036daca484f78b35515eb9c9af22b5ad72696ae&req=cigiHsF%2BlYFcFb4f3HP0gLbFXnVesjavOkufC6Q2t2zoWTmbgjxi%2BcLf%2BuBZ%0AiKA%3D%0A)

Based on my user's collection permissions noOne has the right to write [ edit ] the user documents. So when I perform the update action it fails.

Solution: Make sure you set the write permission correctly, for example, Authenticated users rule is good enough to move forward if you have logged in user.

 

2- The values you try to set to fields on the document have issues.

For example, you try to set a null value to a field or try to set an integer field with a string value.

![](https://downloads.intercomcdn.com/i/o/685882934/527af68aad22203518a7eead/image.png?expires=1741032900&signature=2b3ab93ecea4106a645612c87b55231e82b90d1e4bd9aa802797cf23350b2bfd&req=cigiHsF8lIJbFb4f3HP0gPAWTGHZyg8DJDTz25PITfrkIXBMFETKDwhd3ZWl%0AzIE%3D%0A)

Based on this, I am trying to set a string value from a text field type text to an integer type field.

Solution: Make sure you are setting the right types. If you are not sure or your data came from an API call you can use custom actions to convert the value to the field type you try to set to.

Note: If you want to save a text field value as a number the text field type should be set to Number.

Note: You can check the console logs in your browser developer console [ F12 ] to see the error as well. For example in this picture,e you can see the permission issue error.

​

![](https://downloads.intercomcdn.com/i/o/685893252/46cc36191053d2bf7bcc4510/image.png?expires=1741032900&signature=0b9c5807bb11f8934b14120048f0ae39ab6569e149e439aa8c8bec1c5b284d4e&req=cigiHsB9n4RdFb4f3HP0gPjVFb%2F%2Bo4qllJoEP0NAAeNvqJJdalYXXZvw8U1V%0A43Y%3D%0A)