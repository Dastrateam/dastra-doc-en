---
description: Learn how to create and modify an audit template or DPIA with Dastra.
---

# Create or modify an audit template or DPIA

## Introduction

Creating or modifying an audit template or PIA in Dastra is a breeze. To do so, access the "Audit" functionality.

## Create or modify an audit / PIA template

To create an audit or PIA template, click the "Create Template" button on the "Audit" tab. Then you can select one of the 3 types of audit templates that exist in Dastra: automated, combined or custom.

<figure><img src="../../.gitbook/assets/Create audit.png" alt=""><figcaption></figcaption></figure>

This brings you to the template type selection interface:

<figure><img src="../../.gitbook/assets/Audit type.png" alt=""><figcaption></figcaption></figure>

* By clicking on the "Automated Audit" tab, you will choose an existing predefined audit template from the Dastra Audit Library.&#x20;
* By clicking on "Combined Audit" will combine multiple audits into one.&#x20;
* By clicking on "Custom Audit" you can build your own audit template.

{% hint style="info" %}
Unlike automated audits, custom audits are fully customisable. Based on the answers selected by respondents, you will be able to automatically generate an action plan or map the risks associated with the model.
{% endhint %}

## Create a PIA template

PIA templates are included in the automated audit templates and are freely accessible from the Dastra library. To create or modify a PIA template, click on "Automated Audit", then select "PIA (CNIL) - Privacy Impact Analysis" before clicking "save".

{% hint style="info" %}
In Dastra, PIAs are one of several automated audit models.
{% endhint %}

<figure><img src="../../.gitbook/assets/automatic audit.png" alt=""><figcaption></figcaption></figure>

Once you have selected the template, you will be taken to the planning screen where you can perform one of the 2 actions below:

* either modify the template by clicking on the "Modify template" button or&#x20;
* schedule an audit by clicking on the "Schedule an audit" button

{% hint style="info" %}
For PIAs, an additional option is possible, if applicable: import your PIA from the CNIL tool. To do this, click on the "Import your CNIL PIA" button.&#x20;

Indeed, it is possible to import a PIA made by the CNIL tool. The CNIL PIA must be extracted in .json format and imported into Dastra.&#x20;

A large part of the elements will be included in the Dastra PIA.
{% endhint %}

<figure><img src="../../.gitbook/assets/PIA CNIL.png" alt=""><figcaption></figcaption></figure>

## Automated audit templates&#x20;

Dastra offers a number of automated audit templates to document compliance and drive processes.&#x20;

For example, templates for legitimate interest assessment (LIA) and transfer out of the EU (TIA) are included in the application.

## Customised audit templates

In Dastra, you can create your own custom audit template. To do this, click on the "Custom Audit" option. This will take you to the audit template editing interface.&#x20;

Build the audit template you want and click on "Save and Continue".

<figure><img src="../../.gitbook/assets/Creation assessement template 2.png" alt=""><figcaption></figcaption></figure>

## Items audited

You can link audits to items in Dastra. By choosing the type of item being audited, you force all audit responses based on that template to be linked to an object of the chosen type. For example, you can choose that this audit template will always be linked to a process.

<figure><img src="../../.gitbook/assets/Element audité.png" alt=""><figcaption></figcaption></figure>

You can choose not to link an audit to a particular object. In this case, the response will always be linked to an organisational unit. This may be the case for global compliance audits for example.

## Types of templates

When creating a custom template, you will need to choose a template type.

<figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

These types allow for some customisation of audit models.&#x20;

* **Standard audit**: this is a standard questionnaire&#x20;
* **Compliance audit**: currently a standard questionnaire&#x20;
* **Impact analysis**: this audit template allows a risk matrix to be displayed (with the required configuration) and to be called up at the PIA stage of a processing operation&#x20;
* **Subcontractor audit**: this audit template is called at the subcontractor recipients stage of a processing operation&#x20;
* **Transfer Impact Audit (TIA)**: an audit to analyse the risks related to a data transfer outside the EU&#x20;
* **Legal Basis Audit of the Register (LIA)**: audit of the legal basis of legitimate interests to ensure that the interests do not override the rights and freedoms of individuals&#x20;
* **Training questionnaire**: a questionnaire for conducting training quizzes. This type of questionnaire makes it possible to select a correct answer from the answers and to display the correct answers at the end of the questionnaire.

## Combined audit templates

In Dastra, you can combine several existing audit templates into one. To do this, select the "Combined Audit" option and follow the steps.

## Load an audit template you own

Finally, it is possible to import one of your audit templates, in json format. To do this, when creating the audit, select the "Load a template" option.

## Go further

{% content-ref url="scheduling-an-audit-or-a-pia.md" %}
[scheduling-an-audit-or-a-pia.md](scheduling-an-audit-or-a-pia.md)
{% endcontent-ref %}

{% content-ref url="share-an-audit-report-or-pia.md" %}
[share-an-audit-report-or-pia.md](share-an-audit-report-or-pia.md)
{% endcontent-ref %}
