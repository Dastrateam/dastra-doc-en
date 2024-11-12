# Import your data (Excel, Csv)

## Importing data into Dastra

Dastra allows you to easily import your own data in spreadsheet format directly into the application.

Imports are possible in the following modules:

* import of the record&#x20;
* import of actors&#x20;
* import of assets&#x20;
* import of datasets&#x20;
* import of fields&#x20;
* import of security measures&#x20;
* import of categories of persons concerned&#x20;
* import of audit responses&#x20;
* import of audit models (to come)&#x20;
* import of risk types&#x20;
* import of rights exercise requests&#x20;
* import of data breaches&#x20;
* import of tasks

In each import, the process is the same.

It is done in 4 steps:

1. [Preparation of the data file ](importer-vos-donnees-excel-csv.md#1.-preparation-of-the-data-file)
2. [Downloading the file](importer-vos-donnees-excel-csv.md#2.-download-the-template-file)
3. [Verification of data before import](importer-vos-donnees-excel-csv.md#3.-check-your-data)
4. [Importing the data](importer-vos-donnees-excel-csv.md#4.-import-the-data)

### 1. Preparation of the data file

Dastra supports the following data formats:&#x20;

* **Excel** (.xlsx)&#x20;
* **Flat files** (.csv, .txt) with separator; and UTF-8 encoding (encoding is important to have accents)&#x20;
* **JSON** (Only for the import of the complete record and the treatment models)&#x20;

To access the data import menu, click on the "import" button under each arrow of the create button.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.15.23.png" alt=""><figcaption></figcaption></figure>

Select Excel if asked:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.16.33.png" alt=""><figcaption></figcaption></figure>

### 2. Download the template file

Then, download a file template by clicking on the "Download file template" button:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.18.34.png" alt=""><figcaption></figcaption></figure>

The template file is a **CSV file** that you can easily edit with a Libre Office, Wordpad, Excel or Google Sheet.

This will contain all the necessary columns with sample data.&#x20;

Example file (for the record):

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption><p>Line 2 contains example data that must be replaced</p></figcaption></figure>

#### Fill in the file template

Fill the downloaded file with your data.&#x20;

For each data file, you will be able to display the expected values on the columns:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.22.43.png" alt=""><figcaption><p>Expected values for the record import file</p></figcaption></figure>

#### Load the file

Once your data file is ready, you may need to specify an organizational unit. All imported files will be placed in this organizational unit.

{% hint style="info" %}
Only object imports that can be attached to organizational units are concerned. For example, the processing record or data breaches. Actors, measures or datasets are not concerned.
{% endhint %}

#### Update data via import

It's proposed to check a box allowing to update the existing data.&#x20;

This feature allows you to update data in Dastra from the data in the Excel file.&#x20;

By default, the import will create new objects. If the object already exists (an actor for example), the import will not create a new object.&#x20;

It's possible to update an existing object (for example an actor). In this case, select the "Update to existing data" box and choose the matching field. This field will be the key to identify the fields to be updated.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.38.49.png" alt=""><figcaption></figcaption></figure>

By clicking on the "Overwrite matched row" button, the corresponding data will be replaced by the data from the import.

#### Send the file

Send the file by clicking in the zone:

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.40.56.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You can also upload your files by dragging and dropping them into the file upload area
{% endhint %}

### 3. Check your data

The following utility allows you to validate and possibly choose the columns of your Excel file on the columns expected in import format.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.43.16.png" alt=""><figcaption></figcaption></figure>

If everything seems to be in order, you can start the data import.

### 4. Import the data

Start the data import by clicking on the continue button. The import process will then start.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-17 à 10.45.22.png" alt=""><figcaption></figcaption></figure>

### 5. That's it!

Congratulations! You have reached the end of this guide! We recommend that you verify that the data has been imported into the tool.
