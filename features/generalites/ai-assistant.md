---
description: >-
  Dastra's AI Assistant uses the power of OpenAI GPT-4 AI to automatically
  generate records of data processing activities.
---

# AI Assistant

## What can Dastra be used for?&#x20;

With Dastra, you can use AI for two main purposes:&#x20;

### Generate data processing&#x20;

Quickly generate data processing in the format expected by Dastra, based on a rapid description of your processing activity. Based on the described use of the data, Dastra will propose a processing model including a name, one or more datasets with fields, a retention period, security measures, recipients and a processing description.&#x20;

In no time at all, you'll be up and running. Do you have a modification to make to what is proposed? Edit the processing once it's been created.&#x20;

### Generate assets&#x20;

Quickly generate assets (such as software) in the format expected by Dastra. The AI will suggest a name, provide links to the actor's privacy policy and create an actor as an editor. Save time and let the AI pre-fill this information for you.

{% embed url="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2F3LnwYaR0wxVm1itxA4XH%2Fia-gpt-dastra.mp4?alt=media&token=ba3d66f4-e290-4215-83ec-7a2f91641d39" %}

## Generate datasets&#x20;

Quickly generate datasets in the format expected by Dastra from a simple description. To generate a dataset with AI :&#x20;

1. Go to the datasets page
2. Click on **Create a dataset** > **Create with AI wizard**&#x20;
3. Enter a short description of your dataset in the text field
4. &#x20;Click Next and wait a few moments for your dataset to be created.&#x20;
5. On the dataset overview screen, apply any corrections and click on Create. Once the dataset has been generated? Edit the treatment once it has been created directly.

#### Generate responses to data subject right requests <a href="#generer-des-reponses-aux-demandes-dexercice-de-droits" id="generer-des-reponses-aux-demandes-dexercice-de-droits"></a>

You can easily generate responses to data subject right requests in several languages from the request communication stage. Various customization options are available to adapt the text to your needs (shorten or lengthen the text, adopt a more or less formal tone, etc.).

To generate a reply :

1. Go to a [rights exercise](../gerer-les-exercices-des-droits/manage-data-subject-right-requests.md) in progress
2. Fill in the information up to the **Communication/Transmission** step
3. Click on **Generate with AI** and wait a few moments for the wizard to generate an initial response based on the following information
   1. first and last name of recipient
   2. request message
   3. language to be used
   4. workspace name
   5. purpose
   6. name of request operator
   7. date of request and number of days remaining (depending on complexity)
   8. request status and ID
4. You can then edit the proposed text or use one of the reformulation options to restart the generation (wait a few moments to see the result).
5. Finally, click on **Use this message** and add any attachments, before clicking on **Send** to send.

Note that a limit on the number of trials per minute is in place for this feature.

### How to use Dastra's generative AI ? <a href="#comment-utiliser-lia-generative-de-dastra" id="comment-utiliser-lia-generative-de-dastra"></a>

You can use the AI assistant to generate data processings or assets. To do so, click on the **"New data processing"** button and on **"AI Generated"**. The AI assistant will propose a data model that you can then adapt to your needs.



{% hint style="warning" %}
**What should I do if I don't want this feature in my account?**&#x20;

If you don't want this option to be available in your workspace, you can [contact us](https://www.dastra.eu/en/contacts) so that we can deactivate the functionality for your organisation.
{% endhint %}

## How does it work?

Dastra uses the **OpenAI GPT 4o-mini** and **GPT 4-1mini** AI model (Model of [ChatGPT](https://chat.openai.com/)) provided by the [OpenAI service hosted on Azure](https://azure.microsoft.com/fr-fr/products/cognitive-services/openai-service). The model used is pre-trained. **We do not transfer any data from your organisation** in order to train this artificial intelligence.

Dastra simply uses the power of GPT's generative AI to generate content from simple text queries. Dastra has simply provided the expected document model (JSON) and an example of data processing (from our library) that we want to have and the AI model takes care of the rest.&#x20;

Only the prompt text is transferred to the AI for object generation in Dastra.

For the generation of data subject right request messages, the context of the message is integrated into the generation request in order to propose a personalized response to the request ([see details of transmitted fields](ai-assistant.md#generer-des-reponses-aux-demandes-dexercice-de-droits)).

{% hint style="info" %}
**Warning about the quality of the suggested content**\
\
The data generated by the wizard are **suggestions only**. It is necessary to reread and update the information generated automatically by the wizard. Dastra makes no commitment as to the quality of the information suggested.
{% endhint %}

Dastra **does not transfer any data** from your workspace to the AI service. Text queries and results from the :&#x20;

* **are NOT available to other clients** and are NOT available to OpenAI or MistralAI.&#x20;
* **are NOT used to improve OpenAI or MistralAI** **models.**&#x20;
* **are NOT used to automatically improve Azure OpenAI models** for your use in your resource (models are stateless unless you explicitly refine the models with your training data).

\
For more information on how this model works, go to [this page](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy).

