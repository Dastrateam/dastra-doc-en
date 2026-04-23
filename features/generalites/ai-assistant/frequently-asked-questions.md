---
description: >-
  This FAQ addresses common questions raised during vendor assessments and data
  protection audits.
---

# Frequently Asked Questions

#### **Are there contractual guarantees that AI models will not reuse your organisation's data for training or any other purpose?**

Yes. For all models in the OpenAI, Mistral, and Open source families, Dastra uses **Azure managed services** (not OpenAI's or Mistral's own infrastructure directly). Microsoft Azure contractually guarantees that:

* Your prompts and outputs are **not available to other Azure customers**
* Your data is **not transmitted to OpenAI, Mistral, or any other third party**
* Your data is **not used to train, fine-tune, or improve base models**
* Models are **stateless**: no prompt is retained in the model between requests

These guarantees apply regardless of whether the data is personal or non-personal. They are enforceable contractual commitments from Microsoft, not mere policy statements.

If you use a **Custom AI provider** (your own API key), these guarantees depend on your provider's own terms. Dastra recommends reviewing those terms carefully before activation.

***

#### **Can AI processing of personal data be limited or disabled, and what is known about the data used to train the models?**

**Personal data and AI processing**

The AI assistant is only invoked when a user explicitly triggers a generation action. It is never applied automatically to personal data in the background. For most features, the data sent to the model contains no personal data at all (see the data transmission table in the main documentation). The main exception is the **rights request response generator**, which by design processes the requester's name and request content — but only when the feature is deliberately used by a Dastra operator.

**Disabling AI**

An organisation administrator can **disable the AI assistant entirely** for their organisation by contacting Dastra support. Per-module granular control can be discussed with the Dastra team depending on your specific requirements.

**Training data**

The models used by Dastra (via Azure) are **pre-trained general-purpose models**. They were not trained on Dastra customer data, nor on any data specific to your organisation. Dastra has no visibility into the original training datasets of models such as GPT-4.1-mini or Mistral-Large, as these are proprietary to their respective developers — however, your data is contractually excluded from any further training.

***

#### **Is personal data processed during model training, logging, or improvement — and what retention and minimisation measures are in place?**

**Training and model improvement**

No. Azure's contractual guarantees explicitly exclude customer data from being used for training, validation, or improvement of base models. This applies to all three supported model families (OpenAI, Mistral, Open source).

**Logs and technical traces**

Dastra maintains its own **AI invocation logs** for the past 90 days (accessible under Settings > AI Assistant > AI invocation logs). These logs record:

* Timestamp, operation type, model used, processing duration, status, and the workspace member who triggered the call

They do **not** contain the content of prompts or generated outputs. No personal data from processed records is stored in these logs under normal circumstances.

On the Azure side, in the exceptional case where a prompt is flagged by the automated abuse detection mechanism, a temporary sample may be retained in isolated, per-customer storage for review purposes. For EEA-deployed resources (Dastra's case), any human reviewers involved are also located within the EEA. This is not standard practice and does not apply to normal usage.

**Minimisation measures**

Dastra only transmits to the model the fields strictly necessary for the requested generation. Data from other records in your workspace is never included. Dastra also recommends avoiding the use of personal data in free-text fields (descriptions, custom instructions) wherever possible.

***

#### **How does the AI assistant support compliance with data subjects' rights and traceability of operations?**

**Supporting data subjects' rights**

The AI assistant in Dastra is a **generation tool**, not a decision-making system. It produces draft text that a human operator reviews and validates before any action is taken. This human-in-the-loop design means that:

* Data subjects interact with your organisation's operators, not with an automated AI system
* No decision with legal or significant effect on a data subject is made solely by the AI

Dastra's broader platform directly supports the exercise of rights (access, rectification, erasure, objection, restriction, portability) through its **rights request management module**, which maintains a full audit trail of each request, its processing steps, and the response sent.

**Traceability**

The AI invocation logs (90-day retention) allow your organisation to identify which workspace member triggered an AI generation, when, and with which model — available for internal audit purposes and to support responses to supervisory authority inspections or data subject requests.

***

#### **How transparent and explainable are the AI-generated results — and can they be communicated to data subjects in plain language?**

Dastra's AI assistant covers two distinct types of output, each with its own explainability profile.

**Text generation features**

For most features (generating processing descriptions, privacy notices, rights request responses, etc.), the AI produces draft text based on explicit inputs — structured fields or free text entered by the user. The logic is not algorithmic scoring or automated profiling: it is text generation from clearly defined inputs. In these cases, explainability is straightforward:

* The documentation lists exactly which fields are sent to the model for each feature
* All generated content is presented as a draft for a human operator to review, edit, and validate before any use
* The final output reflects a human decision, not a raw AI output

**Compliance analysis features** _(processing activities and AI systems)_

For the compliance analysis of processing activities and AI systems, the AI reads the full structured record and produces a **criterion-by-criterion assessment**, including a grade, a plain-language justification, and relevant excerpts from the record. This is closer to an analytical reasoning output than simple text generation.

Explainability here is by design:

* Each criterion (purposes, legal basis, data subjects' rights, retention, security, DPIA necessity, etc.) is assessed **independently and transparently**
* The justification for each grade is written in plain language, readable by a non-technical user
* Relevant excerpts from the processing record are surfaced alongside the assessment, making it possible to trace exactly what information led to each conclusion
* Results are clearly labelled as **beta** and are intended to support — not replace — the judgement of a qualified practitioner

**In both cases**, Dastra's AI does not make binding decisions. Outputs are proposals subject to human review. For use cases where explainability is a regulatory requirement (e.g., under Article 22 GDPR or the EU AI Act), this human-in-the-loop design ensures that a human remains accountable for every output before it is used or communicated.
