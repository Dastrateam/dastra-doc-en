---
description: Find out how the Dastra invitation system works.
---

# Invite users

## Invite users

You can invite someone to collaborate on your workspaces by inviting them to the organization to which the workspace belongs.&#x20;

You can invite users to your workspace by clicking on the "settings" button at the bottom left of the screen, then "access management / users" and finally "invite a user":

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-06-01 à 16.30.07.png" alt=""><figcaption></figcaption></figure>

Enter the e-mail address of the person you wish to invite in your Dastra space. If this address is not already attached to the organization, click on it to send an invitation link.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-06-01 à 16.35.11.png" alt="" width="563"><figcaption></figcaption></figure>

A form appears. Enter your surname, first name, role and team, then click on the "Send invitation" button. The invited person will receive an e-mail containing a link which, once clicked, will enable that person to access the space, at this time a notification mail will be sent to you.

That's it, the user has been invited!

## Current invitations

You can control current invitations in the "Users" section of the workspace settings.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-06-01 à 16.37.02.png" alt="" width="360"><figcaption></figcaption></figure>

## Resend invitation link

If the invited user has not clicked on the invitation link and the link has expired (after 10 days), you can resend the invitation link by clicking on the "Resend invitation" button.

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

## Create and assign teams

In Dastra, users are grouped into teams, which in turn are assigned to either legal entities or departments. In this way, roles and responsibilities can be finely managed.

{% hint style="info" %}
There are several default roles in Dastra, representing different levels of authorization:&#x20;

* **Administrator**: They can do everything authors can do, plus modify organization and space settings.&#x20;
* **Contributor**: They can read and edit spaces. They can see drafts and changes not yet published. They can publish modifications. They cannot modify organization or space parameters.&#x20;
* **Reader**: They can only visit spaces published in the organization. They cannot edit and cannot see changes that have not yet been published.
{% endhint %}

## Import a large user list

If you wish to import a large user list (minimum 50 users), you can request the import of a large user list into the platform (maximum 200 users). To do this, you need to go through the Dastra teams.&#x20;

The steps to follow:&#x20;

* Go to this link: [https://app.dastra.eu/general-settings/users](https://app.dastra.eu/general-settings/users?q=\&page=1\&size=20)
* Click on the button "Import"

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-06-01 à 16.48.20.png" alt="" width="186"><figcaption></figcaption></figure>

* Create a file for each workspace in CSV format with the following columns separated by " , " (comma):

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-06-01 à 16.49.11.png" alt=""><figcaption></figcaption></figure>

Mandatory fields:

* Email (user's email)&#x20;
* GivenName (user's first name)&#x20;
* FamilyName(user's last name)&#x20;
* Roles (separated by |) > this corresponds to the roles in Dastra&#x20;
* Teams (separated by |) > this corresponds to teams in Dastra

Optional:&#x20;

* SsoConfigurationId > this corresponds to the SSO login identifier, if applicable

Here is a sample file for you to download and fill in:

{% file src="../../.gitbook/assets/Template_import_users.csv" %}
Import file template
{% endfile %}

**Role identifiers:**&#x20;

By default: basic roles have the following identifiers:&#x20;

* Administrator = 1&#x20;
* Contributor = 2&#x20;
* Reader = 3&#x20;

For custom roles you've created, the identifier is visible from your browser's development console via the network tab.

{% hint style="info" %}
To open the console on Chrome, use the following keyboard shortcut: Cmd + Option + C (on Mac) or Ctrl + Shift + J (on Windows)&#x20;

To open the console on Firefox, use the following keyboard shortcut: Cmd + Option + K (on Mac) or Ctrl + Shift + J (on Windows)&#x20;

To open the console, use the following keyboard shortcut: Cmd + Option + C&#x20;

To open the console on Microsoft Edge, you can use the following shortcut: Ctrl + Shift + I
{% endhint %}

Please note that roles must be created in advance.

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption><p>Here the role identifier is number 115</p></figcaption></figure>

**For team identifiers:**

These can be set when adding a team.

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Please note that teams must first be created in the workspace.
{% endhint %}

Save your file in CSV UTF 8 format

<figure><img src="https://138894690-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2FC1FElrWgEomvNHuCAXgC%2Fimage.png?alt=media&#x26;token=e83fc031-1943-452a-b4b5-40e5f4220813" alt=""><figcaption></figcaption></figure>

Once your file is ready, tell us in which workspace you wish to import users and upload the file via the upload interface.

We'll receive your request and get back to you.
