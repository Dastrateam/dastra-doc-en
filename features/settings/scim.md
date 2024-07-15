---
description: On this page you will learn how to configure SCIM within Dastra
---

# SCIM

### How it works

SCIM (System for Cross-domain Identity Management) is an open standard for automating user provisioning. The SCIM protocol acts as an intermediary, collecting user identity data from identity providers (Azure AD, Google Workspace, Okta...) and communicating it to service providers (such as Dastra) who need the credentials.

{% hint style="info" %}
We strongly recommend that you first set up SSO with the "Force for all users" option enabled.
{% endhint %}

### How do I configure SCIM with Azure Active Directory?

Dastra users can be added, deleted and modified using SCIM 2.0.&#x20;

You define groups in your Azure Directory, and Dastra can synchronize these users. It's an ideal way to save time and hassle managing user accounts. It's also an ideal implementation of security.

#### 1. Log on to Azure and click on Azure Active Directory

<figure><img src="https://www.reftab.com/img/faq/01-azure.png" alt="01-Azure-SCIM"><figcaption></figcaption></figure>

#### 2. Go to "Enterprise applications".

<figure><img src="https://www.reftab.com/img/faq/02-azure.png" alt="01-Azure-SCIM"><figcaption></figcaption></figure>

#### 3. Click on "New application"

<figure><img src="https://www.reftab.com/img/faq/03-azure.png" alt="03-Azure-SCIM"><figcaption></figcaption></figure>

#### 4. Click on "Create your own application".

<figure><img src="https://www.reftab.com/img/faq/04-azure.png" alt="04-Azure-SCIM"><figcaption></figcaption></figure>

#### 5. Name your application

#### 6. In the newly created application, click on "Provision User Accounts".

<figure><img src="https://www.reftab.com/img/faq/06-azure.png" alt="06-Azure-SCIM"><figcaption></figcaption></figure>

#### 7. Click on "Get Started"

<figure><img src="https://www.reftab.com/img/faq/07-azure.png" alt="07-Azure-SCIM"><figcaption></figcaption></figure>

#### 8. Set provisioning mode to automatic. Fill in the tenant URL and secret token from your Dastra account information.

Log on to Dastra as administrator. Go to Organization configuration > click on Security / SCIM

![](<../../.gitbook/assets/image (196).png>)

Click on the "Configure" button

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

Configure your SCIM. Select the workspace you wish to synchronize (teams and users will be automatically provisioned in this workspace). Then choose the default role you wish to give to new users. Note that roles will be managed locally by the Dastra account administrator.&#x20;

Click on **Save changes**



{% hint style="info" %}
Today, Dastra lets you synchronize a single workspace per organization in SCIM (teams + users).
{% endhint %}

Click on "**Test connection**" and "**Save**".  If you encounter an error during the connection test, this may be due to a lack of activated functionality in your subscription. Please contact support

#### 9. Activate provisioning

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

#### 10. Add users and/or groups to the created application

<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

### Let your users log in to Dastra

You should see your AD user accounts automatically synchronized in Dastra. If they log in to Dastra via the login page, they should be able to log in with their e-mail. If SSO is not configured and enforced for all users, users will need to do a password reset to log in.&#x20;

If SSO is enabled and forced for all users, they will be automatically redirected to your identity provider's login form (Azure AD, Google Workspace, Okta...).



