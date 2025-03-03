---
title: "Stripe payment action error: Unknown Error Occurred"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "/"
hide_table_of_contents: true
---

Error Details:

Snackbar: Unknown Error Occurred

Console:

Access to fetch at 'https://us-central1-bayside-festival.cloudfunctions.net/initStripeTestPayment' from origin 'https://ff-debug-service-frontend-ygxkweukma-uc.a.run.app' has been blocked by CORS policy: Response to preflight request doesn't pass access control check: Redirect is not allowed for a preflight request.

Why this Error is caused:

The Cloud function region is different comparing to the region defined in Firebase.

How to Resolve this Error:

Step 1: Head over to the firebase in the settings page (You can also do this from command palette with keys ⌘+K or Ctrl+K and write firebase), Show Advanced settings, Here you will see the Cloud Functions Regions dropdown. 

Step 2: Set the Cloud functions Region to [Default] or a region defined in firebase.

​

![](https://downloads.intercomcdn.com/i/o/694885663/7dcf085444b23d2aff2a7e5f/Screenshot+2023-03-20+at+4.58.08+PM.png?expires=1741032900&signature=8eef6a9891cb86951c72eff9d629555f05a45ac41a51f2f667b2a1743fc84987&req=cikjHsF7m4dcFb4f3HP0gFEk%2BtuVZ4oi5UGojKClQtm%2FOIyY6Y93TrZGN8tG%0Ar4o%3D%0A)

Step 3: Delete the already deployed functions from firebase.

​

![](https://downloads.intercomcdn.com/i/o/694887520/0cd0f46c4ae9786af41808af/Screenshot+2023-03-20+at+5.15.21+PM.png?expires=1741032900&signature=c1063f1976cc05da9cd3c429e0aea1fca763826a411bd33a517e67f262c96e15&req=cikjHsF5mINfFb4f3HP0gG2eie40qfkA6t%2FyPj0NXeTcwc2MncWv4ri%2FMPvf%0AGnw%3D%0A)

Step 4: Re-Deploy Stripe in your project

​

![](https://downloads.intercomcdn.com/i/o/694889625/ed6ed12576791126ff53b9e0/Screenshot+2023-03-20+at+5.14.26+PM.png?expires=1741032900&signature=c86f9b0353ee35ecff435f1d7d633e684f1e58278b3f16e2bfe268dca14b8e48&req=cikjHsF3m4NaFb4f3HP0gBIcfQi9D4U0noYu3tbfbUhK35c0aHcVGImsAirQ%0Au0U%3D%0A)

After these steps, your problem should be resolved, if the problem still persists feel free to contact us at support@flutterflow.io

​