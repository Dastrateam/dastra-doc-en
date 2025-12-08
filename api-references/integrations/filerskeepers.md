# Filerskeepers

### What is Filerskeepers?

[Filerskeepers](https://www.filerskeepers.co/) is a service that provides **ready-to-use data retention schedules**, covering legal retention requirements from all around the world.\
It helps companies **determine how long to keep or delete each type of data** in order to remain compliant with applicable regulations.

#### Prerequisites

* Have a paid Dastra license
* Have a Filerskeepers account. If you don’t have one yet and you are already a Dastra customer, you can [contact our sales team](https://meetings-eu1.hubspot.com/yann-forveille/rendez-vous-avec-un-expert?message=Filerskeepers+Integration), who can offer you preferential pricing.
* Have set up a data retention repository (“Schedule”) in the Filerskeepers software. The integration requires this repository to access your catalog data.

#### Installation

The setup process is very simple:

* **Go to the Filerskeepers integration page** in the Dastra integrations marketplace:\
  [https://app.dastra.eu/workspace/0/settings/integrations/filerskeepers](https://app.dastra.eu/workspace/0/settings/integrations/filerskeepers)
* Click the **“Install”** button.
*   **Enter your Filerskeepers administrator account credentials** (email + password). These credentials will allow us to generate an access token for the Filerskeepers API.

    <figure><img src="https://1301193153-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2FCls3HcfwabQ0ak8kaPxq%2Fimage.png?alt=media&#x26;token=450bc67c-ed5a-43af-afdb-de14e07738b6" alt=""><figcaption></figcaption></figure>
* A configuration window will appear. This configuration is required to finalize the installation. In the form, select the “Schedule” you want to configure with Dastra.

<figure><img src="https://1301193153-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2F50Ptq636RLYEYiIyposg%2Fimage.png?alt=media&#x26;token=2576d278-4e85-4136-a675-0dab1b3026b6" alt=""><figcaption></figcaption></figure>

#### Configuration

* Select the Filerskeepers repository you want to synchronize with Dastra.
* Choose whether you want to enable automatic synchronization of retention periods. (Datasets synchronized with Filerskeepers will be updated every night at 00:00 UTC.)
* Select the people who should be notified in case of modifications/creations of retention periods in the datasets. The selected person will receive an email containing details on the datasets that were updated.
* Checking **"Create new datasets if not exists"** will create a dataset for every data type declared in your Filerskeepers account.

> **ℹ️ Info**\
> Be aware: if you check this box, a large number of datasets will be created automatically in your workspace.

#### Selecting the retention policy

The Filerskeepers connector offers several modes of operation:

* Display of the retention period selector based on your Filerskeepers retention repository (called “Schedule” in the software).

From now on, when you open a dataset in Dastra, in the “Retention Policies” section, a button to select a retention policy will appear.

<figure><img src="https://1301193153-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2FxGZOazurdAFSNB9rVQsA%2Fimage.png?alt=media&#x26;token=f8f95095-4069-442a-a264-bfa593bf3bfb" alt=""><figcaption></figcaption></figure>

By clicking this button, you can directly select a dataset from your Filerskeepers repository. **This retention period will be automatically synchronized** with Dastra if you enabled this option in the integration configuration.

<figure><img src="https://1301193153-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2FusvwbEFIiUr6K2a5JoMu%2Fimage.png?alt=media&#x26;token=6fae00b9-d7aa-46f9-8496-14c30e3b570d" alt=""><figcaption></figcaption></figure>

Select a dataset by clicking the **"Select"** button.

Once you have selected the retention period, the window will close and the following information will be displayed:

<figure><img src="https://1301193153-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2FjBBUvXxRkiMouICp0t8X%2Fimage.png?alt=media&#x26;token=577a42ba-2881-46ed-a671-2f411da64cb5" alt=""><figcaption></figcaption></figure>

> **ℹ️ Info**\
> Only retention periods related to active data stores will be synchronized.

#### How are data synchronized between Dastra and Filerskeepers?

A number of fields from Filerskeepers are automatically mapped to your retention period:

* **The retention duration** (from)
* **The description of the retention policy**
* **The legal justification, link, and jurisdiction**, which are concatenated into the justification field
