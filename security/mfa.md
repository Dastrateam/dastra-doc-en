---
description: Dastra lets you enable strong authentication for your users
---

# Strong authentication

## Introduction

Dastra uses [TOTP](https://en.wikipedia.org/wiki/Time-based_One-time_Password_algorithm) technology to manage [multi-factor authentication](https://en.wikipedia.org/wiki/Multi-factor_authentication) for users.\
Users can then log in using both their usual password and a 6-digit code provided by an authenticator app such as Microsoft Authenticator or Google Authenticator (or others...)

## How to enable strong authentication?

* Go to https://app.dastra.eu/general-settings/two-factor
* Click on "**Enable strong authentication**"
* Download a two-factor authenticator app
* **Scan the QR code** with the app you chose

![](<../.gitbook/assets/settings-2fa-setup-qr-code.png>)

* Store the recovery code somewhere safe.&#x20;
* Log in using the 6-digit code provided by your authenticator app

![Example of an authenticator app](<../.gitbook/assets/settings-2fa-authenticator-app.png>)

{% hint style="warning" %}
Keep your recovery code somewhere safe! It will allow you to recover your account if you lose your authenticator app. Your account will be permanently locked if you cannot provide this code. You would then need to contact your organization's owner so they can reset two-factor authentication on your account.
{% endhint %}

## How to force all users to use strong authentication?

* Go to https://app.dastra.eu/general-settings/security
* Check the box to force two-factor authentication.

{% hint style="info" %}
All users who log in will not be able to access the application without having configured two-factor authentication on their account. Make sure your team is well informed of best practices for storing TOTP secret keys.
{% endhint %}
