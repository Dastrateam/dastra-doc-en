# Configuration

## Setting up APIs in Dastra&#x20;

API stands for _**application programming interface**_.&#x20;

APIs enable you to connect the Dastra platform to other external tools.&#x20;

The possibilities are numerous: connection with CRM software for automated stakeholder retrieval, synchronization of a rights management tool with the Dastra module, etc.&#x20;

Dastra is based on the **API-Rest** standard, including the following HTTP requests:

| URI                                                                | GET                                                                                                | POST                                                                                                                                                                                                                    | PUT                                                                                                                                                                             | PATCH                                                                                                                                                                         | DELETE                                                                        |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| Resource collection, such as `http://api.exemple.com/collection/`  | Retrieves the URIs of the member resources of the resource collection in the body of the response. | Creates a member resource in the collection resource using the instructions in the request body. The URI of the created member resource is automatically assigned and returned in the response's Location header field. | Replaces all representations of the collection resource's member resources with the representation in the request body, or creates the collection resource if it doesn't exist. | Updates all representations of the resource collection's member resources using the instructions in the request body, or creates the resource collection if it doesn't exist. | Deletes all representations of member resources from the collection resource. |
| Member resource, such as `http://api.exemple.com/collection/item3` | Retrieves a representation of the member resource in the body of the response.                     | Creates a member resource in the member resource using the instructions in the request body. The URI of the created member resource is automatically assigned and returned in the response's Location header field.     | Replaces all representations of the member resource, or creates the member resource if it doesn't exist, with the representation in the request body.                           | Updates all representations of the member resource, or creates the member resource if it doesn't exist, using statements in the request body.                                 | Deletes all representations of the member resource.                           |

Source : [_wikipédia_](https://fr.wikipedia.org/wiki/Representational\_state\_transfer)&#x20;

With Dastra, you can configure several APIs. The list of APIs is available here: [https://api.dastra.eu/swagger/index.html](https://api.dastra.eu/swagger/index.html)

### Limitations

An http request limit is set at 500/min or 10000/10min.&#x20;

Security options (such as IP filtering) do not apply to APIs.

{% hint style="info" %}
**TIP**: Only use APIs if you know what you're doing!
{% endhint %}

The Dastra API management interface can be found at: [https://app.dastra.eu/general-settings/api](https://app.dastra.eu/general-settings/api)
