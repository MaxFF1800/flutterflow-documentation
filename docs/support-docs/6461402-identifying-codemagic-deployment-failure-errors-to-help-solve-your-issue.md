---
title: Identifying Codemagic Deployment Failure Errors to Help Solve Your Issue
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6461402-identifying-codemagic-deployment-failure-errors-to-help-solve-your-issue"
hide_table_of_contents: true
---

## How to Identify Your Codemagic Error

Press Cmd/Ctrl + k, type "deployment" and hit enter. It will take you to the deployment page.

​
![](https://downloads.intercomcdn.com/i/o/550342644/e11d9dbb7afdfcd7b5ef6564/Screenshot+2022-07-21+at+11.05.25+PM.png?expires=1741032900&signature=3798b8c2f04cf9d2460256b9f10275b2c2f67ccfec70595d758f975c1271fb29&req=cSUnFc18m4VbFb4f3HP0gE718v8zY9Q0U22IriEYqfASbEjFY2UC0L7UzXaI%0AJZs%3D%0A)

You can also navigate to the Deployment section by clicking Project Settings > Deployment (under App Settings).

​
![](https://downloads.intercomcdn.com/i/o/550384963/47f46a67591c372bbddb5acd/image.png?expires=1741032900&signature=7d99e3a0eda456b53a6716cfe93bffb76798bd0584bb634d0dcdc883b9a90928&req=cSUnFcF6lIdcFb4f3HP0gC08UOSSc7fQxqJ0p2vp8RFxDaxzg8fycz44%2FEQe%0AR88%3D%0A)

​

Click on the Failed (VIEW LOGS) text to see the logs. 

​
![](https://downloads.intercomcdn.com/i/o/561528052/ef0ee0aac52d04a849c180d1/Screenshot+2022-08-11+at+6.11.42+PM.png?expires=1741032900&signature=b5e2e76136814c13a5632b52b457881bd4a935a656a11e041285df555d078932&req=cSYmE8t2nYRdFb4f3HP0gJrNTHzW24B7Ts94a870vOfVhGl3bvNAp1yM3tNj%0Ac7Y%3D%0A)

​

In this step, you'll need to note the Failed Step that been displayed by CodeMagic 

error log. 

​
![](https://downloads.intercomcdn.com/i/o/561534016/8b3e444470a121a404a1ef94/Screenshot+2022-08-11+at+6.20.29+PM.png?expires=1741032900&signature=3d46f16ef34b421ce85f09a94855208a83d6366b55e84f36708fca760540d2ab&req=cSYmE8p6nYBZFb4f3HP0gIw7iG4ZMWut1Iwc7pByFBgEsUNYGYO5auAngtfs%0AwbI%3D%0A)

​

Now, press Cmd/Ctrl + F to search for the term "error" in the logs to find the root cause of the issue. Keep pressing "Enter" till you find the error ( this is usually at the bottom of the logs ).

Tip: Note: If you search of "error" and still don't find and error message that makes sense to you then you can also try with the following keywords:

message

![](https://downloads.intercomcdn.com/i/o/561535697/ef8542f32f679dfe02888efa/image.png?expires=1741032900&signature=01dcaab5f804a5ebbb2e8820096f3825932bcfaf27de751dca9084d32eafe8b2&req=cSYmE8p7m4hYFb4f3HP0gCCP2YSmT9DrIiGtttNUExyLaRH5io3Fh1Pugo%2F7%0AzW4%3D%0A)

Now select and copy this error message and paste it in the Help Center search in the chat icon in the bottom-right corner to search the error. This will help you find the help article for this issue and then you can find the fix for it. 

![](https://downloads.intercomcdn.com/i/o/561539274/e59672aaf172d32330d730f5/search+for+help.gif?expires=1741032900&signature=7f7e7155dc3e8b4d2bcf56b26d3a363c4921d43588549738381d1dcafc5dc2b5&req=cSYmE8p3n4ZbFb4f3HP0gERrMbnU1n4hrq56H3V%2BGHXnBPBeVevRC1ITOK9b%0Amw0%3D%0A)