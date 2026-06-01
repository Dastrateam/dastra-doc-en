---
description: Learn how to customise the workflow stages of each object type in Dastra.
---

# Workflow stages

## What are workflow stages?

Workflow stages let you materialise a work process by moving objects from one step to the next. You can break down your compliance procedures in an operational way by defining exactly which stages to follow directly within Dastra.

Each object type (processing activities, data subject requests, data breaches, tasks, assets, contracts…) has its own set of configurable stages. Stages are organised around two statuses:

* **Draft** — the object is being worked on and is not yet finalised.
* **Published** — the object has been validated and is active.

{% embed url="https://youtu.be/rIPJUY3vylc" %}

## How to customise workflow stages

Go to **Workspace Settings → Workflow stages**.

<figure><img src="../../.gitbook/assets/etapes-processus01.png" alt=""><figcaption></figcaption></figure>

You will see the available stages for each object type. Customise them to match your organisation's processes, then click **"Save"**.

<figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

## Can you delete a workflow stage?

Yes — click the bin icon next to the stage you want to remove.

Any objects currently attached to the deleted stage are automatically reassigned to the first stage within the same status.

For example, if you delete the **"In Progress"** stage in the task workflow:

<figure><img src="../../.gitbook/assets/image (9) (2) (2).png" alt=""><figcaption></figcaption></figure>

Objects attached to it will move to the next available stage — for example **"Needs info"**:

<figure><img src="../../.gitbook/assets/image (11) (2).png" alt=""><figcaption></figcaption></figure>

***

{% hint style="info" %}
**Looking to automate actions when a stage changes?**

Workflow stages define the steps — workflow rules let you trigger automatic actions when an object moves between them (send a notification, create a task, update a field…).

See [Workflow rules](workflow-rules.md) for more details.
{% endhint %}
