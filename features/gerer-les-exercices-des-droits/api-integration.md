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

### API's Endpoints

Here are the main Endpoints that you will need to integrate your applications with the Dastra data subject right request module.
