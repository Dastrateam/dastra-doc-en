---
description: Learn how to conduct a Privacy Impact Assessment (PIA) or Data Protection Impact Assessment (DPIA) with Dastra.
---

# Privacy Impact Assessment (PIA / DPIA)

## What is a PIA / DPIA?

A Data Protection Impact Assessment (DPIA), also known as a Privacy Impact Assessment (PIA), is a process required under Article 35 of the GDPR when a processing activity is likely to result in a high risk to the rights and freedoms of individuals.

A DPIA must be carried out before starting a processing activity that presents such risks, and reviewed whenever the nature of the processing changes significantly.

## Does this processing need a DPIA?

In Dastra, the **Impact assessment** tab of each processing activity helps you determine whether a DPIA is required. It evaluates 9 risk criteria defined by the EDPB:

* Evaluation or scoring including profiling and prediction activities
* Automated decision making with significant effects
* Systematic monitoring
* Sensitive personal data
* Data processed on a large scale
* Combining, linking or cross-referencing data
* Data concerning vulnerable individuals
* Innovative use or application of new technologies
* Processing that prevents data subjects from exercising their rights

For each criterion, select "Yes", "No" or "Not applicable". **Two "Yes" answers are generally sufficient** to trigger a DPIA requirement, though a single criterion may be sufficient depending on context.

{% hint style="info" %}
The list of processing activities requiring a DPIA depends on your national supervisory authority's recommendations. Dastra provides a DPIA Guide with country-specific recommendations to help you identify your obligations.
{% endhint %}

Dastra will display one of two results:

* **"A DPIA is not required"** — the processing does not meet the threshold
* **"You need to carry out a data protection impact assessment (DPIA)"** — a "Create a DPIA" button appears to launch the assessment directly

## PIA / DPIA templates in Dastra

Several PIA/DPIA templates are available in the Dastra library, including:

* **PIA (CNIL) - Privacy Impact Analysis** (57 questions): the standard PIA model from the French data protection authority, for a single processing activity
* **PIA (CNIL) - Privacy Impact Analysis (multi-processing)** (57 questions): the CNIL model adapted for assessments covering multiple processing activities
* **Privacy impact assessment (PIA)** (114 questions): a comprehensive generic PIA template
* **EDPB DPIA Template 2026** (82 questions): the template recommended by the European Data Protection Board
* **DPIA Template for AI Systems** (90 questions): for processing activities involving high-risk AI systems (GDPR + EU AI Act)
* **DPC DPIA Questionnaire - Ireland** (9 questions): the template from the Irish data protection authority
* **DPIA Questionnaire (ICO)** (9 questions): the template from the UK data protection authority
* **US PIA (cross-state)** (86 questions): for US-based processing activities

To access these templates, go to the "Questionnaire templates" tab and click **"Create a template"** → **"Automated questionnaires"**, then filter by type "Privacy impact".

## Structure of the PIA (CNIL) questionnaire

The PIA (CNIL) template is structured around three main parts:

1. **Context** — describe the processing activity: general information, purpose, data involved, stakeholders (controller, processors, joint controllers)
2. **Basic principles** — assess proportionality and data need, and document measures to protect individuals' rights
3. **Risks related to data security** — evaluate risks across four threat categories: security measures implemented, illegitimate access to data, unwanted modification of data, and disappearance of data

{% hint style="info" %}
The PIA (CNIL) questionnaire offers two response modes. The difference between the two modes is solely about the visibility of additional fields per question: in **Expert mode**, the **Justification of the answer**, **Attachments** and **Annotations** fields are displayed for each question. In **Simple mode**, these fields are hidden. You can switch between modes at any time.
{% endhint %}

## Linking a PIA to a processing activity

To get the most out of the PIA functionality in Dastra, configure your PIA template as follows:

1. Set the **template type** to "Impact analysis" — this enables the risk heat map in the questionnaire dashboard and integrates data from the linked processing activity.
2. In the **Assessed element** section, select "Processing activity" — this links each PIA response to a specific processing activity and automatically updates the last DPIA date upon validation.

{% hint style="info" %}
Once a PIA is linked to a processing activity, you can access it directly from the **"Impact assessment"** tab within that processing activity, and launch it with the "Create a DPIA" button when the threshold is met.
{% endhint %}

## Importing a PIA from the CNIL tool

If you have already conducted a PIA using the CNIL's dedicated tool, you can import it directly into Dastra:

1. Export your PIA from the CNIL tool in **.json format**
2. In Dastra, select the PIA (CNIL) template and click **"Import your CNIL PIA"**
3. A large part of the elements will be automatically imported into Dastra

## Conducting a DPIA on multiple processing activities

A single DPIA may cover several processing activities that are similar in nature, scope, context, purposes and risks. Use the **PIA (CNIL) - Privacy Impact Analysis (multi-processing)** template, or configure your template so that it is **not linked to a specific processing activity**. You can then conduct the DPIA, export it, and attach it to the documentation of the relevant processing activities.

## Go further

{% content-ref url="../questionnaire-types/tia.md" %}
[tia.md](../questionnaire-types/tia.md)
{% endcontent-ref %}

{% content-ref url="../questionnaire-types/lia.md" %}
[lia.md](../questionnaire-types/lia.md)
{% endcontent-ref %}
