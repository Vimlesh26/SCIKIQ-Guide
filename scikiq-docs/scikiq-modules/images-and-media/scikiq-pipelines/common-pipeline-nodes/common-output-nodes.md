# Common Output Nodes

After data is processed and transformed in ScikIQ, it can be written or stored in various formats and destinations depending on downstream requirements, target systems, and data formats. This document outlines all the output nodes and methods available in ScikIQ, complete with step-by-step guidance and examples.

### **Table Output**

Allows writing transformed data to relational databases.

**Options:**

* **Create Table**: Creates a new table in the target database schema.
* **Truncate Table**: Deletes all records from an existing table before writing new data.
* **Drop Table If Exists**: Drops an existing table if found, then creates a new one.
* **Existing Table - Select Table**: Enables selection of an already existing table to insert or append data.

#### Steps to Use Table Output Node

1. **Add the Source and Transformation Nodes**: Ensure you have at least one input or transformation node already present on the canvas.
2. **Drag the Table Output Node**:  Drag and drop the **Table Output** node onto the canvas.

<figure><img src="../../../../.gitbook/assets/image (1223).png" alt=""><figcaption></figcaption></figure>

3. **Connect the Table Output Node**: Connect it to the node that contains your final processed/transformed data.
4. **Configure the Connection**: Choose the target database from pre-configured connections (e.g., MySQL, PostgreSQL, etc.).

<figure><img src="../../../../.gitbook/assets/image (1224).png" alt=""><figcaption></figcaption></figure>

4. **Choose an Output Option**:
   1. **Create New Table**: System will prompt for a table name; data will be written into this new table.
   2. **Truncate Table**: Clears all data from the selected existing table before writing.
   3. **Drop Table If Exists**: Deletes the existing table and creates a new one before data insert.

<figure><img src="../../../../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>

5. **Select Existing Table**: Choose from available tables to insert or append data.
6. **Data Quality (Optional)**: define **Data Quality Rules** before the data gets written, ensuring that only clean and valid data enters the database.

<figure><img src="../../../../.gitbook/assets/image (550).png" alt=""><figcaption></figcaption></figure>

7. **Execute and Validate**:

* Click **Preview/Run** to execute the pipeline.
* Verify the data in your target database.

<figure><img src="../../../../.gitbook/assets/image (552).png" alt=""><figcaption></figcaption></figure>

### **File Output**

The **File Output** node allows you to export transformed or cleaned data from your pipeline into various file formats. It is used when the data needs to be stored outside of a database, shared externally, or integrated into another system via files.

#### Purpose

Write pipeline output data into file formats like **CSV**, **Excel (XLSX)**, **Avro**, or **Parquet** and store it in file systems, cloud buckets, or external folders.

#### Supported Output Formats

* **CSV (.csv)** – Simple text format with comma-separated values.
* **Excel (.xlsx)** – Spreadsheet format, ideal for reports and tabular outputs.
* **Avro** – Row-based binary data format often used in big data environments.
* **Parquet** – Columnar storage format for optimized analytics performance

#### Steps to Use File Output Node

1. **Ensure You Have a Source Node**:
   * The data to be exported should already be processed using transformation nodes.
2.  **Add the File Output Node**:

    * Drag and drop the **File Output** node onto the canvas.

    <figure><img src="../../../../.gitbook/assets/image (553).png" alt=""><figcaption></figcaption></figure>
3. **Connect to the Previous Node:** Connect the File Output node to the last transformation node (e.g., Cleaned Data Output).

<figure><img src="../../../../.gitbook/assets/image (554).png" alt=""><figcaption></figcaption></figure>

4. **Select File Storage Type:** Choose a storage type where the file will be written. Supported types include:
   1. **Amazon S3**
   2. **Google Cloud Storage (GCP)**
   3. **FTP/SFTP**

<figure><img src="../../../../.gitbook/assets/image (1227).png" alt=""><figcaption></figcaption></figure>

5. **Choose Storage Connection**\
   Select an existing storage connection, for example: S3 File Storage
6. **Select Target Bucket:** After selecting the S3 connection, click the **Connect** button to fetch available buckets.
   1. If no folders are present in the bucket, none will be displayed.
   2. If folders exist, select the desired **folder path** where you want to write the file.

<figure><img src="../../../../.gitbook/assets/image (1228).png" alt=""><figcaption></figcaption></figure>

7. **Set File Path & Format**
   1. Provide a **file name** (e.g., Product Information)
   2. Select the **file extension/format** (e.g., `.csv`, `.parquet`)

<figure><img src="../../../../.gitbook/assets/image (1229).png" alt=""><figcaption></figcaption></figure>

8. **Run and Validate Output**
   1. Click the **Run** button to execute the pipeline.
   2. The output file will be written in the selected bucket and folder in the chosen format.

<figure><img src="../../../../.gitbook/assets/image (1230).png" alt=""><figcaption></figcaption></figure>

9. **Verify Output in Storage**
   1. Go to the selected S3 bucket and folder path.
   2. Search for the file name you provided.
   3. Verify the file was written correctly in the specified format (e.g., CSV or Parquet).

<figure><img src="../../../../.gitbook/assets/image (1231).png" alt=""><figcaption><p>CSV File</p></figcaption></figure>

You configured the pipeline to export cleaned product data into two formats:

* `product_data.csv` written to S3 in CSV format
* `product_data.parquet` written to S3 in Parquet format

<figure><img src="../../../../.gitbook/assets/image (1232).png" alt=""><figcaption><p>Write data in Parquet format</p></figcaption></figure>



<figure><img src="../../../../.gitbook/assets/image (1233).png" alt=""><figcaption><p>parquet File</p></figcaption></figure>

### Table Update Node

The **Table Update Node** is used to update data in an existing table in a database using the output from previous transformation steps.

This node is helpful when you want to push transformed data into a specific table and update existing records based on certain matching conditions.

<figure><img src="../../../../.gitbook/assets/image (1234).png" alt=""><figcaption></figcaption></figure>

#### **Select a Connection**

1. First, select a **Database Connection** from the available list.
2. If no connection exists, click on **"Create New Connection"** to add one.

<figure><img src="../../../../.gitbook/assets/image (1238).png" alt=""><figcaption></figcaption></figure>

#### **Choose a Target Table**

* After selecting the connection, a list of tables from the database will be displayed.
* Select the **table** you want to update data in.

<figure><img src="../../../../.gitbook/assets/image (1240).png" alt=""><figcaption></figcaption></figure>

#### **Understand the Three Tabs in Configuration Panel**

1. **Column Tab**
   1. This tab shows all columns from the source and target tables.
   2. There is an **Auto Map** toggle:
      1. If **enabled**, it automatically maps columns with the same names.
      2. If **disabled**, users can **manually map** each source column to the target column.

<figure><img src="../../../../.gitbook/assets/image (1241).png" alt=""><figcaption></figcaption></figure>

2. **Condition Tab**
   1. Used to define **matching rules** for updating rows.
   2.  Steps:

       1. Select the **source or target column**.
       2. Choose a comparison **operator** such as:
       3. `=` (Equal)
       4. `!=` (Not Equal)
       5. `>` (Greater Than)
       6. `<` (Less Than)
       7. `>=` (Greater Than or Equal To)
       8. `<=` (Less Than or Equal To)


   3. Provide the **comparison value** or select a column for dynamic value.

<figure><img src="../../../../.gitbook/assets/image (1242).png" alt=""><figcaption></figcaption></figure>

3. **Map Tab**
   1. Used to define how each source column should be mapped to the target column.
   2. Steps:
      1. Select a column from the **source table**.
      2. Select the corresponding column from the **target table**.

<figure><img src="../../../../.gitbook/assets/image (1243).png" alt=""><figcaption></figcaption></figure>

#### &#x20;**Execute the Pipeline**

1. Once all mappings and conditions are set:
   1. Click **Run** to execute the pipeline.
   2. The data will be updated in the target table based on the defined conditions.

<figure><img src="../../../../.gitbook/assets/image (1236).png" alt=""><figcaption></figcaption></figure>

### Kafka Producer Node

The **Kafka Producer Node** in the pipeline allows you to send processed or transformed data into a Kafka topic. This node acts as the producer in the Kafka ecosystem, where it publishes messages to a specified topic on a Kafka server.

#### Key Concepts Recap:

* **Kafka Topic**: A logical channel to which records/messages are published. Data is stored in topics and can be read by consumers.
* **Producer**: A Kafka client that sends records to a Kafka topic.
* **Avro Format**: A data serialization system that provides rich data structures and a compact, fast, binary data format. It requires a schema to serialize/deserialize data.

#### Prerequisites:

* A Kafka connection must be configured in the system (or created during node configuration).
* Input data should be in a JSON-compatible structure before sending it to Kafka.
* Avro schema must be defined if using Avro format.

#### Steps to Use Kafka Producer Node

1. **Add the Kafka Producer Node:** Drag and drop the **Kafka Producer Node** from the node panel to the canvas.

<figure><img src="../../../../.gitbook/assets/image (1244).png" alt=""><figcaption></figcaption></figure>

2. **Connect to the Previous Node:** Connect it to a node that outputs structured data, ideally in JSON format (like a Transform or SQL node).
3. **Configure the Kafka Connection:**&#x20;
   1. Click the node to open its settings panel.
   2. If an existing Kafka connection is available, select it.
   3. Otherwise, create a new Kafka connection by specifying: Kafka Server URL (e.g., `kafka://localhost:9092`)

<figure><img src="../../../../.gitbook/assets/image (1245).png" alt=""><figcaption></figcaption></figure>

4. **Add Kafka Producer**
   1. Click the **“+ Add Kafka Producer”** button.
   2. A new Kafka Producer instance will be added to the configuration.
5. **Topic Configuration**
   1. You have two options:
      1.  **Create a New Topic**:&#x20;

          1. Enable the **Toggle** for "Create New Topic".
          2. Enter the new topic name.
          3. Select the format: **Avro**, **Protobuf**, or **JSON**.
          4. For Avro/Protobuf, click **“Set Schema”** and define the schema (manually or via schema registry)


      2. **Use Existing Topic**
         1. Disable the toggle.
         2. Select a topic from the list of available ones in the Kafka server.

<figure><img src="../../../../.gitbook/assets/image (1246).png" alt=""><figcaption></figcaption></figure>

5. **Set Output Format**
   1. Choose the **Output Format** (e.g., Avro).
   2. Ensure the data you are sending matches the schema format.
   3. **Define Avro Schema**
   4. Provide an Avro schema to structure the data.
      1. {"type":"record","name":"DFtoJSON","fields":\[{"name":"Category","type":"string"},{"name":"Product\_ID","type":"double"},{"name":"Unit\_Price","type":"double"},{"name":"Updated\_Price","type":"double"}]}



<figure><img src="../../../../.gitbook/assets/image (1248).png" alt=""><figcaption></figcaption></figure>

7. **Run and Preview**
   1. Click **Preview** to see how the data looks before being sent.
   2. Click **Run** to execute the pipeline.
   3. The Kafka Producer will publish the messages to the selected topic or create a new topic.

<figure><img src="../../../../.gitbook/assets/image (1249).png" alt=""><figcaption></figcaption></figure>

8. Post Execution
   1. Once the pipeline runs successfully, check your Kafka server or topic logs to verify that the messages have been published.

<figure><img src="../../../../.gitbook/assets/image (1247).png" alt=""><figcaption></figcaption></figure>

### **Write to NoSQL**

The **Write NoSQL Output Node** is used in ScikIQ pipelines to export or write transformed data from the pipeline into a NoSQL database such as **MongoDB**. MongoDB is a document-based NoSQL database that stores data in flexible, JSON-like documents.

This node is useful when you want to persist data from your data pipeline into MongoDB collections for analytics, reporting, or application consumption.

Writes data to NoSQL databases (MongoDB, Cassandra).

#### Supported Output:

* **MongoDB** is supported.
* Data is written as **JSON documents** into the target **collection**.

#### Steps to Use the Write NoSQL Node

**1. Ensure You Have a Source Node**

Before using the Write NoSQL Node, make sure your pipeline already includes transformation or input nodes that process the data you want to export.

<figure><img src="../../../../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure>



**2. Add the Write NoSQL Node**

Drag and drop the **Write NoSQL Output Node** onto the pipeline canvas.

**3. Connect It to the Previous Node**

Connect this node to the output of the previous transformation or input node.

<figure><img src="../../../../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure>

**4. Select or Create a MongoDB Connection**

* Click on the node to open its configuration panel.
* Choose from existing MongoDB connections or click **“+Create New Connection”** to configure:
  * **Connection Name**
  * **Host**
  * **Port**
  * **Database Name**
  * **Authentication (username/password if required)**

<figure><img src="../../../../.gitbook/assets/image (541).png" alt=""><figcaption></figcaption></figure>

**5. Choose a Collection**

* After selecting the connection, the available collections from the selected MongoDB database will be fetched.
* Either select an existing collection or enable the toggle **“Create New Collection”** to create a new one.
* Provide the **name of the collection**.

<figure><img src="../../../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>

6. **Preview and Run**

* Use the **Preview** button to view sample data that will be written to MongoDB.
* Click the **Run** button to execute the pipeline.

<figure><img src="../../../../.gitbook/assets/image (543).png" alt=""><figcaption></figcaption></figure>

**8. Validate Data in MongoDB**

* Open your MongoDB database or MongoDB Compass (GUI tool).
* Navigate to the target database and collection.
* Verify that the data has been inserted correctly.



**Example:**

* Insert JSON order data into MongoDB collection **Product\_Information.**

### **Put API Node**

The **PUT API Output Node** allows you to **send data from your pipeline to an external REST API endpoint** using the PUT method. This is useful when you want to **update or send data to external systems, webhooks, or third-party services** after processing it through your pipeline.

This node supports sending JSON data via HTTP PUT, including **dynamic mapping, authentication, and multiple payload formats**.

#### When to Use It&#x20;

* When you want to **send processed data to an external API**.
* When you want to **update data** in an existing external system.
* Useful for **integration with web apps**, **microservices**, **databases with REST APIs**, etc.

#### **Add PUT API Output Node**

* Drag the **PUT API Output Node** onto the canvas.
* Connect it to the last node which outputs the user profile data (in JSON format)

<figure><img src="../../../../.gitbook/assets/image (527).png" alt=""><figcaption></figcaption></figure>

#### Select Output Type

* Choose **API Type** as:
  * **Webhook** (for simple POST/PUT APIs),
  * **API Write** (for more advanced API requests with headers, tokens, etc.)

In the PUT API Node: WRITE **API Type**

<figure><img src="../../../../.gitbook/assets/image (528).png" alt=""><figcaption></figcaption></figure>

#### Choose or Create API Connection

* Select an **existing API connection** from the dropdown.

<figure><img src="../../../../.gitbook/assets/image (530).png" alt=""><figcaption></figcaption></figure>

#### Configuration Tabs: The node provides multiple configuration tabs:

<figure><img src="../../../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure>

#### Configuration Tabs Explained

1. **Condition Tab:** Used to define **conditions or filters** based on which data is sent to the API.
   1. Select the source and column.
   2. Set conditions (e.g. `id is not null` — to filter which records get sent.
   3. Only matching records will be sent via API.

<figure><img src="../../../../.gitbook/assets/image (533).png" alt=""><figcaption></figcaption></figure>

2. **Mapper Tab**
   1. Maps fields from the previous pipeline node to the placeholders in the API request body.
   2. Supports **simple** fields (e.g., `${name}`) and **nested** JSON structures (e.g., `${addresses[0].city}`).
   3. Ensures dynamic, row-wise data mapping during execution.
   4. Used to populate the API payload with real-time values from the source data.
   5. Placeholder format: `${column_name}` – gets replaced by the actual value.
   6. Must match your API schema structure for successful requests.

<figure><img src="../../../../.gitbook/assets/image (535).png" alt=""><figcaption></figcaption></figure>

3. **Other Tab (Advanced Configurations)**
   1. &#x20;This section shows all the API configuration options:
      1. **Base URL**: Main API domain (e.g., `https://api.vendor.com`)
      2.
      3. **Endpoint**: Specific API endpoint for PUT (e.g., `/updateUser`)
      4.  **Headers**:Key/Value pairs like:

          1. `Content-Type`: `application/json`
          2. `Authorization`: `Bearer <token>`
          3. **Query Parameters**: Optional key-value pairs added to the API URL.


      5. **Request Body Format**&#x20;
         1. Choose between: Raw JSON, Key-Value form and Payload constructed from source data

#### Example Use Case

<figure><img src="../../../../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

**API Schema (Expected JSON Payload):**

```json
{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com",
  "username": "johndoe",
  "addresses": [
    {
      "geo": {
        "lat": "40.7128",
        "lng": "-74.006"
      },
      "city": "New York",
      "street": "123 Main St",
      "zipcode": "10001"
    }
  ],
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-1234"
    }
  ]
}
```

**Actual Payload Sent From ScikIQ:**

```json
{
  "name": "Vimlesh Singh",
  "username": "Vimlesh",
  "email": "vimlesh.singh@scikiq.com",
  "addresses": [
    {
      "street": "123 Main St",
      "city": "Bulandshahr",
      "zipcode": "202390",
      "geo": {
        "lat": "40.7128",
        "lng": "-74.006"
      }
    }
  ],
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-1234"
    }
  ]
}
```

This body is sent to the API using the PUT method.

Execute

* Once mapping and configuration are done, click **Preview** to review the data being sent.
* Then click **Run** to execute the PUT request.

<figure><img src="../../../../.gitbook/assets/image (520).png" alt=""><figcaption></figcaption></figure>

After successful execution, the following response is displayed:

```json
{
  "msg_dtls": "processed",
  "error": 0,
  "task_type": "put_api",
  "name": "Submit a new user",
  "api_response": {
    "0": {
      "name": "John Doe",
      "username": "johndoe",
      "email": "johndoe@example.com",
      "addresses": [
        {
          "street": "123 Main St",
          "city": "New York",
          "zipcode": "10001",
          "geo": {
            "lat": 40.7128,
            "lng": -74.006
          }
        }
      ],
      "phoneNumbers": [
        {
          "type": "home",
          "number": "555-1234"
        }
      ]
    },
    "id": 11
  },
  "api_request": [
    {
      "name": "John Doe",
      "username": "johndoe",
      "email": "johndoe@example.com",
      "addresses": [
        {
          "street": "123 Main St",
          "city": "New York",
          "zipcode": "10001",
          "geo": {
            "lat": 40.7128,
            "lng": -74.006
          }
        }
      ],
      "phoneNumbers": [
        {
          "type": "home",
          "number": "555-1234"
        }
      ]
    }
  ]
}
```

This confirms the API received and processed the data correctly.&#x20;

### **Files to Tables**

1. UCM File Loader Setup
2. Navigate to the Input tab and drag the UCM File Loader node into the canvas.

<figure><img src="../../../../.gitbook/assets/image (544).png" alt=""><figcaption><p>This image displays the UCM File Loader node placed on the pipeline canvas, ready for configuration.</p></figcaption></figure>

3. **In the UCM File Loader configuration**
   1. Connection: Select the Oracle UCM connection.
   2. File Storage: Choose the S3 connection for storing retrieved files.
   3. Bucket: Select the appropriate S3 bucket.
   4. Process: Choose the UCM process which governs workflows like ingestion, approval or lifecycle management.
   5. Tables: Select the relevant Oracle UCM tables containing metadata, permissions, logs and configurations.
   6. Click Preview to validate successful data transfer to S3.



<figure><img src="../../../../.gitbook/assets/image (545).png" alt=""><figcaption><p>UCM File Loader node allows selecting Oracle UCM connection, file storage location and specific process tables.</p></figcaption></figure>

#### Loading Data into Vertica Using Files to Tables Node

After fetching and storing the data from Oracle UCM into the S3 bucket, the next step is to load this data into the Vertica database.

1. From the Output tab drag and drop the Files to Tables node onto the pipeline canvas.
2. The 'Files to Tables' output node is used to transfer processed UCM files into target database tables.

<figure><img src="../../../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>

3. **In the configuration panel**
   1. Select the S3 connection where the UCM files have been stored.
   2. Choose the appropriate bucket within that connection.
   3. Set the file extension to CSV, as the files were dumped in that format.
   4. Select the Vertica connection where the final data will be loaded.
4. **Under File Name Pattern to Table Mapping**
   1. In the File Name Pattern field, enter the expected pattern of the file names (e.g.\*purchasingintype\*.csv).
   2. In the Table field, specify the destination table name in Vertica (e.g. purchasingintypeob).

<figure><img src="../../../../.gitbook/assets/image (548).png" alt=""><figcaption><p>Files to Tables node maps file name patterns from S3 storage to target tables in Vertica for automated data loading.</p></figcaption></figure>

Click Preview to validate and load the data into Vertica in a tabular format. This ensures a smooth transition of data from file-based storage into a structured database for further analysis or reporting.

### **Merge Node**

The **Merge Node** is a powerful operation node used in data pipelines to **synchronize records** between a **source dataset** (transformed data) and a **target database table**. It intelligently performs one or more of the following based on the logic configured:

* **Update existing records**
* **Insert new records**
* **Delete and replace existing records**

Merge Node is essentially used when maintaining **data consistency** between systems or databases.

Combines data with existing table records using specified logic.

**Types:**

* **Row-wise Merge**
* **Using Temp Table**
* **Usine Same Database**

<figure><img src="../../../../.gitbook/assets/image (1250).png" alt=""><figcaption></figcaption></figure>

**Merge Methods:**

* Merge Statement
* Delete-Insert
* Update-Insert

#### **Row-wise Merge**

* **Definition:**\
  Row-wise merging appends the rows of the source table to the target table, assuming both tables have the same structure. It does not perform any deduplication or comparison logic between rows.
* **Use Case:**\
  For example, a company has a **Product** table in two different regions (North and South) with the same schema. When a new product record is added in one region, row-wise merge will append this record to the target product table.

<figure><img src="../../../../.gitbook/assets/image (1251).png" alt=""><figcaption></figcaption></figure>

#### Row-wise Merge

Row-wise merge refers to the process of inserting each record from the source table directly into the target table without checking for duplicates, existing values, or changes. It treats every row in the source as new and appends them into the target.

This type of merge is ideal for appending incremental data where duplication is either controlled upstream or not a concern.

#### Use Case

You receive a daily feed of new products from a supplier. All entries are new, and you want to append them to your master `product` table without deduplication or transformation.

#### Example

| Field         | Source Table Value | Target Table Before Merge | Target Table After Merge |
| ------------- | ------------------ | ------------------------- | ------------------------ |
| product\_id   | 2001               | —                         | 2001                     |
| product\_name | Wireless Keyboard  | —                         | Wireless Keyboard        |
| category      | Electronics        | —                         | Electronics              |
| sub\_category | Accessories        | —                         | Accessories              |
| price         | 899                | —                         | 899                      |
| quantity      | 250                | —                         | 250                      |
| launch\_date  | 2025-05-01         | —                         | 2025-05-01               |

#### Merge Using Temp Table

In this method, the source data is first loaded into a temporary (staging) table. You can apply validations, transformations, or filtering on this temporary table before merging it with the target. This allows better control over data quality and processing logic.

#### Use Case

You receive raw product data with potential errors or missing values. You use a temporary table to clean the data before merging it into the main `product` table.

#### Example

| Field         | Temp Table Value | Transformed Value   | Target Table After Merge |
| ------------- | ---------------- | ------------------- | ------------------------ |
| product\_id   | 2002             | 2002                | 2002                     |
| product\_name | NULL             | "Bluetooth Speaker" | Bluetooth Speaker        |
| category      | Electronics      | Electronics         | Electronics              |
| sub\_category | —                | "Audio"             | Audio                    |
| price         | 0                | 1499                | 1499                     |
| quantity      | 100              | 100                 | 100                      |
| launch\_date  | 2025-05-02       | 2025-05-02          | 2025-05-02               |

***

#### Delete-Insert Merge

#### Definition

This method removes existing records from the target table that match the primary key(s) or identifier(s) from the source, and then inserts the new source records. This is used when the entire row needs to be replaced or refreshed.

#### Use Case

You perform a weekly refresh of product records from an external system. To avoid partial updates or data mismatch, you delete matching records from the target before inserting the updated ones.

#### Example

| Field         | Existing Target Value | Source Value   | Target After Merge |
| ------------- | --------------------- | -------------- | ------------------ |
| product\_id   | 2003                  | 2003           | 2003               |
| product\_name | Wired Mouse           | Wireless Mouse | Wireless Mouse     |
| category      | Electronics           | Electronics    | Electronics        |
| sub\_category | Accessories           | Accessories    | Accessories        |
| price         | 499                   | 699            | 699                |
| quantity      | 300                   | 200            | 200                |
| launch\_date  | 2025-04-20            | 2025-05-01     | 2025-05-01         |

***

#### Update-Insert Merge

#### Definition

This method compares the source and target records based on key fields. If a match is found, the record is updated in the target. If no match is found, the record is inserted. This is often used in Slowly Changing Dimensions (SCD) or upsert logic.

#### Use Case

Your product catalog is updated frequently — some products change in price or quantity, others are newly introduced. You want to update existing records or add new ones based on `product_id`.

#### Example

| Field         | Target Value (Before) | Source Value  | Target Value (After) |
| ------------- | --------------------- | ------------- | -------------------- |
| product\_id   | 2004                  | 2004          | 2004                 |
| product\_name | Smartwatch X1         | Smartwatch X1 | Smartwatch X1        |
| category      | Electronics           | Electronics   | Electronics          |
| sub\_category | Wearables             | Wearables     | Wearables            |
| price         | 2999                  | 2799          | 2799                 |
| quantity      | 120                   | 180           | 180                  |
| launch\_date  | 2025-04-15            | 2025-04-15    | 2025-04-15           |

If product\_id 2005 did not exist, it would be inserted as a new row.

***

#### Delete-Insert (Same Database)

#### Definition

Performs a delete-insert within the same Delta database. No cross-database operations. This method helps maintain consistency and is simpler when data is located in one environment.

#### Use Case

You receive a monthly corrected product dataset from another team in the same database. You delete matching records by `product_id` and insert the new ones.

#### Example

| Field         | Target (Before) | Source             | Target (After)     |
| ------------- | --------------- | ------------------ | ------------------ |
| product\_id   | 2006            | 2006               | 2006               |
| product\_name | Gaming Console  | Gaming Console Pro | Gaming Console Pro |
| price         | 29999           | 34999              | 34999              |

***

#### Update-Insert (Same Database)

#### Definition

Performs an update-insert (merge) operation on data within the same Delta environment. Updates matching records, inserts new ones, and keeps everything consistent within the local storage or catalog.

#### Use Case

Your marketing team frequently uploads updates for product inventory (quantity/price). You apply changes without removing or reloading the full table.

#### Example

| Field         | Target (Before) | Source       | Target (After) |
| ------------- | --------------- | ------------ | -------------- |
| product\_id   | 2007            | 2007         | 2007           |
| product\_name | Drone Camera    | Drone Camera | Drone Camera   |
| price         | 15999           | 14999        | 14999          |
| quantity      | 90              | 110          | 110            |

New `product_id` 2008 (if not found in target) will be inserted.

***

###
