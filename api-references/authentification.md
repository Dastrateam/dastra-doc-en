---
description: Learn how to authenticate with Dastra API.
---

# Authentication

### Obtaining the secret API key&#x20;

The Dastra Rest API uses **API keys** to authenticate each request. You can manage your keys in your organization's configuration interface. You can use an API key for a specific workspace or for the entire organization. Your API key allows you to do many things, so keep it safe. Don't share your secret key in public parts of applications like GitHub, client code...etc.... If you wish to use OAuth2 authentication in "authorization\_code" mode, you'll need to configure the redirection url(s) and the authorized CORs origins.

### API key (X-API-Key)&#x20;

To authenticate yourself, the simplest way is to use an HTTP X-API-Key header containing the private key of your API key, as in the example below:

```bash
curl -X 'GET' \
  'https://api.dastra.eu/me' \
  -H 'accept: */*' \
  -H 'X-API-Key: <your private key here>'

```
