---
description: This guide will explain how to actually block cookies.
---

# Blocking cookies

A COMPLETER



To effectively block cookies, there are several possible methods: blocking a snippet, custom javascript or Google Tag Manage.

{% hint style="info" %}
Go to the service management interface, when editing a service, the simplified name (slug) of the service appears below the cookie name.
{% endhint %}

## Blocking a code snippet in the page

This method allows you to completely disable a code snippet for tracking the page.&#x20;

To do this, replace the following code snippet in the html code of your page:

```ssml
<script >
  alert("hello, I'm a tracking javascript tag");
</script>
```

By:

```ssml
<script data-consent="{your-service-slug}" type="dastra/script">
   alert("hello, I'm a tracking javascript tag");
</script>
```

Replace `{your-service-slug}` with the service slug configured in your widget (visible in the service editing interface, below the cookie name).

***

## FAQ

**Can I block a script by category instead of by service? (e.g. `data-consent="analytics"`)**

No. The `data-consent` attribute expects a **service slug**, not a category slug. Writing `<script data-consent="analytics" type="dastra/script">` to block all services in a category in one directive is not supported.

The reason: a user may accept some services within a category while refusing others in the same category. The widget manages consent at the service level, not the category level.

If you want to conditionally load a script based on whether an entire category has been accepted, use the programmatic API instead:

```javascript
window.addEventListener('dastra:consents:updated', function() {
  if (window.dastra.cookieConsent.consent.getPurposeConsent('Analytical')) {
    // load your analytics scripts here
  }
});
```

