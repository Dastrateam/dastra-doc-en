---
description: >-
  This page explains how to trace the organization's internal identifiers in the
  proof of consent
---

# User identification

## How it works&#x20;

The principle is the following: you send the **unique identifier of the authenticated user** in your intranet to the dastra widget and it will send this id when collecting the user's consent. This will make it possible to reconcile the proofs of consent with the customer base (CRM, customer base, customer repository or other...). Once in the proofs of consent viewing area, the pushed user id will be displayed.

### Step 1: Choose the user ID&#x20;

To make this match, you will need to choose a variable to transfer to the widget. You can use the user's base64 hashed email address, an internal customer ID or a CRM ID. This variable must be available in the web page and will be passed in plain text. It must not mention any personal information about the user (name, first name, email in clear text).

{% hint style="info" %}
If you send a base64 encoded string, it will be automatically decoded when the user consents are received in the Dastra database
{% endhint %}

### Step 2: Adapt the integration code

```ssml
<div id="cookie-consent"></div>
<script src="https://cdn.dastra.eu/sdk/dastra.js?key={YOUR PUBLIC KEY HERE}" async></script>
<script>
​
// Dastra's array's initialization
window.dastra = window.dastra || [];
​
// Load the cookie consent in page
dastra.push(['loadCookieConsent', {
    widgetId: {Paste your widgetId here (digit)},
    selector: '#cookie-consent',
    userId: {The userId's variable (email 64bits hash or whatever...)}
}]);
</script>
```

You can also use the "set" method

```ssml
<div id="cookie-consent"></div>
<script src="https://cdn.dastra.eu/sdk/dastra.js?key={YOUR PUBLIC KEY HERE}" async></script>
<script>

// Dastra's array's initialization
window.dastra = window.dastra || [];

// Load the cookie consent in page
dastra.push(['loadCookieConsent', {
    widgetId: {Paste your widgetId here (digit)},
    selector: '#cookie-consent'
}]);

// Push the userId to dastra's cookies
// It must be pushed after the loadCookieConsent method
dastra.push(['set','cookie:userId',{The userId's variable (email 64bits hash or whatever...)}])
</script>
```
