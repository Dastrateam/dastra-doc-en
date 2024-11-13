---
description: Learn how to integrate Dastra into your favorite data analysis tool!
---

# Integration with data analysis tools (BI)

{% hint style="info" %}
To use this feature, your subscription must include the **Enterprise** plan.
{% endhint %}

Dastra makes it easy to import [customized reports](./) into your favorite BI tool (Power BI, Google Looker, Tableau Software...). The advantage of using this feature is that you can benefit from the power of BI tools to analyze data in depth, while having reports that refresh automatically

### Setting up in Dastra

Go to the customized reports module, access one of them and click on the “Integrate with a BI tool” button.&#x20;

A modal window opens, click on “Create integration link”.&#x20;

Copy the generated link&#x20;

{% hint style="warning" %}
Please note! Do not transfer the generated link to anyone. It will give you access to the raw data in the report.
{% endhint %}

##

## Power BI:

1. **Open Power BI Desktop :**
   * Launch Power BI Desktop on your machine.
2. **Connect to the Web data source:**
   * In Power BI Desktop, go to the Home tab.
   * Click on Get Data, then select **Web**.
3. **Enter the URL of the JSON link:**
   * In the Get Data Web window that appears, enter the URL of your JSON file or API (if you have a JSON share link).
   * Make sure the URL points to a JSON file or API that returns JSON data.
   * Click on OK.
4. **Authentication (if required):**
   * If the URL requires authentication (for example, if it is protected by a password or API key), Power BI will ask you to log in.
   * Select the appropriate authentication type (e.g. Anonymous, OAuth2, API Key, etc.) and enter your credentials if necessary.
5. **Access JSON data:**
   * Power BI will connect to the URL and retrieve the JSON file.
   * Once successfully connected, a JSON data preview window will appear. You can explore the data in the form of nested lists, objects or tables.

{% hint style="info" %}
* **Performance**: If your JSON file is large or contains deep hierarchies, Power BI may take some time to load and transform the data.
* **Data refresh:** If JSON data is regularly updated (e.g. by an API), you can set up a data refresh in Power BI Service to retrieve the latest data automatically.
{% endhint %}

### &#x20;<a href="#google-looker" id="google-looker"></a>

## Google Looker <a href="#google-looker" id="google-looker"></a>

Google Looker connects easily to Google BigQuery, a Google Cloud data warehouse that can store and process JSON files.

**1. Using Google BigQuery as a data source**

1. **Upload the JSON file to Google Cloud Storage :**
   * If your JSON file is accessible via a share link, start by uploading the file to **Google Cloud Storage**.
   * Make it public or set the appropriate permissions.
2. **Load JSON data into BigQuery:**
   * Access the Google Cloud Platform console (Google Cloud Console).
   * Go to **BigQuery** and select or create a project.
   * In **BigQuery**, select your dataset and click on **Create Table.**
   * Select **Google Cloud Storage** as the source and enter the URL of your JSON file in the **URL** field.
   * Set the data format to **JSON** and make sure **BigQuer**y can correctly interpret the structure of your file.
3. **Connect BigQuery to Looker :**
   * Once the JSON file has been loaded into BigQuery, you can connect Looker to BigQuery.
   * In Looker, go to Admin > Connections and add BigQuery as a data source.
   * Once the connection has been established, you can query BigQuery data directly in Looker and visualize it.

**2. Use ETL tools to integrate JSON into Looker**

If you need to automate the integration of JSON data from an API or external file into Looker, you can use ETL (Extract, Transform, Load) tools such as Fivetran, Stitch or Airflow. These tools can extract JSON data, transform it and load it into a Looker-compatible data warehouse.

**Example with Fivetran :**

1. Connect a REST API or JSON source to Fivetran.
2. Transform the data to match the requirements of your data warehouse.
3. Load the data into the warehouse (e.g., BigQuery).
4. Connect Looker to this data warehouse to start querying and visualizing the data.

#### &#x20;<a href="#tableau-software" id="tableau-software"></a>

## Tableau Software <a href="#tableau-software" id="tableau-software"></a>

**1. Open Tableau Desktop** :

* Launch Tableau Desktop on your machine.

**2. Connect to a Web data sourc**e:

* In Tableau Desktop, go to the File menu and select New Data Source.
* In the data source selection window, click on Web Data Connector. This option lets you connect to data from various web sources, including JSON files via an API or URL.

**3. Enter JSON URL:**

* You'll need to enter the URL of the JSON file or API in the window that appears.

**4. Authentication (if required):**

* If the JSON URL requires some form of authentication (e.g. an API key, OAuth token, or login credentials), Tableau will ask you for credentials to access it.
* Select the appropriate authentication type (e.g. API Key or OAuth) and enter the necessary information.

**5. Analyze JSON data in Tableau :**

* Tableau will connect to the URL, download the JSON file and attempt to convert it into an understandable tabular format (a table or structured data view).
* Tableau can automatically detect the structure of JSON data, but in some cases, if the file is very complex or nested, you may need to make adjustments in the data editor to flatten or transform the data into an appropriate format.

{% hint style="info" %}
* **JSON file limitations:** If your JSON file is large or highly nested, Tableau may have difficulty parsing it correctly.\
  Sometimes it may be necessary to transform or simplify it before integrating it.
* **Authentication and security:** If your JSON link requires an API key, be sure to manage authorizations and credentials. Some APIs may have limitations on the number of requests or require specific authorizations.
* **Data refreshment:** If JSON data changes regularly (for example, via an API that provides real-time updates), you can configure Tableau to automatically refresh data at regular intervals, to keep your reports up to date.
{% endhint %}
