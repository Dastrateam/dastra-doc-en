---
description: Learn all about integrating webhooks into Dastra
---

# Webhooks

## Concept 👓 <a href="#configuration" id="configuration"></a>

Simply put, webhooks are used to trigger an action in response to an event. They are generally used to communicate between systems. This is the simplest way to receive an alert when something happens in Dastra. The aim is to notify third-party applications (APIs, CRM, serverless functions, etc.) in real time.\
\


## Configuration 🛠️

To configure your webhooks, go to : [https://app.dastra.eu/general-settings/webhooks](https://app.dastra.eu/general-settings/webhooks)​![](<../../.gitbook/assets/Capture d'écran 2024-12-16 122808.png>)​

* Click on "create a webhook url ”
* Enter your webhook reception url.
* Enter the relevant workspace
* Select the event(s) you wish to subscribe to. The type of data returned will differ according to the type of event. For example, you can trigger the webhook when a new request to exercise a right is created. In this case, the request body will contain a json
* create the webhook

This takes you to the webhook details screen.

![](<../../.gitbook/assets/Capture d'écran 2024-12-16 123229.png>)​

## How to receive the webhook 🛬 <a href="#comment-receptionner-le-webhook" id="comment-receptionner-le-webhook"></a>

To receive webhook requests, you need to create an event capture API endpoint. The request is made as a POST and will always be structured in this way. The request body contains a json with details of the event triggered.\
\
Here is the general structure of the response sent:

#### Tester votre url de webhooks 🧪 <a href="#tester-votre-url-de-webhooks" id="tester-votre-url-de-webhooks"></a>

```
{
 "webhookId": <id of the webhook configured in dastra>,
 "signatureUrl": "https://yourapi.com/webhooks/handle",
 "userId": <The user whot triggered the event>,
 "eventType": <The id of the event>,
 "eventName": <The label of the event>,
 "data": <Event dynamic data>,
 "date": <date of the event>
} 
```

A timeout of 10 seconds is applied to the request, after which the request will be in error. The response code must be 200.&#x20;

There may be a small delay between the moment the event occurs in the application and the webhook triggering (this delay is linked to the asynchronous nature of webhook execution in our infrastructure). This delay is more or less important depending on the load of our infrastructure, and can go up to 60-120 seconds maximum.

{% hint style="info" %}
At present, there is no system for replaying failed webhooks and thus compensating for any unavailability of webhook reception servers. In this case, we recommend manual synchronization of failed events.
{% endhint %}

## Test your webhooks url 🧪

You can now test your webhook in real-life conditions by clicking on the “Send a test webhook” button.



## How to secure the webhook? 🛡️

{% hint style="info" %}
Although it's not mandatory, it is recommended to validate the incoming webhook request to avoid potential attacks by a hacker who has sniffed the network and is thus able to post anything on your webhook url and trigger or spam the creation of elements in your system.
{% endhint %}

Each time a request is made to modify or delete an element in Dastra, we'll post an object to all the urls you've configured for the desired event. Each POST request will include a Dastra-Signature header, which can be retrieved on the server side.

This header corresponds to the entire posted JSON, hashed using the HMAC-Sha256 algorithm with the webhook's validation key.

> DastraSignature = **HMAC256**(\<JSON serialized POST>,\<webhook validation key>)

Here are some examples of query signature validation:

{% tabs %}
{% tab title="PHP" %}
```php
error_reporting(E_ALL);
ini_set('display_errors', 1); 
c
$secret = "your dastra validation key";// your secret key
$payload = "";// equest body
$headers = "";// request message headers array

$signature = "";// the HMAC hash key in the HTTP header 'Dastra-Signature'
$result = false;// verification result

if (isset($_POST)) {
    try {
        $payload = file_get_contents('php://input');
        $headers = get_ds_headers();
        if (array_key_exists("Dastra-Signature", $headers)) {
            $signature = $headers["Dastra-Signature"];
            $result = hash_is_valid($secret, $payload, $signature);
            log_result($signature, $payload, $result);
        }
     } catch (Exception $e) {
        logger("\nException: " . $e->getMessage() . "\n");
    }
    header("HTTP/1.1 200 OK");
}

function get_ds_headers()
{
    $headers = array();
    foreach ($_SERVER as $key => $value) {
        if (strpos($key, 'HTTP_') === 0) {
            $headers[str_replace(' ', '', ucwords(str_replace('_', ' ', strtolower(substr($key, 5)))))] = $value;
        }
    }
    return $headers;
}
 
function compute_hash($secret, $payload)
{
    $hexHash = hash_hmac('sha256', $payload, utf8_encode($secret));
    $base64Hash = base64_encode(hex2bin($hexHash));
    return $base64Hash;
}
 
function hash_is_valid($secret, $payload, $verify)
{
    $computed_hash = compute_hash($secret, $payload);
     return hash_equals($verify,$computed_hash);
 }
```
{% endtab %}

{% tab title="C#" %}
```csharp
[HttpPost]
public IActionResult Handle(){
    string dastraSignature = Request.Headers["Dastra-Signature"];
    string key = "Your validation key";
    string payload = GetRequestBody();
}

private static bool ValidateSignature(string signature, string payload, string secret)
{
    using (var hmacsha256 = new HMACSHA256(Encoding.UTF8.GetBytes(secret)))
    {
        var hash = hmacsha256.ComputeHash(Encoding.UTF8.GetBytes(payload));
        var result = Convert.ToBase64String(hash);
    }
    
    return result.Equals(signature)
}

private static string GetRequestBody()
{
    var bodyStream = new StreamReader(Request.InputStream);
    bodyStream.BaseStream.Seek(0, SeekOrigin.Begin);
    var bodyText = bodyStream.ReadToEnd();
    return bodyText;
} Some code
```
{% endtab %}
{% endtabs %}



### What happens when the url answers something other than 200

The webhook will be automatically blocked and considered in error when the threshold of 5 errors is exceeded.



### How to set up webhooks with APIs

Retrieve webhooks linked to your account (in all workspaces)

{% swagger src="../../.gitbook/assets/dastra api.json" path="/v1/WebHookUrls" method="get" %}
[dastra api.json](<../../.gitbook/assets/dastra api.json>)
{% endswagger %}

Create a new webhook url using the POST endpoint. Fill in the events to which you wish to subscribe your webhook with the subscribedEvents webhooks parameter.

{% swagger src="../../.gitbook/assets/dastra api.json" path="/v1/WebHookUrls" method="post" %}
[dastra api.json](<../../.gitbook/assets/dastra api.json>)
{% endswagger %}



A webhook ID will be returned to you

{% swagger src="../../.gitbook/assets/dastra api.json" path="/v1/WebHookUrls/{id}" method="get" %}
[dastra api.json](<../../.gitbook/assets/dastra api.json>)
{% endswagger %}

{% swagger src="../../.gitbook/assets/dastra api.json" path="/v1/WebHookUrls/{id}" method="delete" %}
[dastra api.json](<../../.gitbook/assets/dastra api.json>)
{% endswagger %}
