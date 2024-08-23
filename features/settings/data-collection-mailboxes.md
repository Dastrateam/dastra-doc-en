---
description: Learn how to set up a data collection email box
---

# Incoming mail data collection

### **Introduction**

This integration allows you to automatically create objects in Dastra from emails received at dedicated email boxes. Dastra provides these boxes and automates the conversion of incoming emails into objects within the Dastra application.

Five types of objects can be associated with these collection email boxes:

* Tasks
* Data Processing
* Data Subject Requests
* Contracts
* Data Breaches

### **Setting up a collection email**

To set up a collection email for any of the objects listed above, go to your workspace settings, under the Integrations tab, and select the "Incomin mail data collection" card.

<figure><img src="../../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>

Then, choose the type of object for which you want to set up the integration by clicking on "Add Integration." Note that you can only have one collection email per object type and per workspace.

<figure><img src="../../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure>



You have the option to specify the destination organizational unit for the objects created through this collection box during the integration setup. If this field is left empty, objects will be created in the default organizational unit.

<figure><img src="../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

By clicking "Create," Dastra finalizes the integration setup and provides you with the email address to use.

<figure><img src="../../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

### **Key Features**

* **Automatic object creation**: Each email received at an associated email box creates a corresponding object in Dastra.
* **Organizational unit configuration**: You can set a destination organizational unit during setup. If specified, the object will be created in that unit.
* **Object fields management**:
  * **Label**: The email subject is used as the name of the created object.
  * **Description**: The email body is used for the description of the created object.
  * **Attachments**: Email attachments are added to the object, subject to validation conditions.

### **Attachment Management**

Email attachments are added to the object, provided that:

* **File extensions are valid**: Only attachments with valid file extensions are retained.

Here are the autorized extensions : `7z`, `csv`, `doc`, `docx`, `eml`, `epub`, `gif`, `htm`, `html`, `jpeg`, `jpg`, `json`, `md`, `msg`, `ods`, `odg`, `odp`, `odt`, `pdf`, `png`, `ppt`, `pptx`, `rar`, `rtf`, `svg`, `txt`, `xls`, `xlsm`, `xlsx`, `zip`.

* **Images meet minimum size**: For image files (jpg, png, gif, etc.), a minimum size of 5 KB is required. This constraint helps avoid including irrelevant images such as email signatures.

### **Finding Objects Generated from a Collection Box**

Objects associated with collection boxes have a 'source' or 'collection origin' field that you can display in table views by showing the source/collection origin column.

All objects generated from a collection box are tagged with "inbound email," making it easy to identify them if needed.

### **Success Notification**

Upon successful creation of an object from an email received at the collection box, an email notification is automatically sent to the address that triggered the integration. This notification confirms that the object has been successfully created in Dastra, providing immediate assurance that the request or action has been processed.

The language of the confirmation email corresponds to the default language of the workspace where the integration is installed (Workspace settings > Default language).
