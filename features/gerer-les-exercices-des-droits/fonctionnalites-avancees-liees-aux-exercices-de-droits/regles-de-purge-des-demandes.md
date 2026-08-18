# Request purge rules

{% hint style="info" %}
You must have **administrator rights** on the workspace to access this feature.
{% endhint %}

You can **automate the purging of requests moved to the trash** in order to comply with your internal retention policies, and in particular the storage limitation principle set out by the GDPR.

This feature lets you define:

* the **scope** of requests covered by the purge,
* the **processing mode** (deletion or anonymization),
* and the **maximum retention period** before automatic triggering.

***

#### 🔍 Data selection criteria

The purge applies **only to requests present in the trash**.\
Requests still being processed, closed, or archived **are not affected**.

Every night, Dastra checks requests based on their **date moved to trash**.\
If a request exceeds the configured maximum duration (for example, 180 days), it becomes eligible for purging.

**The following are therefore affected:**

* Requests **moved to trash** for longer than the configured duration;
* All types of requests (access, deletion, objection, etc.);
* Regardless of their origin (portal, API, import).

***

#### ⚙️ Available purge modes

**1. Deleting requests**

The requests concerned are **permanently deleted** from the system.\
This action is **irreversible**.

Effects:

* Personal data and the content of exchanges are permanently deleted;
* Attachments and associated files are erased;
* Audit logs retain only technical metadata (timestamp, user, operation).

***

**2. Anonymizing requests**

The requests remain visible in Dastra, but **all the personal data** they contain is **replaced with fictitious values**.

This option lets you keep a **non-identifiable statistical record** for your reports and indicators.

Specifically:

* Fields containing personal data (last name, first name, email, ID, message, etc.) are replaced with generic values (`John DOE`, `anonymized@example.com`, `XXXXXX`);
* Attachments are deleted;
* Non-identifying metadata (request type, status, dates) is retained for reporting.
* The associated activity logs are purged

> 💡 **Goal:** enable statistical tracking while guaranteeing the deletion of any identifiable information.

<figure><img src="../../../.gitbook/assets/dsr-settings-purge-rules.png" alt=""><figcaption></figcaption></figure>

***

#### ⏱️ Setting the delay before purging

A setting lets you define the **maximum age of a request in the trash** before it is purged (for example: 180 days).\
This delay is calculated from the **date the request was moved to trash**.

Every night at midnight (UTC), Dastra retrieves the requests concerned and automatically runs the purge according to the selected mode.

***

#### 🧩 Configuration example

* **Purge mode:** Deleting requests
* **Maximum duration:** 180 days (6 months)

\
➡️ Every night, all requests moved to trash more than 180 days ago will be automatically deleted.

***

#### ✅ Best practices

* Set a retention period consistent with your internal request retention policy (for example, 5 years or 1825 days).
* Use **deletion** for complete erasure.
* Use **anonymization** if you want to keep activity statistics.
* Check that automatic purging is **enabled** so that processing runs every night.
