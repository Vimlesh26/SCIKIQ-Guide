---
icon: album-collection-circle-plus
---

# ScikIQ Connect Module



### <mark style="color:blue;">1. Introduction</mark>

The **SCIKIQ Connect Module** is the foundation of the SCIKIQ platform’s integration layer, designed to simplify how organizations connect, manage, and orchestrate data across multiple systems. It provides a **no-code interface** to unify structured, unstructured, and cloud-native sources, ensuring data accessibility, reliability, and governance.

### <mark style="color:blue;">2. Key Features of SCIKIQ Connect</mark>

1. **Broad Connectivity**: Easily configure and manage connections to various data sources, including traditional databases, file systems, APIs, and cloud platforms.
2. **Hassle-Free Migration**: Migrate data from legacy systems to modern architectures with minimal complexity.
3. **Pipeline Automation** – Build API and Delta pipelines for precise, automated data workflows.
4. **Unified Dashboard** – Monitor and manage pipelines from a central console.
5. **Event-Driven Integration** – Leverage Event Hub for responsive, real-time triggers.
6. **Ecosystem Integration** – Deep integration with SCIKIQ Curate and Governance for end-to-end control

### <mark style="color:blue;">**3. Why Connect to a Data Source?**</mark>

Establishing a connection to a data source or database is critical for several reasons:

1. **Data Access**: Enables applications to retrieve and display data.
2. **Data Modification**: Supports operations like insert, update, and delete for dynamic data management.
3. **Data Integration**: Facilitates combining data from multiple sources for unified insights.
4. **Data Analysis**: Powers analytics, reporting, and business intelligence activities.
5. **Security**: Offers user authentication and access controls to protect sensitive data.
6. **Backup & Recovery**: Essential for routine backups and ensuring business continuity in case of data loss.

### <mark style="color:blue;">4. Supported Connection Types in SCIKIQ</mark>

In Scikiq, we utilize a variety of data source types to cater to diverse data requirements. Currently, we support a total of 82 data sources, enabling seamless integration with both traditional and modern data environments.

#### 4.1 Relational Databases

Examples: PostgreSQL, MySQL, Oracle, SQL Server, Teradata, IBM DB2, SAP HANA, Aurora DB, etc.

#### 4.2 Column Store Databases

Examples: Vertica (DnA Hub), Redshift, Apache Druid, MariaDB, Cassandra, ClickHouse, etc.

#### 4.3 Big Data Sources

Examples: Hadoop, HDFS, Hive, Impala, Snowflake.

#### 4.4 File Storage Systems

Examples: SFTP/FTP, Amazon S3, Azure Blob, Google Cloud, Excel/CSV, Dropbox, OneDrive, Shared Location.

#### 4.5 Document Stores

Examples: MongoDB, Elastic Search.

#### 4.6 Application Servers

Examples: SAP ECC, SAP S4 Hana, BW4 Hana.

#### 4.7 SaaS Platforms

Examples: Slack, Teams, ServiceNow, Tableau, Power BI, Azure Purview, CRM APIs, Webhooks, Email.

#### 4.8 Real-Time Data Sources

Examples: Kafka, OpenAI API, Amazon Bedrock, Vertex AI, Hugging Face.

#### 4.9 Vector Databases

Examples: Chroma DB.

<figure><img src="../../../.gitbook/assets/image (1191).png" alt=""><figcaption><p>This image shows the variety of data source types that SCIKIQ Supports.</p></figcaption></figure>

### <mark style="color:blue;">5. Navigating the Connect Module</mark>

Upon logging in, users land on the SCIKIQ Dashboard, which provides access to various features. The left-side navigation panel displays different modules, including SCIKIQ Connect.

* **Connect to Data Store** – Link multiple data sources.
* **SCIKIQ Migration Hub** – Migrate and manage data across environments.
* **SCIKIQ Delta Hub** – Create and manage Delta Pipelines for incremental data updates.
* **SCIKIQ Event Stream** – Manage real-time data ingestion.

<figure><img src="../../../.gitbook/assets/image (1192).png" alt=""><figcaption><p>This image shows the SCIKIQ Connect Module in the left navigation panel, confirming its role as a key component of the platfor</p></figcaption></figure>

### <mark style="color:blue;">6. Connect to Data Store</mark>

Before you begin any operations in SCIKIQ, you must first connect to a data store. This ensures that SCIKIQ has access to the source data it needs for extraction and subsequent transformation.

#### Steps:

1. **Navigate to the “Connect” Module**: From the main dashboard, click on Connect to Data Store in the left-hand menu.

<figure><img src="../../../.gitbook/assets/image (1194).png" alt=""><figcaption><p>This image shows the 'Connect to Data Store' option in the SCIKIQ Connect module, located in the left-hand navigation panel.</p></figcaption></figure>

2. **Manage Data Source:** Within the Connect to Data Store, select Manage Data Sources. Here, you can then add a new data source or configure existing ones to ensure SCIKIQ can                       access your data for pipeline processes.

<figure><img src="../../../.gitbook/assets/image (1190).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7. Detailed Connection Setup Examples</mark>

### <mark style="color:blue;">7.1 Relational Database: PostgreSQL</mark>

**To create a relational database using Postgres, follow these steps:**

1. Access the "SCIKIQ Connect" module from the main menu, choose "Connect to Data Source," and proceed to "Manage Data Source."<br>

<figure><img src="../../../.gitbook/assets/image (766).png" alt=""><figcaption></figcaption></figure>

2. In the "Connect to Data Source" dialog, select the type of database or data source you want to connect to from the list of supported options (e.g. MySQL, SQL Server, PostgreSQL, etc).
3. Here, selecting the "Relational" type reveals all available relational database options, as displayed in the following screen.

<figure><img src="../../../.gitbook/assets/image (932).png" alt=""><figcaption></figcaption></figure>

4. Select the Postgres option to connect in ScikIQ.

<figure><img src="../../../.gitbook/assets/image (933).png" alt=""><figcaption></figcaption></figure>

5. Click on "Create Connection" to open the connection details page.

<figure><img src="../../../.gitbook/assets/image (935).png" alt=""><figcaption></figcaption></figure>

6. In this setup for establishing a connection, decide whether you wish to create a new connection or select an existing one.

<figure><img src="../../../.gitbook/assets/image (936).png" alt=""><figcaption></figcaption></figure>

7. In this setting, provide the essential database information, including the hostname, port, and database password, along with other required details.

<figure><img src="../../../.gitbook/assets/image (937).png" alt=""><figcaption></figcaption></figure>

8. Furthermore, It will ask for administrative metadata information, encompassing details like Catalog, Domain, Name, and Email.

<figure><img src="../../../.gitbook/assets/image (938).png" alt=""><figcaption></figcaption></figure>

9. Following this step, there is a "Test Connection" option available below to verify whether the provided details are accurate or not.
10. Click on **test connection**
11. If the required information is accurate, a green flash message will appear to confirm that the provided details are correct.

<figure><img src="../../../.gitbook/assets/image (940).png" alt=""><figcaption></figcaption></figure>

12. Inside this interface, you'll discover a comprehensive list of tables within the database. You have the option to either display all of them or selectively choose specific tables for discovery in ScikIQ.

<figure><img src="../../../.gitbook/assets/image (941).png" alt=""><figcaption></figcaption></figure>

13. There are additional connection configuration settings that need your attention. Please click "Next" to proceed.

<figure><img src="../../../.gitbook/assets/image (942).png" alt=""><figcaption></figcaption></figure>

14. Please provide a name for the database that will be displayed in the list of connected databases.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FKrHjJBiZOYr8gzHxFOLl%2Fuploads%2FI0zex4s0RKBaEfZWfXD8%2Fimage.png?alt=media&#x26;token=5f76f814-d671-40b6-969f-4e47d60bca64" alt=""><figcaption></figcaption></figure>

\`15. In this particular step, please review the provided details.

<figure><img src="../../../.gitbook/assets/image (943).png" alt=""><figcaption></figcaption></figure>

16. Click finish. Click on the list option to see the newly created connection.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FKrHjJBiZOYr8gzHxFOLl%2Fuploads%2FJKidMJog4E9wttLTIUHo%2Fimage.png?alt=media&#x26;token=3bbd408a-e515-48e9-9880-c734992d41d3" alt=""><figcaption></figcaption></figure>

17. The new data source connection will now be available in the "Data Sources List" section.

​

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FKrHjJBiZOYr8gzHxFOLl%2Fuploads%2Fr1H25rzgeiA76ZlV4Ltd%2Fimage.png?alt=media&#x26;token=d9fcfeff-8b80-4a2c-9d7f-9f3b8de66a5b" alt=""><figcaption></figcaption></figure>

18. &#x20;The outlined steps for establishing a connection with a PostgreSQL data source demonstrate the process of connecting a data source in Scikiq

<mark style="color:purple;">**Note: By following these procedures, you can similarly connect other RDBMS data sources, ensuring a consistent approach across varied systems.**</mark>&#x20;

{% hint style="warning" %}
<mark style="color:orange;">**MySQL database does not contain the schema, it can be created directly by the database.**</mark>

<mark style="color:orange;">**Following the same steps, a MySQL connection can be created when only the database is available.**</mark>
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1073).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.2 Secure Data Source: MySQL with SSL</mark>

To establish a secured connection, enable SSL and configure the necessary security settings, such as providing certificate files, selecting the appropriate SSL mode, and ensuring encrypted communication with the MySQL database.

#### **Enable Secured Connection:**

Configure security settings by enabling SSL and specifying:

* **SSL Mode** (Required, Verify\_CA, Verify\_Identity, etc.)
* **Client Certificate** (if applicable)
* **SSL Key & CA Certificate**

#### **Steps:**

1. Access the "SCIKIQ Connect" module from the main menu.
2. Choose "Connect to Data Source."
3. Proceed to "Manage Data Source."

<figure><img src="../../../.gitbook/assets/image (755).png" alt=""><figcaption></figcaption></figure>

4. In the "Connect to Data Source" dialog, select the type of database or data source you want to connect to from the list of supported options (e.g., MySQL, SQL Server, PostgreSQL, etc.).
5. Here, selecting the "Relational" type reveals all available relational database options. Select the **MySQL** option to connect in ScikIQ.

<figure><img src="../../../.gitbook/assets/image (756).png" alt=""><figcaption></figcaption></figure>

6. Click on "Create Connection" to open the connection details page.
7. Choose whether to create a new connection or use an existing one.

<figure><img src="../../../.gitbook/assets/image (757).png" alt=""><figcaption></figcaption></figure>

8. Provide the essential database information, including the hostname, port, database username, password, and any other required details.

<figure><img src="../../../.gitbook/assets/image (758).png" alt=""><figcaption></figcaption></figure>

9. For a secured connection, select the **secure checkbox**, then enable SSL and provide any necessary security configurations, such as certificate files and SSL mod

<figure><img src="../../../.gitbook/assets/image (764).png" alt=""><figcaption></figcaption></figure>

10. After filling out the details, there is a "Test Connection" option available. Click on **Test Connection** to verify if the provided details are correct.
11. If the required information is accurate, a green flash message will appear to confirm that the provided details are correct.

<figure><img src="../../../.gitbook/assets/image (760).png" alt=""><figcaption></figcaption></figure>

12. There are additional connection configuration settings as follows:
13. **Connection Type:**
    * Owned
    * Third-party
    * Service Managed
    * User Managed
    * **Security Settings:**
      1. Secured Connection: Yes/No
      2. Unsecured Connection: Yes/No
14. Once the required fields are filled, click **"Next"** to proceed with the connection setup.

<figure><img src="../../../.gitbook/assets/image (761).png" alt=""><figcaption></figcaption></figure>

15. Provide a name for the database that will be displayed in the list of connected databases.
16. Click **Finish**.

<figure><img src="../../../.gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure>

17. The new data source connection will now appear in the "Data Sources List" section

<figure><img src="../../../.gitbook/assets/image (763).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.3 Column Store: Vertica & Redshift</mark>

1. We have the same UI interface for the column store type data source as the RDBMS data source.

{% hint style="warning" %}
<mark style="color:orange;">The column store type data source can be connected in the same way as PostgreSQL, following the same steps. connect the column store type data source similarly.</mark>
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1075).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.4 File Storage: SFTP/FTP</mark>

To connect SFTP as a file storage source, follow these steps:

1. Go to the **"SCIKIQ Connect"** module from the main menu.
2. Select **"Connect to Data Source"** and proceed to **"Manage Data Source"**.

<figure><img src="../../../.gitbook/assets/image (1102).png" alt=""><figcaption></figcaption></figure>

3. In the **"Connect to Data Source"** dialog, select **SFTP** from the list of supported options.

<figure><img src="../../../.gitbook/assets/image (1079).png" alt=""><figcaption></figcaption></figure>

4. Click on **"Create Connection"** to open the connection details page.
5. Choose whether to create a new connection or use an existing one

<figure><img src="../../../.gitbook/assets/image (1088).png" alt=""><figcaption></figcaption></figure>

6. Provide the necessary SFTP credentials, including: &#x20;

* **Source Type**: SFTP
* **Hostname**: Enter the **SFTP server address**
* **Port**: Specify the **port number** (default is 22 for SFTP)
* **Username & Password**: Provide the **username** and **password** for authentication



<figure><img src="../../../.gitbook/assets/image (1080).png" alt=""><figcaption></figcaption></figure>

7. Fill in additional details like **Catalog, Domain, Name, and Email** for administrative purposes.
8. Click **"Test Connection"** to verify if the provided details are correct.
9. If successful, a **green confirmation message** will appear.

<figure><img src="../../../.gitbook/assets/image (1081).png" alt=""><figcaption></figcaption></figure>

10. Configure any additional settings:&#x20;

* **Connection Type:**
  * Owned
  * Third-party
  * Service Managed
  * User Managed
* **Security Settings:**
  * Secured Connection: Yes/No
  * Unsecured Connection: Yes/No

11. Once the required fields are filled, click **"Next"** to proceed with the connection setup.

<figure><img src="../../../.gitbook/assets/image (1082).png" alt=""><figcaption></figcaption></figure>

12. Click **"Next"**, provide a **display name** for the connection, and then click **"Finish"**

<figure><img src="../../../.gitbook/assets/image (1083).png" alt=""><figcaption></figcaption></figure>

13. The new data source connection will now be available in the "Data Sources List" section.

<figure><img src="../../../.gitbook/assets/image (1084).png" alt=""><figcaption></figcaption></figure>

14. Go to the **"Data Sources List"** section and check if the newly created SFTP connection is available.

<figure><img src="../../../.gitbook/assets/image (1085).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
<mark style="color:orange;">**Like SFTP connection, the FTP data source can be connected in the same way.**</mark>

<mark style="color:orange;">**Follow the same steps to connect the FTP connection, as both have the same UI.**</mark>
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1086).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.5 File Storage: Azure Blob</mark>

{% hint style="warning" %}
<mark style="color:orange;">To connect an</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Azure Blob Storage**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">data source, follow the same steps as other data sources. The only difference is in the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**Connection Details**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">configuration:</mark>
{% endhint %}

#### **1. Enter Connection Details**

* **Container Name**: Enter the name of the **Azure Blob Storage container**.
* **Connection String**: Enter the connection string in the following format:

<details>

<summary><mark style="color:orange;"><strong>Azure Connection String Format</strong></mark> </summary>

To create a connection string for your Azure storage account, follow the format below:

```
DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey;BlobEndpoint=myBlobEndpoint
```

Example

```
DefaultEndpointsProtocol=https;AccountName=storagesample;AccountKey=<account-key>;BlobEndpoint=https://storagesample.blob.core.windows.net/
```

* **DefaultEndpointsProtocol:** Protocol to use (http or https, https is recommended).
* **AccountName:** Your Azure storage account name.
* **AccountKey:** Your Azure storage account key.
* **BlobEndpoint:** The Blob service endpoint URL.

Ensure BlobEndpoint is specified in the connection string. Either both AccountName and AccountKey are provided, or a SharedAccessSignature is provided, not both.

Find your storage account's connection strings in the [Azure portal](https://portal.azure.com/). Navigate to Security + networking > Access keys in your storage account's settings to see connection strings for both primary and secondary access keys.

For more detailed information, visit the [Azure Storage Connection Strings Documentation](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string).

</details>

<figure><img src="../../../.gitbook/assets/image (1103).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.6 File Storage: AWS S3 & Glue</mark>

1. **Enter S3 Connection Details**
   1. **Bucket Name**: Enter the name of the **Amazon S3 bucket** you wish to connect to.
   2. **Access Key ID**: Enter your AWS Access Key ID. This is used to authenticate requests sent to AWS.
   3. **Secret Access Key**: Enter your AWS Secret Access Key, which works alongside the Access Key ID for authentication.
   4. **Region**: Specify the AWS region where your S3 bucket is located.

{% hint style="info" %}
**AWS Connection Details**

To securely connect to your Amazon S3 bucket, ensure that your AWS credentials (Access Key ID and Secret Access Key) are stored securely and are never hardcoded in your application. Use AWS IAM roles and policies for enhanced security controls.

For more detailed information on connecting and managing access to your S3 bucket, refer to the documentation on [AWS S3 Access and Management](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ways-to-manage-access.html).
{% endhint %}

3. To securely connect to your Amazon S3 bucket, ensure that your AWS credentials (Access Key ID and Secret Access Key) are stored securely and are never hardcoded in your application. Use AWS IAM roles and policies for enhanced security controls.
4. For more detailed information on connecting and managing access to your S3 bucket, refer to the documentation on [AWS S3 Access and Management](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ways-to-manage-access.html).&#x20;
5. In **S3**,  need to provide the **Bucket Name**.
6. In **AWS Glue**, the **Bucket Name is not required**, as it automatically retrieves storage details.

<figure><img src="../../../.gitbook/assets/image (1091).png" alt=""><figcaption><p>File Store -S3</p></figcaption></figure>

{% hint style="warning" %}
**S3 & AWS Glue Considerations**

* For **S3**, the **Bucket Name** is required.
* In **AWS Glue**, specifying the **Bucket Name** is not necessary, as it automatically retrieves storage details.
* For **S3 and AWS Glue**, we have the **same UI** in ScikIQ.
{% endhint %}

7. The **Glue connection** can be established in **ScikIQ** using the same steps as S3, without specifying the bucket name.

<figure><img src="../../../.gitbook/assets/image (1092).png" alt=""><figcaption><p>File Store-Glue</p></figcaption></figure>

### <mark style="color:blue;">7.7 File Storage: Excel</mark>

1. Navigate to the **"SCIKIQ Connect"** module from the main menu.
2. Select **"Connect to Data Source"** and proceed to **"Manage Data Source"**.

<figure><img src="../../../.gitbook/assets/image (1104).png" alt=""><figcaption></figcaption></figure>

3. In the **"Connect to Data Source"** dialog, select **File** as the data source type.
4. Choose **Excel or CSV** from the file types available.

<figure><img src="../../../.gitbook/assets/image (1099).png" alt=""><figcaption></figcaption></figure>

5. Click on **"Create Connection"** to open the connection details page.
6. Choose whether you want to **create a new connection** or **select an existing one**.

<figure><img src="../../../.gitbook/assets/image (1100).png" alt=""><figcaption></figcaption></figure>

7. Click **Browse** to locate and upload the **Excel file** from your system.
8. Provide the **name of the file** in the input field.

<figure><img src="../../../.gitbook/assets/image (1093).png" alt=""><figcaption></figcaption></figure>

9. From the dropdown, select either **"With Dataset"** or **"Without Dataset"**:
   1. **With Dataset**: Automatically creates the dataset for the uploaded file.
   2. **Without Dataset**: Does not create a dataset in ScikIQ.

<figure><img src="../../../.gitbook/assets/image (1094).png" alt=""><figcaption></figcaption></figure>

10. Fill in **administrative metadata details** like **Catalog, Domain, Name, and Email**.

<figure><img src="../../../.gitbook/assets/image (1101).png" alt=""><figcaption></figcaption></figure>

11. Click **Next** to proceed and review the data from the uploaded Excel file.
12. Once you have reviewed the data, click **Finish** to finalize the connection.
13. The new file data source is now created, and the Excel file is uploaded into ScikIQ.

<figure><img src="../../../.gitbook/assets/image (1095).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">7.8 File Storage: Excel CSV</mark>

<mark style="color:$primary;">To connect a</mark> <mark style="color:$primary;"></mark><mark style="color:$primary;">**CSV data source**</mark><mark style="color:$primary;">, follow the same steps as for</mark> <mark style="color:$primary;"></mark><mark style="color:$primary;">**Excel.**</mark>

<figure><img src="../../../.gitbook/assets/image (1097).png" alt=""><figcaption><p>CSV File</p></figcaption></figure>

* **Encoding**: Specify the encoding type for the CSV file (e.g., UTF-8, ISO-8859-1) to ensure proper handling of special characters and non-standard text formats.
* **Delimiter**: Choose the delimiter used in the CSV file (e.g., comma, semicolon, tab) to separate data fields correctly.

{% hint style="info" %}
- **Encoding**:
  * Use **UTF-8** for wide compatibility, especially for files with special characters or multilingual text.
  * **ISO-8859-1** is commonly used for European languages, but may not support some special characters.
  * Always check the source file to determine the correct encoding if unsure.
- **Delimiter**:
  * **Comma (`,`)** is the most common delimiter for CSV files.
  * **Semicolon (`;`)** is often used in CSV files in regions where the comma is used as a decimal separator.
  * If you're unsure, open the CSV file in a text editor to visually inspect the delimiter.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1096).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">**7.9 Document Store: MongoDB**</mark>

MongoDB is a NoSQL database used for high-performance, high-availability, and easy scalability. It provides different methods for connecting to databases, depending on the deployment architecture (e.g., standalone or replica set). The connection URL is essential for establishing a connection to a MongoDB server.

#### **7.9.1 Types of Connection URL for MongoDB**:

When you connect to a MongoDB database, the URL is like the address that tells your application where the database is located and how to connect. There are different ways to set up this URL depending on your MongoDB setup:

1.  **URL Connection (Standalone MongoDB):**  This type of connection involves a single MongoDB server. You'll need to provide a direct URL, which includes the server’s IP or hostname and the port number. It's specifically used for connecting to a standalone MongoDB instance, using an IP and port (default is 27017). Suitable for scenarios where only one server without redundancy is available.

    1. **Format:**



{% code overflow="wrap" %}
```css
mongodb://<hostname>:<port>
```
{% endcode %}

&#x20;      **b. Example**

{% code overflow="wrap" %}
```css
mongodb://103.178.248.128:27017
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (753).png" alt=""><figcaption></figcaption></figure>

2. **Replica Set**
   1. A MongoDB replica set connects multiple server nodes to form a group that replicates the same dataset.
   2. It provides redundancy and high availability.
   3. Applications can connect to any available server in the replica set, ensuring continued access.
   4. If one server fails, the system automatically switches to another replica node.
   5. A replica set is used for backup and reliability, ensuring data safety and availability across multiple servers.
   6. It minimizes downtime by distributing data management across several servers.

**Format:**

{% code overflow="wrap" %}
```css
mongodb://<host1>:<port1>,<host2>:<port2>,<host3>:<port3>/?replicaSet=<replicaSetName>
```
{% endcode %}

**Example**

{% code overflow="wrap" %}
```css
mongodb://103.178.248.128:60711,103.178.248.128:60712,103.178.248.128:60710/?replicaSet=rs0
```
{% endcode %}

<figure><img src="../../../.gitbook/assets/image (754).png" alt=""><figcaption></figcaption></figure>

3. **IP Address Connection (Connecting via IP)**

* IP Address Connection allows direct connection to a MongoDB server using its IP address.
* It can be used for both single-server setups and replica sets.
* This method is useful when DNS resolution is unavailable.
* It can connect to a standalone server or a replica set.
* It bypasses DNS resolution to establish the connection.

**Format**

{% code overflow="wrap" %}
```css
mongodb://<ip_address>:<port>
```
{% endcode %}

**Example**

```css
mongodb://103.178.248.128:27017
```

<figure><img src="../../../.gitbook/assets/image (752).png" alt=""><figcaption></figcaption></figure>

### Connecting to App Server- S4 hana/BW4 Hana <a href="#data-spporuce-type-app-server" id="data-spporuce-type-app-server"></a>

1. Log in to **SCIKIQ Connect** and navigate to **"Connect to Data Source."**
2. Click on **"Manage Data Source."**

<figure><img src="../../../.gitbook/assets/image (728).png" alt=""><figcaption></figcaption></figure>

3. Select **"SAP Application Server"** as the data source type.

<figure><img src="../../../.gitbook/assets/image (729).png" alt=""><figcaption></figcaption></figure>

4. Click on "Create Connection" to open the connection details page.
5. Choose whether to create a new connection or use an existing one.

<figure><img src="../../../.gitbook/assets/image (730).png" alt=""><figcaption></figcaption></figure>

6. **Select Data Source Type**:  Choose either **SAP S/4HANA** or **SAP BW/4HANA**.

<figure><img src="../../../.gitbook/assets/image (731).png" alt=""><figcaption></figcaption></figure>

7. **Enter Application Server Details**:

* **Application Server**: Provide the hostname or IP of the SAP Application Server.
* **Instance No.**: Enter the instance number assigned to SAP.
* **System ID**: Input the SAP **System ID (SID)**.
* **SAP Router Configuration**:
  * **SAP Router String**: Enter the SAP router details if required for connectivity.
* **User Authentication**:
  * **Client ID**: Specify the SAP **Client ID** (e.g., `100` for the default client).
  * **User Name**: Provide the SAP user credential.
  * **Password**: Enter the password securely.
* **Additional Details**:
  * **Description:** Enter a short description (Max 300 characters).
  * **Connection Type**: Select from **Application Server, Message Server**, or **Cloud Connector**.

8. **Click "Next"** to proceed.

<figure><img src="../../../.gitbook/assets/image (732).png" alt=""><figcaption></figcaption></figure>

9. Provide **Metadata Information**:

* **Catalogue**: Enter the catalog name.
* **Domain**: Specify the domain of the data source.
* **Sub-Domain**: Define the sub-domain if applicable.
* **Business Owner**: Enter the business owner responsible for this connection.
* **Technical Owner**: Provide the name of the technical owner.

10. Configure **Connectivity Mechanism**:

* Choose between **Secured, Unsecured, or SSH Tunneling** based on the organization's security policy.

11. **Enter Supporting Email** (for troubleshooting & notifications).
12. **Provide Service Type & Application ID** (if applicable).
13. Click **"Next"** to proceed.

<figure><img src="../../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure>

14. **Discovery:** The system will automatically **detect tables and objects** within the SAP system.

<figure><img src="../../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

#### **Source Type-** SAP Tables :

#### **Tables** in SAP are fundamental objects that store the transactional or master data in the system. These tables can contain a wide variety of information ranging from financial records to material data.

#### **Work with SAP Tables in Discovery:**

* **Select Tables**: During discovery, you can select the tables you want to work with. These tables are typically organized based on their usage, e.g., **Financial Accounting (FI)**, **Material Management (MM)**, etc.
* **Example Tables**:
  * **BKPF**: Document Header
  * **BSEG**: Document Segment
  * **MARA**: General Material Data
  * **TCURR**: Currency Rates
* **Filter Options**:
  * You can **filter tables** based on criteria such as the **table name** or **specific fields** within the table.

<figure><img src="../../../.gitbook/assets/image (737).png" alt=""><figcaption></figcaption></figure>

16. After entering the table name, click on the search button to display the table.

<figure><img src="../../../.gitbook/assets/image (744).png" alt=""><figcaption></figcaption></figure>

**Source Type- CDS Views (Core Data Services Views)**

**CDS Views** are a set of semantic layers used to represent the data model in SAP HANA. They provide a more flexible and powerful way to query data compared to regular database tables. CDS Views offer a semantic representation of complex data models and can be defined with annotations for reporting and analytics.

**CDS Views in Discovery:**

* **Select CDS Views**: You can choose from a variety of **predefined** or **custom** CDS views based on business needs. These views typically represent aggregated or calculated data.
* **Example CDS Views**:
  1. **I\_Customer**: Customer master data (e.g., names, addresses).
  2. **I\_SalesOrder**: Sales order details (e.g., items, quantities).
  3. **I\_Product**: Product information (e.g., categories, pricing).
  4. **I\_PurchaseOrder**: Purchase order data (e.g., vendors, delivery dates).
* **Filter Options**:
  * You can apply filters for selecting CDS Views that match certain **business areas** or **data entities**.

<figure><img src="../../../.gitbook/assets/image (739).png" alt=""><figcaption></figcaption></figure>

After entering the CSD View name, click on the search button to display the view.

<figure><img src="../../../.gitbook/assets/image (743).png" alt=""><figcaption></figcaption></figure>

#### **Source Type-BAPI Functions (Business Application Programming Interface)**

**BAPIs** are standard SAP functions that allow external systems to interact with SAP. These functions provide a way to read, create, update, and delete SAP data from an external system using remote function calls (RFC).

**How to Work with BAPI Functions in Discovery:**

* **Select BAPI Functions**: BAPIs enable users to interact with business objects. These functions can be used to manipulate master data, transactional data, or other objects.
* **Example BAPI Functions**:
  * **BAPI\_SALESORDER\_CREATEFROMDAT2**: Create a sales order.
  * **BAPI\_MATERIAL\_SAVEDATA**: Save material master data.
  * **BAPI\_INCOMINGINVOICE\_CREATE**: Create an incoming invoice.
* **Filter Options**:
  * You can filter BAPI Functions by **transaction type**, **module** (e.g., **Sales and Distribution**), or **business context**.



<figure><img src="../../../.gitbook/assets/image (740).png" alt=""><figcaption></figcaption></figure>

After entering the function name, click on the search button to display the Bapi functions.

<figure><img src="../../../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure>

**TCURR (Currency Exchange Rates Table)**

The **TCURR** table in SAP holds the exchange rates between different currencies. It is crucial for financial transactions where currency conversion is required.

#### How to Work with TCURR in Discovery:

**Select TCURR:** The TCURR table can be selected for discovering exchange rate data. It typically contains:

* **Currency Pair**: The source and target currencies (e.g., USD to EUR).
* **Exchange Rate**: The rate for converting one currency to another.
* **Valid From Date**: The date when the exchange rate is applicable.

#### Filter Options:

You can apply filters to view the exchange rates for specific dates or currency pairs.

**Select Single Value / Select Ranges**: Single Value and Ranges refer to how you can filter or limit the data for discovery:

1. **Select Single Value**:
   * Filters results for a specific value.
   * Example: Filter TCURR table by a specific currency, like USD or EUR.
   * **Use**: Enter the desired value (e.g., USD).

<figure><img src="../../../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure>

1. **Select Ranges**:
   * Defines a range of values for comprehensive filtering.
   * Example: Specify a date range in the TCURR table to retrieve exchange rates valid within a certain period.
   * **How to Use**:
     * Enter **Lower Limit**: Specify the starting point of the range (e.g., start date).
     * Enter **Upper Limit**: Specify the end point of the range (e.g., end date).

* **Filtering Date Ranges** (e.g., TCURR Table for Currency Exchange Rates):
  * **Lower Limit**: January 1, 2022
  * **Upper Limit**: December 31, 2022
  * **Result**: Filters exchange rates within these dates, providing data only for the specified time period.
* **Filtering Numerical Ranges** (e.g., Table for Financial Amounts):
  * **Lower Limit**: 1000
  * **Upper Limit**: 5000
  * **Result**: Filters financial transactions, providing only records within the specified range

<figure><img src="../../../.gitbook/assets/image (746).png" alt=""><figcaption></figcaption></figure>

* Define **Connection Configuration**:
  * Owned: **Yes/No**
  * Third Party: **Yes/No**
  * Service Managed: **Yes/No**
  * User Managed: **Yes/No**
  * Secured Connection: **Yes/No**
  * Unsecured Connection: **Yes/No**

<figure><img src="../../../.gitbook/assets/image (747).png" alt=""><figcaption></figcaption></figure>

* Review the **Data Source Summary**:
  * **Connection Name**: Enter up to 50 characters (e.g., "S4 Hana Connection").
  * **Description**: Enter up to 300 characters.
* Click **Finish** to create the connection.

<figure><img src="../../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>

Click finish. Click on the list option to see the newly created connection.

<figure><img src="../../../.gitbook/assets/image (749).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
<mark style="color:orange;">Similar to connecting an S4 Hana source in ScikIQ, a BW4 Hana connection can be established as well. However, BW4 Hana offers an expanded range of source type options, including:</mark>
{% endhint %}

| Source Type        | Description                                                                                           | Example                                                            | Use Case                                          |
| ------------------ | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------- |
| **Tables**         | Basic data storage units containing rows and columns.                                                 | `SalesOrders`                                                      | Storing transactional order data                  |
| **CDS Views**      | Logical data views that combine data from multiple tables for flexible reporting and analysis.        | `SalesOrderDetails` (joins `SalesOrders`, `Customers`, `Products`) | Unified sales order details                       |
| **BAPI Functions** | Interfaces for external systems to interact with SAP applications.                                    | `BAPI_SALESORDER_CREATEFROMDAT2`                                   | Creating sales orders via external systems        |
| **InfoObjects**    | Representations of business entities, such as customer or product, used in SAP BW for reporting.      | `0CUSTOMER`                                                        | Categorizing and analyzing customer data          |
| **InfoCubes**      | Multidimensional data structures used for reporting and analysis, consisting of facts and dimensions. | `SalesCube`                                                        | Aggregated sales data by product, customer, time  |
| **DSO**            | Objects for storing detailed transactional data before further processing or aggregation.             | `SalesDso`                                                         | Storing detailed sales transaction data           |
| **ADSO**           | Advanced version of DSO with improved performance and flexibility for transactional and master data.  | `AdvancedSalesADSO`                                                | High-performance sales data storage for reporting |

<figure><img src="../../../.gitbook/assets/image (750).png" alt=""><figcaption></figcaption></figure>

To further understand the differences between these SAP systems, refer to the table below comparing S4 HANA, BW4 HANA, and SAP ECC in terms of their primary features and capabilities:

| **Feature**              | **S4 HANA**                                                   | **BW4 HANA**                                                        | **SAP ECC (ERP Central Component)**                        |
| ------------------------ | ------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Purpose**              | Next-gen ERP suite for managing core business processes.      | Data warehousing and advanced analytics.                            | Core enterprise resource planning (ERP) solution.          |
| **Technology Base**      | Built on SAP HANA, leveraging in-memory computing.            | Built on SAP HANA, optimized for data processing.                   | Built on traditional database technologies (non-HANA).     |
| **Data Handling**        | Real-time transactional and analytical data processing.       | Handles large volumes of historical data for reporting.             | Primarily transactional data management.                   |
| **Use Cases**            | Finance, procurement, sales, manufacturing, etc.              | Data warehousing, reporting, analytics.                             | Core business functions like finance, HR, logistics.       |
| **Real-Time Processing** | Yes, for both transactional and analytics.                    | Yes, optimized for real-time data processing and analytics.         | Limited, focused mainly on transactions (not real-time).   |
| **User Interface**       | SAP Fiori (modern, intuitive UI).                             | Integrated with SAP Fiori for visualization and reporting.          | Traditional SAP GUI (more classic interface).              |
| **Deployment Options**   | On-premise, Cloud, Hybrid.                                    | Primarily on-premise, with cloud options.                           | Primarily on-premise.                                      |
| **Analytics Capability** | Real-time analytics embedded within business processes.       | Advanced data analytics, reporting, and dashboards.                 | Limited analytics capability; often integrated with BW.    |
| **Data Integration**     | Integrates business processes with real-time data flow.       | Integrates data from SAP and non-SAP systems into a data warehouse. | Limited integration compared to S4 HANA and BW4 HANA.      |
| **Example Use Case**     | Real-time order management, financial planning, HR processes. | Aggregating data for reporting, analytics on sales, finance.        | Core financial management, procurement, inventory control. |

This comparison highlights the unique strengths of each solution, aiding in selecting the appropriate system based on business needs and processes.

### Steps to Configure Kafka Connection in ScikIQ

Access ScikIQ Connect Module

1. Navigate to the **SCIKIQ Connect** module from the main menu.
2. Select **Connect to Data Source** and proceed to **Manage Data Source**.
3. In the "Connect to Data Source" dialog, select **Kafka** from the list of supported data sources.

<figure><img src="../../../.gitbook/assets/image (1106).png" alt=""><figcaption></figcaption></figure>

2. Click on "Create Connection" to open the connection details page.
3. Choose whether to create a new connection or use an existing one.

<figure><img src="../../../.gitbook/assets/image (1107).png" alt=""><figcaption></figcaption></figure>

4. **Connection Details-**

Broker URL

* The **Kafka Broker URL** represents the Kafka Broker, which is the central part of a Kafka system.
* It acts as a server responsible for storing data and managing the data exchange between producers (data generators) and consumers (data processors).
* The broker enables producers to send messages and consumers to retrieve them, facilitating a scalable and fault-tolerant communication process.

**Example URL**: `localhost:9092` (local setup).&#x20;

**Connect Url**

* **Kafka Connect** simplifies data integration between Kafka and external systems (e.g., databases, file systems, or cloud storage).
* It uses **predefined connectors** for integration, like the **JDBC connector** to stream data from a database into Kafka topics automatically.
* **Source Connectors** pull data into Kafka, while **Sink Connectors** push data out of Kafka.
* Kafka Connect automates the movement of data between Kafka and external systems without manual intervention.
* The **Connect URL** (e.g., `localhost:8083`) is used to connect Kafka with external systems via Kafka Connect.

**Schema Registry URL**

* The Schema Registry is a service for managing and storing schemas used in Kafka topics.
* It stores schemas for Kafka messages, allowing for consistent data serialization and deserialization.
* Kafka producers and consumers can use the Schema Registry to validate and retrieve schemas when sending or receiving messages.
* The Schema Registry commonly supports **Avro**, but can also work with **JSON** and **Protobuf** formats for data serialization.
* The **Schema Registry URL** allows Kafka clients to interact with the Schema Registry service for managing schemas.
* The **Schema Registry URL** (e.g., `localhost:8081`) is the address where the Schema Registry service is hosted.

**Zookeeper URL**

* Zookeeper is a service used by Kafka to manage cluster state and metadata.
* An example of the Zookeeper URL is `localhost:2181`.
* It tracks active Kafka brokers, manages their configurations, and stores important metadata like topic configurations and partition assignments.
* Zookeeper handles leader election for partitions, ensuring high availability and fault tolerance.
* Kafka uses Zookeeper to assign partitions to brokers and track their responsibilities.
* If a broker fails, Zookeeper reassigns its partitions to another broker to maintain availability.
* If Broker A (leader of a partition) fails, Zookeeper promotes Broker B as the new leader to ensure uninterrupted data flow.

**Rest Proxy URL**

* The Rest Proxy allows clients to interact with Kafka using HTTP REST APIs instead of Kafka’s native protocol.
* An example of the Rest Proxy URL is `localhost:8082`.
* It enables communication with Kafka through RESTful HTTP requests, simplifying integration with non-Kafka clients.
* The Rest Proxy exposes APIs to produce and consume messages to/from Kafka topics over HTTP.
* It is commonly used for integrating Kafka with systems that prefer RESTful communication, such as web applications and mobile apps.

<figure><img src="../../../.gitbook/assets/image (1108).png" alt=""><figcaption></figcaption></figure>

Add Metadata

* Fill in additional details like **Catalog, Domain, Name, and Email** for administrative purposes.
* Click **"Test Connection"** to verify if the provided details are correct.
* If successful, a **green confirmation message** will appear.

<figure><img src="../../../.gitbook/assets/image (1109).png" alt=""><figcaption></figcaption></figure>

There are additional connection configuration settings as follows:

1. **Connection Type:**
   * Owned
   * Third-party
   * Service Managed
   * User Managed
   * **Security Settings:**
     1. Secured Connection: Yes/No
     2. Unsecured Connection: Yes/No
2. Once the required fields are filled, click **"Next"** to proceed with the connection setup.

<figure><img src="../../../.gitbook/assets/image (1110).png" alt=""><figcaption></figcaption></figure>

Review & Submit

1. Provide a display name for the Kafka data source (e.g., "Kafka Real-Time Logs").

<figure><img src="../../../.gitbook/assets/image (1111).png" alt=""><figcaption></figcaption></figure>

Click **Finish** to complete the setup.

<figure><img src="../../../.gitbook/assets/image (1112).png" alt=""><figcaption></figcaption></figure>

Navigate to the **Data Sources List**.

1. new Kafka connection appears in the list.
2. Use this connection for real-time data ingestion and analysis.

<figure><img src="../../../.gitbook/assets/image (1113).png" alt=""><figcaption></figcaption></figure>

Connecting SaaS Platforms with SAP Systems

To integrate various SaaS platforms with SAP systems, you can utilize the following methods for seamless data exchange and process automation:

* **HTTP API**: Facilitates direct data transfer between platforms.
* **SAP OData API**: Enables easy access to SAP data.
* **Webhook**: Provides real-time notifications and data updates.
* **Integration with Tools**:
  * **Slack** and **Teams** for communication.
  * **Service Now** for IT service management.
  * **Tableau** and **Power BI** for data visualization.
  * **Azure Purview** for data governance.
  * **Dynamic CRM API** for customer relationship management.
  * **HTTP Write API** for writing data to external sources.
  * **Email** for notifications and communication.

### Connect OneDrive and SharePoint to SCIKIQ

**1. Prepare Azure Active Directory (Azure AD)**

Before you connect OneDrive and SharePoint to SCIKIQ, you first need to set up an application in **Azure Active Directory (Azure AD)**. This process involves creating an app and generating credentials that SCIKIQ will use to access your OneDrive and SharePoint data.

**1.1 Register an Application in Azure AD**

1. **Log in to Azure Portal**:
   * Visit Azure Portal and sign in with your admin credentials.
2. **Register a New App**:
   * In the left sidebar, click **Azure Active Directory**.
   * Then, click on **App registrations** > **New registration**.
   * **Name**: Enter a name like "SCIKIQ Integration".
   * **Supported account types**: Choose **Accounts in this organizational directory only**.
   * **Redirect URI**: Leave this empty unless you need it for specific use cases.
   * Click **Register**.

**1.2 Configure API Permissions**

Next, assign the correct permissions to allow SCIKIQ to access SharePoint and OneDrive data.

1. **Go to API Permissions**:
   * Click on **API permissions** > **Add a permission**.
   * Select **Microsoft Graph** and choose **Delegated permissions** (to access data on behalf of users).
2.  **Add SharePoint and OneDrive Permissions**:

    * For **OneDrive**, add:
      * `Files.Read`
      * `Files.ReadWrite`
    * For **SharePoint**, add:
      * `Sites.Read.All`
      * `Sites.FullControl.All`

    Click **Add permissions**.
3. **Grant Admin Consent**:
   * Click **Grant admin consent for \[Your Organization]** to ensure these permissions are applied.

**1.3 Generate Client Secret**

A **Client Secret** is required to authenticate SCIKIQ to access your Azure AD data.

1. In **Certificates & Secrets**, click **New client secret**.
2. **Description**: Enter something like "SCIKIQ Integration Secret".
3. Choose the **Expiration** period (e.g., 1 year).
4. Click **Add** and **copy the secret** immediately. You’ll need this later.

**1.4 Obtain Client ID and Tenant ID**

You will need two IDs from Azure:

1. **Tenant ID**: Go to **Azure Active Directory > Properties** to find the **Tenant ID**.
2. **Client ID**: In the **Overview** section of your app registration, copy the **Application (client) ID**.

### Connecting OneDrive to SCIKIQ

This document provides detailed instructions on how to connect OneDrive as a data source within SCIKIQ.

1\. Navigating to the Connect Module

Upon logging into SCIKIQ, users will land on the SCIKIQ Dashboard. The left-side navigation panel provides access to various modules, including SCIKIQ Connect.

<figure><img src="../../../.gitbook/assets/image (1522).png" alt=""><figcaption></figcaption></figure>

2\. Accessing the "SCIKIQ Connect" Module

* From the main menu, navigate to SCIKIQ Connect.
* Choose Connect to Data Source and proceed to Manage Data Source.

<figure><img src="../../../.gitbook/assets/image (1523).png" alt=""><figcaption></figcaption></figure>

. Selecting OneDrive as the Data Source

* In the "Connect to Data Source" dialog, select the files option.

<figure><img src="../../../.gitbook/assets/image (1524).png" alt=""><figcaption></figcaption></figure>

* Choose OneDrive from the list of available cloud sources.

<figure><img src="../../../.gitbook/assets/image (1525).png" alt=""><figcaption></figcaption></figure>



In this setup for establishing a connection, decide whether you wish to create a new connection or select an existing one.

<figure><img src="../../../.gitbook/assets/image (1526).png" alt=""><figcaption></figcaption></figure>

Connection Details Configuration

You will be required to provide the following information:

When setting up the OneDrive connection in SCIKIQ, you will need to provide the following details:

1. Client ID: A unique identifier for your registered OneDrive application in Azure AD.\
   _&#x46;ind it in the Azure portal under App registrations._
2. Client Secret: A secure key used to authenticate the application.\
   _&#x47;enerate it in the Azure portal under Certificates & Secrets._
3. Tenant ID: A unique identifier for your Azure AD organization.\
   _&#x46;ind it in the Azure portal under Azure Active Directory > Properties._
4. Username: The OneDrive account’s email address (usually your work email).\
   _&#x55;se the account you wish to connect to OneDrive._
5. Password: The password for the OneDrive account provided above.\
   _&#x55;se the login password for the specified OneDrive account._

<figure><img src="../../../.gitbook/assets/image (1527).png" alt=""><figcaption></figcaption></figure>

Adding Metadata

1. add metadata to categorize and enrich your OneDrive data. Metadata can help improve the organization and searchability of your data.

<figure><img src="../../../.gitbook/assets/image (1528).png" alt=""><figcaption></figcaption></figure>

Testing the Connection

* Click the Test Connection button to ensure that SCIKIQ can connect to your OneDrive account.
* If the connection is successful, a green confirmation message will appear.
* Click next

<figure><img src="../../../.gitbook/assets/image (1529).png" alt=""><figcaption></figcaption></figure>

Select Files for Discovery:\
Click on the Search button.

<figure><img src="../../../.gitbook/assets/image (1530).png" alt=""><figcaption></figcaption></figure>

Then, select the file extension (e.g., CSV) and click the Search button again. This will display a list of available folders or document libraries (for OneDrive)

<figure><img src="../../../.gitbook/assets/image (1531).png" alt=""><figcaption></figcaption></figure>

It will show folders with matching files (e.g., Documents, Desktop).

Select the folder you want (e.g.csv File).

Optionally, apply filters like Include/Exclude Patterns or set Skip Row(s) if needed.

<figure><img src="../../../.gitbook/assets/image (1532).png" alt=""><figcaption></figcaption></figure>

Click "Save" to display all .csv files in the selected folder.

Select few files then Click Next to proceed.

<figure><img src="../../../.gitbook/assets/image (1533).png" alt=""><figcaption></figcaption></figure>

&#x20;

1. There are additional connection configuration settings as follows:
2. Connection Type:
3.
   * Owned
   * Third-party
   * Service Managed
   * User Managed
   * Security Settings:
   *
     1. Secured Connection: Yes/No
     2. Unsecured Connection: Yes/No
4. click "Next" to proceed with the connection setup.

<figure><img src="../../../.gitbook/assets/image (1534).png" alt=""><figcaption></figcaption></figure>

* Provide a name for the database that will be displayed in the list of connected databases.
* Click Finish.

<figure><img src="../../../.gitbook/assets/image (1535).png" alt=""><figcaption></figcaption></figure>

Viewing the Connection

After completing the setup, navigate to the Data Sources List to confirm the OneDrive connection is successfully listed

<figure><img src="../../../.gitbook/assets/image (1536).png" alt=""><figcaption></figcaption></figure>

### Connecting SharePoint to SCIKIQ

1\. Navigating to the Connect Module

Upon logging into SCIKIQ, users will land on the SCIKIQ Dashboard. The left-side navigation panel provides access to various modules, including SCIKIQ Connect.

2\. Accessing the "SCIKIQ Connect" Module

* From the main menu, navigate to SCIKIQ Connect.
* Choose Connect to Data Source and proceed to Manage Data Source.

<figure><img src="../../../.gitbook/assets/image (1537).png" alt=""><figcaption></figcaption></figure>

Selecting SharePoint as the Data Source

* In the Connect to Data Source dialog, select the files option.
* Choose SharePoint from the list of available cloud sources.

<figure><img src="../../../.gitbook/assets/image (1538).png" alt=""><figcaption></figcaption></figure>

Deciding on the Connection Setup

* In this setup for establishing a connection, decide whether you wish to create a new connection or select an existing one.

<figure><img src="../../../.gitbook/assets/image (1539).png" alt=""><figcaption></figcaption></figure>

Connection Details Configuration

When setting up the SharePoint connection in SCIKIQ, please provide the following details:

1\.      URL: The full address for your SharePoint site.\
Example:\
https://example.sharepoint.com/sites/yoursitename

2. User ID: The email address associated with the SharePoint account you are connecting to.
3. Password: The login password for the SharePoint account provided above. Ensure that this is the correct password for the User ID you entered.

<figure><img src="../../../.gitbook/assets/image (1540).png" alt=""><figcaption></figcaption></figure>

Adding Metadata

* Add metadata to categorize and enrich your SharePoint data.\
  Metadata can help improve the organization and searchability of your data.

<figure><img src="../../../.gitbook/assets/image (1541).png" alt=""><figcaption></figcaption></figure>

Testing the Connection

* Click the Test Connection button to ensure that SCIKIQ can connect to your SharePoint account.
* If the connection is successful, a green confirmation message will appear.
* Click Next.

<figure><img src="../../../.gitbook/assets/image (1542).png" alt=""><figcaption></figcaption></figure>

Select Files for Discovery

* Click on the Search button.

<figure><img src="../../../.gitbook/assets/image (1543).png" alt=""><figcaption></figcaption></figure>

* Then, select the file extension (e.g., CSV) and click the Search button again. This will display a list of available folders or document libraries for SharePoint.

<figure><img src="../../../.gitbook/assets/image (1544).png" alt=""><figcaption></figcaption></figure>

* It will show folders with matching files (e.g., Documents, Shared Documents).
* Select the folder you want (e.g., Documents).
* Optionally, apply filters like Include/Exclude Patterns or set Skip Row(s) if needed.

<figure><img src="../../../.gitbook/assets/image (1545).png" alt=""><figcaption></figcaption></figure>

Click Save to display all .xls files in the selected folder.\
Select a few files, then click Next to proceed.

<figure><img src="../../../.gitbook/assets/image (1546).png" alt=""><figcaption></figcaption></figure>

Additional Connection Configuration Settings

There are additional connection configuration settings as follows:

1. Connection Type:
   1. Owned
   2. Third-party
   3. Service Managed
   4. User Managed
2. Security Settings:

* Secured Connection: Yes/No
* Unsecured Connection: Yes/No

Click Next to proceed with the connection setup.

<figure><img src="../../../.gitbook/assets/image (1547).png" alt=""><figcaption></figcaption></figure>

Finalizing the Connection

* Provide a name for the database that will be displayed in the list of connected databases.
* Click Finish.

<figure><img src="../../../.gitbook/assets/image (1548).png" alt=""><figcaption></figcaption></figure>

Viewing the Connection

* After completing the setup, navigate to the Data Sources List to confirm the SharePoint connection is successfully listed.

<figure><img src="../../../.gitbook/assets/image (1549).png" alt=""><figcaption></figcaption></figure>
