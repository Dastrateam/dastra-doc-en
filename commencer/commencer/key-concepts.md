# Key concepts

Before you start using Dastra, it's essential to understand the fundamental concepts that structure the platform.\
They will help you effectively organize your processing activities, teams, and responsibilities.

***

### 📚 Summary

* [Organization](key-concepts.md#organization)
* [Workspace](key-concepts.md#workspace)
* [Organizational unit](key-concepts.md#organizational-unit)
* [Entity](key-concepts.md#entity)
* [Department](key-concepts.md#department)
* [Organization owner](key-concepts.md#organization-owner)

***

### 🏢 Organization

An **organization** groups together the accounts and users linked to your Dastra subscription.\
It's the "root" structure that contains all your workspaces, your billing settings, and your API keys.

You can see your organization's name at the top right of the interface, below your user profile.

{% hint style="info" %}
An organization can contain several **workspaces**, each dedicated to a different project, entity, or team.\
A user can belong to several organizations.
{% endhint %}

***

### 🧰 Workspace

A **workspace** is the environment in which you collaborate with your team.\
It groups together the modules and data linked to your entities: processing activities, audits, risks, breaches, data subject rights requests, etc.

You select your workspace when logging in via the **access tiles** displayed on your homepage.

{% hint style="info" %}
Remember to name your workspaces clearly (e.g. "Group Compliance", "France Entities").\
This makes navigation and multi-entity management easier.
{% endhint %}

***

### 🧩 Organizational unit

**Organizational units** let you structure your workspace according to your internal organization.\
They are used to group entities, departments, users, and processing activities in a hierarchical logic.

Each unit can contain:

* **entities** (legal structures),
* **departments** (internal teams),
* **users**,
* **processing activities** or **tasks**.

{% hint style="info" %}
Organizational units make delegation, governance, and traceability easier in compliance projects.\
They are often used as a reference for reports or access permissions.
{% endhint %}

***

### 🏛️ Entity

An **entity** generally corresponds to a **legal entity** or a **data controller** (e.g. a company, a subsidiary, an association).\
This is the level to which you attach processing activities and key legal information.

Each entity can contain:

* the **data controller's** contact details,
* the **DPO** (data protection officer),
* the **relevant supervisory authorities**,
* and the **departments** attached to it.

Example:

> Entity: _Dastra France SAS_\
> Department: _Marketing_\
> DPO: _John Doe_ :::

***

### 🧭 Department

A **department** represents a service or division of an entity (e.g. HR, IT, Marketing, Legal).\
It lets you refine how activities are distributed within a given entity and track responsibilities by team.

Departments are notably used to:

* filter processing activities or audits by scope,
* assign tasks or requests to a targeted group,
* better visualize internal information flows.

{% hint style="info" %}
Departments are optional, but strongly recommended for medium to large organizations.\
They make it easier to manage responsibilities and track operations.
{% endhint %}

***

### 👑 Organization owner

The **owner** is the main administrator of the Dastra organization.\
They have all management rights, including creating and deleting workspaces, configuring API keys, and managing roles.

Their main responsibilities:

* Manage **users and teams** at the global level,
* Oversee **workspaces**,
* Access **advanced settings** (API, security, billing),
* Delete an account or an organization.

{% hint style="info" %}
Limit the number of owners to ensure security and consistent governance.\
Other users can be assigned appropriate roles (Admin, Contributor, Reader, etc.).
{% endhint %}

***
