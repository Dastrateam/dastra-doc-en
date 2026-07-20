---
description: >-
  The threat library helps identify and document the causes or events likely to
  trigger a risk.
---

# Threats

In Dastra, a threat represents the **triggering factor** of a risk:\
it describes _how_ or _why_ a risk can materialize.

👉 Threats enrich risk analysis without making its assessment more complex.

***

### Threats, risks and controls: causal logic

The Dastra model is based on a simple and readable chain:

> **Threat → Risk → Controls → Tests**

* A **threat** describes a situation, a behavior or an event
* A **risk** describes the potential impact for the organization
* **Controls** aim to limit the occurrence or the effects of the risk
* **Tests** make it possible to verify the effectiveness of the controls

📌 Example:

* **Threat**: lack of monitoring of AI logs
* **Risk**: information leakage through AI queries
* **Controls**: logging, monitoring, awareness training
* **Tests**: log review, periodic audits

***

### Threat library view

<figure><img src="../../../.gitbook/assets/image-501.png" alt=""><figcaption></figcaption></figure>

The threat library centralizes all the identified threats, with:

* their name and reference,
* their creation date,
* filters to facilitate navigation.

👉 This view makes it possible to:

* reuse existing threats,
* ensure consistent terminology,
* structure coherent risk scenarios.

***

### Creating and managing a threat

{% columns %}
{% column %}


When creating or editing a threat, the user provides:

* **the name of the threat**
* **an internal reference**
* an **optional description** used to contextualize the threat
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/image-502.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

The module is deliberately **lightweight**:\
threats do not carry a quantified assessment and are not linked directly to controls.

***

### Association with risks

A threat is associated with **one or more risks**.

This association makes it possible to:

* precisely document risk scenarios,
* improve the understanding of causes,
* strengthen the consistency of the overall analysis.

👉 The same threat can contribute to several risks, and vice versa.

***

### Why use threats

Using threats makes it possible to have:

* a finer and more realistic analysis of risks,
* better traceability of scenarios,
* clearer communication with stakeholders (CISO, DPO, business teams).

Threats complement the analysis without adding to the operational management burden.

***

### Summary

Threats are a **clarification tool**.\
They make it possible to better understand **the origin of risks**, and therefore to better justify the controls that are in place.
