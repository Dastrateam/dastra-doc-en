---
description: >-
  This chapter will teach you how to manage the consents of our cookie widget
  programmatically.
---

# Manage consent programmatically

## Where are the consents stored?

The entire proof of user consent is stored in the browser's localStorage (the storage key is named dastra-consents) in json format. The propagation of consents depends on it, that's why it's not recommended to directly modify the data of this key

{% hint style="info" %}
It's not recommended to directly modify the data in the localStorage. Preferably use the Javascript SDK of dastra.
{% endhint %}

### Access to the consent service

The dastra consent service can be accessed in this way:

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    console.log(manager.consent)
});
</script>
```

### List of methods available in the consent manager

In manager.consent, you have the following methods:

* open(): opens the consent widget
* close(): closes the consent widget
* getAllConsents(): retrieve all consents
* hasConsented(): returns `true` if the user has already recorded an explicit consent
* getPurposeConsent(purposeLabel:string): get consent for a cookie category
* setPurposeConsent(purposeLabel:string, consent:bool): set the consent for a category
* getServiceConsent(serviceShortName:string): retrieves consent for a particular service
* setServiceConsent(serviceShortName:string, consent:bool): sets the consent for a particular service

### Get the list of user's consents (getAllConsents)

Once you access the consent manager, it is very easy to retrieve the consents of the current user:

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady', function(manager){
    // Get the complete consent services list
    var consents = manager.consent.getAllConsents()
});
</script>
```

The above method returns a list of all the user's consents

```javascript
[
  {
    "id":"000000-0000000-000000",
    "name": "Service name",
    "purpose": 1,
    "logoUrl": "https://logo-url/img.jpg",
    "privacyPolicyUrl":"",
    "description": "Short description",
    "defaultConsent": true,
    "requiredConsent":true
  },
  ...
]
```

### Query consents by category (getPurposeConsent/setPurposeConsent)

Cookie categories are identified by the following string labels:

| Category     | Label          |
| ------------ | -------------- |
| Necessary    | `Necessary`    |
| Preferences  | `Preference`   |
| Analytics    | `Analytical`   |
| Marketing    | `Marketing`    |
| Other        | `Other`        |
| Unclassified | `Unclassified` |

{% hint style="warning" %}
Always use the **string labels** (e.g. `'Analytical'`) — numeric values are not supported by the API.
{% endhint %}

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    let consents = manager.consent.getPurposeConsent('Analytical');
    manager.consent.setPurposeConsent('Analytical', false);

    // persist consent
    manager.consent.save();
});
</script>
```

### Handle consents by service

To manipulate consents by service, you will need the simplified service name available in the service management interface of your widget.

{% hint style="info" %}
**How to find the simplified name of the service?**\
Go to the service management interface, when editing a service, the simplified name (slug) of the service appears below the cookie name.
{% endhint %}

![Location of simplified cookie name](<../../../.gitbook/assets/image (218).png>)

```javascript
<script> 
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    // Get the complete consent services list
    let cookiePurpose = 'google-analytics'; // 2 = Analytic
    let consents = manager.consent.getServiceConsent(cookiePurpose );
    manager.consent.setServicePurpose(cookiePurpose, false)
});
</script>
```

### Example of use

The following example shows how to apply a full opt-out programmatically — for instance when the user clicks a "Reject all" button you have built yourself, or when honouring a browser privacy signal.

```javascript
<script>
dastra = dastra || [];
dastra.push(['cookieReady', function(manager) {

  // Only act if the user hasn't already made an explicit choice
  if (!manager.consent.hasConsented()) {

    // Opt out of all non-essential categories
    manager.consent.setPurposeConsent('Preference',   false);
    manager.consent.setPurposeConsent('Analytical',   false);
    manager.consent.setPurposeConsent('Marketing',    false);
    manager.consent.setPurposeConsent('Other',        false);
    manager.consent.setPurposeConsent('Unclassified', false);

    // Persist the choice in the browser
    manager.consent.save();
  }

}]);
</script>
```

You can equally opt-in selectively — for example to accept analytics only:

```javascript
<script>
dastra = dastra || [];
dastra.push(['cookieReady', function(manager) {

  manager.consent.setPurposeConsent('Analytical', true);
  manager.consent.setPurposeConsent('Marketing',  false);
  manager.consent.save();

}]);
</script>
```

