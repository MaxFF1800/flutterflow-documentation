---
title: How to Retrieve and Upload Your Keystore File in FlutterFlow for an Existing Google Play Project
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8154282-how-to-retrieve-and-upload-your-keystore-file-in-flutterflow-for-an-existing-google-play-project"
hide_table_of_contents: true
---

## Introduction

Publishing an updated version of your app using FlutterFlow can be a challenging task, especially when the app was initially published on Google Play using another platform. 

This guide aims to walk you through the process of obtaining or resetting keys from Google Play, creating a new keystore on your local machine, uploading it to FlutterFlow, and successfully deploying the app to your existing Google Play project.

If you run into any roadblocks, we recommend reaching out to Google Play support or FlutterFlow Support for further assistance.

![](https://flutterflow.intercom-attachments-1.com/i/o/825180891/e21e5bc9c033719cb85551fc/image.png?expires=1741032900&signature=2d59e7847d40a707b8c7297f2f9b0ab8ed1da9f81b4cfe03eae051673658b87f&req=fCIiF8F%2BlYheFb4f3HP0gGG6vJo42sL7yv%2FeGiMrI%2FEYbk9WHClqU03dwiGy%0A69I%3D%0A)

![](https://flutterflow.intercom-attachments-1.com/i/o/825180905/e661855370ff7393781ed068/image.png?expires=1741032900&signature=67ef7fa50cb5337bb9d1955e6da8f811a175d73ead6b31eb42a7e8de8214366a&req=fCIiF8F%2BlIFaFb4f3HP0gJ8JTa%2FGNfiATesBq4zpVB5T6wMM6tjghrvK5WQ0%0A8jg%3D%0A)

![](https://flutterflow.intercom-attachments-1.com/i/o/825180920/b46a8e60e0499cac5c065f91/image.png?expires=1741032900&signature=a2e9c9e340848e829f3a624a753363961d1870b79bd5035002a4e10370bfe5fe&req=fCIiF8F%2BlINfFb4f3HP0gAFLyIc7lxFRI3B4RHMyAOv3Tyf8%2BdUHZG96WAPS%0AYxs%3D%0A)

## Create the new keystore

keytool -genkeypair -alias allyou -keyalg RSA -keysize 2048 -validity 10000 -keystore allyou.keystore

Export the pem public key from it

keytool -export -rfc -lkeystore allyou.keystore -alias allyou -file allyou.pem 

Provide it to the google play request

Wait for them to approve

Then next steps is to use the keystore to deploy to google play

## Step 1: Create a New Keystore

Begin by generating a new keystore. Open your command line tool and enter the following command:
bashCopy codekeytool -genkeypair -alias allyou -keyalg RSA -keysize 2048 -validity 10000 -keystore allyou.keystore
This command creates a new keystore named 'allyou.keystore' with an RSA key pair, a key size of 2048 bits, and a validity period of 10,000 days. The alias for your key should be 'allyou'.

## Step 2: Export the PEM Public Key

Once your keystore is created, you need to export the public key. Use the following command to do so:
bashCopy codekeytool -export -rfc -keystore allyou.keystore -alias allyou -file allyou.pem
This command exports the public key into a file named 'allyou.pem'. Ensure you have access to the keystore ('allyou.keystore') as it is required for this step.

## Step 3: Provide the PEM Public Key to Google Play

After exporting the PEM public key, you need to provide it to Google Play. Log in to your Google Play Console and follow the necessary steps to submit your 'allyou.pem' file. This process is typically required for app signing or other verification purposes.

## Step 4: Wait for Approval from Google Play

After submitting your PEM public key, wait for approval from Google Play. This process can vary in time, so check your Google Play Console regularly for updates. Approval is necessary before you can proceed with deploying your app.

## Step 3: Deploy to Google Play Using the Keystore

Once your PEM public key is approved, you can use your keystore ('allyou.keystore') to deploy your app to Google Play. 

Proceed with the app upload process in the Google Play Console, ensuring that you select the 'allyou.keystore' file when prompted for your keystore details.

## ------

Step 1: Requesting a New Upload Key from Google Play (If Necessary)

If you've lost your original upload key, or it has been compromised, you can request a new one from Google Play. Here's how:

Sign in to your Google Play Console.

Select the app you want to manage.

On the left menu, click on "Setup" and then "App Integrity."

Look for the "Request upload key reset" option.

Note: If you can't find the app integrity you can use the search bar on top of the Google Play console

​

![](https://downloads.intercomcdn.com/i/o/823930853/5b586163e23f399bddc1a6be/image.png?expires=1741032900&signature=4714f616b2ebf8a5ac0420f232f585e90b9a72f70ed4a07daecd6c8d4b0bc9bc&req=fCIkH8p%2BlYRcFb4f3HP0gC4BwOrTLFuqu2jhycp%2FU%2FVajpI1cSuinhOuukdG%0AKs0%3D%0A)

## 

![](https://downloads.intercomcdn.com/i/o/825004677/f1f5db82dcbd6cdeae2a8602/image.png?expires=1741032900&signature=0d2da7f5c40a175c3603b2a69ec0f6da0f17bc576ad4b9ba6029bbf11fe2db3b&req=fCIiFsl6m4ZYFb4f3HP0gHYgUDMRvHCzZbWpfg%2FEz7iFAxC%2Bv1qnqUAjR16J%0Acxw%3D%0A)

Note: You'll see a lock icon next to this option, indicating that you need special permission to perform this action. If you don't have the necessary permission, you will need to get it from the account owner.

Follow the on-screen instructions to complete the request.

This process will generate a new upload key for you, but remember, it takes about 48 hours for the new key to become available for use.

​

Important: Keep this new key safe and back it up immediately. Losing your upload key can severely complicate the app update process on Google Play.

​

​

## Step 2: After Receiving the New Upload Key

Once Google Play has approved your request and provided you with a new upload key, you'll typically receive it in a .jks or .p12 format. Here's what to do next:

​Verify the Key: Open a terminal and use the following command to list the key's details:

​

```
`keytool -list -v -keystore path/to/your_new_key.jks`
```

Replace path/to/your_new_key.jks with the actual path to your new key. This command will display the key's fingerprint, which should match the one provided by Google Play.

​Prepare for FlutterFlow: Make sure the key is in .jks format as FlutterFlow requires this specific type. If your key is in .p12 format, you can convert it using:

​

```
`keytool -importkeystore -srckeystore your-key.p12 -srcstoretype pkcs12 -destkeystore your-key.jks -deststoretype JKS`
```

​Upload to FlutterFlow: Log in to your FlutterFlow account, go to the 'Deploy' section, and upload the new .jks key under Android settings. Make sure to input the keystore password, key alias, and key password that are associated with the new key.

​

![](https://downloads.intercomcdn.com/i/o/766833917/be2ee5165be3791d032a0c01/image.png?expires=1741032900&signature=261e5d6db33fdc619b42c7dc2ed37209f645092e671ef2e07c5b53946750d02c&req=cyYhHsp9lIBYFb4f3HP0gKa64yYVYUjDbWdY0Vd0caiCYJS4ko2E1T7FcwCE%0AZ3g%3D%0A)![](https://downloads.intercomcdn.com/i/o/823932293/4dc796b059ddc1910aded719/image.png?expires=1741032900&signature=ce584ebae0375cb66f9db835fc55fa68a6b094e8bc65c2a7789d88db5e675d0f&req=fCIkH8p8n4hcFb4f3HP0gFBygyvcpdroexEXboC%2BnZ4pl8fq2QUnXTc2ocFW%0Az8s%3D%0A)

Deploying to the Google Play Store: Before deploying your app to Google Play, consider running a test build within FlutterFlow using the newly uploaded key. This will help you identify any issues before the final deployment.

​

Note: Your key store file Flutterflow used to sign your app, is accessible on the deploy page with the orange key button.

​

![](https://downloads.intercomcdn.com/i/o/789196438/9f0ab9215d3f5bbb44345fa9/image.png?expires=1741032900&signature=5ad74f56cb681591b9c48c800df290ff5366b7a91ebd3d904867918656c17a8f&req=cyguF8B4mYJXFb4f3HP0gD1FtzmZPtQpZAxvTkdIQtZroRHlr4V8qq8gUVzs%0AbBc%3D%0A)

## 

Conclusion

We hope this guide assists you in deploying your app using FlutterFlow. Managing keystores is an essential part of app development. Always back up your keystore and remember the passwords you set for it. A lost keystore can create severe complications for your app's updates on Google Play.

​

For further assistance, feel free to contact FlutterFlow Support or Google Play Support.