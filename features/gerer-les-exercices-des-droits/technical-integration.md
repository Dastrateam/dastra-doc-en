---
description: >-
  This article shows you how to integrate the data subject right request widget
  into a web page
---

# Technical integration

## Purpose

The data subject right request widget allows you to automatically collect from a page of your site data subject right request of various types (deletions, modifications, rectifications...)&#x20;

The widget is integrated to the dastra javascript SDK.

## Prerequisites

In order to set up thedata subject right request widget, you need an API public key: read the documentation or go directly to the API key management page

## Setting up the widget in the dedicated interface

To start with, you need to set up the widget in the rights exercise widget management panel:

<figure><img src="../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

Here is a simple example of how to integrate the widget (in popup mode with an open button):

```html
<div id="customer-subject-form-custom" ></div>
<button id="customer-request-button">Open the widget</button>
<script src="https://cdn.dastra.eu/sdk/dastra.js?key={YOUR PUBLIC KEY}" async></script>
<script>
  window.dastra = window.dastra || [];
  dastra.debug = true;
  window.dastra.push(function(){
    dastra.loadCustomerSubjectForm({
      selector: '#customer-subject-form-custom',
      widgetId: {your widget id},
      onLoad: function (form) {
        document.getElementById('customer-request-button').addEventListener('click',function () {
          form.open()
        })
      }
    })
  })
</script>
```

## How to force the language of the form?

By default, the browser language will be taken. If the language is not available in the widget translations, the default language will be selected automatically. You can force the current language of the widget by adding the data-lang property to the div where the form will be displayed.

In this example, the Italian language will be selected by default (if available)

```html
<div id="customer-subject-popup" data-lang="it"></div>
```

## How to automatically send form values to the widget?

```html
<script>
  var myCustomerId = '{your custom userId}';
  dastra.push(['set','dsr:refId', myCustomerId ]);
</script>
```

You can replace the name of the refId column with the following property name:

* refId : the unique identifier of the user
* familyName
* givenName
* email
* city
* zipCode
* countryCode
* address
* phoneNumber
* message
* additionalDatas

\*For the specific case of custom fields, you must reference the name additionalDatas :

```html
<script>
  var payload = {
    customFieldSlug1: 'test', 
    customFieldSlug2: 'test'
  };
  
  // You can use this synthax for setting global custom fields as an object
  dastra.push(['set','dsr:additionalDatas', payload]);
  
   // Or directly for a single field, use the prefix @
   dastra.push(['set','dsr:@customFieldSlug1', 'test']);
</script>
```

Additional fields will be automatically merged

## Sending parameters using page mode

It is also possible to pass these parameters using querystring parameters, just prefix the parameter name with dsr\_ :

```
https://api.dastra.eu/v1/client/customer-subject-form?id=<Your widget id>
&key=<your public key>
&dsr_email=test@github.org
&dsr_givenName=Dastonaute
&dsr_refId=123456
&...etc...
```
