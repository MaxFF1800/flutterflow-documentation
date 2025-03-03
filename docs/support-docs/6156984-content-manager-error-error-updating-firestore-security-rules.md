---
title: "Content Manager Error: Error Updating Firestore Security Rules"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "6156984-content-manager-error-error-updating-firestore-security-rules"
hide_table_of_contents: true
---

## Issue

I see this issue when I try to use the FlutterFlow Content Manager (CMS)

```
`Error updating Firestore Security Rules... Make sure you set up Firebase for your project under "Settings" > "Firebase".`
```

![](https://downloads.intercomcdn.com/i/o/542848432/eee838cb97c5b7b2b93e1541/image.png?expires=1741032900&signature=680759248e97d78363a3569e85553584c2d2b6b8cc183d0e0c315154ae0b59c6&req=cSQlHs12mYJdFb4f3HP0gPLjjsPcgoiNPeenZy86DUyJSnJmxUs1LNBqce0f%0Abh8%3D%0A)---

### Why You Are Seeing This Error

You are seeing this error because your Firebase permission have not been set up correctly. No worries, this is easy to fix!

---

# Ensure Email Sign-In Is Enabled

Open the Firebase console, and click on Authentication (in the left side menu).

Click on the Get started button.

Select the Sign-in method tab.

Check to see if you see Email/Password with that is turned on with a green check Enabled:

![](https://downloads.intercomcdn.com/i/o/542838399/e484613a15c191761157611b/image.png?expires=1741032900&signature=7429bce1aa7cad63581fc65c248b3608cd68683c915c1005b30c1b14e676ce58&req=cSQlHsp2nohWFb4f3HP0gKKNijYsETs%2B%2FOYAbYglBsLFAg7Ki%2BFpCcfcCxTY%0Alb0%3D%0A)

If you don't see this, you will need to use these instructions to turn on email sign-in.

---

# Ensure you have added the required cloud permissions

For push notifications to work, you will need to add the following cloud permissions for firebase@flutterflow.io: Editor, Cloud Functions Admin, and Service Account.

Head to the Firebase Console and open the project dashboard for your project (click the project tile). Select Project Settings > Users & Permissions.

If you don't have Cloud Functions Admin, Editor, and Service Account listed next to firebase@flutterflow.io, you have not completed this step.

![](https://downloads.intercomcdn.com/i/o/501028815/d4d5ea7c25cc3f0f78aa459a/image.png?expires=1741032900&signature=108d49a8022ae903c290a081fa5ef9b8f7c7c7060aa44794c0afb2f140fc10e9&req=cSAmFst2lYBaFb4f3HP0gN%2F1m%2Bu6JT8H1hOQeSs8p7Fnl4slsaAHCw%2Bs5eE4%0Ag%2B8%3D%0A)

Here are the instructions on how to add the required cloud permissions to your project.

---

# Update Your Firebase Rules

From within your FlutterFlow project, select Firestore > Settings > Scroll down to Firestore Rules > select Deploy/Redploy.

![](https://downloads.intercomcdn.com/i/o/542842569/4fa37c4ab1d84ede8080c334/image.png?expires=1741032900&signature=003fdb04717f6b513a8bc90efc0b1fbd98b4d3409ed86698b5f4af59528bec59&req=cSQlHs18mIdWFb4f3HP0gIhZKW7BbJIhpfRVGq9Fwl04l8qX8Nw%2BkBqZZJzK%0A9s4%3D%0A)---

# Ensure Firebase Schema Is Defined

Ensure you have defined the fields in your Firebase schema. Only fields defined in your Firebase schema are shown in the Firebase Content Manager.

---

# Ensure you are using the latest version of FlutterFlow

To upgrade to the latest version of FlutterFlow select Ctrl + R on Windows or Cmd + R on Mac.

After you have done this, clear your browser cache and log out/in to FlutterFlow.

If the above wasn't helpful full please make sure you check this Link as well.

---

# Create Permissions From Scratch

If you have already completed the above steps, the final troubleshooting method is to remove the existing permissions and complete a new setup from scratch. Here are instructions on how to do this.