# Functioning of the widget

## Overall operation:

Overall, the consent widget works in 3 main steps:&#x20;

1. The **proposal** of the consent window&#x20;
2. The **collection** of consent (storage of evidence)&#x20;
3. The actual **execution** of the user's consent

{% hint style="info" %}
The Dastra widget can cover the first two steps partially automatically. For the third step of actually enforcing the user's cookie preferences, you will need to technically integrate the consent system with third-party services that may potentially set cookies. See the [Blocking Cookies Guide](blocage-des-cookies/) for more information.
{% endhint %}

The widget's javascript SDK must be called on all pages of the site using cookies.

<mark style="color:red;">/IMAGE</mark>

### 1. Visit to the client's website

The user visits the website where the js code snippet is installed. In order not to impact the performance and the SEO of the web pages, the SDK is loaded in a totally asynchronous way with a one day caching period.

### 2. and 3. : Collect and cache the widget configuration

For the widget to work properly on the site, it will need an up-to-date client configuration retrieved from the Dastra servers. To get the freshest version possible, it will make a GET request of the widget with the public API key to check the widget's membership to the client.

{% hint style="info" %}
If the client has not correctly entered his domain in the widget editor, the editor will not allow the request and it will be impossible to display the widget correctly. To fix this, go to [this page](https://app.dastra.eu/workspace/1449/cookie-widget/list), choose your widget and add the missing domain.
{% endhint %}

### 4. Requesting consent from the user

If the "euconsent" cookie (you can choose the name of the cookie if you wish) is missing, the consent window will appear. To test if the widget is displayed correctly, you can delete this cookie from your browser.

### 5. Collecting consent

Consents will be automatically collected by the Dastra API via a POST request in json.&#x20;

Although in the widget interface, the expression of consent is done by purpose, the storage is done by service.&#x20;

Here is what the proof of consent looks like as stored in our databases:

```json
{
    "id": "6185fe65-0924-410d-9132-3cde838c4627",
    "sessionId": "0b93b823-ff36-4d61-8959-e9e8deee5ef8",
    "date": "2020-05-19T16:54:03.272Z",
    "dateExpiration": "2020-11-19T16:54:03.272Z",
    "type": 2,
    "widgetId": 43,
    "typeDevice": 2,
    "workSpaceId": 19,
    "consentId": "8a5e89c4-2243-4598-97c5-ba3cfb35a138",
    "consents": {
        "lang": "fr-FR",
        "versionKey": null,
        "cookieConsents": [
            {
                "id": "584ffef3-251c-4e9a-efb8-08d7fbfbee92",
                "tenantId": 0,
                "name": "Drift",
                "slug": "drift",
                "consent": true,
                "version": "6f65cb1d-85eb-4a64-976d-519679189f8d",
                "date": "2020-05-19T16:53:59.511Z",
                "purpose": 3
            }, {
                "id": "1c3baa61-0d05-44e4-da3d-08d7eeadee05",
                "tenantId": 0,
                "name": "Google Analytics (universal)",
                "slug": "analytics",
                "consent": true,
                "version": "6f65cb1d-85eb-4a64-976d-519679189f8d",
                "date": "2020-05-19T16:54:00.568Z",
                "purpose": 2
            }
        ]
    }
}
```

In return, the api will return a string named "consentId" which will then be stored in the browser in the localStorage for up to 180 days. This string is the unique identifier of the consent proof. In the case of a dispute, it's this identifier that will be searched in the client's browser.

### 6. Execution of consent

Once we have collected the user's consent, it's now necessary to actually carry out the user's wish by transmitting the consent information to all the services on the site.&#x20;

For this phase, we invite you to consult the guide on blocking cookies:

{% content-ref url="blocage-des-cookies/" %}
[blocage-des-cookies](blocage-des-cookies/)
{% endcontent-ref %}

{% hint style="info" %}
With the exception of strictly necessary cookies, all third-party tracking services should be blocked by default.
{% endhint %}

Congratulations, you are ready to start the technical integration of the widget:

{% content-ref url="quick-start/" %}
[quick-start](quick-start/)
{% endcontent-ref %}
