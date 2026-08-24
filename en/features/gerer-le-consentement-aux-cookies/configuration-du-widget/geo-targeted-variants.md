---
description: Display a different cookie banner depending on the user's geographic location.
---

# Geo-targeted variants

## Overview

The Dastra consent module allows you to create **geo-targeted variants** of your cookie banner. Each variant is a customised version of the widget — appearance, texts, exposed services — that is automatically displayed based on the **user's geographic location**, detected via their IP address.

This feature is particularly useful for organisations operating across multiple countries or regulatory zones, since cookie consent obligations vary significantly by jurisdiction (GDPR/ePrivacy in Europe, CCPA in California, LGPD in Brazil, etc.).

{% hint style="info" %}
**Why this matters legally**

A banner that is compliant in France is not necessarily compliant for a Californian user (opt-out rather than opt-in) or a UK user (post-Brexit, the ICO has its own guidelines). Geo-targeted variants let you adapt your CMP precisely to each legal context without multiplying widgets.
{% endhint %}

***

## Creating a geo-targeted variant

### 1. Access the configuration

From the **Cookies** module, select your widget, then go to the **Variants** tab.

Click **"Create a geo-targeted variant"**.

### 2. Name the variant

Enter a descriptive **label** (80 characters max). Choose an explicit name to make management easier, for example: `Banner – California (CCPA)` or `Banner – EEA zone`.

### 3. Select the targeted geographic zones

Choose the **countries or regions** to which this variant will apply. A search is available within the list.

Dastra provides two shortcuts:

* **EU/EEA**: automatically pre-selects all countries in the European Economic Area.
* **All adequate countries**: pre-selects countries recognised as adequate by the European Commission under Article 45 GDPR.

The list is organised by country, with the ability to target **sub-national regions** (e.g. French regions, US states). This allows you to create, for instance, a variant specific to California only, within a more general widget for the United States.

{% hint style="warning" %}
**Variant priority order**

If multiple variants can apply to the same user (e.g. a user in Île-de-France with a "France" variant and an "Île-de-France" variant), the **most specific** variant (region) takes priority over the more general one (country).
{% endhint %}

### 4. Customise the variant

Once the variant is created, you can configure it **entirely independently** of the main widget:

* **Appearance**: colours, layout, buttons
* **Texts & translations**: labels adapted to the local legal context
* **Exposed services**: you can restrict or extend the list of trackers presented
* **Triggers**: specific display conditions

### 5. Disable banner display (optional)

An option allows you to **not display a banner** for users in the targeted zone.

When enabled, no consent window is shown to the relevant visitors. All cookies are then triggered with their **default consent**, as configured at the service level within the widget.

{% hint style="warning" %}
**For zones without a prior consent requirement only**

This option is relevant for countries where local regulations do not require active consent before placing cookies (e.g. certain non-EEA countries without equivalent ePrivacy legislation). It must **never** be used for users located in the EU/EEA, the UK, or any other jurisdiction requiring opt-in.
{% endhint %}

{% hint style="info" %}
The "default consent" for each service can be configured in the widget settings, under the **Services** section. Check these values before enabling this option.
{% endhint %}

***

## Typical use cases

| Situation                                           | Recommended configuration                                                |
| --------------------------------------------------- | ------------------------------------------------------------------------ |
| European site with US traffic                       | EEA variant (strict opt-in) + US/California variant (CCPA opt-out)       |
| French site with a German subsidiary                | France variant + Germany variant with texts adapted to BfDI requirements |
| Global site with minimal compliance outside the EEA | Default global widget + EEA-compliant GDPR variant                       |

***

## How it works technically

Geographic detection is performed automatically by the Dastra SDK based on the **user's IP address**, with no additional configuration required on your end.

No location data is stored in the user's consent profile: geolocation is used solely to select which variant to display.

{% hint style="info" %}
To test the display of a specific variant from your browser, you can use a VPN or contact Dastra support to enable a zone preview mode.
{% endhint %}
