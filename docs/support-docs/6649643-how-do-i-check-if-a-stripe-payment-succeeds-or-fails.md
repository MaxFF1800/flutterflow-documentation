---
title: "How do I check if a Stripe Payment succeeds or fails?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6649643-how-do-i-check-if-a-stripe-payment-succeeds-or-fails"
hide_table_of_contents: true
---

## Understanding Action Output Variables in FlutterFlow

FlutterFlow actions come with a feature that allows you to name an action output variable, which holds the return value after the action's execution. This functionality is crucial in tracking the status of operations, including payments.

​

## Default PaymentId in Stripe Actions

In the context of Stripe payments, FlutterFlow assigns a default variable named "paymentId" to the action output. This variable is instrumental in discerning the payment's status.

​

![](https://downloads.intercomcdn.com/i/o/599391734/93463315e77a79968f19eae0/image.png?expires=1741032900&signature=ef02bc562ffc7d870a0d657d844cce5896723d43c5a111c83f0e12d463b62dfd&req=cSkuFcB%2FmoJbFb4f3HP0gBRUvloRqAYqw87ABGQx2h8TpwBWlJH0lbu5RORw%0A8%2BA%3D%0A)

## 

​Checking Payment Status

When a Stripe payment action runs, the next immediate step is to verify if the "paymentId" is set and non-empty.

A non-empty "paymentId" signifies a successful transaction, as it indicates that Stripe has returned a valid identifier for the processed payment.

![](https://downloads.intercomcdn.com/i/o/599392598/e7bb1415569328a1ebc0fe46/image.png?expires=1741032900&signature=f7c5efa2b3747e8599ec2b598db0728792547bd69ca87ce5867cd70bdd064a74&req=cSkuFcB8mIhXFb4f3HP0gJRwBVsG1zcGVhv7g6MX3d8t4QsqbaiDQ2BSRQy6%0A7eY%3D%0A)![](https://downloads.intercomcdn.com/i/o/599393179/1205f90740f90b0f77484fe1/image.png?expires=1741032900&signature=f64c4c6bdd9a0cc40e443dbaaabde11ebf568e6baa3d869e31fc65a10b7b1286&req=cSkuFcB9nIZWFb4f3HP0gD8O5ZAqJjhQxT87%2FSi3Q7d2P%2BCb7QddEwVIVBZY%0Al3s%3D%0A)

## 

Subsequent Actions Based on Payment Status

Upon confirming the payment status, you can trigger the corresponding actions:

Indicating Successful Payment to Your Users:

Display a confirmation message using a snack bar.

Navigate the user to a success screen with a thank-you message.

Perform any other success-related actions such as updating the database, sending confirmation emails, etc.

Indicating Failed Payment to Your Users:

Prompt the user to attempt payment again.

Reset the payment inputs and guide the user through the payment process once more or let them try again if they want to.

Provide feedback on what might have gone wrong to improve user experience.

## Conclusion

FlutterFlow's capability to handle action outputs, particularly with payment systems like Stripe, gives developers a powerful tool to create seamless and responsive payment flows in their apps. By following the steps outlined, you can ensure that your app appropriately responds to the outcome of each Stripe payment, enhancing the user's experience.

​

![](https://downloads.intercomcdn.com/i/o/599394672/d8f4862cbc792674d72fccba/image.png?expires=1741032900&signature=b668ad1000c9c5cf5d45b981e2a99058353c9ffbca2ff6c7f2778b81d65d5205&req=cSkuFcB6m4ZdFb4f3HP0gNt%2BpIaqTSVSkj%2BJRCu61M55KBiUz6Eha4cDbUQl%0AP%2FY%3D%0A)

​

​