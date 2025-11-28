# Integration of external providers (Office 365 / Gmail)

## 📌 Objective <a href="#objectif" id="objectif"></a>

By default, all notifications sent by Dastra come from the address no-reply@dastra.eu. Thanks to integration with your external email providers (Office 365 or Gmail), you can configure sending via your own email addresses, allowing you to:<br>

* Build trust with your recipients (emails sent with your domain).
* Centralize your sending and deliverability logs directly in your email infrastructure.
* Manage your own security, compliance, and archiving rules.

***

## 📩 Scope of emails concerned <a href="#perimetre-des-mails-concernes" id="perimetre-des-mails-concernes"></a>

This configuration applies to all notification emails sent by Dastra within your organization, for example:

* Notifications of new tasks or requests.
* Invitations and reminders.
* Compliance alerts.
* Tracking requests to exercise rights, incidents, workflows, etc.

👉 In other words, all outgoing emails will replace no-reply@dastra.eu with the configured address.

> ⚠️ Please note: this applies to all emails sent from the organization. All workspaces will be affected.

***

## ⚙️ Integration configuration <a href="#configuration-de-lintegration" id="configuration-de-lintegration"></a>

### Step 1: Access the supplier integration and authorize the connection

* Go to Workspace Settings > Integrations.
* Click Add a configuration for Office 365 or Gmail.

You can also access the configuration from this URL: [https://app.dastra.eu/general-settings/smtp](https://app.dastra.eu/general-settings/smtp)

![](<../../../.gitbook/assets/Capture d'écran 2025-09-19 110910.png>)

* Select the provider you want to use :
  * **Microsoft 365 (Office 365)**
  * **Google (Gmail / Google Workspace)**
* When adding for the first time, Dastra will ask you to authorize the connection :
  * A window will open for you to authenticate via OAuth with Microsoft or Google.
  * You must use an account with sufficient rights (e.g., an account with administrator privileges or permission to send on behalf of the domain).
* Once authentication is successful, Dastra will confirm the connection and display the sender configuration screen.

⚠️ Please note: this step is essential for Dastra to be authorized to send emails via your provider. Without it, the sender configuration will not be effective.

### Step 2: Fill in the requested information

![](<../../../.gitbook/assets/Capture d'écran 2025-09-19 111634.png>)

Two mandatory fields must be filled in:

1. **Sender email**
   * The email address that will be used as the sender of notifications (example: `notifications@yourdomaine.com`).
2. **Sender alias**
   * The name displayed as the sender (example:`Compliance team - Your company`).

Once completed, click Save and Test to validate the configuration.

### Step 3: Verification and testing

* Dastra will perform a test send to confirm the validity of the configured address.
* Check your inbox and your Office 365/Gmail logs to ensure that the test message has been delivered.

The message will look like this :

![](https://doc.dastra.eu/~gitbook/image?url=https%3A%2F%2F1301193153-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LvBxs22wUMicv9uWp6C-2584506019%252Fuploads%252FhyrKMIgfbDpIjYCWBGfJ%252Fimage.png%3Falt%3Dmedia%26token%3D1b54be65-be71-4723-877c-3ee444de40f1\&width=768\&dpr=4\&quality=100\&sign=e465d1ed\&sv=2)

***

## ✅ Important points to remember <a href="#points-importants-a-retenir" id="points-importants-a-retenir"></a>

1. **Responsibility for logs**
   * By using your own provider (Office 365 or Gmail), **you are in control of your sending logs.**
   * Information related to email delivery, rejection, or blocking is no longer visible to Dastra teams.
2. **IP/domain reputation management**
   * Your infrastructure (Office 365 or Gmail) is responsible for ensuring good deliverability.
   * Make sure that :
     * Your SPF/DKIM/DMARC records are configured correctly.
     * Your sender reputation is good.
     * Your domain and IP are not listed as spam.
3. **Impact on your recipients**
   * Notifications will appear as if they were sent directly by your organization.
   * This facilitates recognition and reduces the risk of confusion with generic addresses.

***

## 🔒 Security best practices <a href="#bonnes-pratiques-de-securite" id="bonnes-pratiques-de-securite"></a>

* Limit the addresses used for sending (example : `no-reply@yourdomain.com` or `notifications@yourdomain.com`).
* Enable multi-factor authentication on accounts used for integration.
* Regularly monitor your sending logs in Office 365/Gmail to identify any anomalies.

***

👉 Once integration is enabled, Dastra will no longer use no-reply@dastra.eu: all your notification emails will be sent via your configured provider.
