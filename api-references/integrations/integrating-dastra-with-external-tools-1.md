---
description: >-
  This page is a comprehensive guide on how to integrate Dastra with external
  tools, outlining different integration models (Zapier, microservices, direct
  API), detailed workflows and practical use case
---

# Integrating Dastra with External Tools

Organizations often need to integrate **Dastra’s compliance and orchestration capabilities** with external systems such as data discovery/redaction tools, IT asset inventories, CRMs, vendor management, or task management platforms. These integrations allow teams to:

* Automate repetitive compliance tasks.
* Synchronize data across systems.
* Ensure legal and regulatory consistency (GDPR, CCPA, etc.).
* Enhance visibility and collaboration.

This guide introduces three integration models (from lightweight to enterprise-grade), provides example workflows, and outlines **typical use cases** with relevant Dastra API endpoints.

***

### 🔹 Integration Models

#### 1. Lightweight Workflows via Zapier (Webhooks + APIs)

**Best for:** Simple automations with low–moderate data volumes.

**Workflow:**

1. **Trigger in Dastra** → DSAR or event triggers a webhook.
2. **Zapier receives webhook** → calls external tool’s API.
3. **Results processed** → external tool returns data to Zapier.
4. **Update in Dastra** → Zapier uses Dastra’s REST API to attach results (`POST /requests/{id}/attachments`) or update statuses.

✅ **Pros:** Quick to set up, no development needed.\
⚠️ **Cons:** Limited payload size, execution timeouts.

***

#### 2. Intermediate Workflows via Zapier + Microservice

**Best for:** Mid-scale workflows requiring more flexibility than Zapier alone.

**Workflow:**

1. **Trigger in Dastra → Zapier.**
2. **Zapier calls a custom microservice** (AWS Lambda, Azure Function, GCP Cloud Run).
3. **Microservice handles heavy logic** → retries, pagination, file processing.
4. **Microservice returns results** → Dastra REST API updates.

✅ **Pros:** Combines low-code visibility with backend robustness.

***

#### 3. Direct API Integration

**Best for:** Enterprise-grade deployments with strict SLAs, high volumes, and advanced security requirements.

**Workflow:**

1. **Dastra calls the external API directly** when a trigger occurs.
2. **External system executes workflow** (discovery, classification, redaction, etc.).
3. **Results pushed back to Dastra** via API (`PATCH /requests/{id}`, `POST /requests/{id}/attachments`).
4. **Dastra orchestrates compliance response** across systems.

✅ **Pros:** Robust, scalable, eliminates Zapier limitations.\
⚠️ **Cons:** Requires dedicated development, careful API security, and rate-limit handling.

***

### 🔹 Choosing the Right Approach

| **Scenario**                             | **Recommended Approach** |
| ---------------------------------------- | ------------------------ |
| Proof of concept, small datasets         | Zapier (Webhooks + APIs) |
| Mid-scale, moderate complexity           | Zapier + Microservice    |
| Enterprise-grade, high-volume, regulated | Direct API Integration   |

***

### 📘 Typical Use Cases & API Endpoints

Below are common integration scenarios, what they achieve, and the **Dastra API endpoints** to use ([API reference](https://doc.dastra.eu/api-references/liste-des-endpoints-dapi?utm_source=chatgpt.com)):

#### 1. Data Subject Right Orchestration with External Tools

* **Purpose:** Trigger external discovery/redaction workflows when a DSAR is received; aggregate and attach results.
* **Endpoints:**
  * `POST /v1/ws/{workspaceId}/DataSubjectRequests` → create a DSAR.
  * `POST /v1/ws/{workspaceId}/DataSubjectAttachments/{dataSubjectRequestId}` → attach exports.
  * `PATCH /v1/ws/{workspaceId}/DataSubjectRequests/{id}` → update status.

***

#### 2. Integration with IT Asset Inventory Management

* **Purpose:** Synchronize IT assets with Dastra, link assets to processing records, and update automatically.
* **Endpoints:**
  * `GET /v1/ws/{workspaceId}/Assets` / `POST /v1/ws/{workspaceId}/Assets`.
  * `PATCH /v1/ws/{workspaceId}/Assets/{id}`.
  * `POST /v1/ws/{workspaceId}/Assets/import`.

***

#### 3. Integration with CRM Systems

* **Purpose:** Synchronize customer data, manage consent, create DSARs directly from CRM events.
* **Endpoints:**
  * `GET /v1/ws/{workspaceId}/Actors`, `POST /v1/ws/{workspaceId}/Actors`.
  * `POST /v1/ws/{workspaceId}/DataSubjectRequests`.
  * `GenericRelationships` / `DataProcessingRelationships`.

***

#### 4. Integration with Vendor Management Systems

* **Purpose:** Manage supplier contracts, monitor third-party risks, and link vendors to processing activities.
* **Endpoints:**
  * `GET /v1/ws/{workspaceId}/Contracts`, `POST /v1/ws/{workspaceId}/Contracts`.
  * `GET /v1/ws/{workspaceId}/Assets` / `Actors`.
  * `GenericRelationships`.

***

#### 5. Integration with Data Catalog Systems

* **Purpose:** Import metadata, classify fields, and enrich data processing registries.
* **Endpoints:**
  * `GET /v1/ws/{workspaceId}/DataFields`.
  * `POST /v1/ws/{workspaceId}/DataProcessings`, `PATCH /v1/ws/{workspaceId}/DataProcessings/{id}`.
  * `DataProcessingRelationships`.

***

#### 6. Integration with Content Management Systems (CMS)

* **Purpose:** Automate redaction, archival, or attachment of content/documents in compliance workflows.
* **Endpoints:**
  * `CloudStorage` APIs: `GET /v1/ws/{workspaceId}/CloudStorage/{providerName}/{fileId}`, `POST /v1/ws/{workspaceId}/CloudStorage/{providerName}`.
  * `DataSubjectAttachments`.
  * Document management APIs.

***

#### 7. Integration with Task Management Systems

* **Purpose:** Create and assign compliance tasks (audits, reviews, follow-ups) linked to Dastra workflows.
* **Endpoints:**
  * `GET /v1/ws/{workspaceId}/Tasks`, `POST /v1/ws/{workspaceId}/Tasks`.
  * `PATCH /v1/ws/{workspaceId}/Tasks/{id}`.
  * `Users`, `Teams`, `Workflows` for assignment & lifecycle management.

***

### 🚀 Key Takeaways

* **Zapier + Dastra** enables fast, no-code integrations for simple use cases.
* **Hybrid models** (Zapier + microservices) handle mid-scale complexity reliably.
* **Direct API integrations** are the gold standard for enterprise-grade compliance.
* With these models, organizations can integrate Dastra seamlessly into IT, data, and business ecosystems.
