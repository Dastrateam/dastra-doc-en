---
description: This page details the implementation of SSO within Dastra
---

# Single Sign On (SSO)

**Working Principle Single**

Sign-on (SSO), a method that allows a user to access multiple computer applications (or secure websites) by only undergoing a single authentication process, is often referred to by its English acronym, SSO (from single sign-on).

A company can use its own authentication system instead of the default local login provided by Dastra. Among the most used SSO systems, one can mention Microsoft Active Directory, Google Workspace (formerly GSuite), Auth0, etc.

**The process works as follows:**

A user (User Agent) will request a connection to the service provider (Service Provider) who will in turn solicit an identity provider (Identity Provider) to authenticate the user. This authentication is then sent back to the service provider who will accept the user's connection request.&#x20;

In our case, the User Agent is a Dastra user's browser. The Service Provider is Dastra, and the Identity Provider is your preferred authentication provider (for example: Active Directory).

<figure><img src="../../../.gitbook/assets/sso&#x26;.png" alt=""><figcaption></figcaption></figure>

**Implementation**

Within a Dastra subscription, you have the option, if you have subscribed to the feature, to manage one or several SSO logins. To access the SSO configuration, go to the [SSO login configuration page](https://app.dastra.eu/general-settings/sso) in the security tab of the subscription account configuration panel.

{% hint style="info" %}
Note: You must be the owner of the organization to access this page.
{% endhint %}

Dastra offers two single sign-on authentication protocols, [SAML 2](https://app.gitbook.com/s/-LvBxs22wUMicv9uWp6C-2584506019/features/settings/single-sign-on-sso/saml-2) and [Open ID](https://app.gitbook.com/s/-LvBxs22wUMicv9uWp6C-2584506019/features/settings/single-sign-on-sso/openid). To access configuration assistance, click on the links below.



{% content-ref url="saml-2.md" %}
[saml-2.md](saml-2.md)
{% endcontent-ref %}

{% content-ref url="openid.md" %}
[openid.md](openid.md)
{% endcontent-ref %}

{% content-ref url="adfs.md" %}
[adfs.md](adfs.md)
{% endcontent-ref %}



**How to Enable Automatic User Provisioning?**



If you want users from your identity provider not to need to create accounts to access the entity, you can check the box "automatic user provisioning." If you provide your users with an SSO provider URL like this one:

https://account.dastra.eu/account/loginexternal?provider={your provider id}\&returnUrl=https://www.dastra.eu

\=> in the case of validated authentication, they will automatically have an account created in Dastra and a notification mail will be sent to you a few hours later.



{% hint style="warning" %}
If the user's account is deleted or invalidated in the authentication provider, their account will not be erased in Dastra, but they will no longer be able to connect. You have the option to purge these accounts via the [user manager of the subscription](https://app.dastra.eu/general-settings/users?q=\&page=1\&size=20).
{% endhint %}

You can choose **the default role assigned** across all organizations associated with your subscription.



{% hint style="info" %}
Currently, Dastra does not support binding roles through the properties of the authentication server. If this feature is important to you, you can report it to us via the [support page](https://app.dastra.eu/general-settings/support).
{% endhint %}





**Team Binding**

It is possible to bind teams of a workspace to a property (Claim) returned by your authentication servers.



**How to Administer User Logins?**

You can configure the type of user login by going to the user management page of the subscription. By visiting a user profile, it will be possible to choose the preferred SSO login.

From then on, the user who connects to Dastra with their email address will be automatically redirected to the login page of the authentication provider you have set up.

You can also define the type of login when inviting new users.
