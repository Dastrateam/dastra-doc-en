# Geo-targeted variations

### Overview

The Dastra consent module lets you create **geo-targeted variations** of your cookie banner. Each variation is a fully customized version of the widget — appearance, texts, exposed services — that is automatically displayed based on the **user's geographic location**, detected via their IP address.

This feature is particularly useful for organizations operating across multiple countries or regulatory zones, as cookie consent requirements vary significantly depending on local legislation (GDPR/ePrivacy in Europe, CCPA in California, LGPD in Brazil, etc.).

{% hint style="info" %}
**Why this matters legally**

A banner that is compliant in France is not necessarily compliant for a Californian user (opt-out rather than opt-in) or a UK user (post-Brexit, the ICO has its own guidelines). Geo-targeted variations allow you to tailor your CMP precisely to each legal context without having to manage multiple separate widgets.
{% endhint %}

### Creating a geo-targeted variation

#### 1. Access the configuration

From the **Cookies** module, select your widget, then go to the **Variations** tab.

Click **"Create a geo-targeted variation"**.

<figure><img src="../../../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure>

#### 2. Name the variation

Enter a descriptive **label** (up to 80 characters). Choose a clear name to make management easier, for example: `Banner – California (CCPA)` or `Banner – EEA Zone`.

#### 3. Select the targeted geographic zones

Choose the **countries or regions** for which this variation will apply. A search bar is available within the list.

Dastra provides two shortcuts:

* **EU/EEA**: automatically pre-selects all countries in the European Economic Area.
* **All adequate countries**: pre-selects all countries recognized as adequate by the European Commission under Article 45 GDPR.

The list is organized by country, with the ability to target **sub-national regions** (e.g. French regions, US states). This makes it possible, for instance, to create a variation that applies only to California within a broader widget for the United States.

{% hint style="warning" %}
**Variation priority order**

If multiple variations could apply to the same user (e.g. a user in Île-de-France with both a "France" variation and an "Île-de-France" variation), the **most specific** variation (region) takes precedence over the more general one (country).
{% endhint %}

#### 4. Disable the banner display (optional)

An option allows you to **suppress the banner entirely** for users in the targeted zone: **"Disable the banner display (all cookies with default consent will be triggered)"**.

When enabled, no consent window is shown to visitors from the targeted area. All cookies are fired using their **default consent value**, as configured at the service level within the widget.

{% hint style="warning" %}
**For zones with no prior consent requirement only**

This option is relevant for countries where local regulations do not require active consent before setting cookies (e.g. certain non-EEA countries without equivalent ePrivacy legislation). It must **never** be used for users located in the EU/EEA, the UK, or any other jurisdiction that mandates opt-in consent.
{% endhint %}

{% hint style="info" %}
The "default consent" value for each service is configurable in the widget's **Services** section. Make sure to review these values before enabling this option.
{% endhint %}

#### 5. Customize the variation

Once the variation is created, you can configure it **entirely independently** from the main widget:

* **Appearance**: colors, layout, buttons
* **Texts & translations**: labels adapted to the local legal context
* **Exposed services**: you can restrict or expand the list of trackers presented to users
* **Triggers**: specific display conditions

***

### Typical use cases

| Situation                                           | Recommended setup                                                               |
| --------------------------------------------------- | ------------------------------------------------------------------------------- |
| European site with US traffic                       | EEA variation (strict opt-in) + US/California variation (CCPA opt-out)          |
| French site with a German subsidiary                | France variation + Germany variation with texts adapted to BfDI requirements    |
| Global site with minimal compliance outside the EEA | Default worldwide widget + GDPR-compliant EEA variation                         |
| Non-EEA country with no opt-in requirement          | Country-specific variation with banner disabled + default consent set to `true` |

***

### How it works technically

Geographic detection is performed automatically by the Dastra SDK based on the **user's IP address**, with no additional configuration required on your end.

No location data is stored in the user's consent profile: geolocation is used solely to select which variation to display.

{% hint style="info" %}
To test the display of a specific variation from your browser, you can use a VPN
{% endhint %}
