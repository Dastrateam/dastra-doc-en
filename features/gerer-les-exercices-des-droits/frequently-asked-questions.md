# Frequently Asked Questions

### Do applicants receive an email notification when a request is closed?

By default, no email is sent automatically. A closure notification is sent to the applicant **only if the "Send a closure notification to" checkbox** is explicitly checked at the time of closure.

{% hint style="info" %}
Make it a habit to check this option whenever you want to inform the data subject that their request has been resolved — it is a recommended practice for demonstrating compliance with the GDPR response deadline.
{% endhint %}

\---

### How long does the applicant retain access to the secure space after a request is closed?

Once a request is closed, the applicant retains access to their secure space (exchange history, transmitted documents) for **60 days**.

After this period, access is automatically revoked.

***

### Does the request collection page set any cookies? Is a consent banner required?

No. The Dastra widget page (URL of the form `https://api.dastra.eu/v1/client/data-subject-request/page?id=…`) sets **only one cookie**: `acaAffinity`.

This is a **load balancing cookie** (Azure Application Gateway), whose sole function is to maintain server session stability by routing requests to the same backend node. It is **session-scoped**, secured (`Secure`, `HttpOnly`), and falls within the **consent exemption** provided by Article 5§3 of the ePrivacy Directive, as confirmed by the guidelines of the French data protection authority (CNIL) for cookies strictly necessary for the operation of the service.

**No consent banner is required on this page.**

{% hint style="success" %}
Audit conducted on 27 April 2026: 0 analytics cookies, 0 advertising cookies, 0 third-party trackers detected. Third-party resources loaded (Bootstrap via cdnjs.cloudflare.com, Poppins font via fonts.bunny.net, SDK via cdn.dastra.eu) set no cookies.
{% endhint %}

\---

### Should the `acaAffinity` cookie appear in our cookie register?

Yes, for the sake of documentary completeness, even though it is exempt from consent. Below is the recommended register entry:

| Field            | Value                                        |
| ---------------- | -------------------------------------------- |
| Name             | `acaAffinity`                                |
| Domain           | `api.dastra.eu`                              |
| Category         | Technical / Strictly necessary               |
| Purpose          | Load balancing — server session stability    |
| Duration         | Session (deleted when the browser is closed) |
| Issuer           | Dastra (data processor)                      |
| Legal basis      | ePrivacy exemption — strictly necessary      |
| Consent required | No                                           |
