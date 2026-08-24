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
* A configuration window will appear. This configuration is required to finalize the installation. In the form, select the “Schedule” you want to configure with Dastra.

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

By clicking this button, you can directly select a dataset from your Filerskeepers repository. **This retention period will be automatically synchronized** with Dastra if you enabled this option in the integration configuration.

Select a dataset by clicking the **"Select"** button.

Once you have selected the retention period, the window will close and the retention period details will be displayed.

> **ℹ️ Info**\
> Only retention periods related to active data stores will be synchronized.

#### How are data synchronized between Dastra and Filerskeepers?

A number of fields from Filerskeepers are automatically mapped to your retention period:

* **The retention duration** (from)
* **The description of the retention policy**
* **The legal justification, link, and jurisdiction**, which are concatenated into the justification field
