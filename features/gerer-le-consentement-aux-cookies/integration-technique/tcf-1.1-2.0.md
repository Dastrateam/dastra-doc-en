# TCF 1.1/2.0

{% hint style="danger" %}
For the moment, this functionality is still in an experimental phase. Any implementation of TCF will not be effective
{% endhint %}

The [consent management platform (CMP)](https://github.com/InteractiveAdvertisingBureau/GDPR-Transparency-and-Consent-Framework) framework is currently supported by the Dastra widget. To enable the IAB vendor opt-in, you just need to go to the "services" part of the widget configuration and enable the corresponding checkbox.&#x20;

Once the box is checked, you can see the changes in the widget interface:

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-28 à 15.49.17.png" alt=""><figcaption></figcaption></figure>

Automatically, when the IAB opt-in, the cookie containing the encoded information about the user's consent to the IAB vendors is automatically created in the browser:

<figure><img src="../../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This cookie has a default lifetime of 180 days and is named "eupubconsent"
{% endhint %}

### Capture the IAB chain of consent&#x20;

When the user applies consent, it is possible to capture the consent string directly using the following event listener:

```javascript
document.addEventListener('dastra:consentstring',function(consentString){
    console.log(consentString); // BOybBVKOybbNhABABBENCoAAAAAq6AAA
});
```
