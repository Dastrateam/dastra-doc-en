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

### Implementation in the BI tool :

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

#### Google Looker <a href="#google-looker" id="google-looker"></a>

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

**Exemple avec Fivetran :**

1. **Connectez une API REST ou une source JSON dans Fivetran**.
2. **Transformez les données** pour qu'elles correspondent aux exigences de votre entrepôt de données.
3. **Chargez les données dans l'entrepôt** (par exemple, BigQuery).
4. **Connectez Looker à cet entrepôt de données** pour commencer à interroger et visualiser les données.

#### Tableau Software <a href="#tableau-software" id="tableau-software"></a>

**1. Ouvrir Tableau Desktop :**

* Lancez **Tableau Desktop** sur votre machine.

**2. Se connecter à une source de données Web :**

* Dans **Tableau Desktop**, allez dans le menu **Fichier** et sélectionnez **Nouvelle source de données**.
* Dans la fenêtre de sélection des sources de données, cliquez sur **Web Data Connector**. Cette option permet de se connecter à des données à partir de diverses sources web, y compris des fichiers JSON via une API ou une URL.

**3. Entrer l'URL JSON :**

* Vous devrez entrer l'URL du fichier JSON ou de l'API dans la fenêtre qui apparaît.

**4. Authentification (si nécessaire) :**

* Si l'URL JSON nécessite une forme d'authentification (par exemple une clé API, un jeton OAuth, ou des identifiants de connexion), Tableau vous demandera les informations d'identification pour y accéder.
* Sélectionnez le type d'authentification approprié (par exemple, **Clé API** ou **OAuth**) et entrez les informations nécessaires.

**5. Analyser les données JSON dans Tableau :**

* Tableau va se connecter à l'URL, télécharger le fichier JSON et tenter de le convertir en un format tabulaire compréhensible (une table ou une vue de données structurées).
* Tableau peut automatiquement détecter la structure des données JSON, mais dans certains cas, si le fichier est très complexe ou imbriqué, vous devrez peut-être effectuer des ajustements dans **l'éditeur de données** pour aplatir ou transformer les données dans un format approprié.
* **Limites du fichier JSON :** Si votre fichier JSON est volumineux ou très imbriqué, Tableau peut avoir des difficultés à l'analyser correctement. Parfois, il peut être nécessaire de le transformer ou de le simplifier avant de l'intégrer.
* **Authentification et sécurité :** Si votre lien JSON nécessite une clé API, assurez-vous de bien gérer les autorisations et les informations d'identification. Certaines API peuvent avoir des limitations sur le nombre de requêtes ou nécessiter des autorisations spécifiques.
* **Rafraîchissement des données :** Si les données JSON changent régulièrement (par exemple, via une API qui fournit des mises à jour en temps réel), vous pouvez configurer Tableau pour **rafraîchir automatiquement les données** à intervalles réguliers, afin de garder vos rapports à jour.
