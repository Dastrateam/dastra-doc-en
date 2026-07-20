---
description: >-
  The item merge tool lets you merge items that are duplicates or have many
  similarities.
---

# Merging elements

## What the merge tool does

Dastra's **item merge** feature has been designed to simplify the management of duplicates and similar items in your compliance data. It lets you **combine several identical or similar items** into a single one, without having to manually perform the **complex linking to all the associated entities** (processing activities, controllers, records, etc.).

This feature aims to **ensure the consistency of your referential** while **limiting manual handling**, saving you time and increasing reliability.

## On which elements can the merge tool be used?

The merge tool can be used on:

* Processing activities
* Assets
* Stakeholders
* Datasets
* Data glossaries
* Measures
* Categories of data subject
* Tasks
* Compliance controls (applied controls and reference controls)
* Compliance tests (operational tests and reference tests)

{% hint style="info" %}
Merging compliance controls and tests is done from the library or the project of the Compliance module, via grouped actions. You can select up to 30 items to merge. For the details of this operation, see the [Controls](../compliance/library/controls.md) and [Tests](../compliance/library/tests.md) pages.
{% endhint %}

## How do I merge elements?

Simply select the items you wish to merge:

<div align="left"><figure><img src="../../.gitbook/assets/image-416-1.png" alt=""><figcaption><p><br></p></figcaption></figure></div>

Then click on "Choose a grouped action" and "Merge data":&#x20;

\
![](<../../.gitbook/assets/audit-questionnaire-icone-oblig-repondue.png>)



You will then be taken to a dedicated page that lets you:

Select the main element to be retained after merging.

Choose the fields of the elements to be deleted that you wish to retrieve into the main element.\
![](<../../.gitbook/assets/image-418.png>)

<figure><img src="../../.gitbook/assets/processing-merge-tool-field-comparison.png" alt=""><figcaption></figcaption></figure>

If fields do not appear on this page, the values of the fields in the retained element are automatically retained.\
\
You can then click the "Save" button to launch the merge.

{% hint style="info" %}
The entities (processing activities, analyses, etc.) associated with the deleted elements are automatically re-attached to the retained element, avoiding any loss or disconnection in your record.
{% endhint %}

## Data quality tool — automatic duplicate detection

Dastra includes a **data quality tool** that automatically scans your repository to detect potentially duplicate items, without requiring a manual pre-selection.

### How automatic detection works

The algorithm uses **explainable scoring**: for each pair of potential duplicates, it analyses several dimensions (name, publisher, organisational unit, URL, category) and assigns a **confidence score**. This score lets you make an informed decision before merging or deleting anything.

### Supported modules

The data quality tool is available for:

* Assets
* Measures
* Stakeholders
* Datasets
* Data glossaries
* Processing activities
* Categories of data subjects

### How to access the tool

In each of these modules, click the **main menu button** (⋮ or "Actions") and select **"Data quality tool"**. All detected duplicates are listed with their confidence score. You can then choose to **merge** or **delete** each identified duplicate.
