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

You can automatically send form values to the widget by using the `dastra.push` method. This method allows you to set various properties of the form widget, such as user identifiers and personal data fields.

Here's a simple example of how to pass additional user information to the form widget:

```html
<script>
  // Set the user's family name
  var familyName = 'Rossi'; // Replace with actual user's family name
  
  // Set the user's given name
  var givenName = 'Mario'; // Replace with actual user's given name
  
  // Push user information to the DSR form widget
  dastra.push(['set', 'dsr:familyName', familyName]);
  dastra.push(['set', 'dsr:givenName', givenName]);
  
  // Add more properties as needed, e.g., email, phone number
  // dastra.push(['set', 'dsr:email', userEmail]);
  // dastra.push(['set', 'dsr:phoneNumber', userPhoneNumber]);
</script>
```

Ensure you replace the placeholder values (`'Rossi'`, `'Mario'`, etc.) with the actual user data retrieved from your system. This approach helps personalize the user experience by pre-filling form fields with known data.

In the specific case of a custom userId (in session cookie for example), you can do it as following :

```html
<script>
  // Read your custom userId (e.g. in session cookie)
  var customerId = '{your custom userId}';
  
  // Send the customerId to the DSR form widget
  dastra.push(['set','dsr:refId', customerId ]);
</script>
```



You can replace the name of the refId column with the following property name :

* refId : the unique identifier of the user in your system (customerId, sessionId...). This column is not visible and will be not accessible to the customer.
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
