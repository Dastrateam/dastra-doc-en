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

Replace the "{your-service-slug}" with your service id entered when configuring your widget:

