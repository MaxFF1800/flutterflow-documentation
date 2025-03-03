---
title: "How do I import a flutter package?"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6367505-how-do-i-import-a-flutter-package"
hide_table_of_contents: true
---

To get started with Custom Code in FlutterFlow, please watch this tutorial. The steps for creating a custom widget or an action are somewhere similar. But, here are some links to our documentation that provide some step-by-step instructions on how to create them.

Custom Widget Documentation

Custom Action Documentation

# Here are the instructions on how to get a dependency in FlutterFlow.

Dependency is a package (library) hosted on pub.dev. While creating the Custom Action, you may need the dependency name and its version so that FlutterFlow can download that dependency for your project.

To get the package/dependency name and its latest version:

Open the package/dependency page on pub.dev.

Click on the Copy icon on the right side of the package name.
![](https://downloads.intercomcdn.com/i/o/542513452/50da27015dcacc331e86d20d/image.png?expires=1741032900&signature=551e4c35d4e7d731f31701239960d7b090c2eb6c72647ff1427d2c040c27d6ad&req=cSQlE8h9mYRdFb4f3HP0gL2sCHAQhR8Vp1whz%2BmoQOq%2BV7Qj9GWlmL2pMZAv%0Aydw%3D%0A)

Paste the copied dependency inside the FlutterFlow.

![](https://flutterflow.intercom-attachments-1.com/i/o/542518747/0646bce3fbb08f4bd1ee8d43/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FmpEYYxF6CyEZs0jEJ3aM-2Fezgif.com-gif-maker-20%2810%29.gif?expires=1741032900&signature=e6b373ee57707bee33d1166d150ae5a1ac1329837e37534815e826cf64edb584&req=cSQlE8h2moVYFb4f3HP0gFCjEnfyk6pgg3vT8LessAcnM1sieyGDzmuPEd7d%0AyZo%3D%0A)

The next important step is getting the package import statement.

Package Import Statement is usually a path where the code (you are using to create Custom Widget/Action) resides. While creating Custom Widget/Action, you need the package import statement to be written at the top in the code editor.

To get the package/dependency import statement:

Open the package/dependency page on pub.dev.

Select the installing tab.

Under the Import it section, copy the import statement by clicking on the Copy icon. Paste it inside the Custom code editor.

![](https://flutterflow.intercom-attachments-1.com/i/o/542518764/26709e6a5df5f53e9fa494c1/spaces-2F-MhFNOxEwcl8ED58MUC_-2Fuploads-2FI82y5LKGYOFIJXb21CHQ-2Fezgif.com-gif-maker-20%2811%29.gif?expires=1741032900&signature=e66c66bcdebb81573220e3e4b5b8ea5cbc590024cfcc32b7d93acea4b755d72a&req=cSQlE8h2modbFb4f3HP0gLeR7%2BTIDkl%2FOSz3VNNHXFvlqoGPZTICQrSlfYHl%0AZmY%3D%0A)

---

# Here are some additional important points to note while working with custom actions/widgets

Make sure your pub.dev widget has WEB support. This is required to use the widget in Run/Test mode within FlutterFlow.

Inside the Required Pubspec Dependencies enter the package name with its latest version. It should be something like packagename: ^version. If you don't use a version it imports the last version specified on pub.dev for the package.

Every time when you add a new parameter, make sure you compile the Custom Widget.

You won't be able to delete a Custom Widget/Action if it is being used in the app. To successfully delete a Custom Widget/Action, make sure you are not using it anywhere.