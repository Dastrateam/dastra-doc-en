---
description: Learn how to manage documents and files in Dastra.
---

# Document management

Dastra natively integrates a **document management module** that allows you to centralise and share access to all documents associated with your compliance work.

This is where you can store all documentation useful for proving your GDPR compliance — from internal procedures and policies to training records, DPIAs and contracts.

{% hint style="info" %}
**Focus on GDPR documentation**

The documentation requirement stems from the **accountability principle** set out in Article 24 of the GDPR.

In practice, this goes beyond the record of processing activities and includes (non-exhaustive list):

* Internal procedures for creating new personal data processing activities
* DPIA methodology and completed assessments
* Written data protection policies
* Data mapping and inventory procedures
* Training records for staff involved in data processing
* Data subject rights management procedures
* Internal complaint handling mechanisms
* Data breach management and notification procedures
* Internal or external audit reports and findings
* Contract documentation for processors and joint controllers
{% endhint %}

## Accepted file formats

Many formats are supported:

* PDF
* Word (.docx)
* Excel (.xlsx)
* Images (JPG, PNG, etc.)
* Archives (.zip)
* And many more

{% hint style="info" %}
If a specific format is not accepted, you can add it to a `.zip` archive and upload that instead.
{% endhint %}

## Creating a document

With Dastra, you can quickly create a document for note-taking directly in the platform.

Go to the document management module and click **"Write a document"**.

The new document is saved in **Markdown format** (.md) and can be edited directly in Dastra.

### Generate a document with AI

The AI assistant can **automatically generate a document** from a prompt and, where needed, additional files provided as context.

To use it, click **"Generate with AI"** in the document management module, describe the document you need (type, purpose, expected content) and optionally attach existing files to enrich the context. The assistant generates the document directly in Dastra, where you can then review, edit and save it.

{% hint style="info" %}
This feature is particularly useful for quickly drafting data protection policies, internal procedures, or any other GDPR compliance documentation.
{% endhint %}

## Creating folders

You can organise your documents into folders for easy retrieval. Sub-folders are supported.

## Access rights management

It is possible to restrict access to specific folders and files. Permissions can be assigned to both folders and files, and can be configured by the workspace administrator or any user with the "File management: manage" permission.

{% hint style="info" %}
**Important:** By default, no restrictions are applied to the folder tree. User role permissions are still enforced.
{% endhint %}

The workspace owner (or administrator) can configure access rights by clicking the settings icon on the relevant row, then adding teams and users with the appropriate permission level.

Permissions are applied to all **child elements** (i.e. all items contained within the folder, including sub-folders).

{% hint style="info" %}
A folder with no defined permissions is accessible to all users.

If permissions have been defined or inherited on an element, it will be hidden from users who do not have the required authorisations.
{% endhint %}

## Cloud storage integration

By default, Dastra stores files on a secure Azure Blob Storage system (encrypted, virus-scanned, redundant). You can also connect your own cloud storage provider — Google Drive or OneDrive — to avoid duplicating files across systems.

{% content-ref url="../settings/integrations-onedrive-google-drive.md" %}
[integrations-onedrive-google-drive.md](../settings/integrations-onedrive-google-drive.md)
{% endcontent-ref %}

## Document templates

Dastra provides ready-to-use document templates to help you build your compliance documentation.

{% content-ref url="document-templates.md" %}
[document-templates.md](document-templates.md)
{% endcontent-ref %}
