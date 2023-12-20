# SMTP configuration

## Introduction

By default, Dastra routes a significant number of email notifications for the following services:&#x20;

* Real time [Notifications](notifications.md) (New comments, tasks, ...)
* Email exchanges as part of a rights exercise request
* Invitations to audits for respondents
* Invitations for new users

By default, Dastra uses its own SMTP service.

### How to configure your SMTP sending server?

{% hint style="warning" %}
Customizing SMTP can lead to platform instabilities. Only perform this manipulation if you are certain of the proper functioning and deliverability of your email sending service.
{% endhint %}

### Benefits of customizing SMTP

Dastra strives to ensure maximum availability and security for transactional email delivery. However, depending on your internal security policy, you may need to internalize the routing of transactional emails to control messaging flows.

### Prerequisites

You need to have the configuration details of your SMTP server:

* SMTP Host (e.g., smtp.yourservice.com)&#x20;
* SMTP Port (default is to use port 25)&#x20;
* Username&#x20;
* Password
* A valid sender email address (e.g., [noreply@yourservice.com](mailto:noreply@yourservice.com)): this address must be properly validated by your SMTP provider.

{% hint style="warning" %}
Note that your SMTP server must support a secure connection using SSL.
{% endhint %}

### Configuration

Go to the SMTP [server configuration page](https://app.dastra.eu/general-settings/smtp).&#x20;

Fill in the form fields using the data requested in the [prerequisites](configuration-du-smtp.md#prerequisites).

Note that server connectivity is automatically tested to ensure that the server login credentials are correct. A test email will be automatically sent from our servers.&#x20;

### Testing

Once you have submitted the form, your SMTP server should be operational. You can verify that the notification emails are indeed coming from your SMTP server. To do this, for example, create a comment in a process and see if you receive the notification email in your mailbox.

* **If you do not receive an email**: either you failed to trigger the notification, or there is a problem with your SMTP configuration.&#x20;
* **If you receive an email**: verify that your SMTP and sender are properly displayed in the email details.

{% hint style="info" %}
[How to view email details in GMAIL](https://app.gitbook.com/s/-LvBxs22wUMicv9uWp6C-2584506019/)

[How to view email details in Outlook](https://support.microsoft.com/fr-fr/office/afficher-les-en-t%C3%AAtes-de-message-internet-dans-outlook-cd039382-dc6e-4264-ac74-c048563d212c)
{% endhint %}
