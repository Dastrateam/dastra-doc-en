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

* open(): opens the consent widget&#x20;
* close(): close the consent widget&#x20;
* getAllConsents() : retrieve all consents&#x20;
* getPurposeConsent(purposeId:number): get consent for a category of cookies&#x20;
* setPurposeConsent(purposeId:number, consent:bool): set the consent for a category&#x20;
* getServiceConsent(serviceShortName:string): Retrieves consent for a particular service
* setServiceConsent(serviceShortName:string, consent:bool): Sets the consent for a particular element

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

The categories of cookies are represented by the following ids:

| Type        | Id |
| ----------- | -- |
| Necessary   | 0  |
| Preferences | 1  |
| Analytical  | 2  |
| Marketing   | 3  |
| Other       | 4  |

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    // Get the complete consent services list
    let cookiePurpose = 2; // 2 = Analytic
    let consents = manager.consent.getPurposeConsent(cookiePurpose);
    manager.consent.setPurposeConsent(cookiePurpose, false)
});
</script>
```

### Handle consents by service

To manipulate consents by service, you will need the simplified service name available in the service management interface of your widget.

{% hint style="info" %}
**How to find the simplified name of the service?**\
Go to the service management interface, when editing a service, the simplified name (slug) of the service appears below the cookie name.
{% endhint %}

![Emplacement du nom du cookies simplifié](<../../../.gitbook/assets/image (218).png>)

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

### Exemple d'utilisation

Pour illustrer la chose, voici un exemple complet qui permet de manipuler les consentements dans le navigateur sans utiliser le widget :



```javascript
todo
```

