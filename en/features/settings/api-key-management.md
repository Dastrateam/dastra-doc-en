# API key management

### What are API keys used for?

* **Create a Dastra API client** to retrieve or modify data outside the application. This client can be server-to-server (Client credential) or javascript (Authorization code). To find out more, please [read the Dastra API authentication documentation](../gerer-les-exercices-des-droits/api-integration.md).
* **Configure a data subject right request form** (public key only). Read the[ documentation about DSR forms](../gerer-les-exercices-des-droits/implementez-un-widget-dexercice-des-droits.md).
* **Configure a cookie widget** (public key only). Read the [documentation related to cookies](../gerer-le-consentement-aux-cookies/configuration-du-widget/implementez-un-widget-de-consentement-aux-cookies.md).

### How generate an API key?

1. Access the [Dastra Key Manager](https://app.dastra.eu/general-settings/api) (Only tenant owners have access to this section)
2. Click on Create a new API Key
3. Enter the name of the key and the redirection and cors urls (if you want to use the javascript API in OAuth2)
4. Click on "save".
5. Once you have created your API key, you can copy and paste it directly from the manager (private or public key).

{% hint style="warning" %}
**Keep your API keys safe! The private key must never be made public!**

**If the security of your API key is compromised**, you can delete it from the manager and/or generate a new one.
{% endhint %}
