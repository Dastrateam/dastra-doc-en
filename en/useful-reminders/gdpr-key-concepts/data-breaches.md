---
description: Learn how to manage data breach notifications.
---

# Data breaches

### 📖 Definition

According to [Article 4.12 of the GDPR](https://gdpr-info.eu/art-4-gdpr/), a **personal data breach** is:

> _A breach of security leading to the accidental or unlawful destruction, loss, alteration, unauthorised disclosure of, or access to, personal data transmitted, stored or otherwise processed._

In other words, it is any **security incident**, whether **intentional or accidental**, that compromises:

* **Confidentiality** (unauthorised access, disclosure),
* **Integrity** (alteration, falsification),
* **Availability** (loss, deletion, unavailability).

***

### ⚠️ Typical examples

* Accidental deletion of medical data not saved elsewhere.
* Loss of an unencrypted USB key containing a customer database.
* Server hack exposing email addresses and passwords.
* Email containing personal data sent to the wrong recipient.
* HR information leak on an unsecured shared space.

***

### 🧩 Three main types of breach

| Type                | Description                                | Example                              |
| ------------------- | ------------------------------------------ | ------------------------------------ |
| **Confidentiality** | Unauthorised access or disclosure          | Data leak through phishing           |
| **Integrity**       | Unauthorised modification or falsification | Alteration of a medical record       |
| **Availability**    | Accidental loss or destruction             | Data deleted without backup          |

***

### 🕓 Legal obligations for the data controller

#### 1️⃣ Notification to the supervisory authority

* **Deadline**: 72 hours after becoming aware of the breach.
* **Content**: nature of the breach, categories and volume of data involved, likely consequences, measures taken or planned.

> If notification cannot be made within 72 hours, the **delay must be justified**.

📚 Reference: [Article 33 of the GDPR](https://gdpr-info.eu/art-33-gdpr/)

***

#### 2️⃣ Communication to data subjects

If the breach **presents a high risk to individuals' rights and freedoms**, they must be informed **without undue delay**: nature of the breach, data affected, measures taken, recommendations (e.g. change password).

📚 Reference: [Article 34 of the GDPR](https://gdpr-info.eu/art-34-gdpr/)

***

#### 3️⃣ Mandatory internal documentation

Even when no notification is required, **every breach must be recorded** in an internal register (facts, effects, corrective measures). This allows you to **demonstrate compliance** (accountability).

***

### 🔁 The breach management cycle

1. **Detection** → Identification of an incident or abnormal behaviour.
2. **Qualification** → Verify whether personal data is involved.
3. **Risk assessment** → Impact on individuals' privacy.
4. **Notification (if required)** → Supervisory authority within 72h, data subjects if high risk.
5. **Remediation** → Corrective and preventive measures.
6. **Documentation** → Entry in the breach register.
7. **Lessons learned** → Organisational or technical adjustments.

***

### 🧠 Security best practices

* Prepare an **incident management plan** and test it regularly.
* Train teams on **rapid detection and escalation** of incidents.
* Implement **preventive measures** (MFA, network segmentation, backups).
* Use a **centralised register** to track each breach and its resolution.

***

### 🧾 Managing breaches in Dastra

| Step         | Dastra feature                                                  |
| ------------ | --------------------------------------------------------------- |
| Declaration  | Customisable breach report form                                 |
| Assessment   | Automatic risk calculation for individuals' rights              |
| Notification | Report generation for the DPA and communication to data subjects |
| Monitoring   | Action log and remediation plan                                 |
| Reporting    | Dashboards and compliance indicators                            |

***

### 📚 Useful resources

* [ICO – Reporting a data breach](https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/personal-data-breaches/)
* [ENISA – Data Breach Notification Guidelines](https://www.enisa.europa.eu/)

***

{% hint style="success" %}
💡 **Good practice:** A quickly reported incident limits the impact, reinforces transparency and demonstrates compliance mastery. Dastra helps you structure and document each step of the process.
{% endhint %}

***

### 📘 For more information

{% content-ref url="../../features/notifier-les-violations-de-donnees/" %}
[notifier-les-violations-de-donnees](../../features/notifier-les-violations-de-donnees/)
{% endcontent-ref %}
