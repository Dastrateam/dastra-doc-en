---
description: Learn how to set up a cookie consent widget on your site.
---

# Implement a cookie consent widget

DASTRA allows you to set up a cookie consent widget directly on your site in compliance with the recommendations of the CNIL (French Data Protection Authority) on cookies and other tracking devices.

## What is the Dastra cookie consent widget?

This widget is composed of several elements

<figure><img src="https://138894690-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2F6C7JDBYbJydNYzQ8vGjp%2FCapture%20web_6-5-2022_93427_www.dastra.eu.jpeg?alt=media&#x26;token=bab7e0b0-450a-4ff4-8117-91e121d03c94" alt=""><figcaption><p>A "cookies" symbol appearing at the bottom left of the screen</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-21 à 15.11.52.png" alt=""><figcaption><p>A fold-out introduction window</p></figcaption></figure>

## Prerequisites&#x20;

To implement your cookie consent widget, you must first **identify** and **classify** the cookies **placed on your website by purpose**. DASTRA's Cookie Consent module allows you to do this in just a few clicks.

{% hint style="info" %}
To make the implementation of the cookie consent widget easier, Dastra has integrated all the necessary steps, from setting up the prerequisites to the lines of code, in the same module.
{% endhint %}

To scan the cookies placed on your website, go to the following page:

{% content-ref url="scannez-les-cookies-deposes-sur-votre-site-web.md" %}
[scannez-les-cookies-deposes-sur-votre-site-web.md](scannez-les-cookies-deposes-sur-votre-site-web.md)
{% endcontent-ref %}

To classify cookies by consent categories, go to the following page:

{% content-ref url="classifiez-les-cookies-par-categories-de-consentement.md" %}
[classifiez-les-cookies-par-categories-de-consentement.md](classifiez-les-cookies-par-categories-de-consentement.md)
{% endcontent-ref %}

## Set the appearance of your target cookie consent widget

To set up a cookie consent widget on your website, you must go to the "Appearance" interface of the DASTRA cookie consent module.

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-21 à 15.18.41.png" alt=""><figcaption><p>DASTRA Cookie Consent Module "Templating" Interface</p></figcaption></figure>

From this interface, you can **fully customize your widget** so that it displays the way you want it to on your website.

{% hint style="info" %}
You can also make other more general changes to the widget in the "Configuration", "Texts and translations" and "Triggers" sections.
{% endhint %}

Once the settings are complete, click on "Save and continue".

![](<../../../.gitbook/assets/image (274).png>)

## Insert the widget code on your website

Once you have defined your target cookie consent widget, you can integrate it directly into your website using **lines of code automatically generated by DASTRA**.

To do this, go to the "Installation" interface of the DASTRA Cookie Consent module, and insert the automatically generated code before the end of the html tag on your website.

![Widget html code generation](<../../../.gitbook/assets/image (247).png>)

{% hint style="info" %}
You can use the Google tag manager to dynamically insert this code on each page.
{% endhint %}

Don't hesitate to ask your webmaster to do this step. Once this is done, a widget will appear on your screen.

{% hint style="info" %}
For security reasons, only sites with an "https" SSL certificate can set up a widget.
{% endhint %}
