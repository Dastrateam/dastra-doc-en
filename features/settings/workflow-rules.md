---
description: Integrate complex processes using customised workflow rules
---

# Workflow rules

### How it works&#x20;

Workflow Rules in Dastra are a set of actions (email notifications, audit scheduling, tasks and field updates) that are executed when certain conditions are met. These rules automate the process of sending email notifications, assigning tasks and updating certain fields in a record when a rule is triggered.

<figure><img src="../../.gitbook/assets/image (328).png" alt=""><figcaption><p>Diagram of the basic principle</p></figcaption></figure>

### How do I create a workflow rule in Dastra?&#x20;

* Go to the [Workflow rules configuration page in your workspace ](https://app.dastra.eu/workspace/0/settings/workflow-rules)
* Click on "New workflow rule".&#x20;
* Choose a name and the type of entity concerned (Processing, Violations, etc.)
* You are now in the rules designer

#### Defining the trigger

You can trigger a workflow rule on two events:

* When **an action is taken on the entity concerned**: creation, modification, state change or recycle bin (if available) .&#x20;
* **When a specific date for the entity is reached**. For example: send a notification 10 days after the publication date.

Only one trigger can be defined per workflow rule.

Note that you can choose whether the workflow can be run more than once per entity. **It is strongly recommended that workflows are executed only once per entity**, as executing a workflow several times can easily lead to problems of repetitive task creation or duplicate notifications.

#### Defining conditions

You can configure one or more execution conditions per rule.

#### Defining actions

To add a new action, click on the "**Add an action**" button and choose the model you wish to set up

Here are the **different types of action** you can trigger:

* Email notification&#x20;
* Update a field in the entity concerned&#x20;
* Add a tag to the entity&#x20;
* Automatic audit scheduling&#x20;
* Define the owner of the item (the assigned person, for example)&#x20;
* Automatic creation of a task

Conditions can be chained together. You can add several actions per condition by clicking on "add an action" again.

{% hint style="info" %}
Example: send a notification to several people when a task is created. To do this, select the "tasks" trigger and, depending on the conditions of the task (for example, adding a tag), add a "notification" action.
{% endhint %}

#### Custom variables

Very often, in personalised notifications for example, it will be useful to inject information from the object that is entered in the workflow: the name of the processing, its publication date, etc. are all variables that you can easily inject into the text of your notifications using the variable injection system.&#x20;

Internally, Dastra uses a templating engine based on [LiquidJS ](https://shopify.github.io/liquid/basics/introduction/)

**To access the different variables in the trigger object, type "\{{"**. This will display a list of suggested variables that you can inject into the content.
