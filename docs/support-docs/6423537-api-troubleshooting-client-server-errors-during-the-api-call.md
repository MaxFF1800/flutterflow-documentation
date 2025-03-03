---
title: "API Troubleshooting, Client-Server Errors during the API call"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6423537-api-troubleshooting-client-server-errors-during-the-api-call"
hide_table_of_contents: true
---

# Application programming interfaces (APIs)

Simply APIs exist to let 2 programs talk to each other and transfer data.

An API call is the process of a client application submitting a request to an API and that API retrieving the requested data from the external server or program and delivering it back to the client.

Error Status Codes When Building APIs

1: Client-Side Status Codes

404 Not Found

This is by far the most common HTTP status code you can get. It indicates that the URL you used in your request doesn’t exist on the API server or origin server. While this is a 4XX error, which usually means something on the client-side is wrong, this can also indicate a server problem. Sometimes API URL paths change after a version update, but sometimes they change because something on the server went wrong.

The best course of action is to check if you have a typo in your client code before checking if the API has issues.

In this picture, I have a typo in my URL and I get the 404 error code.

​

![](https://downloads.intercomcdn.com/i/o/560718079/967e1bd9fe5c861ff2a34457/image.png?expires=1741032900&signature=19d759fd194faadad1ba876d242e1b176df99e8d58953fdf6605717295013d07&req=cSYnEch2nYZWFb4f3HP0gMlCSnLY6rH53d0x1%2FcH4rJT4DIjl32YauSb1ujC%0AjeY%3D%0A)

401 Unauthorized

This status code means you haven’t yet authenticated against the API. The API doesn’t know who you are and it won’t serve you.

For most APIs you need to sign up and get an API key. This key is then used inside an HTTP header field when you send a request, telling the API who you are.

This http status code is similar to the less common 407 Proxy Authentication Required, which means you haven’t authenticated with the proxy.

​

![](https://downloads.intercomcdn.com/i/o/560728048/a692b0396b47684c3728c0d0/image.png?expires=1741032900&signature=976e564d4ab984680c8ca02b03404f43727758ca570d6dc6a89693384b894c82&req=cSYnEct2nYVXFb4f3HP0gCXaCVzdgY2z43DBRYAWAc6n5BXMgQH8MhM%2BGvfe%0Az2Q%3D%0A)

403 Forbidden

The forbidden status indicates that you don’t have permission to request that URL. You’re authenticated, but the user or role you’re authenticated for isn’t permitted to make the API request.

This also occurs when you have an authentication issue, like when using the wrong API key or trying to access features your subscription plan doesn’t allow for.

![](https://downloads.intercomcdn.com/i/o/560735762/5e153ba90991ce2ffb36d219/image.png?expires=1741032900&signature=f9abccb2c2883259ad48deb77dd585cc314b1a975f9b35c5f288cf2d1f5386be&req=cSYnEcp7moddFb4f3HP0gBotuLosh8ptXiMYKTZcOJkluw%2FVpT%2F9lumDnft5%0ALhg%3D%0A)

400 Bad Request

The 400 Bad Request error message is one of the most generic HTTP status codes. It implies that you did not correctly format your API request. If no additional error information is given in the response body, you have to check the docs. You could be missing a query, a field in the request body, or a header field could be wrong. It could also be that some of your request data might have incorrect syntax.

This is different from the 422 Unprocessable Entity error message, which appears when your request is correctly formatted, but cannot be processed.

in this case, I pass a bad formatted latlang value to the API [ the correct one was: 40.714224,73.961452 } and I missed a single " , " in the field.

​

![](https://downloads.intercomcdn.com/i/o/560737119/59cf46ed7fe8b70bf6607001/image.png?expires=1741032900&signature=bffa1bfe19bbbbef5d3738bdf7edc9266cfece5140ed10cb31b4c4cfda19905a&req=cSYnEcp5nIBWFb4f3HP0gErYswl8GvvpNS9wJqv4IAWYsruLmpbscO2wb2A2%0A3kA%3D%0A)

429 Too Many Requests

Most API subscription plans have limits — the cheaper the plan, the fewer requests per second are allowed for your API key.

If you’re sending too many requests in a short amount of time, consider throttling them in your client. This response can also indicate that you hit a daily, weekly, or monthly limit on your account. Without implementing API analytics, it’s possible to reach these limits without receiving a push notification or email alert.

​

Sometimes an API sounds like a right fit until you see the limits, and suddenly it doesn’t work for your use case anymore. Check what’s part of your API subscription before integrating, otherwise, you may run into problems weeks or months after integrating the API.

2: Server-Side Status Codes

Sometimes you set up your server-side API and then it is matter you check these errors to be able to fix them

500 Internal Server Error

This HTTP status code can mean anything really, but it usually indicates the API server crashed. It could have been caused by something related to your API call.

Double-check the docs to make sure you did everything right: query fields, body fields, headers, and format.

If that didn’t fix the problem, it might also have been related to an API update that introduced buggy code, or data the API loaded from an upstream service. In that case, your only cause of action is contacting the API’s support.

​

![500 Internal Server Error upon entering module configuration page FAQ. Best tools for PrestaShop ➜ MyPrestaModules.com](https://flutterflow.intercom-attachments-1.com/i/o/560807281/0c34e32261a2cca76eeff7ed/500.png?expires=1741032900&signature=c9bcbde593cc0bf48f770b39cf603b235bef66aa3ab0fbc8dcd33c465d7cbd92&req=cSYnHsl5n4leFb4f3HP0gK7s%2BS81ki4zHG4Uv5lFw149XSk8eyIwZ0FU59ot%0ADso%3D%0A)

502 Bad Gateway

This response tells you that the server you were calling wasn’t the actual API server, but a gateway or proxy. The proxy server tries to call the API server in your name. This error response also indicates that the API server didn’t answer. This could be related to a network problem, or simply because the API server crashed, or was down for maintenance.

A “bad gateway” error is usually temporary and should be solved by the API provider, but you have to contact support if it persists.

​

![How to Fix the 502 Bad Gateway Error in WordPress | Elegant Themes Blog](https://flutterflow.intercom-attachments-1.com/i/o/560807291/b5b0283d2ff62dd238670bf8/bad-gateway-example.png?expires=1741032900&signature=14dd5df9f5161ac11a461dbbe9a64194d663dd818085accf113b49ceb7a3fdbe&req=cSYnHsl5n4heFb4f3HP0gC5MtlzWR154ljt0W7O2546UtNttQ9J4W5DqqzDC%0A1r8%3D%0A)

503 Service Unavailable

The 503 Service Unavailable Status indicates a server error. Too many API requests were sent and now the API can’t handle any more of them. This problem solves itself when clients send fewer future requests, but it could also mean that the API provider didn’t plan enough resources for all of its customers.

If it fits your use case, you can make your client more resilient to this error by waiting to send another request. But if the error code keeps showing up, you have to contact the API provider.

​

![503 Service Unavailable Error Explained - Crazy Domains Support](https://flutterflow.intercom-attachments-7.com/i/o/560807313/6233b60b69d97e35e53728bb/503-service-unavailable-error-explained?expires=1741032900&signature=1780b9f5dece68501a244ff3ff947a3f1e4a4092bc2459ec45535d67ff5fcdb0&req=cSYnHsl5noBcFb4f3HP0gLkwPmaCBvUjMYvAShSuFqiPAU7y%2BByuAPgOkg9u%0AEPM%3D%0A)

504 Gateway Timed Out

Like the 502 Bad Gateway status, this response code tells you that the server you were calling is a proxy for the real API server. This time, the problem is the API server’s slow response.

This could be related to high network latency between the proxy and the API server. It could also mean that the API server takes too long to process your request.

To solve this problem, check if your request’s content could be related to that timeout. If you are requesting too much data or a calculation that takes too long, you should try and reduce it.

If you think your request is reasonable and the status doesn’t go away, contact support.

​

![How to reload a page if 504 gateway timeout error appears anytime in an automated process on Python? Selenium related - Stack Overflow](https://flutterflow.intercom-attachments-1.com/i/o/560807319/83748133e940ebaed001409f/CS0ln.png?expires=1741032900&signature=aab98fe38290c2693c528e53afda223f3d1cdcbbb31178698cbb8227ed50868d&req=cSYnHsl5noBWFb4f3HP0gLJjXFXTSYg5vjx13ZfcNUzRaJEYglBg8KmOA%2FS1%0Acf0%3D%0A)

501 Not Implemented

The 501 Not Implemented status code is related to the HTTP method you used to request an URL. You can try a different HTTP method to make the request.

Usually, an HTTP request with an inappropriate method simply results in a 404 not found status. A not-implemented status implies that the method isn’t implemented “yet.” The API creator can use this status to tell the clients that this method will be available to them in future requests.

​

![How to Fix the HTTP 501 Not Implemented Error](https://flutterflow.intercom-attachments-1.com/i/o/560807323/20215c4ec3981daf5e777975/501-not-implemented-error-nginx-2.png?expires=1741032900&signature=4a82ba4a9abce7b7d4c631ff93b81e8859167dbea12d757f8f683643ba352a54&req=cSYnHsl5noNcFb4f3HP0gBYkLNd%2BZYGN0JOEh74LX23o0NcHGdHW94p7KgGQ%0ACtk%3D%0A)

Undoubtedly you’ll see many error codes when using APIs, but most have reasonable fixes. Some are related to server errors and some to client-side errors, where often one can cause the other.

Always try to read the docs and API notes thoroughly, so you don’t forget something while integrating. If things are simply broken, contact the API provider.

In some cases, the API provider won’t ever fix an issue for an API consumer. If you’re using a popular API you can also search the web for answers, especially StackOverflow, to find a fix for your error responses. Stay determined, and you’ll see your 200 ok status codes in no time.