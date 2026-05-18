---
description: Learn how to create and modify a questionnaire template with Dastra.
---

# Create or modify a questionnaire template

## Introduction

Creating or modifying a questionnaire template in Dastra is a breeze. To do so, access the "Questionnaires" functionality.

## Create or modify a questionnaire template

To create a questionnaire template, click the "Create Template" button on the "Questionnaires" tab. Then you can select one of the template types available in Dastra: automated, custom, or import from file.

<figure><img src="../../.gitbook/assets/Create audit.png" alt=""><figcaption></figcaption></figure>

This brings you to the template type selection interface:

<figure><img src="../../.gitbook/assets/Audit type.png" alt=""><figcaption></figcaption></figure>

* By clicking on the "Automated Questionnaire" tab, you will choose an existing predefined questionnaire template from the Dastra Questionnaire Library.
* By clicking on "Custom Questionnaire" you can build your own questionnaire template.

{% hint style="info" %}
Unlike automated questionnaires, custom questionnaires are fully customisable. Based on the answers selected by respondents, you will be able to automatically generate an action plan or map the risks associated with the model.
{% endhint %}

## Automated questionnaire templates

Dastra offers a number of automated questionnaire templates to document compliance and drive processes. These include templates for privacy impact analysis (PIA/DPIA), legitimate interests assessment (LIA), transfer impact assessment (TIA), processor assessments, and more.

<figure><img src="../../.gitbook/assets/automatic audit.png" alt=""><figcaption></figcaption></figure>

Once you have selected a template, you will be taken to the planning screen where you can either:

* modify the template by clicking on the "Modify template" button, or
* schedule a questionnaire by clicking on the "Schedule a questionnaire" button.

{% hint style="info" %}
Some questionnaire types (PIA, TIA, LIA) can also be launched directly from within a processing activity — for example from the "Impact assessment", "Recipients" or "Purposes" tabs. See the dedicated pages below for details.
{% endhint %}

## Customised questionnaire templates

In Dastra, you can create your own custom questionnaire template. To do this, click on the "Custom Questionnaire" option. This will take you to the questionnaire template editing interface.

Build the questionnaire template you want and click on "Save and Continue".

<figure><img src="../../.gitbook/assets/Creation assessement template 2.png" alt=""><figcaption></figcaption></figure>

## Items assessed

You can link questionnaires to items in Dastra. By choosing the type of item being assessed, you force all questionnaire responses based on that template to be linked to an object of the chosen type. For example, you can choose that this questionnaire template will always be linked to a process.

<figure><img src="../../.gitbook/assets/Element audité.png" alt=""><figcaption></figcaption></figure>

You can choose not to link a questionnaire to a particular object. In this case, the response will always be linked to an organisational unit. This may be the case for global compliance questionnaires for example.

## Types of templates

When creating a custom template, you will need to choose a template type.

<figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

These types allow for some customisation of questionnaire models.

* **Standard questionnaire**: this is a standard questionnaire
* **Compliance questionnaire**: currently a standard questionnaire
* **Impact analysis**: this questionnaire template allows a risk matrix to be displayed (with the required configuration) and to be called up at the PIA stage of a processing activity
* **Subcontractor questionnaire**: this questionnaire template is called at the subcontractor recipients stage of a processing activity
* **Transfer Impact Assessment (TIA)**: a questionnaire to analyse the risks related to a data transfer outside the EU
* **Legitimate Interest Assessment (LIA)**: questionnaire of the legal basis of legitimate interests to ensure that the interests do not override the rights and freedoms of individuals
* **Training questionnaire**: a questionnaire for conducting training quizzes. This type of questionnaire makes it possible to select a correct answer from the answers and to display the correct answers at the end of the questionnaire.

## Load a questionnaire template you own

Finally, it is possible to import one of your questionnaire templates, in json format. To do this, when creating the questionnaire, select the "Load a template" option.

## Go further

{% content-ref url="scheduling-an-audit-or-a-pia.md" %}
[scheduling-an-audit-or-a-pia.md](scheduling-an-audit-or-a-pia.md)
{% endcontent-ref %}

{% content-ref url="share-an-audit-report-or-pia.md" %}
[share-an-audit-report-or-pia.md](share-an-audit-report-or-pia.md)
{% endcontent-ref %}

{% content-ref url="pia-dpia.md" %}
[pia-dpia.md](pia-dpia.md)
{% endcontent-ref %}

{% content-ref url="tia.md" %}
[tia.md](tia.md)
{% endcontent-ref %}

{% content-ref url="lia.md" %}
[lia.md](lia.md)
{% endcontent-ref %}
