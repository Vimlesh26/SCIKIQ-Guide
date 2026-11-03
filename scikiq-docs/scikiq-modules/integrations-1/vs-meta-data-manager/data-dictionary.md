# Data Dictionary

### <mark style="color:blue;">Overview</mark>

The SCIKIQ Data Dictionary is a centralized repository designed to manage and document metadata about tables, fields, and data structures within a data source. It allows business and technical users to collaborate on data understanding, enforce governance, and standardize terminology across systems. Users can define technical specifications, assign business context, and even generate descriptions using Large Language Models (LLMs).

Users can:

* Define and manage business/technical metadata.
* Link columns to business glossary terms.
* Import/export metadata files.
* Generate AI-powered definitions.
* Apply keys and relationships across tables.

#### Step 1: Access the Data Dictionary

* From the left navigation menu, click on **Data Dictionary**.
* This opens the main screen with search filters and metadata sections.

<figure><img src="../../../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

#### Step 2: Select Type, Data Source, and Table

* Use the top filters to narrow your search:
  * **Select Type**: Choose between file and Database.
  * **Select Data Source**: Pick the desired source from dropdown.
  * **Select Table**: Choose the relevant table for which metadata is to be managed

<figure><img src="../../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

#### Step 3: View Metadata Tabs

After selecting a table, you’ll see three tabs—**Business**, **Technical**, and **User**. Each tab shows different metadata attributes.

<figure><img src="../../../.gitbook/assets/image (1498).png" alt=""><figcaption></figcaption></figure>

#### A. Business Tab (Default)

This tab allows business stewards or analysts to input and edit business-facing metadata for each column.

**Editable Fields:**

* Element Name
* Status
* Business Name
* Business Term _(linked to Glossary)_
* Business Definition
* Data Owner
* Classification _(Confidential, Internal, Public, Secret)_

<figure><img src="../../../.gitbook/assets/image (1499).png" alt=""><figcaption></figcaption></figure>

#### B. Technical Tab

This tab is used by data engineers or architects to define technical attributes.

**Editable Fields:**

* Element Name
* Data Owner
* Field Type
* Classification
* Value / Length / Format
* Min/Max Range
* Is Nullable

<figure><img src="../../../.gitbook/assets/image (1500).png" alt=""><figcaption></figcaption></figure>

**C. User Tab**

This tab is intended for collaborative input from business users and includes:

* **Element Name**
* **Status**
* **Business Name**
* **Business Term**
* **Tags**
* **Rating**

<figure><img src="../../../.gitbook/assets/image (1501).png" alt=""><figcaption></figcaption></figure>

### **Add Relationships and Map Terms**

Use the top menu bar to access the following tools:

**Foreign Key**

To define relationships between tables:

1. Click **Foreign Key**, then **Add Foreign Key**.
2. Fill in:
   * Source Connection, Source Table, Column
   * Target Connection, Target Table, Column
3. Relationships will appear in a table:\
   `Table | Column | Reference Table | Reference Column`

<figure><img src="../../../.gitbook/assets/image (1508).png" alt=""><figcaption></figcaption></figure>

**Map Terms**

* Link columns to glossary terms for semantic consistency.
* Mapped terms will show under the **Business Term** column.

<figure><img src="../../../.gitbook/assets/image (1509).png" alt=""><figcaption></figcaption></figure>

**Preview and Update Metadata**

Click the **Preview** button:

*   View a formatted summary of all metadata before saving.

    <figure><img src="../../../.gitbook/assets/image (1510).png" alt=""><figcaption></figcaption></figure>
*   Options available on this screen:

    * **DQ (Data Quality)** and **EDA (Exploratory Data Analysis)** – click to navigate to respective modules.

    <figure><img src="../../../.gitbook/assets/image (1511).png" alt=""><figcaption></figcaption></figure>

**Save Dictionary**

Once metadata is added or edited:

* Click **Save Dictionary** to commit all changes across tabs.

<figure><img src="../../../.gitbook/assets/image (1512).png" alt=""><figcaption></figcaption></figure>

**LLM Configuration**

Click **LLM Config** to:

* Choose or change the AI model used to auto-generate business definitions.
* Useful when descriptions are missing or require standardization.

<figure><img src="../../../.gitbook/assets/image (1513).png" alt=""><figcaption></figcaption></figure>

To auto-generate a business definition:

1. Select the element.
2. Click **Generate Definition using LLM**.

<figure><img src="../../../.gitbook/assets/image (1504).png" alt=""><figcaption></figcaption></figure>

**Table-Level Metadata**

Under the table name, users can provide:

* **Table Business Name**
* **Table Description**

<figure><img src="../../../.gitbook/assets/image (1514).png" alt=""><figcaption></figcaption></figure>

Click **Update** to save these values.

<figure><img src="../../../.gitbook/assets/image (1515).png" alt=""><figcaption></figcaption></figure>

**View Modes – All Rows vs Selected Rows**

* **All Rows**: View/edit all metadata rows.
*   **Selected Rows**: Use checkboxes to filter and apply changes only to selected elements.

    * Useful for batch edits.

    <figure><img src="../../../.gitbook/assets/image (1516).png" alt=""><figcaption></figcaption></figure>

**Import / Export Metadata**

**Export File**

* Click **Export File** to download the metadata in Excel format.

<figure><img src="../../../.gitbook/assets/image (1517).png" alt=""><figcaption></figcaption></figure>

* You can update fields like Element Name or Business Definition offline.

<figure><img src="../../../.gitbook/assets/image (1518).png" alt=""><figcaption></figcaption></figure>

**Upload File**

* Click **Choose File** → Select your updated Excel file → Upload.

<figure><img src="../../../.gitbook/assets/image (1519).png" alt=""><figcaption></figcaption></figure>

* System will update metadata based on the file contents.

<figure><img src="../../../.gitbook/assets/image (1520).png" alt=""><figcaption></figcaption></figure>

**Export to Glue (AWS)**

To export metadata into AWS Glue:

1.  Click **Export to Glue**.

    <figure><img src="../../../.gitbook/assets/image (1521).png" alt=""><figcaption></figcaption></figure>
2. Fill in the following:
   * Select Connection
   * Select Database
   * Select Table
3. If **Create Table** is enabled:
   * Provide the new table name.
   * Otherwise, data is written to the existing table.

**Primary Key and Composite Key**

You can define:

* **Primary Key**: A single unique identifier.
* **Composite Key**: Combination of multiple columns as a key.

Set these from the top menu options when needed.

<figure><img src="../../../.gitbook/assets/image (1507).png" alt=""><figcaption></figcaption></figure>

**Find and Replace**

Use **Find and Replace** to:

* Quickly replace metadata values across multiple columns or fields.

<figure><img src="../../../.gitbook/assets/image (1505).png" alt=""><figcaption></figcaption></figure>

**Status and Classification**

* **Status Options**: `Draft`, `Submit`
* **Classification Types**: `Confidential`, `Internal`, `Public`, `Secret`

<figure><img src="../../../.gitbook/assets/image (1506).png" alt=""><figcaption></figcaption></figure>



