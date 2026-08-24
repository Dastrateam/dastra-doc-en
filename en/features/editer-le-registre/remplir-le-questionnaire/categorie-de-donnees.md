---
description: Define the dataset and retention policy involved in the processing activity.
---

# Dataset

[**Article 30 of the GDPR**](https://gdpr-info.eu/art-30-gdpr/) also requires the registration of the categories of data processed.

it is a question here of defining the categories of data processed. These can be said to be common or sensitive. A distinction is made between data which present a greater risk to natural persons such as data relating to the health of persons, data relating to political opinions or trade union activity. Data relating to offenses or other measures for the execution of sentences also constitute particularly protected data.

Similarly, the social security number can be considered as a special category data.

### How to deal with datasets?

The dataset groups the data of a specific element, for example, a table in a database or a paper collection form.&#x20;

Datasets can be used in several ways:&#x20;

**Case 1**: by associating a dataset with a single asset. In this case, the dataset corresponds to the data of the asset and is not generic&#x20;

**Case 2**: by associating a dataset to the data processing. This dataset can be specific to the data processing and is not reused in another data processing&#x20;

**Case 3**: by associating generic datasets to the data processing. In this case, the dataset can be reused in several data processing.&#x20;

To use generic datasets, we recommend the following procedure:&#x20;

* Open the dataset processing page&#x20;
* Open a new tab on the datasets page in the mapping&#x20;
* Select the dataset in the dataprocessing&#x20;
* If the dataset needs to be modified, create another one: go to the other tab and duplicate the generic dataset by removing or adding the desired fields&#x20;
* For more clarity, we recommend you to use a tag for these datasets (this will allow you to distinguish them easily in the dataset selector). For example: a "generic" tag and a tag for the added or removed data&#x20;

The long-term objective may be to limit the use of generic datasets and to move towards a more precise mapping either via data processing (case 2) or via assets (case 1).&#x20;

On the other hand, it is possible to remain even more generic by not specifying the data associated with the dataset but by naming the dataset as a category of data (which is also valid in the sense of the RGPD for example).&#x20;

Depending on the processing, you may have different approaches, depending on the sensitivity of the processing with regard to the rights and freedoms of the data subjects.

## Special category data

The collection of sensitive data is in principle prohibited. Only the exceptions provided for in [**article 9 of the GDPR** ](https://gdpr-info.eu/art-9-gdpr/)allow them to be collected.



## Data retention

The limited retention of data is part of the general principles of personal data law and is recalled in [**Article 5 1. e) of the GDPR**](https://gdpr-info.eu/art-5-gdpr/). Special category should be

> kept in a form which permits identification of data subjects for no longer than is necessary for the purposes for which the personal data are processed.

The retention period depends on the purpose of the processing and the nature of the data. The retention periods can be defined according to the types of data. For example, for payroll management, the data relating to the salary slip are kept for 1 month in active database and 5 years in intermediate archiving while the data relating to the transfer order for payment are kept for the time necessary for the 'issue of the payslip on an active basis and 10 years from the closing in an intermediate archive.

The duration can be expressed in value or, if this is not possible, the criteria used to define the retention period (until unsubscription for example). It is recommended to set up procedures to manage the retention periods at the level of the category of data and in particular, manage purges or destruction of data.
