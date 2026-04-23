---
description: >-
  Dastra's AI assistant uses the power of AI to quickly generate elements in
  Dastra
---

# AI Assistant

Dastra's AI assistant allows you to generate and enrich elements in your workspace from simple text descriptions. It relies on generative AI models hosted on Azure, in France and within the European Economic Area, without any of your organization's data being used to train these models.

{% hint style="info" %}
The AI assistant is available on all Dastra workspaces. If you wish to disable it for your organization, please contact our [support team](../../commencer/support/request-support.md).
{% endhint %}

***

### How does it work?

#### **Models and hosting**

Dastra uses pre-trained generative AI models, available from four model families:

| Family                          | Configured models                                                                    | Hosting                         |
| ------------------------------- | ------------------------------------------------------------------------------------ | ------------------------------- |
| OpenAI (recommended by default) | Fast: gpt-4o-nano · Smart: gpt-5-mini · Large context: gpt-4.1-mini                  | Azure, France / EEA             |
| Mistral                         | Fast: mistral-small-2503 · Smart: Mistral-Large-3 · Large context: Mistral-Large-3   | Azure, France / EEA             |
| Open source                     | Fast: Ministral-3B · Smart: DeepSeek-V3.2 · Large context: Llama-4-Maverick-17B-128K | Azure, France / EEA             |
| Custom AI provider              | Your own provider via API key (see below)                                            | Depending on your configuration |

For the first three families, models are hosted on Microsoft's Azure infrastructure, in France. They are not operated directly by OpenAI or Mistral: Dastra uses Azure managed services, meaning your data does not transit through OpenAI's or Mistral's own infrastructure.

For each family, three model tiers are used depending on task complexity:

* **Fast** — simple actions: generating descriptions, suggesting tags
* **Smart** — actions requiring more reasoning: generating structured elements in Dastra
* **Large context** — actions processing large volumes of data: answering a questionnaire, analysing a processing activity

You can configure the model family in **Account Settings >** [**AI Assistant**](https://app.dastra.eu/general-settings/ai).

#### Custom AI provider

Dastra allows you to connect your own AI provider via an API key, provided it is compatible with the OpenAI API standard. Supported providers include OpenAI, Google (Gemini), Mistral, Microsoft Foundry, and any compatible self-hosted LLM.

To configure a custom provider, go to **Settings > AI Assistant > Custom AI provider**, then enter your credentials and map them to the three model tiers (Fast, Smart, Large context).

{% hint style="warning" %}
When using a Custom AI provider, data sent to the model is subject to your provider's privacy policy, not the Azure guarantees described on this page. Review your provider's terms before enabling this option, particularly if your prompts may contain personal data.
{% endhint %}

#### **What Dastra sends to the model**

Dastra only transmits the information necessary for the requested generation: the text entered by the user, and where applicable the structured fields of the object in question (processing activity, AI system, rights request, etc.).

#### **What Dastra does not do**

{% hint style="success" %}
The following points are contractually guaranteed by Microsoft Azure for all models in the OpenAI, Mistral, and Open source families:

* Your prompts and outputs are not available to other Azure customers
* Your data is not transmitted to OpenAI, Mistral, or any other third party
* Your data is not used to train or improve base models
* Models are stateless: no prompt is stored in the model between two requests
{% endhint %}

#### **Abuse monitoring and human review**

Microsoft Azure maintains an automated mechanism for detecting potentially abusive content. In exceptional cases where content is flagged, a sample of prompts may be temporarily retained in a per-customer isolated storage environment for review purposes. For resources deployed within the EEA (which is the case for Dastra), any human reviewers are also located within the EEA.

This retention is exceptional and does not apply to normal platform usage. For more details, consult the Microsoft [documentation on Azure Direct Models data privacy](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/data-privacy).

#### **AI invocation logs**

Dastra retains a history of AI assistant calls for the past 90 days, accessible from **Settings > AI Assistant > AI invocation logs**. For each call, the following information is recorded:

| Field     | Description                                   |
| --------- | --------------------------------------------- |
| Date      | Timestamp of the call                         |
| Status    | Success or failure of the generation          |
| Operation | Type of prompt used                           |
| Model     | Name of the model called                      |
| Duration  | Request processing time                       |
| User      | Workspace member who triggered the generation |

{% hint style="info" %}
These logs serve as an internal traceability and audit tool. They allow you to identify who used the AI assistant, when, and with which model — particularly useful in the context of a compliance audit or an AI usage review within your organisation.
{% endhint %}

***

#### What data is sent to the AI model?

{% hint style="info" %}
Dastra **does not transmit any workspace data** to the AI model unless you initiate it. Only the information listed below, depending on the feature used, is included in the request sent to the model.
{% endhint %}

| Feature                                      | Data sent to the model                                                                                                                                       | Potential personal data                                        |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------- |
| Generate a processing activity               | Free text entered by the user                                                                                                                                | No — unless the user mentions individuals in their description |
| Generate an asset                            | Free text + URL of the privacy policy provided                                                                                                               | No                                                             |
| Generate an actor                            | Free text + URL or attachment provided                                                                                                                       | No                                                             |
| Generate a dataset                           | Free text entered by the user                                                                                                                                | No                                                             |
| Generate a security measure                  | Free text entered by the user                                                                                                                                | No                                                             |
| Generate a privacy notice                    | Structured fields of the processing activity (purposes, legal basis, retention periods, recipients, rights)                                                  | Potentially — if fields contain named references               |
| Generate a description                       | Free text entered by the user                                                                                                                                | No                                                             |
| Suggest tags                                 | Text content of the object (name, description)                                                                                                               | No                                                             |
| Generate a questionnaire template            | Free text entered by the user                                                                                                                                | No                                                             |
| Answer a questionnaire (PIA, risk analysis…) | Structured fields of the linked processing activity + any custom instructions                                                                                | Potentially — depending on the processing activity content     |
| Generate a response to a rights request      | First and last name of the requester, request message, language, workspace name, purposes, operator name, date and remaining deadline, request status and ID | Yes — first name, last name, and request content               |
| Generate a data breach post-mortem           | Structured fields of the breach (description, affected data, measures taken)                                                                                 | Potentially — depending on the content of the breach record    |
| Extract contract metadata                    | Text content of the transmitted document (attachment or URL)                                                                                                 | Potentially — depending on the contract content                |
| Generate a custom document                   | Instructions entered by the user + any source content                                                                                                        | Potentially — depending on the instructions provided           |
| Generate a custom report                     | Instructions entered by the user                                                                                                                             | No — unless the user includes data in their instructions       |
| Risk analysis (AI system)                    | Structured fields of the AI system (description, purposes, data processed, stakeholders)                                                                     | Potentially — depending on the AI system content               |
| Generate an AI system description            | Free text + URL or attachment provided                                                                                                                       | No                                                             |
| Generate an AI system notice                 | Structured fields of the AI system concerned                                                                                                                 | Potentially                                                    |
| Suggest controls / requirements / tests      | Context of the object concerned (name, description, framework)                                                                                               | No                                                             |

{% hint style="warning" %}
**Best practice:** Avoid including personal data directly in free-text fields (descriptions, custom instructions). Use identifiers or generic terms wherever possible.
{% endhint %}

#### **Data that is never transmitted**

The following are never included in requests sent to the AI model:

* Dastra user credentials and passwords
* Data from other records in your workspace (only the object you are working on is involved)
* Session metadata (name of the logged-in user, IP address, etc.)
* Attachments not explicitly provided within the relevant feature

#### **Retention period for requests**

The Azure models used by Dastra are **stateless**: prompts and outputs are not stored in the model and are not used to retrain or improve base models.

{% hint style="info" %}
**Exception — abuse detection:** Microsoft Azure maintains an automated mechanism for monitoring potentially abusive content. If a prompt is flagged, a sample may be temporarily retained in a per-customer isolated storage environment for review purposes. For resources deployed within the European Economic Area (which is the case for Dastra), any human reviewers are also located within the EEA. This retention is exceptional and does not apply to normal platform usage.
{% endhint %}

For more information, consult the Microsoft [documentation on Azure Direct Models data privacy](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/data-privacy).

***

### Use cases

{% hint style="warning" %}
**Warning on the quality of generated content:** Data generated by the assistant are suggestions only. They must be reviewed and updated before any use. Dastra makes no commitment regarding the quality of the information provided.
{% endhint %}

#### **Generate processing activities**

Quickly generate processing activities in the format expected by Dastra from a brief description of your processing. Based on the described data use, Dastra will suggest a processing template including a name, one or more datasets with their fields, a retention period, security measures, recipients, and a description. Edit the processing activity once created to make your corrections.

#### **Generate assets**

Quickly generate assets (software, tools, etc.) in the format expected by Dastra. The AI will suggest a name, links to the actor's privacy policy, and will create an actor as the publisher.

#### **Generate datasets**

1. Go to the Datasets page
2. Click **Create a dataset > Create with AI assistant**
3. Enter a short description of your dataset
4. Click **Next** and wait a few moments
5. On the summary screen, apply any corrections and click **Create**

#### **Generate privacy notices for processing activities**

1. Go to the editing page of a processing activity
2. In section **11. Documentation**, click **Generate a privacy notice**
3. Choose the desired format, or customise the instructions by clicking **Custom**
4. Click **Generate**, then copy or insert the text into your documentation

#### **Generate a response to a questionnaire (PIA, risk analysis…)**

1. Go to the **Questionnaires** section and select the desired template
2. Click **Schedule a questionnaire**
3. Select **AI-assisted response**
4. Enter the source processing activity or provide custom instructions
5. Once the response is generated, make your corrections directly

#### **Generate responses to rights requests**

Generate responses to rights requests in multiple languages, with customisation options (length, formal or informal tone, etc.).

1. Go to an ongoing rights request
2. Fill in the information up to the **Communication/Transmission** step
3. Click **Generate with AI** — the response is generated from the following fields: requester's first and last name, request message, language, workspace name, purposes, operator name, date and remaining deadline, request status and ID
4. Edit the suggested text or use the rephrasing options
5. Click **Validate this message**, add any attachments, then click **Send**

{% hint style="info" %}
A rate limit on the number of calls per minute is in place for this feature.
{% endhint %}
