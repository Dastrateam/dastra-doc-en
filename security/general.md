---
description: >-
  Security is an integral part of the structure of our Cloud products, our
  infrastructure and our processes, so you can be sure that your data is
  protected.
---

# Security at Dastra

## Two-factor authentication required

All organization owners have the ability to force the use of two-factor authentication.

## Authorization list of IP addresses

Organization's owner are able to secure the application's connection using Ip whitelisting

## Secure cloud hosting

All of your data is stored at Microsoft Azure in hosting resources located in France and Netherland.

## Encryption of data in transit

All data exchanged between our customers and applications is encrypted in transit using the TLS (Transport Layer Security) protocol with PFS (Perfect Forward Secrecy). The encryption certification authority is CloudFlare inc.

## Data encryption at rest

The data disks on the servers hosting customer data in the Azure cloud are all encoded at rest using "Transparent data encryption" technology.

The physical files are also statically encrypted in the Azure Storage service with a 256-bit transparent encryption system AES encryption, one of the strongest algorithms which is FIPS 140-2 compliant.

## Organization audit logs

Organization administrators can track all changes to user management and access permissions.

## Unique identifiers

Each user has a unique identifier and the use of accounts shared between several users is not authorized.

## **Data backup**

All of the data (Azure SQL) and files (Azure Blob Storage) of our users are regularly backed up with a history of one month.

## Data archiving rules

In the case of an account deletion, the data is kept for 1 month before its final deletion.

## Password rules

At least 8 characters comprising 3 of the 4 types of characters (uppercase, lowercase, numbers, special characters)**.**

Delay in accessing the account after several failures.

&#x20;Encryption of passwords in databases with strong encryption rules**.**

## API token controls

View and manage all API keys used by developers in your organization

## Full access control

Use of the role-base-access-control (RBAC) access management model. The person in charge of the organization is able to choose the roles and permissions of each user.

## Secure authentication based on OpenIdConnect for all of our sites

![](<../.gitbook/assets/image (293).png>)

The authentication authority is [https://account.dastra.eu](https://account.dastra.eu) uses IdentityServer4 technology to ensure the authentication of all our users.

OpenID is a decentralized authentication system that enables single sign-on, as well as attribute sharing. It allows a user to authenticate with several sites (having to support this technology) without having to remember an identifier for each of them but by using each time a unique OpenID identifier.

