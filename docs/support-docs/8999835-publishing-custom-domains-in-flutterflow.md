---
title: Publishing Custom Domains in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "8999835-publishing-custom-domains-in-flutterflow"
hide_table_of_contents: true
---

Having trouble connecting your custom domain in FlutterFlow? Don't worry – we've got you covered. In this article, we've outlined some common issues users face and step-by-step solutions to get you back on track.

---

## 
Issue: Unable to Connect Custom Domain (Error: Expected DNS records not found)

Scenario: You've set up the DNS records for your domain, but the connection still fails.

Tip: Misconfigured DNS is often the culprit.

Background: FlutterFlow requires specific DNS records for custom domain connection, and you should set them according to your domain. Here's where you'll find them:

![](https://downloads.intercomcdn.com/i/o/976937082/2cca94c2046d531ff89c883c/Screenshot+2023-08-25+at+6_14_34+AM.png?expires=1741032900&signature=7b8f4c7958be5e2f5c5dcb2434ccccee2d1c319adcf52f64c1abe17181b77b7e&req=fSchH8p5nYldFb4f3HP0gPYAmH7BedjK9FBeLxytfDJ0TpotPGrsdPf9o6qR%0AxXs%3D%0A)

Please note that if you uncheck “Also www...” you won’t need to create the second, CNAME record.

​

## Troubleshooting Steps:

Verify DNS Records: Use tools like nslookup.io to check your DNS records against the required configuration.

Ensure the required A and CNAME records exist. No other A, AAAA, or CNAME records should interfere. Here's an example:
![](https://downloads.intercomcdn.com/i/o/976942042/e78b812619479fce3d0756de/Screenshot+2023-09-28+at+9_38_32+AM+%281%29.png?expires=1741032900&signature=f164f3c1854df2a1d10386cf7de24411982e8b6619cc0ac0b36548bc60735946&req=fSchH818nYVdFb4f3HP0gBFq4jCl3fidq5k%2Fuq%2BgICPKdN0SDonsPlhDEn6p%0AlW4%3D%0A)

Wait Period: DNS changes may take up to 24 hours to generate. Please wait at least an hour after making changes before retrying.

Retry: If records are correct, retry connecting after some time.

​

Reach out to support: If all the settings are correct and you are still facing the issue after 48 hours, please communicate with the domain registrar.

---

## Issue: Difficulty Creating DNS Records

Tip: Each registrar may have a different interface, complicating the process.

Suggestions:

When you create a record for a root domain, e.g. example.com, some registrars require the “name” field for the record to be empty, some require “@”, and some - a full domain name (example.com).

When they create a record for a subdomain, e.g. test.example.com, some registrars require the “name” field for the record to be the name of the subdomain (”test”), some - full name (test.example.com).

Please refer to Registrar-specific documentation to learn more about how you can set up the DNS records.

---

## Issue: Error 404 After Connecting Domain

Solution:

Please try publishing the project after connecting the domain, it should resolve the issue that you are experiencing regarding Error 404.

---

## DNS Restrictions for SSL Certificates

Background: The DNS might be restricting the SSL certificate authorities, which results in an error while connecting the domain.

​

​Solution:

Verification: Use nslookup.io to check for CAA records. you should be able to check that using this link: https://www.nslookup.io/domains/your-site-name/dns-records/caa/. consider replacing "your-site-name" with your site.

Adjustment: Add "letsencrypt.org" to allow authorities or remove CAA records.

Outcome: FlutterFlow should connect once DNS is adjusted.

---

By following these steps, you can troubleshoot and resolve common issues encountered when connecting a custom domain in FlutterFlow. If you still face challenges, don't hesitate to reach out to our support team through Live chat or by emailing support@flutterflow.io

Additional Resources:

Youtube Tutorial: Web Publishing

FlutterFlow Documentation: FlutterFlow Docs

Community Tutorials: FlutterFlow Community

YouTube Channel: FlutterFlow YouTube

Blog: FlutterFlow Blog

Marketplace: FlutterFlow Marketplace

Intercom Articles: Intercom Help