---
description: Configuration of an SSO Connection Using the OpenId Protocol
---

# OpenId

**Operating Principle**

The specifications of OpenId can be found [here](https://openid.net/connect/).



<figure><img src="../../../.gitbook/assets/openid1.png" alt=""><figcaption></figcaption></figure>

The configuration of SSO with OpenID is done in three steps:

1. Configuration of the Authentication Provider: Active Directory, Google Workspace, etc.
2. Configuration of the Service Provider: Dastra
3. Testing of the authentication



1. **Configuration of the Authentication Provider You need to set up an OpenId configuration in your authentication provider.**

For Active Directory: [https://docs.microsoft.com/fr-fr/azure/active-directory/develop/v2-protocols-oidc](https://docs.microsoft.com/fr-fr/azure/active-directory/develop/v2-protocols-oidc)

To link the local accounts (those hosted in Dastra), you need to provide a property containing the user's email (by default, Dastra looks for the property named http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress).

Here are the details you need to configure the service provider:

* **Authority/domain (e.g., https://account.oauth.sso.com)**
* **Client ID: ClientId**
* **Secret key**
* **Response Type, by default id\_token**
* **Scope: by default "openid profile email"**

To configure your authentication provider, you will need the following information:

* **The provided Redirect URI in this format: https://account.dastra.eu/signin-{schemeId}**

2. **Configuration of the Service Provider**

In dastra.eu, go to the [SSO administration page](https://app.dastra.eu/general-settings/sso) and click on "add an SSO login".

Fill in the form fields using the information from the entity configuration:



<figure><img src="../../../.gitbook/assets/openid2.png" alt=""><figcaption></figcaption></figure>



{% hint style="danger" %}
It is possible to force all users of the subscription account to use a specific SSO (by checking the box "force users to use this SSO"). Be cautious before activating this option, as if the SSO malfunctions, you will no longer be able to access your account as an administrator. It is preferable to manage the SSO on a per-user basis.
{% endhint %}

{% hint style="warning" %}
Special Cases of External Users Only accounts that are internal to a subscription will be subject to the SSO. Accounts of external users (who have an additional subscription) will not be subject to the SSO.
{% endhint %}

3. **Testing the SSO with OpenId**

Once the configuration is complete, you can test the authentication by clicking on the test button at the bottom right. If you encounter any problems during the SSO configuration, do not hesitate to approach support by going to the support ticket [management page](https://app.dastra.eu/general-settings/support).\


<figure><img src="../../../.gitbook/assets/openid3.png" alt=""><figcaption></figcaption></figure>
