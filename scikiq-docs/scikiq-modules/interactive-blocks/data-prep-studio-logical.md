---
hidden: true
icon: school
---

# Data Prep Studio - Logical

* Data Preparation Studio - Logical" is to streamline the process of preparing data for analysis, modeling, or reporting by ensuring data is clean, accurate, and properly structured.
* It can save time and improve data quality, making it an essential tool in data management and data-driven decision-making.

### Navigating to Data Prep Studio - Logical

To access Data Preparation Studio - Logical, follow these steps:

### Step 1:

A Dataset is created by clicking on the following option in SCIKIQ.

<figure><img src="../../.gitbook/assets/image (870).png" alt=""><figcaption></figcaption></figure>

### Step 2:  <a href="#step-2" id="step-2"></a>

On clicking the above option, we get the below page where we can start creating the Dataset.

<figure><img src="../../.gitbook/assets/image (872).png" alt=""><figcaption></figcaption></figure>

Step 3:

There are 4 main functions that can be used while creating a DATASET on SCIKIQ

<figure><img src="../../.gitbook/assets/image (873).png" alt=""><figcaption></figcaption></figure>

### Common Features

In the Dataset creation page, additional functionalities are conveniently located on the right side. These features are consistently available across all four input options provided in SCIKIQ.

### Node Information&#x20;

* It gives the information about nodes worked on.

<figure><img src="../../.gitbook/assets/image (874).png" alt=""><figcaption></figcaption></figure>

### Job Logs

* Logs for executed jobs can be viewed here.

<figure><img src="../../.gitbook/assets/image (875).png" alt=""><figcaption></figcaption></figure>

#### **Database Input Suggestion**

It gives input suggestions as to which table you want to connect.

<figure><img src="../../.gitbook/assets/image (876).png" alt=""><figcaption></figcaption></figure>

#### Node validation

* It gives information on success or failure by validating the table node.

<figure><img src="../../.gitbook/assets/image (877).png" alt=""><figcaption></figcaption></figure>

#### **Full Screen**

This option helps the user to view the Dataset page on full screen.

<figure><img src="../../.gitbook/assets/image (878).png" alt=""><figcaption></figcaption></figure>

Clicking on this will maximize the size of the screen.

<figure><img src="../../.gitbook/assets/image (879).png" alt=""><figcaption></figcaption></figure>

#### **Delete**

It will delete the current node which the user is working on.

<figure><img src="../../.gitbook/assets/image (880).png" alt=""><figcaption></figcaption></figure>

When you click on the "Delete Node" option, it will trigger an alert window displaying two options, as shown in the attached screen below.

<figure><img src="../../.gitbook/assets/image (881).png" alt=""><figcaption></figcaption></figure>

### **Clear**&#x20;

It will clear the entire nodes or functionalities created on the ETL page.

<figure><img src="../../.gitbook/assets/image (882).png" alt=""><figcaption></figcaption></figure>

* An alert window will appear. If you click the "OK" button, it will clear the entire screen. Choosing the "Cancel" option will keep the screen as it is.

<br>

<figure><img src="../../.gitbook/assets/image (883).png" alt=""><figcaption></figcaption></figure>

### **Save**&#x20;

This helps the user to save the dataset created.

<figure><img src="../../.gitbook/assets/image (884).png" alt=""><figcaption></figcaption></figure>

After clicking the "Save" button, a window for saving the logic appears, as displayed in the screen below.

<figure><img src="../../.gitbook/assets/image (885).png" alt=""><figcaption></figcaption></figure>

### Input

Input refers to the information or data provided to a system, device, or process, which it uses for various tasks or actions.

* \
  In ScikIQ we can extract data from four types of inputs.
  * Database input.
  * File input.
  * Query Input.
  * SAP APP.
  * No SQL.

#### Database Input <a href="#database-input" id="database-input"></a>

The database input node connects to the source database, retrieves data, and readies it for further processing, enabling the integration of data from multiple databases for reporting and analytics.CommentScikIQ supports several databases that were discussed in the ScikIQ Connect module.

#### File Input: <a href="#file-input" id="file-input"></a>

The file input node is in charge of taking in data from different types of files, including text files, CSV files, Excel spreadsheets, XML files, and more. It makes sure the data is gathered, checked for accuracy, and ready for the next steps in the process.

#### Query Input <a href="#query-input" id="query-input"></a>

The query input node empowers users to have precise control over the data extraction process. It lets users input custom queries or commands to extract specific data from source systems like databases, tailoring the process to their unique data needs.

#### SAP APP  <a href="#sap-app" id="sap-app"></a>

The SAP Application Server Node facilitates the connection to SAP application servers and the extraction of data from different SAP modules like SAP ERP or SAP BW. This extraction process makes sure that crucial data from SAP systems is accessible for subsequent processing and analysis.

#### NoSQL <a href="#nosql" id="nosql"></a>

A NoSQL node is particularly valuable when handling data that doesn't neatly fit into traditional relational databases, like JSON or XML data. NoSQL databases come in specialized types, such as document stores suitable for content management systems and graph databases tailored for data with complex relationships.. These databases are built to manage large volumes of unstructured or semi-structured data, making them useful in a variety of data storage situations.

### Database Input

The user can select the ‘Database Type’ and select the connection from existing or new connection options available.

If there is no existing connection in the database list such as SQL server, My SQL, ORACLE, Vertica, etc, then only the user can select the option for 'New Connection'.

There are multiple new connection data source types where users can connect such as below:-

Data source type - Relational database

* SQL Server.
* MySql
* PostgreSQL.
* ORACLE&#x20;
* Teradata&#x20;
* IBM DB2
* Amazon Athena&#x20;
* Scikiq DnA hub

Data source type - Big Data

* Hadoop
* HDFS
* HIVE
* Impala
* Snowflake

for more connection information check the data source module.&#x20;

{% content-ref url="../images-and-media/scikiq-connect-module/" %}
[scikiq-connect-module](../images-and-media/scikiq-connect-module/)
{% endcontent-ref %}

### Step 1

A Dataset on SCIKIQ is created by clicking on the following option.

Steps 1: Access the "SCIKIQ CURATE" module from the main menu, and click on "[Data Prep Studio - Logical](https://qa3.scikiq.com/build/model/)"

<figure><img src="../../.gitbook/assets/image (886).png" alt=""><figcaption></figcaption></figure>

### Step 2:&#x20;

* On clicking the above option, we get the below page where we can start creating the Dataset.

<figure><img src="../../.gitbook/assets/image (887).png" alt=""><figcaption></figcaption></figure>

Select Database input from the input Option&#x20;

<figure><img src="../../.gitbook/assets/image (888).png" alt=""><figcaption></figcaption></figure>

Choose the "Database Input" option by simply dragging and dropping it.

<figure><img src="../../.gitbook/assets/image (889).png" alt=""><figcaption></figcaption></figure>

* After selecting an input node, the next step is to choose the data source type. You will be presented with two options: "Asset" and "DataSource."&#x20;
* You can select either of these options. For this example, choose the "DataSource" option.&#x20;

<figure><img src="../../.gitbook/assets/image (890).png" alt=""><figcaption></figcaption></figure>

If you don't see an existing connection in the database/asset list, which includes options like SQL Server, MySQL, Oracle, Vertica, and others, you can choose the "New Connection" option.

<figure><img src="../../.gitbook/assets/image (891).png" alt=""><figcaption></figcaption></figure>

* You can find more detailed instructions on how to set up new connections and create assets in both the Data Source and Asset modules.&#x20;
* The steps for creating new connections and assets are already provided in these modules
* After choosing the source type, proceed by selecting the data source from the existing source connections.

<figure><img src="../../.gitbook/assets/image (892).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (894).png" alt=""><figcaption></figcaption></figure>

### Schema Properties

* When you pick a connection, you'll need to go to the "Schema Properties" section and select the tables. Here, you'll see a list of all the tables available in that connected data source.

<figure><img src="../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

### Toggle Button&#x20;

* In the "Schema Properties" section, you'll notice a toggle button highlighted in green. This button allows you to switch to a full view of the schema section.
* Table Name: These are the default tables that already exist in the connected database.
* Alias Name: You can change the table name by using this option; otherwise, it will use the default table name.

<figure><img src="../../.gitbook/assets/image (896).png" alt=""><figcaption></figcaption></figure>

### Save Columns:&#x20;

* user must click on the 'Save ' button and a green color flash will appear that contains 'Column Details Saved' at the bottom right corner.

<figure><img src="../../.gitbook/assets/image (897).png" alt=""><figcaption></figcaption></figure>

Once the setup is complete, the user will need to click on the "Preview" button for the table. This "Preview" button can be found on the table node.

> Each node is designed to work with a single table. If a user wants to work with multiple tables, they will need to select and use additional nodes for each table.

**Refresh Button**&#x20;

* This option just refreshes the table.

<figure><img src="../../.gitbook/assets/image (898).png" alt=""><figcaption></figcaption></figure>

### New Column

* This feature allows you to create new columns using functions.&#x20;
* You can add a new column by applying a function to existing columns. The new column's name must not contain spaces between characters. Once created, the new column will be displayed under "Preview."&#x20;
* You can also edit or delete the new column by hovering the mouse over it.&#x20;

### Step 4: Table

* It will display all column header names. including the aggregate functions such as (Count, sum, average, min, and max)

<figure><img src="../../.gitbook/assets/image (899).png" alt=""><figcaption></figcaption></figure>

### Table column Search box&#x20;

* There is a search box available under the table option (as shown above). As per the input level, the user can filter a few columns out of the list.

<figure><img src="../../.gitbook/assets/image (900).png" alt=""><figcaption></figcaption></figure>

### Step 5: Filters

* It includes two operators: "AND" and "OR." Depending on the selected function, users can input conditions to filter the data, and the results can be viewed in the "Preview" section.

<figure><img src="../../.gitbook/assets/image (901).png" alt=""><figcaption></figcaption></figure>

Select the "Add Filters" tab to open a new screen where you can apply conditions to the selected tables.

<figure><img src="../../.gitbook/assets/image (902).png" alt=""><figcaption></figcaption></figure>

Apply the filter conditions as displayed in the screen below, and then click on the "Save" button.

<figure><img src="../../.gitbook/assets/image (903).png" alt=""><figcaption></figcaption></figure>

Click the "Preview" button, and it will display filtered data based on the applied conditions, as shown in the screen below.

<figure><img src="../../.gitbook/assets/image (904).png" alt=""><figcaption></figcaption></figure>

### Step 6: Limit By

* Users can filter data based on either a fixed limit or a custom limit.

<figure><img src="../../.gitbook/assets/image (905).png" alt=""><figcaption></figcaption></figure>

For example, apply a custom limit as shown in the attached screen below. This action will result in...

<figure><img src="../../.gitbook/assets/image (906).png" alt=""><figcaption></figcaption></figure>

### Step 7: Order by:

* Users have the option to select any column and arrange it in either ascending or descending order.
  * For example, apply for the "Order By", then click on the "Preview" button. This will display the data of the selected columns in ascending order.

<figure><img src="../../.gitbook/assets/image (907).png" alt=""><figcaption></figcaption></figure>

### Step 8: Group By

* Users can use this functionality to group data based on one or more columns.
* click on the preview button&#x20;

<figure><img src="../../.gitbook/assets/image (908).png" alt=""><figcaption></figcaption></figure>

#### Step 9: Save the Model <a href="#step-9-save-the-model" id="step-9-save-the-model"></a>

<figure><img src="../../.gitbook/assets/image (910).png" alt=""><figcaption></figcaption></figure>

<br>

<figure><img src="../../.gitbook/assets/image (912).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (913).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (914).png" alt=""><figcaption></figcaption></figure>

### Step 10: List

<figure><img src="../../.gitbook/assets/image (915).png" alt=""><figcaption></figcaption></figure>

### Transform

the "Transform" phase is about preparing and modifying extracted data to make it suitable for the target database. It includes tasks like cleaning, mapping, aggregating and applying business rules to ensure data quality and compatibility.

It aims to make data more accurate, consistent, and valuable. It is a crucial step that ensures the data is ready for analysis and decision-making, and it may involve various operations based on the data's nature and the requirements of the target system or analysis.

In ScIKIQ, we have 13 transformation nodes, each with its unique purpose. Let's explore how each of these transformation nodes is used within ScIKIQ.

### Transformation Nodes

* Filter By

**Calculated By** - It will apply mathematical or logical functions with the available table fields and give the output on a new column.
