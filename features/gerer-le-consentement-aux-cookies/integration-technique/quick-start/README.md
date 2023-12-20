---
description: >-
  Learn how to integrate the Dastra cookie widget into a web page using the
  javascript SDK.
---

# Quick start

## Prerequisite: recovery of an API public key

to get a public key from the Dastra SDK, go to this page: [https://app.dastra.eu/general-settings/api](https://app.dastra.eu/general-settings/api)

<figure><img src="../../../../.gitbook/assets/Capture d’écran 2023-02-21 à 17.13.48.png" alt=""><figcaption></figcaption></figure>

## Configure your widget

Configure your widget by following the guide below:

{% content-ref url="../../configuration-du-widget/" %}
[configuration-du-widget](../../configuration-du-widget/)
{% endcontent-ref %}

## Insert the html integration code

Insert the HTML code available in the "Code" section of the Dastra Cookie Consent Module **before the end of the \<BODY> tag** on your website, on all pages. You can use the Google tag manager to dynamically insert this code on each page.

{% hint style="info" %}
For the code to work properly, make sure the public key of your API is configured correctly beforehand.
{% endhint %}

Here is how the widget integration code looks:

```ssml
<div id="dastra-cookie-consent" data-widgetid="{your_widget_id}"></div>
<script src="https://app.dastra.eu/sdk/dastra.js?key={your_public_key}" async>
</script>
```

The div with the id "dastra-cookie-consent" will be the rendering location of your consent widget. The "data-widgetid" attribute is used to identify the widget being invoked, it is often a number (int32). {your\_public\_key} is your API public key which [can be retrieved here](https://app.dastra.eu/general-settings/api).

Once the code is inserted in the tag of your site, the widget will display on your site.

{% hint style="warning" %}
For optimal performance, the widget is automatically cached by the browser in the sessionStorage
{% endhint %}

## Wordpress

If you use Wordpress, you will find in the link below more information on how the generated code can be inserted at the end of the html tag of your website.

{% content-ref url="wordpress.md" %}
[wordpress.md](wordpress.md)
{% endcontent-ref %}

Once the widget is integrated, move on to the testing phase.

{% content-ref url="../comment-tester-lintegration-dun-widget.md" %}
[comment-tester-lintegration-dun-widget.md](../comment-tester-lintegration-dun-widget.md)
{% endcontent-ref %}
