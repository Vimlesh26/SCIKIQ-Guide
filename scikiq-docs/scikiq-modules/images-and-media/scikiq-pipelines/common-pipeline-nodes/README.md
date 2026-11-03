# Common Pipeline Nodes

### Join Node

**Purpose:** The Join Node is essential for combining datasets from multiple sources into a unified view. It allows users to enrich and correlate data by joining tables based on specific conditions.

The **Join Node** is used to merge data from two or more sources based on specified join conditions. It supports the following types of joins:

#### Types of Joins:

1. **Inner Join**: Returns records that have matching values in both tables.
2. **Left Join**: Returns all records from the left table and matching records from the right table. If there's no match, NULLs are returned from the right.
3. **Right Join**: Returns all records from the right table and matching records from the left. If there's no match, NULLs are returned from the left.
4. **Outer Join**: Returns all records when there is a match in either left or right table.

#### Steps to Use:

1. Drag and drop the **Join Node** onto the canvas.

<figure><img src="../../../../.gitbook/assets/image (567).png" alt=""><figcaption></figcaption></figure>

1. Connect it with two or more source nodes (e.g., Database Input nodes).

<figure><img src="../../../../.gitbook/assets/image (568).png" alt=""><figcaption></figcaption></figure>

1. Click on the Join node to open the configuration panel and Choose the Join Type (Inner, Left, Right, Outer).

<figure><img src="../../../../.gitbook/assets/image (570).png" alt=""><figcaption></figcaption></figure>

1. Select the Left and Right tables.

<figure><img src="../../../../.gitbook/assets/image (571).png" alt=""><figcaption></figcaption></figure>

1. Set Join Conditions:
   * Use **Add Rule** for individual conditions.
   * Use **Add Group** to group multiple conditions.

<figure><img src="../../../../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (573).png" alt=""><figcaption></figcaption></figure>

1. To remove any condition, click the **Delete** icon.
2. Click **Save** to apply the join settings.

<figure><img src="../../../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (576).png" alt=""><figcaption></figcaption></figure>

1. Use the **Preview** button to view the resulting data.

<figure><img src="../../../../.gitbook/assets/image (575).png" alt=""><figcaption></figcaption></figure>

### Variable Node

**Purpose:** The Variable Node helps in storing reusable data such as a constant value, a selected column, or an entire table. It improves flexibility and modularity in ETL workflows by allowing references to dynamic or static content.

The **Variable Node** allows users to store and reuse:

* A single value
* A single column
* A table

#### Steps to Use:

1. Drag the **Variable Node** onto the canvas.
2. the variable type: **Single Value**, **Single Column**, or **Table**.
3. Define a name for the variable.

<figure><img src="../../../../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure>

1. Connect it to a source node.
2. Click the **Preview** button to validate and store the variable.

<figure><img src="../../../../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure>

1. This variable can now be used in other nodes like **Transform** or **Calculated Field Node**.

<figure><img src="../../../../.gitbook/assets/image (1213).png" alt=""><figcaption></figcaption></figure>

### SQL Statement Node

**Purpose:** The SQL Statement Node enables advanced users to directly manipulate data using SQL. It allows for granular control over updates, transformations, and conditional logic that may be more complex or not available in other nodes.

The **SQL Statement Node** lets you define and execute custom SQL queries in the ETL pipeline.

#### Use Cases:

* Update or copy data from one table to another
* Apply transformations via SQL

#### Steps to Use:

1. Drag and drop the **SQL Stmt Node** on the canvas.
2. it to a **Preview Node** or any output node.
3. Open the SQL editor panel.

<figure><img src="../../../../.gitbook/assets/image (577).png" alt=""><figcaption></figcaption></figure>



1. Select the connection and target table.
2. Write your SQL statement (e.g., `UPDATE table SET column = value WHERE condition`).
3. Click **OK**.
4. Click **Preview** to verify the SQL execution.

<figure><img src="../../../../.gitbook/assets/image (578).png" alt=""><figcaption></figcaption></figure>

1. Connect this node with source/input nodes and validate data post-update.

<figure><img src="../../../../.gitbook/assets/image (579).png" alt=""><figcaption></figcaption></figure>

### Notify Node

**Purpose:** The Notify Node sends automated alerts or messages when certain conditions in the data pipeline are met. This helps in proactive monitoring, error detection, or reporting.

The **Notify Node** sends notifications based on conditions.

#### Notification Types:

* Email
* Webhook
* API Write

#### Steps to Use:

1. Drag and drop the **Notify Node** onto the canvas.

<figure><img src="../../../../.gitbook/assets/image (1214).png" alt=""><figcaption></figcaption></figure>

1. Connect it with the node whose output triggers the notification.
2. Click **Add** to configure notification settings.

<figure><img src="../../../../.gitbook/assets/image (1215).png" alt=""><figcaption></figcaption></figure>

1. Choose the notification type (Email, Webhook, API).
2. For Email:
   * Select an existing email configuration or create a new template.
   * Define the subject, content, and attach table or column data.
   * Enable toggles for repeated data or attached tables.

<figure><img src="../../../../.gitbook/assets/image (1216).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (1219).png" alt=""><figcaption></figcaption></figure>

1. Click **Preview** to test.
2. Once triggered, the notification is sent to the configured email address.

<figure><img src="../../../../.gitbook/assets/image (1218).png" alt=""><figcaption></figcaption></figure>

### ML Model Node

**Purpose:** The ML Model Node allows integration of machine learning models into ETL pipelines for predictions, classifications, or other intelligent data operations.

The **ML Model Node** is used to apply machine learning models within the ETL pipeline.

#### Steps to Use:

1. Drag and drop the **ML Model Node** onto the canvas.
2. Select the model or create a new one.
3. Choose the **Source Column** and the **Target Column** for prediction or classification.
4. Test the model by clicking on the **Test** button.
5. View the prediction results in the preview.

<figure><img src="../../../../.gitbook/assets/image (1220).png" alt=""><figcaption></figcaption></figure>

### Group Node

**Purpose:** The Group Node allows aggregation of data based on defined grouping fields. It is commonly used for summarization, analytics, and reporting.

The **Group Node** is used to group data based on specific columns and apply aggregations.

#### Steps to Use:

1. Drag and drop the **Group Node** onto the canvas.
2. Connect it with the input node.
3. Choose the **Group By** columns.
4. Select the **Aggregation Function** (e.g., SUM, AVG, COUNT).
5. Click **Preview** to check grouped and aggregated data output.

<figure><img src="../../../../.gitbook/assets/image (1221).png" alt=""><figcaption></figcaption></figure>

### Unstructured Data Processing Nodes

**Purpose:** These nodes handle the ingestion, transformation, and enrichment of unstructured text data. This is vital for natural language processing (NLP), document parsing, and AI-based use cases.

#### 1. Text Partitioning

**Use Case:** Breaks large unstructured documents into manageable text blocks.

* Helps in pre-processing long articles, PDFs, or logs.
* Enables downstream NLP by segmenting content into logical or consistent chunks.

#### 2. Text Extraction

**Use Case:** Extracts meaningful content like named entities, dates, emails, and structured fields from raw text.

* Often used in document digitization, invoice processing, or chatbot context building.
* Output can be passed to variable or transformation nodes.

#### 3. Chunking

**Use Case:** Groups phrases or sections of a text into semantically meaningful blocks.

* Common in NLP for segmenting sentences or paragraphs for summarization or sentiment analysis.
* Useful for preparing training data or embeddings.

#### 4. Text Embeddings

**Use Case:** Converts text into numerical vectors using language models like BERT, Word2Vec, etc.

* Prepares text for machine learning or search applications.
* Enables similarity comparison, classification, or semantic clustering.

#### 5. Vector DB

**Use Case:** Stores and indexes embeddings for efficient semantic search.

* Powers AI features like recommendation engines, semantic filters, and nearest neighbor search.
* Compatible with external tools or services like FAISS, Pinecone, or Qadrant.

<figure><img src="../../../../.gitbook/assets/image (1222).png" alt=""><figcaption></figcaption></figure>

