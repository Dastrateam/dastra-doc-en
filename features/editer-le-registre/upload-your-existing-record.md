---
description: Learn how to export and import a complete existing record into Dastra.
---

# Export / import the record

## Record export

To export the entire record, simply go to the "Record of processing activities" module, click on the arrow at the top right next to the creation of a treatment, then select "Export".

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-01-30 à 11.12.33 (1).png" alt=""><figcaption><p>Register drop-down menu with export functionality</p></figcaption></figure>

Then choose the export format as well as the type of export desired (complete or article 30 format), and click on "Download file". That's it, your record is exported !

### Article 30/CNIL format

The so-called article 30 format corresponds to what is required by the GDPR. The export will take into account the mandatory fields according to the GDPR. Indeed, the GDPR requires the creation of the record of processing activities. The information contained is:

* Name of the treatment&#x20;
* Purposes (without legal basis)&#x20;
* Data and storage&#x20;
* Recipients and possible transfers&#x20;
* Security measures

### Complete format

The complete format is the native Dastra format. You export all the fields that make up the treatment form.

{% hint style="info" %}
It's also possible to export only one or several treatments of the record, instead of the whole record. To do this, select the concerned treatments manually by checking the boxes on the left of the record, then "Select a batch action" and "Export".
{% endhint %}

## Record import

In order to avoid filling in each processing by hand and to take into account all possible record formats, Dastra has designed a methodology based on the principle of **segregating the record into data domains**. Thus, 7 steps are recommended to import an entire existing record into Dastra.

{% hint style="info" %}
These steps, which are not mandatory, are nevertheless strongly recommended, especially when the processing record contains many treatments.
{% endhint %}

Don't hesitate to consult our library of data processing models: [https://www.dastra.eu/en/data-processing/referentials](https://www.dastra.eu/en/data-processing/referentials)

### Step 1: Import of treatment labels

To import your existing treatment labels, click on the "Import" tab in the Record section:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-01-30 à 11.27.32.png" alt=""><figcaption></figcaption></figure>

Next, download a sample of our file as shown on the screen.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-01-30 à 11.31.36.png" alt=""><figcaption></figcaption></figure>

Indicate the organizational unit:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-01-30 à 11.32.35.png" alt=""><figcaption></figcaption></figure>

That's it, your treatment labels are imported!

### Step 2: Import of the asset referential

To import your existing applications/assets, click on the "Import" tab in the Data mapping module, Assets tab:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-01-30 à 11.40.35.png" alt=""><figcaption></figcaption></figure>

That's it, your assets are imported!

### Step 3: Import of the actors' referential

Repeat the procedure similar to the previous ones from the Data mapping module, Actors tab.

Your actors referential refers to all the parties involved in a processing operation. Legal entities such as data processor, customers or joint controllers, or natural persons such as processing contact persons.&#x20;

This referential serves as an internal directory in the workspace. For each actor, you can define a type that characterizes him. For example, if you want to add your subcontractor repository, you add all the actors and each subcontractor will have to be associated with a processing.

### Step 4: Import of the security measures referential

Repeat the procedure similar to the previous ones from the Data mapping module, Measures tab.

### Step 5: Import the data glossary

Repeat the procedure similar to the previous ones from the Data mapping module, Data glossary tab.

### Step 6: Import of the datasets referential

Repeat the procedure similar to the previous ones from the Data mapping section, Datasets tab.

### Step 7: Construction of links

Now that the repositories have all been imported, edit each of the treatments and fill in the information based on the imported information following the guide below:

{% content-ref url="remplir-le-questionnaire/" %}
[remplir-le-questionnaire](remplir-le-questionnaire/)
{% endcontent-ref %}

That's it, the links are built!
