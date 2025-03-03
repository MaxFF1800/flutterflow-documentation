---
title: Custom Authentication in FlutterFlow
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "9030551-custom-authentication-in-flutterflow"
hide_table_of_contents: true
---

# Pre-Requisites to Enabling Custom Authentication:

Ensure you have a custom server with login and sign-up endpoints that return a JWT token upon success

Custom authentication must be enabled in FlutterFlow, with entry and logged-in pages correctly set

Here's an example: 

![](https://downloads.intercomcdn.com/i/o/981943920/2526fc51b97707e23b221849/sign-up.png?expires=1741032900&signature=2edf84ae45c2c491abc9a288ce8634ecc1e8e6872880f595776fa51468640947&req=fSgmH819lINfFb4f3HP0gJGQJ3yL01DLdkaWlqKi2OG5JOzxxvmuV%2FOGLmaS%0AuQ8%3D%0A)

# Checklist for Troubleshooting

## Verify Server and API Endpoints

Confirm that your server is correctly returning JWT tokens for login and sign-up requests. The server's response should include the authentication token, refresh token, expiration time, and user ID (UID).

Double-check the API endpoint configurations in FlutterFlow to match your server's requirements.

## FlutterFlow Configuration

Make sure custom authentication is enabled in the project settings.

Verify that the entry point and logged-in pages are set correctly.

## UI Configuration

To facilitate the authentication flow, ensure your app has at least three pages: 

Login

Sign Up

Home Page (i.e. the landing page when a user successfully authenticates)

## API Integration and Authentication Flow

Test API calls from FlutterFlow to your server and ensure responses are received as expected.

Upon successful authentication, use the backend FlutterFlow action to call the API. Then, utilize the response data to perform a "custom login" action within FlutterFlow.

## Handling Tokens and User Data

Set up your FlutterFlow actions to correctly parse the API response, capturing the auth token, refresh token, expiration time, and user ID (UID). This data is crucial for managing user sessions.

![](https://downloads.intercomcdn.com/i/o/981944200/b580b053d6be6a0da8d82cd0/login-params.png?expires=1741032900&signature=3e6cea5c0f08ea96429d64dbfa7a4ab2387b23e83b446b860044b9151cefad59&req=fSgmH816n4FfFb4f3HP0gOC4O1ovhSGnW1%2F3rifdC6T%2F82DYER5j0KfARn%2F6%0ARsY%3D%0A)

## Navigation

If automatic navigation after login or sign-up is not working, you can disable it. 

Then, opt for manual navigation to ensure users are directed to the correct page after authentication.

## General Tips

Utilize logging both on your server and within FlutterFlow (snack bars, alerts) actions to track the authentication flow and identify any points of failure.

Test the entire authentication flow, from entering credentials to accessing protected pages after login, to ensure there are no breaks in the process.

By carefully following this guide, you should be able to troubleshoot and resolve common issues encountered when setting up custom authentication in FlutterFlow.

## More resources:

https://www.youtube.com/watch?v=hnX3CvBtGvI

Sample project: https://app.flutterflow.io/project/custom-auth-checklist-fdjkno

https://docs.flutterflow.io/data-and-backend/custom-authentication