---
title: "RevenueCat for Subscription and One-Time Payments in FlutterFlow – PayWall"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8999321-revenuecat-for-subscription-and-one-time-payments-in-flutterflow-paywall"
hide_table_of_contents: true
---

In the evolving landscape of mobile applications, in-app purchases and subscriptions represent a significant revenue stream. RevenueCat emerges as a powerful tool to simplify the management of these monetization strategies, particularly when integrated with platforms like FlutterFlow. This article delves into how RevenueCat orchestrates paywalls for both subscription and one-time payment models, ensuring seamless entitlement management across different user scenarios.

​

## Understanding RevenueCat's Role

RevenueCat serves as a middleman between your app and the app stores (Google Play and Apple App Store), managing in-app subscriptions and purchases. By abstracting the complexities of store-specific APIs, RevenueCat provides a unified interface to track subscription revenue, handle user subscriptions, and manage in-app receipts.

## 

Preparing Your App

Before diving into RevenueCat's implementation, ensure your app is deployed on Google Play Store and Apple App Store. FlutterFlow facilitates this in the "Settings and Integrations > Mobile Deployment" section. It's crucial to define your subscriptions and one-time purchases in both app stores prior to integration with RevenueCat.

## 

Configuring Products in RevenueCat

Subscriptions: In RevenueCat, subscriptions are set up as auto-renewable products. Each subscription needs a unique identifier and should be added under the "Product Setup" section. This includes defining the subscription details like duration, price, and available tiers.

One-Time Purchases: Similarly, one-time purchases are configured in RevenueCat as non-consumable products. Each one-time purchase requires a unique identifier, allowing you to track and manage these transactions separately from subscriptions.

![](https://downloads.intercomcdn.com/i/o/974144027/a41b8c40216533b76cd09a5b/image.png?expires=1741032900&signature=136bbc6e412e48fdf3cc2a7192a6acaccff62ece22bc0b5ca5141cd2b0fe8c0c&req=fScjF816nYNYFb4f3HP0gJcfUfTVo%2FzpjmJtBMY2DwFJf1RpoJ%2Fh92GQ1bz%2F%0A3ak%3D%0A)

## 

Entitlements and Offerings

Entitlements in RevenueCat help in determining user access to content or features based on their purchases. For example, you might have an entitlement named "PremiumAccess" that unlocks additional app functionality for subscribed users.

Offerings and their associated packages describe the actual products available for purchase. They represent the bridge between your app's paywall and the products defined in RevenueCat, ensuring users are presented with the correct options for subscriptions or one-time purchases.

​

​

![](https://downloads.intercomcdn.com/i/o/974134536/6bf9104db1dcba02c24a4387/image.png?expires=1741032900&signature=1dc16531b3e53b46a0bb199f1572e7789815db84e152877ec251aafe58e86931&req=fScjF8p6mIJZFb4f3HP0gDuWQNrINCo9PM%2FEYcgYXs7JMUAqHEGWMfHaHKRh%0Ay%2F0%3D%0A)

If you have different types of products, like subscription and one-time payment products, you may need to check the list of the user's entitlements to see if it contains a specific entitlement (instead of using the paywall action).

​

​Why? Even if the user bought a one-time product (i.e., not a subscription), a paywall will be passed. ​If you allow users to purchase items like tokens, buying tokens will enable users to bypass the paywall. This purchase adds a one-time product to their entitlements. The paywall treats subscriptions and one-time products the same, accommodating users who prefer to grant access through a single purchase.

​

​

## Implementing the Paywall in FlutterFlow

The paywall is the pivotal point in your app where users decide to make a purchase or subscribe. In FlutterFlow, you can design a paywall page or modal displaying the offerings fetched from RevenueCat. Utilizing FlutterFlow actions like "Check Subscription Status" and "Initiate Purchase," you can manage user interactions with the paywall, guiding them through the subscription or purchase process.

![](https://downloads.intercomcdn.com/i/o/974131731/fa949cceb9722a76eac66fa1/image.png?expires=1741032900&signature=5386dc27c45df4df76bcde9d94313dff635f7c94951424b03c2eea9ee513dde7&req=fScjF8p%2FmoJeFb4f3HP0gEzQYCDISREi02M1YfBoZ6EZgYQ%2FC4DHthEWnSKj%0AvzQ%3D%0A)

In Flutterflow Paywall is an action, and the result of the action is a boolean value, If you add a condition after the paywall action Flutterflow will set the condition automatically to the paywall result, #3 if the user has entitlement then we do the next actions, If not we could show a modal for users to subscribe or navigate to another page to let them subscribe

In Flutterflow, a paywall is an action that produces a boolean value. When you follow the paywall action with a condition, Flutterflow automatically applies the result of the paywall to this condition. If the user has entitlements, subsequent actions are triggered. Some other options are to:

Display a modal prompting the user to subscribe

Redirect users to another page for subscription purposes

​

​

![](https://downloads.intercomcdn.com/i/o/974144531/c697d44ffcf3934af681d179/image.png?expires=1741032900&signature=d28213198df143edf799cf05508d8e04d70f074104114784f4086df516002cf7&req=fScjF816mIJeFb4f3HP0gG1WNOATX3OfcGhkctQFe3ozwrH5wbUHsgQyDo7N%0AvlM%3D%0A)

## 

Managing User Transactions

After a user selects a product or subscription, the Purchase action in FlutterFlow initiates the buying process. 

RevenueCat handles the transaction with the app store, ensuring secure and reliable payment processing. Post-purchase, the user's entitlements are updated, granting them access to the paid content or features.

If a user needs to restore previous purchases, the Restore Purchase action in FlutterFlow facilitates this process. By implementation this action, you ensure users can reclaim their subscriptions or purchases across devices or after reinstalling the app.

​

![](https://downloads.intercomcdn.com/i/o/974141189/2b4d012ee5862bc29151c86a/image.png?expires=1741032900&signature=c6f25593f70eecce68890fdbcd6208e0805abc11a2865abb4f443ee4a49ad54d&req=fScjF81%2FnIlWFb4f3HP0gFm5pLwCzzqlot5t1y%2FO4CkH2O8F1yHWg5cqL1vb%0AUO0%3D%0A)

The outcome of the action is a string labeled as "paymentId." You can examine this string in the action's output via the source menu. 

One important check: ensure the "paymentId" is present and not null. If this condition is met, you can proceed with the actions you've planned for after a successful payment.

## 

Conclusion

Integrating RevenueCat with FlutterFlow for managing subscriptions and one-time payments offers a robust solution to monetize your app effectively. By understanding the configuration of products, entitlements, and the paywall mechanism, developers can provide a seamless user experience, encouraging purchases while simplifying the management of in-app revenue streams. For detailed guidance on setting up RevenueCat and FlutterFlow, refer to the FlutterFlow documentation and the RevenueCat SDK documentation.

​

​

## Additional Resources

FlutterFlow YouTube Channel for tutorials and tips.

RevenueCat Non-Subscription Purchases Documentation for insights into managing one-time payments.

FlutterFlow Community for support and discussions with other developers.