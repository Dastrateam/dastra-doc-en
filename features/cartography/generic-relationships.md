---
description: Learn how to create generic relationships between elements in Dastra.
---

# Generic relationships

## What is a generic relationship?

A **generic relationship** is a simple, labelled link between two elements in Dastra. It allows you to document connections between objects that are not automatically inferred by the platform — for example, linking an asset to a stakeholder, or a risk to a data breach.

A relationship is characterised by:

* a **source object** and a **target object**,
* a **relation label** (optional, e.g. "Controller", "Managed by"),
* a **summary** (optional, for additional context),
* a **direction** — which can be inverted if needed.

{% hint style="info" %}
One element can be linked to multiple other elements of different types.
{% endhint %}

## Where are generic relationships available?

Generic relationships can be created from the following elements:

* **Assets**
* **Stakeholders**
* **Security measures**
* **Data breaches**
* **Datasets**
* **Risks**

They are primarily used in the **Assets** module and the **referentials** (cartography), where the full relationship graph is visualised.

## How to add a generic relationship

1. Open an element (e.g. an asset).
2. Click the **"Linked elements"** icon in the top toolbar — it shows the current count of linked elements.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (4).png" alt=""><figcaption></figcaption></figure>

3. Click **"Add a relationship"** and select the type of object to link to (Stakeholder, Security measure, Data breach, Asset, Dataset or Risk).
4. In the dialog:
   * Toggle **"Inverse relationship"** if the direction should be reversed.
   * Choose **"Existing element"** to link to an element already in Dastra, or **"Create element"** to create a new one on the fly.
   * Select the target object from the dropdown.
   * Optionally add a **Relation label** and a **Summary**.
5. Click **"Add"** to save the relationship.

<figure><img src="../../.gitbook/assets/image (2) (1) (4).png" alt=""><figcaption></figcaption></figure>

## Visualising relationships

Once relationships are created, they appear in:

* The **"Linked elements"** panel of each element, showing all direct links.
* The **node graph** in the cartography view, where all relationships are displayed as a connected network.

<figure><img src="../../.gitbook/assets/image (4) (7).png" alt=""><figcaption><p>Example of a generic relationship visualised in the cartography graph</p></figcaption></figure>

## Go further

{% content-ref url="../cartography.md" %}
[cartography.md](../cartography.md)
{% endcontent-ref %}
