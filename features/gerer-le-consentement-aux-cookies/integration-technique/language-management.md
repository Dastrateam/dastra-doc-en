---
description: This page explains how to manage the languages of the consent widget
---

# Language management

## How to manage multiple languages for the widget?

Go to the settings page of the desired widget, then to the "Texts and translations" tab. You can add one or more languages.

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-28 à 14.55.55.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Please note that only French and English are supported today.
{% endhint %}

## How is the widget language detected?&#x20;

By default, the language is detected automatically according to the browser language&#x20;

## How to force the language of the widget?&#x20;

To force the language of the widget, you just have to add a data-lang="" attribute to the widget's div

```ssml
<div id="cookie-consent" data-lang="fr"></div>
```
