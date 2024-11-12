---
description: >-
  This documentation page explains how Dastra natively integrates with your
  preferred cloud file provider for DMS file storage.
---

# OneDrive/Google Drive integrations

## The benefits of customized cloud storage

By default, Dastra's file manager relies on a standard secure storage system based on Azure Blob Storage. Files are encrypted and scanned for viruses. Files are redundantly stored on another server. To find out more, see our Dastra security documentation.

Although very secure and practical in most scenarios, file storage in the Dastra application can duplicate other EDMs or cloud file managers. To remedy this problem, Dastra integrates natively with the leading cloud file providers.



## Setting up customized cloud storage

Setting up your cloud file manager is easy:

* Go to the Dastra's file manager
* Click on the **selector at the top left of the files**

<div align="left">

<figure><img src="../../.gitbook/assets/image.avif" alt=""><figcaption></figcaption></figure>

</div>

* Click on **Manage cloud storage**
* Choose your provider (Google Drive or OneDrive)

<div align="left">

<figure><img src="../../.gitbook/assets/image (1).avif" alt=""><figcaption></figcaption></figure>

</div>

* **Click on the “Add” button**, and you'll be redirected to the provider's login page, where you'll be asked for the authorizations needed to establish a connection with Dastra.
* At the end of the process, you'll be asked to choose the drive disk you wish to use (a Google Drive or a Sharepoint disk for OneDrive).



## Attach files from your cloud to Dastra

* Edit any entity: task, treatment, actor...
* Choose the data source at the top left of the file upload box.

![](https://doc.dastra.eu/\~gitbook/image?url=https%3A%2F%2F1301193153-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LvBxs22wUMicv9uWp6C-2584506019%252Fuploads%252FX7IKm0XiPWhu4YB4bzle%252Fimage.png%3Falt%3Dmedia%26token%3D541572c6-4155-4766-8983-c4ad544cf6de\&width=300\&dpr=4\&quality=100\&sign=b188786e\&sv=1)

* Upload files directly to your Drive (Modify them, move them)
* Click on select in the manager and choose the file to attach

<figure><img src="https://doc.dastra.eu/~gitbook/image?url=https%3A%2F%2F1301193153-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-LvBxs22wUMicv9uWp6C-2584506019%252Fuploads%252FQBfPZ9LRcQAFd2rmIiMt%252Fimage.png%3Falt%3Dmedia%26token%3D034f575b-1127-49e6-ba5c-79d98f912c7f&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=67ad21f9&#x26;sv=1" alt=""><figcaption></figcaption></figure>

## Limitations

Google Drive: please note that only files created in your Dastra space can be added or modified in your Google Drive. Dastra does not have access rights to files created on your side in the Drive. This is a limitation of this connector. You can share files created in Dastra with other collaborators without any problem.

One Drive: the system has only been tested on the personal version of OneDrive. If you encounter any problems with the enterprise versions, please contact support.

By default, Dastra will create files in the “ApplicationsDastraOneDrive” directory, which it will consider its root.



{% hint style="warning" %}
Please note! Setting up the OneDrive connection **gives access to all the files in your personal Drive**. You must therefore be very careful, as the connector will be made available to all users with “Files” reading rights.

We recommend that you use a service account that cannot contain personal files, with a folder that you can share with other users.
{% endhint %}
