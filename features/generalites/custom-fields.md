---
description: Dastra gives you the ability to customize your forms endlessly
---

# Custom fields

{% hint style="warning" %}
This feature is still in beta. It may still have some instabilities.
{% endhint %}

## When to use custom fields?

There may be some information specific to your industry that is not present in the native fields of the treatment register, such as rights exercises, tasks, etc.&#x20;

Dastra will allow you to create custom form fields that you can easily add to enrich the data entered.&#x20;

## Functionalities concerned

{% hint style="warning" %}
Please note! Not all features are concerned by custom fields
{% endhint %}

You can customize the following forms:&#x20;

* [Processing activities ](../editer-le-registre/)
* [Data subject right request](../gerer-les-exercices-des-droits/)
* [Tasks](../planifier/)&#x20;
* [Assets](../editer-le-registre/remplir-le-questionnaire/applications.md)&#x20;
* Actors&#x20;
* Measures&#x20;
* Data sets&#x20;
* Data fields&#x20;
* [Incidents](../notifier-les-violations-de-donnees/)
* [Risk assessments](../risk-management/attach-a-risk-to-a-processing-activity.md)

{% hint style="warning" %}
**Limitations on the number of fields**

The amount of custom fields is limited depending on the plan you use. We invite you to consult the [application's pricing page](https://www.dastra.eu/en/pricing) for more information on this subject.
{% endhint %}

## Available field types

Dastra offers several types of custom fields:&#x20;

* Simple text&#x20;
* Long text&#x20;
* Rich text&#x20;
* Whole number&#x20;
* Decimal number&#x20;
* Date&#x20;
* Date and time&#x20;
* Check box (multiple response) (**unfilterable**)&#x20;
* Check box (single response)&#x20;
* Single selector&#x20;
* Multiple selector&#x20;
* Check box (Yes/No)

## Using custom fields

You can:&#x20;

* View and edit custom field data in the forms of each module&#x20;
* Custom fields can be displayed in all the application's visualization tables. To display them, click on the table column settings button
* Custom fields are **present in all Excel data exports**. For more information on exports, see [the page on exports](../editer-le-registre/upload-your-existing-record.md)&#x20;
* Custom fields can be present in HTML, Word and PDF exports as an option (by checking the "Exportable in reports" box on the field in question)&#x20;
* **With the exception of multiple response fields**, custom fields are all filterable via the [advanced filter system](advanced-filters.md)
* Custom fields can be updated en masse in data tables&#x20;
* Custom fields can be imported via flat files using [the import system](importer-vos-donnees-excel-csv.md)&#x20;
* Custom fields **are accessible and modifiable via all APIs**. To do this, you will need to use the variable name assigned to each column. See the section on [API modifications of custom fields](custom-fields.md#handling-custom-fields-in-apis)

## Setting up custom fields

* Go to your **Workspace**
* Click on the **Workspace Settings** menu on the left
* Click on the **Custom fields** menu
* Choose the module in which you want to add a custom field
* Fields must be created in groups. These groups can be positioned in a certain way in the form Click on "**Create a group of fields**"

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 15.06.51.png" alt=""><figcaption></figcaption></figure>

**Fill in the name and location** in the form that you want

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 15.08.23.png" alt=""><figcaption></figcaption></figure>

For some elements, it is possible to define the location you want in the form!&#x20;

* Once the group is created, you can now **drag and drop the field types** you want to set up!

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 15.11.17.png" alt=""><figcaption></figcaption></figure>

Fill in all the information! Click on save and that's it!&#x20;

* Your first personal data field is in place!&#x20;
* You can drag and drop to reorder the fields as you see fit.

## Handling custom fields in APIs

Dastra allows you to retrieve, modify and create via the Rest API all entity values that include custom fields.&#x20;

A "customFields" property will be available in all entities you retrieve in get in Dastra.c:

```json
 {
   "id": 1234,
   "label": "Test asset",
   etc...
   "customFields": {
     "dpo_name":"jean-marc le dpo",
     "dpo_email":"dpo@github.com",
     "dpo_habilitations": ["Expert","Consulting","Data Mapping"],
     "has_large_dataset":false,
     etc...
   }
 }s
```

To modify this property, you just have to post (POST) or modify (PUT) the element by updating the elements of the collection.

To collect the name of the custom variables, you must go to the custom fields configuration page.

{% hint style="info" %}
Attention, all custom fields will be validated by the server. If a colonen is not present in the configuration, it will be automatically deleted.&#x20;

If a field is not valid (for example, if it's not filled in even though it's marked as mandatory), it will raise an exception with the code 400
{% endhint %}

## Limitations

You cannot **filter custom fields of the multiple type (checkbox (Multiple) and selector (Multiple))**. This is a known limitation that we are working on.
