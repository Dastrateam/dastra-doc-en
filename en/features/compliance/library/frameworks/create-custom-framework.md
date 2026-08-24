---
description: >-
  Dastra lets you create your own regulatory framework and adapt it to your
  needs with the help of artificial intelligence
---

# Create a custom framework

#### Introduction

Creating a custom framework makes it possible to build a compliance framework **adapted to the organization's specific context**: internal policy, sector-specific framework, AI initiative, security, quality or governance.

A custom framework can be:

* built **entirely from scratch**,
* or serve as a **common foundation** for several compliance projects.

***

### Step 1 – Creating the framework

{% columns %}
{% column %}
When creating a custom framework, the user defines:

* **The framework name** (e.g. _Custom AI_, _AI ISSP – Demo_)
* **The framework language**, which will determine the default language of the requirements and controls

Once created, the framework is added to the Library, in a **draft** state.
{% endcolumn %}

{% column %}
<figure><img src="../../../../.gitbook/assets/image-448.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

### Step 2 – Viewing and available actions

By default, a newly created framework is:

* **empty**
* **read-only**

#### Actions available as long as the framework has not been modified

* **Export**: retrieve the framework in JSON / Excel format
* **Duplicate**: create a copy of the framework
* **Move to trash**: delete the framework

👉 **No addition or modification is possible until the framework is in edit mode.**

***

### Step 3 – Switching to edit mode

{% columns %}
{% column %}
To enrich the framework (chapters, requirements, controls…), it is necessary to:

1. Click on **Edit**
2. Switch the framework to **edit mode**

In edit mode, the user can:

* Create **chapters**
* Add **requirements**
* Progressively structure the framework
{% endcolumn %}

{% column %}


<figure><img src="../../../../.gitbook/assets/image-449.png" alt=""><figcaption></figcaption></figure>


{% endcolumn %}
{% endcolumns %}

***

## Creating and structuring requirements

Once the framework has been created and switched to **edit mode**, the user can begin structuring the framework using **chapters** and **requirements**.\
This step makes it possible to translate a regulatory, normative or internal framework into elements that can be used in Dastra.

***

### Structuring by chapters

{% columns %}
{% column %}
<figure><img src="../../../../.gitbook/assets/image-450.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
Chapters make it possible to organize the framework in a readable and coherent way.
{% endcolumn %}
{% endcolumns %}

#### Structuring rules

Dastra allows:

* **root chapters**
* **sub-chapters**

👉 The depth is intentionally limited to a **maximum of two levels** in order to:

* guarantee the readability of the framework
* avoid overly complex structures
* make it easier to use the requirements in compliance projects

#### Fields to fill in

When creating a chapter:

* **Reference**: internal identifier of the chapter
* **Name**: functional title of the chapter

&#x20;

{% hint style="info" %}
_Best practice_: use chapters to structure by major themes\
(e.g. governance, security, operations, uses…).
{% endhint %}

***

### Creating a requirement

{% columns %}
{% column %}
Requirements express the **compliance expectations** the organization must meet.\
They constitute the direct link between the framework and the operational controls.
{% endcolumn %}

{% column %}
<figure><img src="../../../../.gitbook/assets/image-451.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

#### Available fields

* **Reference (required)**\
  Unique identifier of the requirement within the framework
* **Name (required)**\
  Concise formulation of the requirement
* **Description (optional)**\
  Details of the expected content, scope and objectives of the requirement

***

### AI assistance for the requirement reference

{% columns %}
{% column %}
<figure><img src="../../../../.gitbook/assets/image-452.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
When creating a requirement, Dastra offers **AI assistance** to automatically generate a reference consistent with:

* the name of the requirement
* the parent chapter
* the context of the framework


{% endcolumn %}
{% endcolumns %}

👉 This feature makes it possible:

* to harmonize naming conventions
* to avoid inconsistencies or duplicates
* to save time when creating custom frameworks

The user remains free to modify the proposed reference.

***

### Organizing and managing requirements

<figure><img src="../../../../.gitbook/assets/image-476.png" alt=""><figcaption></figcaption></figure>

Once created, requirements can be:

* moved to another chapter
* deleted
* progressively enriched

Each requirement also displays summary indicators (links with controls, risks, tests), making it easier to understand its level of coverage.

***

### Associating controls with a requirement

{% columns %}
{% column %}
Controls are the **operational** elements that make it possible to demonstrate compliance with one or more requirements.

To associate controls with a requirement, two approaches are possible.
{% endcolumn %}

{% column %}
<figure><img src="../../../../.gitbook/assets/image-453.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

#### Option 1 – Associate existing controls

{% columns %}
{% column %}


The user can select one or more controls already present in the Library and attach them to the requirement.


{% endcolumn %}

{% column %}
<figure><img src="../../../../.gitbook/assets/image-454.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

👉 A single control can be associated with **several requirements**, promoting:

* sharing
* consistency of the framework
* better traceability

***

#### Option 2 – Create or associate controls with AI

{% columns %}
{% column %}
<figure><img src="../../../../.gitbook/assets/image-455.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
Dastra offers an AI assistance feature that makes it possible to:

* automatically identify **relevant existing controls**
* propose the **creation of new controls** when necessary

The AI relies on:

* the content of the requirement
* the context of the framework
* the controls already present in the Library
{% endcolumn %}
{% endcolumns %}

👉 Controls created via AI can automatically include:

* their description
* their attachment to the requirement
* the associated tests

***

### Benefits of this approach

This approach makes it possible to achieve:

* a **progressive structuring** of the framework
* **intentional overlaps** between requirements
* the creation of cross-cutting controls covering several requirements
* a solid basis for risk management and compliance projects
