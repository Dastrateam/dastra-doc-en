---
description: >-
  Learn how to refine the display of your reports in the data tables of all
  modules with the advanced filters
---

# Advanced Filters

## Use

Advanced filters allow you to filter your data on almost any field in your entities.

* Go to a Dastra module (for example, the data subject rights module)
* Click on the "Filters" button at the top right of the data table.

<figure><img src="../../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure>

* A small window will appear, showing you a list of the most commonly used standard filters, by applying one of these filters, the table will update automatically.

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption><p><em><mark style="color:$info;">Advanced filter combo for data subject requests</mark></em></p></figcaption></figure>

{% hint style="info" %}
Combo of advanced filters for exercise requests

_The combination of these filters is cumulative. For example: if I filter on one or two tags "Access" and "pending" + I select an organizational unit "Dastra SAS": it will show me all rows that contain the 2 tags "complex" and "pending" **and** that are in the organizational unit "Dastra SAS"._
{% endhint %}

* If you don't find any filters that suit you, you can click on the "Add filter" button. There you can edit the combination of filters that best suits your needs.

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

By default, Dastra persists the filters you select, which means that if you change pages or refresh your browser, the filters are retained. These filters are specific to your browser and workspace (they are stored in **LocalStorage**).

## Custom views

You can save the current state of your filters (and your column selection) as a **named view**, then switch between your views with a single click from the toolbar of each list.

To create a view  :

1. Apply the desired filters and column selection.
2. Click the **"Save"** button in the toolbar.
3. Give your view a name and confirm.

The view then appears directly in the toolbar of the relevant section — accessible with one click, without going back through the "Filters" panel.

<figure><img src="../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

You can also **share a view** with other users in your workspace. Shared views appear under the **"Shared views"** section in the toolbar.

<figure><img src="../../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure>

This feature is available in all sections listing objects: data subject right requests, processing records, assets, contracts, AI systems, data breaches…

## Known problems

### My data is not displayed anymore?

If you encounter difficulties with the filters: you lose the display of your data, we recommend you to clear the browser data (cookies, localstorage...). This will reset the status of your filters in your workspace.

### Some columns are not present in the advanced filters?

It may not be technically possible to set up these filters for various reasons. In this case, we recommend that you either export the data in a raw form, and run the report in tools like Excel.

If it's a filter that is essential to your business, do not hesitate to ask us for a new feature via the Dastra community or the request system.
