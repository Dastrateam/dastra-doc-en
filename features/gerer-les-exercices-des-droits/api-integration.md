---
description: >-
  This page explains how to manipulate your data subject right requests directly
  in Dastra without integrating the javascript SDK thanks to our Rest API.
---

# API integration

As Dastra does not integrate natively with all development platforms, we provide you with a Rest API to manage your data subject right request from your applications.

## The object of the data subject right request

Below is the template for a data subject right request in Dastra&#x20;

<details>

<summary>The object of the data subject right request</summary>

```
{
  "closedByUser": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "area": {
    "order": 0,
    "children": [
      "string"
    ],
    "teams": [
      {
        "id": 0,
        "label": "string",
        "ref": "string",
        "areas": [
          0
        ],
        "users": [
          0
        ]
      }
    ],
    "id": 0,
    "type": "Entity",
    "parentId": 0,
    "ref": "string",
    "label": "string",
    "description": "string",
    "logoUrl": "string",
    "address": "string",
    "zipCode": "string",
    "city": "string",
    "countryCode": "str",
    "immatriculationNumber": "string",
    "phoneNumber": "string",
    "mailAddress": "string",
    "dpo": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-05T12:19:43.722Z",
      "dateUpdate": "2022-08-05T12:19:43.722Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "referent": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-05T12:19:43.722Z",
      "dateUpdate": "2022-08-05T12:19:43.722Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "representative": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-05T12:19:43.722Z",
      "dateUpdate": "2022-08-05T12:19:43.722Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "dataProtectionAuthority": {
      "id": 0,
      "label": "string",
      "siteURL": "string",
      "phoneNumber": "string",
      "email": "user@example.com",
      "countryCode": "str",
      "address": "string",
      "city": "string",
      "zipCode": "string"
    }
  },
  "creator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "operator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "attachments": [
    {
      "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "extension": "string",
      "size": 0,
      "nbDownload": 0,
      "transmitted": true,
      "fileName": "string",
      "label": "string",
      "userRequestMessageId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "userRequestId": 0,
      "dateCreation": "2022-08-05T12:19:43.722Z",
      "dateUpdate": "2022-08-05T12:19:43.722Z",
      "creator": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "expiration": "2022-08-05T12:19:43.722Z",
      "dateLastDownload": "2022-08-05T12:19:43.722Z",
      "dateFileRemoved": "2022-08-05T12:19:43.722Z",
      "deleted": true,
      "expired": true,
      "color": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "label": "string",
      "type": "DataProcessing",
      "color": "string"
    }
  ],
  "id": 0,
  "title": "string",
  "locale": "string",
  "archived": true,
  "archivedDate": "2022-08-05T12:19:43.722Z",
  "personCategory": "Prospect",
  "complex": true,
  "dateClosed": "2022-08-05T12:19:43.722Z",
  "areaId": 0,
  "state": "Open",
  "description": "string",
  "message": "string",
  "resolutionMessage": "string",
  "email": "string",
  "phoneNumber": "string",
  "givenName": "string",
  "familyName": "string",
  "dateCreation": "2022-08-05T12:19:43.722Z",
  "dateUpdate": "2022-08-05T12:19:43.722Z",
  "workFlowStep": {
    "id": 0,
    "label": "string",
    "color": "string",
    "order": 0,
    "itemLimit": 0,
    "type": "DataSubject",
    "finalStep": true,
    "initialStep": true,
    "descriptionHtml": "string",
    "mappedState": "string"
  },
  "workFlowStepId": 0,
  "channel": "Internal",
  "refId": "string",
  "userId": "string",
  "purposes": [
    "Unknown"
  ],
  "closedReason": "None",
  "closedReasonDescription": "string",
  "expiryTime": "2022-08-05T12:19:43.722Z",
  "address": "string",
  "zipCode": "string",
  "city": "string",
  "countryCode": "st",
  "nbMessages": 0,
  "nbMessagesNotViewed": 0,
  "remainingDays": 0,
  "closingTime": 0,
  "additionalDatas": "string",
  "userNotified": true,
  "dateUserNotified": "2022-08-05T12:19:43.722Z",
  "sendNotification": true,
  "emailValidationDate": "2022-08-05T12:19:43.722Z",
  "mailValidated": true,
  "referrerUrl": "string",
  "demandId": "string",
  "identityValidated": true,
  "dateIdentityValidated": "2022-08-05T12:19:43.722Z",
  "widgetId": 0
}
```

</details>

To retrieve the Object format of your configured custom fields, you can export a request in JSON format and obtain the JSON model.

### API's Endpoints

Here are the main Endpoints that you will need to integrate your applications with the Dastra data subject right request module.

{% swagger method="post" path="{workspaceId}​/DataSubjectRequests" baseUrl="/v1​/ws​/" summary="Create a new data subject rights request in Dastra" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
L'Id du workspace dans lequel vous souhaitez poster la demande d'exercice de droits
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
  "id": 0,
  "title": "string",
  "locale": "string",
  "archived": true,
  "archivedDate": "2022-08-31T10:24:32.381Z",
  "personCategory": "Prospect",
  "complex": true,
  "dateClosed": "2022-08-31T10:24:32.381Z",
  "areaId": 0,
  "state": "Open",
  "description": "string",
  "message": "string",
  "resolutionMessage": "string",
  "email": "string",
  "phoneNumber": "string",
  "givenName": "string",
  "familyName": "string",
  "dateCreation": "2022-08-31T10:24:32.381Z",
  "dateUpdate": "2022-08-31T10:24:32.381Z",
  "workFlowStep": {
    "id": 0,
    "label": "string",
    "color": "string",
    "order": 0,
    "itemLimit": 0,
    "type": "DataSubject",
    "finalStep": true,
    "initialStep": true,
    "descriptionHtml": "string",
    "mappedState": "string"
  },
  "workFlowStepId": 0,
  "channel": "Internal",
  "refId": "string",
  "userId": "string",
  "purposes": [
    "Unknown"
  ],
  "closedReason": "None",
  "closedReasonDescription": "string",
  "expiryTime": "2022-08-31T10:24:32.381Z",
  "address": "string",
  "zipCode": "string",
  "city": "string",
  "countryCode": "st",
  "nbMessages": 0,
  "nbMessagesNotViewed": 0,
  "remainingDays": 0,
  "closingTime": 0,
  "additionalDatas": "string",
  "userNotified": true,
  "dateUserNotified": "2022-08-31T10:24:32.381Z",
  "sendNotification": true,
  "emailValidationDate": "2022-08-31T10:24:32.381Z",
  "mailValidated": true,
  "referrerUrl": "string",
  "demandId": "string",
  "identityValidated": true,
  "dateIdentityValidated": "2022-08-31T10:24:32.381Z",
  "widgetId": 0
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="{workspaceId}​/DataSubjectRequests​/{id}" baseUrl="​/v1​/ws​/" summary="Retrieve an existing data subject rights request via its ID" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" type="Integer" required="true" %}
L'id de la demande d'exercice de droits que vous souhaitez requêter
{% endswagger-parameter %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez requêter
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
  "closedByUser": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "area": {
    "order": 0,
    "children": [
      "string"
    ],
    "teams": [
      {
        "id": 0,
        "label": "string",
        "ref": "string",
        "areas": [
          0
        ],
        "users": [
          0
        ]
      }
    ],
    "id": 0,
    "type": "Entity",
    "parentId": 0,
    "ref": "string",
    "label": "string",
    "description": "string",
    "logoUrl": "string",
    "address": "string",
    "zipCode": "string",
    "city": "string",
    "countryCode": "str",
    "immatriculationNumber": "string",
    "phoneNumber": "string",
    "mailAddress": "string",
    "dpo": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:29:26.246Z",
      "dateUpdate": "2022-08-31T13:29:26.246Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "referent": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:29:26.246Z",
      "dateUpdate": "2022-08-31T13:29:26.246Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "representative": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:29:26.246Z",
      "dateUpdate": "2022-08-31T13:29:26.246Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "dataProtectionAuthority": {
      "id": 0,
      "label": "string",
      "siteURL": "string",
      "phoneNumber": "string",
      "email": "user@example.com",
      "countryCode": "str",
      "address": "string",
      "city": "string",
      "zipCode": "string"
    }
  },
  "creator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "operator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "operatorId": 0,
  "attachments": [
    {
      "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "extension": "string",
      "size": 0,
      "nbDownload": 0,
      "transmitted": true,
      "fileName": "string",
      "label": "string",
      "userRequestMessageId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "userRequestId": 0,
      "dateCreation": "2022-08-31T13:29:26.246Z",
      "dateUpdate": "2022-08-31T13:29:26.246Z",
      "creator": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "expiration": "2022-08-31T13:29:26.246Z",
      "dateLastDownload": "2022-08-31T13:29:26.246Z",
      "dateFileRemoved": "2022-08-31T13:29:26.246Z",
      "deleted": true,
      "expired": true,
      "color": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "label": "string",
      "type": "DataProcessing",
      "color": "string"
    }
  ],
  "id": 0,
  "title": "string",
  "locale": "string",
  "archived": true,
  "archivedDate": "2022-08-31T13:29:26.246Z",
  "personCategory": "Prospect",
  "complex": true,
  "dateClosed": "2022-08-31T13:29:26.246Z",
  "areaId": 0,
  "state": "Open",
  "description": "string",
  "message": "string",
  "resolutionMessage": "string",
  "email": "string",
  "phoneNumber": "string",
  "givenName": "string",
  "familyName": "string",
  "dateCreation": "2022-08-31T13:29:26.246Z",
  "dateUpdate": "2022-08-31T13:29:26.246Z",
  "workFlowStep": {
    "id": 0,
    "label": "string",
    "color": "string",
    "order": 0,
    "itemLimit": 0,
    "type": "DataSubject",
    "finalStep": true,
    "initialStep": true,
    "descriptionHtml": "string",
    "mappedState": "string"
  },
  "workFlowStepId": 0,
  "channel": "Internal",
  "refId": "string",
  "userId": "string",
  "purposes": [
    "Unknown"
  ],
  "closedReason": "None",
  "closedReasonDescription": "string",
  "expiryTime": "2022-08-31T13:29:26.246Z",
  "address": "string",
  "zipCode": "string",
  "city": "string",
  "countryCode": "st",
  "nbMessages": 0,
  "nbMessagesNotViewed": 0,
  "remainingDays": 0,
  "closingTime": 0,
  "additionalDatas": "string",
  "userNotified": true,
  "dateUserNotified": "2022-08-31T13:29:26.246Z",
  "sendNotification": true,
  "emailValidationDate": "2022-08-31T13:29:26.246Z",
  "mailValidated": true,
  "referrerUrl": "string",
  "demandId": "string",
  "identityValidated": true,
  "dateIdentityValidated": "2022-08-31T13:29:26.246Z",
  "widgetId": 0
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="{workspaceId}​/DataSubjectRequests" baseUrl="​/v1​/ws​/" summary="Retrieve a paginated list of data subject rights requests" %}
{% swagger-description %}
You can pass optional search parameters to your query to filter the API response
{% endswagger-description %}

{% swagger-parameter in="query" name="page" type="Integer" %}
La page que vous souhaitez requêter&#x20;
{% endswagger-parameter %}

{% swagger-parameter in="query" name="size" type="Integer" %}
Le nombre d'éléments retournés par page
{% endswagger-parameter %}

{% swagger-parameter in="query" name="sortBy" type="String" %}
Le champ sur lequel filtrer l'ordre des éléments
{% endswagger-parameter %}

{% swagger-parameter in="query" name="q" %}
Recherche texte dans le titre de la demande
{% endswagger-parameter %}

{% swagger-parameter in="query" name="asc" type="Boolean" %}
true pour ordonner de manière ascendante
{% endswagger-parameter %}

{% swagger-parameter in="query" name="skip" type="Integer" %}

{% endswagger-parameter %}

{% swagger-parameter in="query" name="purposes" type="Array[String]" %}
Filtrer les demandes par type (Unknown, Information, Access, Rectification, Erasure, Restriction, Opposition, Portability, AdvanceDirectives, AutomatedDecision)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="states" type="Array[String]" %}
Filtrer les demandes par état (Open, IdentityValidation, Processing, Active, Closed)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="widgetId" type="Integer" %}
filtrer les demandes issues d'un widget de collecte
{% endswagger-parameter %}

{% swagger-parameter in="query" name="archived" type="Boolean" %}
Retourner les demandes archivées
{% endswagger-parameter %}

{% swagger-parameter in="query" name="overtaking" type="Boolean" %}
Rechercher les demandes dont le délai légal de réponse à a été dépassé
{% endswagger-parameter %}

{% swagger-parameter in="query" name="ids" type="Array[Integer]" %}
Sélectionner une liste de demandes par leurs ids
{% endswagger-parameter %}

{% swagger-parameter in="query" name="tags" type="Array[Integer]" %}
Sélectionner les demandes ayant des tags spécifiques (passer un array de tagIds en query string)
{% endswagger-parameter %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
Le workspace id que vous souhaitez requêter
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Un objet contenant les demandes d'exercices de droits retournées (propriété items), la page, la taille de la requête et le nombre total d'éléments" %}
```json
{
  "items": [
    {
      "closedByUser": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "area": {
        "order": 0,
        "children": [
          "string"
        ],
        "teams": [
          {
            "id": 0,
            "label": "string",
            "ref": "string",
            "areas": [
              0
            ],
            "users": [
              0
            ]
          }
        ],
        "id": 0,
        "type": "Entity",
        "parentId": 0,
        "ref": "string",
        "label": "string",
        "description": "string",
        "logoUrl": "string",
        "address": "string",
        "zipCode": "string",
        "city": "string",
        "countryCode": "str",
        "immatriculationNumber": "string",
        "phoneNumber": "string",
        "mailAddress": "string",
        "dpo": {
          "id": 0,
          "displayName": "string",
          "dateCreation": "2022-08-31T10:30:53.839Z",
          "dateUpdate": "2022-08-31T10:30:53.839Z",
          "logoUrl": "string",
          "actorType": "Physical",
          "vendorType": "B2B",
          "accessLevel": "None",
          "givenName": "string",
          "familyName": "string",
          "companyName": "string",
          "description": "string",
          "countryCode": "st",
          "readonly": true,
          "email": "string",
          "phoneNumber": "string",
          "contactName": "string",
          "contactPosition": "string",
          "immatriculationNumber": "string",
          "websiteUrl": "string",
          "address": "string",
          "zipCode": "string",
          "city": "string"
        },
        "referent": {
          "id": 0,
          "displayName": "string",
          "dateCreation": "2022-08-31T10:30:53.839Z",
          "dateUpdate": "2022-08-31T10:30:53.839Z",
          "logoUrl": "string",
          "actorType": "Physical",
          "vendorType": "B2B",
          "accessLevel": "None",
          "givenName": "string",
          "familyName": "string",
          "companyName": "string",
          "description": "string",
          "countryCode": "st",
          "readonly": true,
          "email": "string",
          "phoneNumber": "string",
          "contactName": "string",
          "contactPosition": "string",
          "immatriculationNumber": "string",
          "websiteUrl": "string",
          "address": "string",
          "zipCode": "string",
          "city": "string"
        },
        "representative": {
          "id": 0,
          "displayName": "string",
          "dateCreation": "2022-08-31T10:30:53.839Z",
          "dateUpdate": "2022-08-31T10:30:53.839Z",
          "logoUrl": "string",
          "actorType": "Physical",
          "vendorType": "B2B",
          "accessLevel": "None",
          "givenName": "string",
          "familyName": "string",
          "companyName": "string",
          "description": "string",
          "countryCode": "st",
          "readonly": true,
          "email": "string",
          "phoneNumber": "string",
          "contactName": "string",
          "contactPosition": "string",
          "immatriculationNumber": "string",
          "websiteUrl": "string",
          "address": "string",
          "zipCode": "string",
          "city": "string"
        },
        "dataProtectionAuthority": {
          "id": 0,
          "label": "string",
          "siteURL": "string",
          "phoneNumber": "string",
          "email": "user@example.com",
          "countryCode": "str",
          "address": "string",
          "city": "string",
          "zipCode": "string"
        }
      },
      "creator": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "operator": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "operatorId": 0,
      "attachments": [
        {
          "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "extension": "string",
          "size": 0,
          "nbDownload": 0,
          "transmitted": true,
          "fileName": "string",
          "label": "string",
          "userRequestMessageId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "userRequestId": 0,
          "dateCreation": "2022-08-31T10:30:53.839Z",
          "dateUpdate": "2022-08-31T10:30:53.839Z",
          "creator": {
            "id": 0,
            "displayName": "string",
            "familyName": "string",
            "givenName": "string",
            "email": "string",
            "color": "string",
            "avatarUrl": "string",
            "tenantId": 0
          },
          "expiration": "2022-08-31T10:30:53.839Z",
          "dateLastDownload": "2022-08-31T10:30:53.839Z",
          "dateFileRemoved": "2022-08-31T10:30:53.839Z",
          "deleted": true,
          "expired": true,
          "color": "string"
        }
      ],
      "tags": [
        {
          "id": 0,
          "label": "string",
          "type": "DataProcessing",
          "color": "string"
        }
      ],
      "id": 0,
      "title": "string",
      "locale": "string",
      "archived": true,
      "archivedDate": "2022-08-31T10:30:53.840Z",
      "personCategory": "Prospect",
      "complex": true,
      "dateClosed": "2022-08-31T10:30:53.840Z",
      "areaId": 0,
      "state": "Open",
      "description": "string",
      "message": "string",
      "resolutionMessage": "string",
      "email": "string",
      "phoneNumber": "string",
      "givenName": "string",
      "familyName": "string",
      "dateCreation": "2022-08-31T10:30:53.840Z",
      "dateUpdate": "2022-08-31T10:30:53.840Z",
      "workFlowStep": {
        "id": 0,
        "label": "string",
        "color": "string",
        "order": 0,
        "itemLimit": 0,
        "type": "DataSubject",
        "finalStep": true,
        "initialStep": true,
        "descriptionHtml": "string",
        "mappedState": "string"
      },
      "workFlowStepId": 0,
      "channel": "Internal",
      "refId": "string",
      "userId": "string",
      "purposes": [
        "Unknown"
      ],
      "closedReason": "None",
      "closedReasonDescription": "string",
      "expiryTime": "2022-08-31T10:30:53.840Z",
      "address": "string",
      "zipCode": "string",
      "city": "string",
      "countryCode": "st",
      "nbMessages": 0,
      "nbMessagesNotViewed": 0,
      "remainingDays": 0,
      "closingTime": 0,
      "additionalDatas": "string",
      "userNotified": true,
      "dateUserNotified": "2022-08-31T10:30:53.840Z",
      "sendNotification": true,
      "emailValidationDate": "2022-08-31T10:30:53.840Z",
      "mailValidated": true,
      "referrerUrl": "string",
      "demandId": "string",
      "identityValidated": true,
      "dateIdentityValidated": "2022-08-31T10:30:53.840Z",
      "widgetId": 0
    }
  ],
  "total": 0,
  "size": 0,
  "page": 0
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="{workspaceId}​/DataSubjectRequests​/{id}" baseUrl="/v1/ws/" summary="Update a data subject rights request" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="path" name="id" type="Integer" required="true" %}
L'id de la demande d'exercice de droits existante que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="body" type="Object" name="dataSubjectRequest" %}
Poster l'objet complet de la demande d'exercice de droits (voir plus haut ou notre [documentation d'api swagger](https://api.dastra.eu/swagger/index.html))
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```json
{
  "closedByUser": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "area": {
    "order": 0,
    "children": [
      "string"
    ],
    "teams": [
      {
        "id": 0,
        "label": "string",
        "ref": "string",
        "areas": [
          0
        ],
        "users": [
          0
        ]
      }
    ],
    "id": 0,
    "type": "Entity",
    "parentId": 0,
    "ref": "string",
    "label": "string",
    "description": "string",
    "logoUrl": "string",
    "address": "string",
    "zipCode": "string",
    "city": "string",
    "countryCode": "str",
    "immatriculationNumber": "string",
    "phoneNumber": "string",
    "mailAddress": "string",
    "dpo": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:44:54.781Z",
      "dateUpdate": "2022-08-31T13:44:54.781Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "referent": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:44:54.781Z",
      "dateUpdate": "2022-08-31T13:44:54.781Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "representative": {
      "id": 0,
      "displayName": "string",
      "dateCreation": "2022-08-31T13:44:54.781Z",
      "dateUpdate": "2022-08-31T13:44:54.781Z",
      "logoUrl": "string",
      "actorType": "Physical",
      "vendorType": "B2B",
      "accessLevel": "None",
      "givenName": "string",
      "familyName": "string",
      "companyName": "string",
      "description": "string",
      "countryCode": "st",
      "readonly": true,
      "email": "string",
      "phoneNumber": "string",
      "contactName": "string",
      "contactPosition": "string",
      "immatriculationNumber": "string",
      "websiteUrl": "string",
      "address": "string",
      "zipCode": "string",
      "city": "string"
    },
    "dataProtectionAuthority": {
      "id": 0,
      "label": "string",
      "siteURL": "string",
      "phoneNumber": "string",
      "email": "user@example.com",
      "countryCode": "str",
      "address": "string",
      "city": "string",
      "zipCode": "string"
    }
  },
  "creator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "operator": {
    "id": 0,
    "displayName": "string",
    "familyName": "string",
    "givenName": "string",
    "email": "string",
    "color": "string",
    "avatarUrl": "string",
    "tenantId": 0
  },
  "operatorId": 0,
  "attachments": [
    {
      "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "extension": "string",
      "size": 0,
      "nbDownload": 0,
      "transmitted": true,
      "fileName": "string",
      "label": "string",
      "userRequestMessageId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "userRequestId": 0,
      "dateCreation": "2022-08-31T13:44:54.781Z",
      "dateUpdate": "2022-08-31T13:44:54.781Z",
      "creator": {
        "id": 0,
        "displayName": "string",
        "familyName": "string",
        "givenName": "string",
        "email": "string",
        "color": "string",
        "avatarUrl": "string",
        "tenantId": 0
      },
      "expiration": "2022-08-31T13:44:54.781Z",
      "dateLastDownload": "2022-08-31T13:44:54.781Z",
      "dateFileRemoved": "2022-08-31T13:44:54.781Z",
      "deleted": true,
      "expired": true,
      "color": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "label": "string",
      "type": "DataProcessing",
      "color": "string"
    }
  ],
  "id": 0,
  "title": "string",
  "locale": "string",
  "archived": true,
  "archivedDate": "2022-08-31T13:44:54.781Z",
  "personCategory": "Prospect",
  "complex": true,
  "dateClosed": "2022-08-31T13:44:54.781Z",
  "areaId": 0,
  "state": "Open",
  "description": "string",
  "message": "string",
  "resolutionMessage": "string",
  "email": "string",
  "phoneNumber": "string",
  "givenName": "string",
  "familyName": "string",
  "dateCreation": "2022-08-31T13:44:54.781Z",
  "dateUpdate": "2022-08-31T13:44:54.781Z",
  "workFlowStep": {
    "id": 0,
    "label": "string",
    "color": "string",
    "order": 0,
    "itemLimit": 0,
    "type": "DataSubject",
    "finalStep": true,
    "initialStep": true,
    "descriptionHtml": "string",
    "mappedState": "string"
  },
  "workFlowStepId": 0,
  "channel": "Internal",
  "refId": "string",
  "userId": "string",
  "purposes": [
    "Unknown"
  ],
  "closedReason": "None",
  "closedReasonDescription": "string",
  "expiryTime": "2022-08-31T13:44:54.781Z",
  "address": "string",
  "zipCode": "string",
  "city": "string",
  "countryCode": "st",
  "nbMessages": 0,
  "nbMessagesNotViewed": 0,
  "remainingDays": 0,
  "closingTime": 0,
  "additionalDatas": "string",
  "userNotified": true,
  "dateUserNotified": "2022-08-31T13:44:54.781Z",
  "sendNotification": true,
  "emailValidationDate": "2022-08-31T13:44:54.781Z",
  "mailValidated": true,
  "referrerUrl": "string",
  "demandId": "string",
  "identityValidated": true,
  "dateIdentityValidated": "2022-08-31T13:44:54.781Z",
  "widgetId": 0
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="delete" path="{workspaceId}​/DataSubjectRequests​/{id}" baseUrl="​/v1​/ws​/" summary="Delete a data subject rights request via its ID" %}
{% swagger-description %}
Please note that this action is irreversible, and your request will be permanently deleted from our databases.
{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="path" name="id" type="Integer" required="true" %}
L'id de la demande d'exercice de droits existante que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="{workspaceId}​/DataSubjectRequests​/workflow" baseUrl="/v1​/ws​/" summary="Change the process step of the data subject right request" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" required="true" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" type="Integer" %}
L'id de la demande d'exercice de droits dont vous souhaitez modifier l'étape de processus
{% endswagger-parameter %}

{% swagger-parameter in="body" name="stepId" type="Integer" %}
L'id de l'étape de processus que vous souhaitez appliquer à la demande d'exercice de droits
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="{workspaceId}​/DataSubjectRequests​/archive​/{id}" baseUrl="/v1​/ws​/" summary="Archive a data subject right request via its ID" %}
{% swagger-description %}
This endpoint applies the "Archived" state to the DSR request
{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="path" name="id" type="Integer" %}
L'id de la demande d'exercice de droits que vous souhaitez archiver
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Success" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="{workspaceId}​/DataSubjectRequests​/restore​/{id}" baseUrl="​/v1​/ws​/" summary="Remove archived status from a DSR request" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="workspaceId" type="String" %}
L'id de l'espace de travail dans lequel se trouve la demande d'exercice de droits que vous souhaitez supprimer
{% endswagger-parameter %}

{% swagger-parameter in="path" name="id" type="Integrer" %}
L'id de la demande d'exercice de droits que vous souhaitez restaurer
{% endswagger-parameter %}
{% endswagger %}
