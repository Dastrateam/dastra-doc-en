---
description: Learn how to authenticate with Dastra API.
---

# Authentication

The Rest Dastra API uses API keys to authenticate each request. You can manage your keys in the configuration interface of your organization.

You can use an API key for an entity or the entire organization.

Your API key allows you to do a lot of things, which is why you must keep it preciously. Do not share your secret key in the public parts of applications like GitHub, client code etc.

API authentication is performed using the HTTP Basic Auth protocol. Provide your API key as a username. The password is not necessary (You can put a random one like 123).

```
curl https://api.dastra.eu/v1/actors\
  -u asdskdskgfdkghfdkhg:
# The colon prevents curl from asking for a password.
```

{% hint style="info" %}
Cross-origin requests are not allowed by the API. So never make requests to the REST API by passing the secret key in clear in the client side!

They will in any case be blocked by the browser with CORS
{% endhint %}

All requests must be made in HTTPS and always on the server side. Queries without authentication will fail with error code 401\
