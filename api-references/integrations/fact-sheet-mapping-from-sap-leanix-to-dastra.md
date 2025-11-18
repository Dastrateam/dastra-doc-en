---
description: '(Planned release: Q1 2026)'
---

# Fact Sheet Mapping from SAP LeanIX to Dastra

### **Overview**

The LeanIX → Dastra connector provides an automated, scheduled synchronization that transfers selected information from **SAP LeanIX Fact Sheets** of type **Application** into **Dastra Assets**.\
Dastra acts as the **destination system**, receiving application metadata from LeanIX via the **LeanIX Pathfinder API**:

```
GET /services/pathfinder/v1/factSheets (type = Application)
```

During each synchronization cycle, the connector evaluates incoming LeanIX applications and performs one of the following actions in Dastra:

* **Update an existing Asset** if a corresponding LeanIX Fact Sheet already exists in Dastra
* **Create a new Asset** if no match is found
* **Flag an existing Asset** if the LeanIX Fact Sheet has been removed

This ensures continuous alignment between the LeanIX application inventory and Dastra’s asset catalog.

### **Architecture Overview**

Below is a conceptual representation of the end-to-end synchronization:

```
SAP LeanIX (Pathfinder API)
     |
     | GET /services/pathfinder/v1/factSheets (Application)
     v
 Fact Sheets (Applications)
     |
     |  Overnight Data Sync
     v
 Dastra (Assets)
```

During the import process, selected fields from LeanIX Fact Sheets are **directly mapped** to Dastra Asset properties.\
![](<../../.gitbook/assets/image Dastra SAP LeanIX (1).png>)

### **Synchronization Process**

#### **1. Extraction from LeanIX**

The connector retrieves all **Application**–type Fact Sheets from LeanIX through the Pathfinder API.

Each Fact Sheet contains identifiers, descriptive fields, tags, and relational attributes. Only selected attributes are mapped into Dastra.

#### **2. Asset Matching in Dastra**

Each incoming application is matched against existing Dastra assets using the LeanIX **Fact Sheet identifier** (`ref`).

Matching rules:

* If an Asset exists with the same `ref` → **Asset is updated**
* If no Asset exists → **New Asset is created**

#### **3. Lifecycle Handling**

If an Asset exists in Dastra but the associated LeanIX application is no longer present in the API response:

* Dastra **does not delete the Asset**
* Instead, the Asset is marked with a special tag:

```
leanix-todelete
```

This enables controlled lifecycle management instead of automatic deletion.

#### **4. Scheduling**

The synchronization runs **once per night** by default.\
Additional triggers may be implemented depending on system configuration.

***

### **Field Mapping (LeanIX → Dastra)**

The following table lists all fields imported from LeanIX and their corresponding target fields in Dastra:

| LeanIX Field       | Dastra Asset Field | Description                                            |
| ------------------ | ------------------ | ------------------------------------------------------ |
| `displayName`      | **name**           | Name of the LeanIX application                         |
| `description`      | **description**    | Free-text description of the application               |
| `tags[]`           | **tags**           | LeanIX application tags copied into Dastra             |
| `user` (if mapped) | **user**           | Linked user in Dastra, only if the user already exists |
| `id`               | **ref**            | LeanIX Fact Sheet unique identifier                    |
| _(N/A)_            | **type**           | Always set to `"Software"` for imported assets         |

***

### **Tag Behavior**

#### **Inherited Tags**

All LeanIX tags are transferred to Dastra during creation or update.

#### **Deletion Marker**

If a LeanIX application disappears from the portfolio, Dastra adds:

```
leanix-todelete
```

This tag persists until manually processed, enabling administrators to:

* Archive the Asset
* Retire it
* Or remove the tag if the application reappears

***

### **Error Handling & Diagnostics**

The connector logs data synchronization events, including:

* Number of applications fetched
* Assets created or updated
* Assets marked for deletion
* API response status codes
* Mapping inconsistencies or missing required attributes

Administrators may review logs within Dastra (future log interface planned) or external monitoring tools depending on system configuration.

***

### **Benefits**

#### **Automated Inventory Alignment**

Ensures that Dastra’s asset catalog stays consistent with LeanIX without manual intervention.

#### **Controlled Asset Lifecycle**

Soft-delete behavior prevents accidental data loss while preserving auditability.

#### **Consistent Tag Propagation**

LeanIX tagging strategies are reflected in Dastra, supporting classification, workflows, and reporting.

#### **Standardized Software Asset Model**

All inbound applications use a uniform Dassian Asset type (`Software`), simplifying governance and downstream processing.

***

### **Future Enhancements (Post-2026 Roadmap)**

Potential extensions under consideration:

* Bi-directional synchronization
* Custom field mapping configurations
* Support for additional Fact Sheet types (IT Component, Business Capability, etc.)
* Real-time sync triggers instead of overnight batching
