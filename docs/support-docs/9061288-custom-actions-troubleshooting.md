---
title: Custom Actions Troubleshooting
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9061288-custom-actions-troubleshooting"
hide_table_of_contents: true
---

At times, the pre-built actions provided by FlutterFlow might not suffice to your specific needs. In such cases, you may often turn to custom actions, a flexible and powerful feature, to create the functionality you desire. 

​

Basic checks should always be performed, but debugging custom code actions can be difficult due to the varying complexity of the code. Some errors may be complex logical issues, while others may be simple syntax errors. A custom strategy may be required when dealing with these types of errors. 

## Let's Fix These Errors!

It's important to read the error message that is printed, whether you're running the code in test mode, compiling, or trying to compile locally. 

⚠️ The message often provides a clue about the potential issue. ⚠️

## Does the name in the action match the custom action within the actual code?

---
![](https://downloads.intercomcdn.com/i/o/989387741/f540ed078dfc3af872548352/image.png?expires=1741032900&signature=c5698020535cb87a49d2d86a3d232e10b07943a28fbe1fe97ff8b249e7ff0aff&req=fSguFcF5moVeFb4f3HP0gAQ0IUOQuiosnsqAzY47vExwAnGzFDCDxggEUxlZ%0ANAc%3D%0A)

If this is the error you are having, you a lucky one! This can be simply fixed by making sure the names match in the action name and within your custom action main code declaration.

You Can always also use the “Add BoilerPlate Code” option to add pre-made FlutterFlow code which generates with the current action name.

![](https://downloads.intercomcdn.com/i/o/989388166/be237a278dbc610c60e99d4a/image.png)

## Do all the imports match the declared imports in the action settings? Are all arguments passed within the builder itself?

---
![](https://downloads.intercomcdn.com/i/o/989389597/b6b51518d55ef2265724a74d/image.png?expires=1741032900&signature=35a197a9230cd54aa40fee45937485ccd2e24341b222993f69bbb30c23c1ef21&req=fSguFcF3mIhYFb4f3HP0gH%2BHNOmk33UwIOewQRNpejBz1pTwx4LhOJjr4p12%0ADnY%3D%0A)

You take a look at your custom code action and something is off? Some arguments are missing while others look different? As we see within our example custom action argument, 1 is missing a definition within the settings panel argument 2 is perfectly imported while argument 3 has nullable selected while it's not specified as nullable within the custom code.

There is two ways to fix this:

Go in and manually replace your arguments and make sure everything matches up within the settings panel and your actual code.

Add BoilerPlate Code option, on web you can copy only the part you need, but on native desktop apps it will replace all the code for you, and you may need to copy some code to your clipboard.

![](https://downloads.intercomcdn.com/i/o/989391205/023373e01cc3e6c1e56fe712/MathchingImports.gif?expires=1741032900&signature=22e1efc23d22e4ec33f493594a034d2560e380e332d4238574be63d44b7cca87&req=fSguFcB%2Fn4FaFb4f3HP0gAjCs30NO%2F0PdGXV76SRKoCOcoiExDIIIVBusjQW%0A5HQ%3D%0A)

## Is the name of the main action the same as any of the arguments?

---

Using the same name for the custom action and arguments can occasionally cause issues. Therefore, it's suggested to use different names for the action and arguments.

![](https://downloads.intercomcdn.com/i/o/989392183/7329e6d7e5baa4bc37f0c431/image.png?expires=1741032900&signature=279cb5526fb377df8a9e1d544e09f3731a73c61e7bb0aec0ccf039e23160da8f&req=fSguFcB8nIlcFb4f3HP0gI4DxKa679rJ3uHNZ8rj66EOi%2F3eNbQC%2B8Uz2PmV%0AqS4%3D%0A)

## Do the names of the arguments avoid conflict with any of Dart's / Flutter's reserved names?

---

Some variable names are reserved by the Dart/Flutter programming language.

Exampels: abstract, else, import, show, as, enum, in, static, this

![](https://downloads.intercomcdn.com/i/o/989392766/f6eb0cbf28bac5f827eaf0c7/image.png)

The FlutterFlow builder should automatically warn you about these keywords but some may not be caught so its always a good practise to double check.

## Does the custom action return the correct data type?

---

Custom actions often return values as part of their process. Occasionally, these actions may need adjustment. For instance, you might be returning the wrong type of data, or the returned value doesn't match the one defined in the action settings. It's crucial to ensure these all correspond to one variable type.

![](https://downloads.intercomcdn.com/i/o/989399943/fe81dcbf85305c9ef525c225/image.png?expires=1741032900&signature=e203f997ae6afaf32f9ecde260809dac438b704c25585e448342a3266eb8d226&req=fSguFcB3lIVcFb4f3HP0gA3mq%2B5minS1sTXDkZSDRheXSsKNObR4ONJ9BA2s%0ARZo%3D%0A)
Consider it this way: in the settings menu, you define the type of value to be returned. In the code, your action should reflect that defined value type. Ultimately, the action is simply a function that returns a specific value, so you need to ensure that you are indeed returning that variable.

## Does the custom action import internal libraries, e.g., import “../../flutterflow”?

---

Sometimes, you might want to use components, assets, or elements already present in the project or built with the no-code builder. In such cases, you may need to set the "exclude from compilation" option to true. This is because the compiler might not recognize the newly created elements, even though they will be present in the actual build.

## Does the custom action include pub spec dependencies?

---

### 
Do those dependency imports match up with the custom action settings? 

You may forget to include imports in the PubSpec Dependencies or forget to to include the import within the code.

![](https://downloads.intercomcdn.com/i/o/989400626/5129c8e2a4ad83b57ddd94f6/image.png?expires=1741032900&signature=b7f5f4df5ea1f8d2e12f0766e9c006a06121662fabda5e666e7155717e829923&req=fSguEsl%2Bm4NZFb4f3HP0gLXiKJ8eVIyBGQn9lDhOJobJMBrhxzMkQci8UAVn%0AkjY%3D%0A)

### Are specific version numbers specified for the dependencies?

Specific version numbers may have issues, or may not match with the other version that need to be imported. You will needs to check that these versions do not conflict with other dependencies. This can be checked on pub.dev

![](https://downloads.intercomcdn.com/i/o/989401350/3eca857b4579178b8c3895ee/image.png?expires=1741032900&signature=a1732bb0422b835ecb240f8cab33ff317945f0f15cd055dc069d8caca05d1f46&req=fSguEsl%2FnoRfFb4f3HP0gH1aURtD%2F7dZ%2BQ53XIBL%2FXtQwFGYCW3OqnXXg8vT%0A9tE%3D%0A)

### 
Do any other custom functions include similar dependencies but with different versions? 

You may sometimes import the same dependency into multiple spots, but with different versions, which creates conflicts. Make sure that you have one version set globally.

### Do FlutterFlow imports conflict with any of the imports?

FlutterFlow automatically imports a couple of dependencies which may sometimes conflict with import you have. 

![](https://downloads.intercomcdn.com/i/o/989402667/fa0bf1294e3aee98c7c27395/image.png?expires=1741032900&signature=cfc73d6214f106474b19e7a35831169602a5a742e346764621756291cb4805d6&req=fSguEsl8m4dYFb4f3HP0gEWLi3H55rrJ2vNndKZGiQYZBPDNnPEyXsLrr%2FaM%0Aivw%3D%0A)

## Is there an actual code error within the code?

---

### Have you added null values where necessary?

You may sometimes forget to include null values. Ensure that null values are present in all the correct locations.

```
`📝 int example = passingIntWhichMayBeNullable ?? 0;`
```

### Have you provided the correct data type in the correct spots

You may sometimes forget pass the right data type in the right spot.

```
`📝 String numberAsString = “5”; 

 int example = thisWord; ←

 ↗️ User is passing a string to an integer without conversion`
```

Can be converted with functions like: .toString(); .toInt(); .toDouble()

​

### Are single elements passed in as arrays or vice versa?

You may sometimes pass single elements to lists or lists to single elements. In these cases, they need to incorporate functions to either add an element or retrieve an individual item from the list.

## Is “Exclude from compilation” unchecked?

---

If this option is selected, the code may contain errors as it won't be checked during FlutterFlow compilation or error checking. This selection implies that the code will be excluded from error checks, but will still be included during execution / build during Test or Run Mode.

![](https://downloads.intercomcdn.com/i/o/989408122/8826dfc56e03e8a014e94845/image.png?expires=1741032900&signature=5a2f3546f31087f1b62c8211867a21037ca8faae53181f122e6c78acdb061aa4&req=fSguEsl2nINdFb4f3HP0gPMNfecROqWweFLLmfsWbleGhCUdna%2FIfCtdPVhA%0AhpA%3D%0A)

## Are data types / structs not recreated within the code itself (new class created within custom action)?

---

These days, it's common to generate custom code with tools like ChatGPT or to borrow code from existing projects. However LLMs or external code sources may lack context about where this code will be used. Custom data types or structs, are defined by FlutterFlow within the data schema panel, and do not need to be redefined within the custom code. This could lead to project build errors. Ensure there are no "double definitions".

![](https://downloads.intercomcdn.com/i/o/989408496/f81673412447d78cca8bf550/image.png?expires=1741032900&signature=4dda562082d47345848696c03a84c43ae3acea8be95cf7d25c33e77203f73b4a&req=fSguEsl2mYhZFb4f3HP0gHrEPg2AvgXzISgHg5nxEq3wk%2Fcs%2BQd6odQwbdc4%0AxbQ%3D%0A)

## Are CallBack Actions within custom actions passing the correct data-type back?

---

Example, you may either forget or pass the wrong type of variable back in the callback action.

![](https://downloads.intercomcdn.com/i/o/989408969/b6e3d231f9ae6551e989434b/image.png?expires=1741032900&signature=72e5fd57cb975cbe97b7439a0bed046ca0538f1b3afcd2f50f3f79756843fe3a&req=fSguEsl2lIdWFb4f3HP0gGXFzGSUhHrHcrgDyT%2FdJuEYJQmc9ZITCQIJyvaX%0Af2g%3D%0A)

## Additional Resources

---

Below is an excellent article on how to debug specific custom code issues or errors using the browser debug console. This is particularly useful when dealing with logic errors, rather than syntax errors:

Testing Custom Actions using Debug Console | FlutterFlow Help Center

Below is an excellent video from FlutterFlow University about custom actions. It guides you through the basics of creating custom actions:

Full in-depth docs can be found here:

Custom Actions | FlutterFlow Docs

​

​

​