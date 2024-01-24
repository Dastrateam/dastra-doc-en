---
description: >-
  Learn how to use email templates and generate emails with dynamic content to
  communicate with your customers or colleagues.
---

# Email templates

## General

Email templates are a feature of data subject rights management, customised workflows and audits. Once saved, they are a quick way of communicating with stakeholders. The data set of an object can be incorporated into them, and it is even possible to set up conditions and loops to retrieve more information.

## How to use

To select or create a template, click on "Select or create a template".

![](<../../.gitbook/assets/image (322).png>)

you can then search for an existing template in the list or the search function, or look at the templates available in the workspaces to which you have access or the templates created by Dastra). \
\
If you don't find a suitable template, click on "New template".

![](<../../.gitbook/assets/image (323).png>)

The model creation interface comprises 4 elements:

* &#x20;The name (so that the model can be found later)&#x20;
* The input field (body of the template, framed in green)&#x20;
* A Preview tab: displays the rendering of the email in real time&#x20;
* An Input Data tab: lets you view the data for the object concerned by the template

![](<../../.gitbook/assets/image (324).png>)

## Customise the model



You can edit the template and apply styles, insert images or tables as required. You will see the result in the preview tab. If you click on "Custom fields" you will have access to a list of fields to insert. The value of the field will be inserted at the level of the mouse cursor. Of course, you can format the text as you wish.



## Going further with custom fields

The fields surrounded by double braces are "variables". In other words, they will be replaced by the values of the corresponding object (in this case, a request to exercise a right).\
\
![](<../../.gitbook/assets/image (325).png>)



## Create new custom fields from Input Data



By clicking on the "Input Data" tab, you can access the list of properties of the linked object. In the example below, I decide to display the message linked to the request:&#x20;

* I search for the field in "Input Data".&#x20;
* I enter the name of the field in the body of the message using the syntax \{{message\}}&#x20;
* I check the result using the "Preview" tab

![](<../../.gitbook/assets/image (326).png>)

That's it! Now you can create your own custom fields. But that's not all! You can also go even further by creating loops, conditions and applying formats to make the dates easier to read!

## Conditional blocks

It is also possible to create conditional blocks that will only be displayed under certain conditions. To do this, you need to use the conditional tag system, which starts with

. In this way, I can write the following condition:

> \{% if attachments != blank %\}
>
> You have an attachment
>
> \{% endif %\}

The block will only be displayed if there is an attachment in the request.



## The loops

Loops work in the same way, except that this time we generate a variable internal to the loop. It works as follows:

```
{% raw %}
{% for purpose in purposes %}
  {{ purpose }}
{% endfor %}
{% endraw %}i
```

In the example above, I declare that I want to loop through the "purposes" list and assign the "purpose" variable to each item that I display directly.

## Date format

You will quickly see that the dates you retrieve from Input Data are not presentable as they are. Don't worry, you can assign a format to the date.



> \{{dateCreation | date: "%d-%m-%Y à %H:%M"\}}
>
> Will be transformed into 15-03-2023 at 15:40

## A more complex example



The body text below uses all the above elements



> Hello, We have received your request to exercise your rights on \{{dateCreation | date: "%d-%m-%Y à %H:%M"\}} concerning Mr or Mrs \{{givenName\}} \{{familyName\}}. The request relates to the following purposes :
>
> \{% for purpose in purposes %\}
>
> * \{{ purpose \}}
>
> \{% endfor %\}
>
> \{% if attachments != blank %\}
>
> We have received the following attachments:
>
> \{% for attachment in attachments %\}
>
> * \{{ attachment.fileName \}}
>
> \{% endfor %\}
>
> \{% endif %\}
>
> Please accept my sincerest greetings and I will keep you informed of the progress of your request.&#x20;
>
> Yours faithfully \{{operator.displayName\}}

For the request currently being processed, it will be transformed as follows:

![](<../../.gitbook/assets/image (327).png>)



> Hello,\
> \
> We have received your request to exercise your rights on 31-07-2023 à 11:55 concerning Mr or Mrs . The request relates to the following purposes :
>
> * Access
>
> Please accept my sincerest greetings and I will keep you informed of the progress of your request.
>
> Yours faithfully,\
> \
> Paul-Emmanuel Bidault



For more information regarding the Liquid syntax, please go to [this page](https://shopify.github.io/liquid/).
