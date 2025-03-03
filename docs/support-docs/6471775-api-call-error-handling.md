---
title: "API Call Error Handling."
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6471775-api-call-error-handling"
hide_table_of_contents: true
---

Why do we need error handling?

​

![](https://downloads.intercomcdn.com/i/o/563225657/13ecd35bef53623529f113a5/2022-08-15_15-34-18+%281%29.gif?expires=1741032900&signature=98ec887dd41fe6a74dc56aae3615ff88de574fdf88c680e2b41d1680b55f68d5&req=cSYkFMt7m4RYFb4f3HP0gJ%2BogeAjbzKLwyYkoveBREDrQdyQi9InOM3LNG6K%0AFZI%3D%0A)

1: We need to know whether the API call was successful or not

2: If the API call was successful, is the response valid or not

## 
3: if the API call fails, what is the error code [ for troubleshooting ]

We need the error code, in case the API call fails, so we can find out where is the issue.

Let's set up an API call throw the actions [ the principles for the API calls in the UI are the same ]

1: Add an API call action. 

Notice: when you make an API call action make sure you write a name for the action output variable, this way we can access the result of the API call throw the action output.

​

![](https://downloads.intercomcdn.com/i/o/563173362/ccdd234d2f2446bcef439efc/image.png?expires=1741032900&signature=195b56979cd5f8d877d8f6edb1cda44f9ffd4359bf80b0db88c88a7402ade357&req=cSYkF859noddFb4f3HP0gCr%2F8mPQCCfmS%2BKT1r1q62z4Ek2BSDNhUZY1zizt%0AcJc%3D%0A)

In general, if you want to be a silly developer, you can leave this here, and just use the result.

But the point is, this works only when API calls success and there is some data to use.

But what if the API call fails? yes, this is the exact time we need to handle the errors and check the API call situation before using the response.

​

## 

2: Add a conditional action

We need to check the API call status if it is a success or not.

![](https://downloads.intercomcdn.com/i/o/563174975/649c8857f0008a3f0ec6daf7/image.png?expires=1741032900&signature=2765796019fb0f8cb13f95ecac979ca2de08bbf4d18f7706b7f796d6d6927728&req=cSYkF856lIZaFb4f3HP0gByZHp%2BiMMeuw58PThA1uLI%2BOYbKHqqpxg9QTAVw%0AJsE%3D%0A)

After we select the result [ the output variable of the call ] we have access to a boolean type variable name Succeeded. this variable is true if the API was successful.

this is the easiest way to find out whether our call was successful or not

![](https://downloads.intercomcdn.com/i/o/563175595/7aa4a52e30bf550ba0bc87f9/image.png?expires=1741032900&signature=09d611e292726a4764181d6ea23fd556442ed7d16616e7451645b9e9318ec54e&req=cSYkF857mIhaFb4f3HP0gBqpgFSqHdNj25zb%2FJqZbYViQjxPQZQ9MYyhSQJs%0ABys%3D%0A)

Notice: if after an API call you want to search for a specific error code, then you can choose the condition and then select the status code.

for example, if I want to check the status code of the API is 400 or not, I can do this:

* sometimes we want to do something specific when a status code was there

![](https://downloads.intercomcdn.com/i/o/563177531/d5ad564b8a8bd5a172b3103f/image.png?expires=1741032900&signature=f51f720e1f857bd676567ab07b04e703287e36027005ea79b3190db5df590d2c&req=cSYkF855mIJeFb4f3HP0gC1WXHnFTtHKUhJLSc51dCkASErLa2l2yk%2Bm%2FEZH%0A%2FnQ%3D%0A)

![](https://downloads.intercomcdn.com/i/o/563177749/f047d85ccb0f5efd802dbd45/image.png?expires=1741032900&signature=e38378218ca9a5d02677a95c779cbd89ea34dd51307c6c09e40eb405a0ced1cf&req=cSYkF855moVWFb4f3HP0gD6awtJZ7HR503BQWtVhXjBagAs0AMjIwkQ47vNp%0AoCg%3D%0A)

in this article, we check the boolean field Succeeded, and based on this we continue

​

## 

3: add the action for when the call fails.

now we show a snack bar and the message we want to show is the error code, simply now if the API call fails, we can see the error code.

you can use combine text and show more data or some static texts, or you can show alert dialogs or even navigate to another page, the action after success or failure is up to you and your logic.

![](https://downloads.intercomcdn.com/i/o/563179873/c3144a6402d95235838ea907/image.png?expires=1741032900&signature=0414898b8f1ab21493d8dfea3dccb246da38abe393e2025a8534b81292956b0f&req=cSYkF853lYZcFb4f3HP0gN6%2B4U1pNo3WfReY3ZNU%2F0ofJwsk1dhN9GfjinSD%0ABUc%3D%0A)

Ok, Do you think we are done?? NO. why?

some times even when our call was successful, the response body is not what we expected.

for example here. I try to retrieve my full address from geoCoding google API.

when I give it the wrong KEY, the API call is a success but the response is not a valid response, it is a failure response.

so in my case, a success call is like this picture:

![](https://downloads.intercomcdn.com/i/o/563182681/4b6cf13be5b1bdfb094d1b7e/image.png?expires=1741032900&signature=e565b76280af7b2f59381b4af62ec843f1b27d9aa1ef41c3f174cb233b099cfb&req=cSYkF8F8m4leFb4f3HP0gLr4W7PKBjPgETZHI3VTsiIMGiZxhXL0H9c0fO%2BG%0Aa%2Bo%3D%0A)

But now, a success call with no valid data is like this:

![](https://downloads.intercomcdn.com/i/o/563183303/32da1db485399edf839c6f9e/image.png?expires=1741032900&signature=48b68aa109c9f4d4ffd19d8743ebb51642168107d19ad52525fffeaa409b301b&req=cSYkF8F9noFcFb4f3HP0gNh97%2BrHAoVIJ1%2FstiEb2iaGhG7%2FZXS49I9E4KID%0AwWQ%3D%0A)

As you can see, the status is code 200, and it is a success, but we don't have a valid response here, and if I use the custom path I have, it will show NULL in my app, and I wonder why?

So for better logic, it is better we check the response body data before using it.

*Notice: this depends on the API servers you are calling them, so maybe you don't need to do this, but in most cases, it helps you save time and reduce the debug sessions.

​

## 

4: Check whether the response is valid data or not

this part is a bit tricky and can be done base on the response data you will get from each API call, but most of the time we can check one of our custom oaths.

for example here, I will check whether my custom path is null or not

in my API call, I have a custom path for the full address, and I want to check this path, after the success call, if this field is not null, then means the call has a valid response

​

*Notice: based on your API call and your response you can check all the responses, or check the response in a custom function and search for specific data.

​

![](https://downloads.intercomcdn.com/i/o/563190752/9eb17abb2a43be930781d9a5/image.png?expires=1741032900&signature=afbea180922cc3091b368296e1c5b6e7bdc214a69e1bece68bf60207fb1fd714&req=cSYkF8B%2BmoRdFb4f3HP0gLXUzkK5rkHsUF4HXI4faVjmCPXDcC6AITs4pFQd%0ANdU%3D%0A)

And this is the conditional action

​

![](https://downloads.intercomcdn.com/i/o/563192201/fff9aa4c0d0468a9fe7554b6/image.png?expires=1741032900&signature=27ff63573c78cea56cd1be585f0c0405477cf5fe666a7c8a57771733a0da32c7&req=cSYkF8B8n4FeFb4f3HP0gJZCisu2iqtiU2AnWPonB0lZWTxcR5d1EP9KDu4l%0AXU8%3D%0A)

I chose the custom path I have, here is the full address, and then use the powerful set or not set in Flutterflow.

I say, if this JSON path is set, then do: here I show my full address in a snack bar.

On the other hand, when is not set, I show the whole response body in a snack bar, so I can see the response.

​

*Notice most of the time in this situation, we can see the error code and error message in the response, so printing the error message can help us to know what is happening.

​

![](https://downloads.intercomcdn.com/i/o/563194396/ea8762407c6536a656774e77/image.png?expires=1741032900&signature=c1349e586f30ad4ec32a1fa048ab1edbdd274398833f292f7477a2adf0b38b8d&req=cSYkF8B6nohZFb4f3HP0gFE7qzujcne2DAsh9K%2FJgtZn%2B3RIZQgzD7kBJcej%0AHxw%3D%0A)

## FINAL:

now let's see our action flow.

​

![](https://downloads.intercomcdn.com/i/o/563195951/ef8cdfed8cfdcb216ec13a19/image.png?expires=1741032900&signature=867d8b33f19909b2feabf21b3ac50b4344d13c455485551552bb8e3fc4a70eb6&req=cSYkF8B7lIReFb4f3HP0gHhE38kCg5IeD86ZMdjKh%2F428CC4StvZtWPDLdQe%0AWGE%3D%0A)

This is a simple flow, but the point is, with this, nothing can happen that we don't expect it.

and now we are sure in any condition, we know how to deal with the data and situation, so we can properly show the best possible UI to the user.

Here I made an example. 

we have 3 separate API calls

1: Fail call

2: success call, but not a valid response

3: Success call with a valid response

Run Link for this example

![](https://downloads.intercomcdn.com/i/o/563197308/4164308309233eb06156cd39/image.png?expires=1741032900&signature=c29ee05f1e3e85e95918b4bc3aa87d6ad5fe24ca4ef955c276df7c4383e341e1&req=cSYkF8B5noFXFb4f3HP0gBPZcMkiPBG8cYFLDqe3gBPOkXM1Qo7QB%2BAN6OSK%0ALiM%3D%0A)

Here is what happens in each call

![](https://downloads.intercomcdn.com/i/o/563198413/116e33032d40ef55fcc45ecb/image.png?expires=1741032900&signature=803c9861124c9709fba200094e1c4807702672bdc1b0164029152e8e2a570870&req=cSYkF8B2mYBcFb4f3HP0gKOQt7c%2B%2F0dUnPOZSmNo3HWMOQ4UGh2Bm%2FUFZ3DL%0A3LI%3D%0A)

Now we know that API fails and our error code is 400

Now you can do research on error codes and find the cause.

Here is our article about error codes 

​

![](https://downloads.intercomcdn.com/i/o/563199494/9f62e45981a9ee3fa7330bd9/image.png?expires=1741032900&signature=5dc433355118638d7e461642b0711874816e9f1a4372da1a64bca8194d023544&req=cSYkF8B3mYhbFb4f3HP0gF4M%2FjSDXBiYx%2Fw5ECCcm1p%2F2E4MzNHpSItfluc3%0ACpg%3D%0A)

Now the second situation: call is a success but the custom path [ full address ] is not set means it is empty.

i print the response now I can see it and the message is "REQUEST_DENIED"

Now I can search for the request denied error message to find out where I fail.

And the last one is my successful call

![](https://downloads.intercomcdn.com/i/o/563200679/90e4433f1e9d7409514933ac/image.png?expires=1741032900&signature=250554ce1980855b77ede9cf37b3d5bd879896ffdd8f0dc1f6f503508d21a4ad&req=cSYkFMl%2Bm4ZWFb4f3HP0gHnFTd3Pbthth0f%2F0C985ltMKZNNVyx0eeIDVlOp%0AyOk%3D%0A)

Now my call is successful and my custom path is not null, so with peace of mind I can use my custom path and show my full address.

This is a safe way to deal with an API call. with peace of mind. Enjoy!

![](https://downloads.intercomcdn.com/i/o/563225360/c480f45c8c09cddde22b8171/2022-08-15_15-33-14+%281%29.gif?expires=1741032900&signature=24a82de63a409bb393c1474f2f1f74b7150008161b5671fe4cddf6028c697470&req=cSYkFMt7nodfFb4f3HP0gFOodsXAOSimFzAbNVusJw56J9MDi48%2Bw3P8Orcm%0Acyk%3D%0A)