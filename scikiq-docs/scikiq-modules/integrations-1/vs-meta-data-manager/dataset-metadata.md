# Dataset MetaData

### <mark style="color:blue;">**Overview**</mark>

**Dataset metadata** refers to information that describes the structure, content, and management of data. It provides context and detailed explanations about a dataset, such as who owns it, how it should be used, and the data classification. Properly managing metadata ensures the correct usage, governance, and access control of the data. This is crucial in keeping the data organized, secure, and understandable for different users involved in a project.

In this guide, we will walk you through the essential components of **dataset metadata** and explain how to use the **ScikIQ** platform to manage it. We will break down the metadata into key categories, including **Business**, **Technical**, and **User** metadata, and guide you through the platform’s interface so that you can easily manage your dataset metadata, classify data elements, and assign proper ownership and tags.

### <mark style="color:blue;">**What is Dataset Metadata?**</mark>

Metadata, in simple terms, is data about data. It provides descriptive information that helps users understand and manage data. Dataset metadata typically contains three categories:

1. **Business Metadata**: This pertains to the context of the data, like business names, definitions, and data owners.
2. **Technical Metadata**: This includes information about how the data is stored, its type, range, and format.
3. **User Metadata**: This focuses on the interaction with the data, such as user-specific tags, ratings, and other classifications.

Dataset metadata helps in data governance, ensuring the right access levels, the accurate definition of data elements, and proper data classification and security.

### <mark style="color:blue;">Dataset Metadata Workflow</mark>

When managing dataset metadata, the user typically interacts with different tabs and options to manage the data at various levels.

#### **1. Business Tab**

This tab is focused on the business perspective of the dataset. You’ll see the following columns:

* **Element Name**: The unique identifier for each data element.
* **Status**: Current state (e.g., Draft, Published).
* **Business Name**: A human-readable name for the data element.
* **Business Term**: The business-relevant terminology.
* **Business Definition**: Explanation of what the data element represents.
* **Data Owner**: Who is responsible for the dataset.
* **Classification**: The security level (e.g., Public, Confidential).
* **Tags**: Keywords that can be used for search or categorization.

<figure><img src="../../../.gitbook/assets/image (1495).png" alt=""><figcaption></figcaption></figure>

#### **2. Technical Tab**

This tab handles the technical aspects of the dataset. The columns include:

* **Element Name**: The name of the element as it is defined technically.
* **Data Owner**: Who is responsible for the dataset from a technical perspective.
* **Field Type**: The technical type of the data (e.g., string, integer).
* **Classification**: Security level (same as in the Business tab).
* **Value**: The value associated with the data element.
* **Length**: The size or character length of the field.
* **Format**: The format of the data.
* **Min Range / Max Range**: Constraints on the value range.
* **Is Nullable**: Indicates if the field can have a null value.

<figure><img src="../../../.gitbook/assets/image (1496).png" alt=""><figcaption></figcaption></figure>

#### **3. User Tab**

This tab allows for user-specific input on the dataset:

* **Element Name**: The data element name as per the user's view.
* **Status**: The current status of the element (Draft, Submitted).
* **Business Name**: A business-friendly name.
* **Business Term**: The user-friendly term for the data.
* **Tags**: Keywords assigned by the user.
* **Rating**: User ratings (e.g., a 5-star system).

<figure><img src="../../../.gitbook/assets/image (1497).png" alt=""><figcaption></figcaption></figure>

### **Key Features**

#### 1. **Bulk Actions**

You can select either all rows or specific rows from the dataset to apply certain actions (like changing the classification or status). The “All Rows” checkbox lets you change the metadata for all elements, while the “Selected Rows” checkbox allows you to modify only the selected elements.

#### 2. **Generate Definitions with LLM (Language Model)**

The "Generate definition" option uses a large language model (LLM) to automatically generate definitions for dataset elements. This can save time and ensure consistency across the dataset.

#### 3. **Export and Import Dataset Metadata**

You can export the metadata to Excel for offline editing. Once changes are made, you can re-upload the edited file to update the dataset.

### **Using the Interface**

#### **1. All Rows vs. Selected Rows**

* If you select the "All Rows" option, you can modify the status, classification, or data owner for the entire dataset.
* If you choose "Selected Rows", only those rows you have manually selected will be affected by your changes.

#### **2. Draft Status**

You can mark the dataset as “Draft” if it’s still under review or hasn’t been finalized. Once it’s ready, you can change its status to “Submitted” or any other appropriate value.

#### **3. Generate Definitions**

* Clicking on the "Generate definition using LLM" button automatically generates a standard definition for the selected data elements using machine learning. This helps ensure that your metadata is accurate and consistent.



#### **4. File Upload**

The “Choose file” button lets you upload metadata from an Excel file, so you can import or update large datasets at once.

### <mark style="color:blue;">**Managing Dataset Metadata**</mark>

#### **Step 1: Accessing the Dataset Metadata**

1. **Open the Dataset Metadata Dashboard**
   * Navigate to the platform’s main page and locate the "Dataset Metadata" section.

#### **Step 2: Understanding the Tabs**

1. **Business Tab**\
   This tab is where you’ll define business-related metadata for your dataset elements.
2. **Technical Tab**\
   Here, you’ll configure the technical aspects like field types, length, and range.
3. **User Tab**\
   This tab allows you to configure user-specific metadata like ratings and tags.

#### **Step 3: Working with Dataset Rows**

1. **Selecting Rows**
   * **All Rows**: If you want to edit all rows in your dataset, check the "All Rows" checkbox.
   * **Selected Rows**: If you want to edit specific rows, select the rows individually.

#### **Step 4: Changing the Status and Classification**

1. **Changing Status**
   * Under the **Business Tab**, change the **Status** of a dataset element (Draft, Published, etc.).
2. **Changing Classification**
   * In the **Business Tab**, change the **Classification** of the element.

#### **Step 5: Editing the Data Owner**

1. **Assigning Data Owner**
   * Under both the **Business** and **Technical Tabs**, you can assign or change the **Data Owner**.

#### **Step 6: Adding Tags for Better Classification**

1. **Tagging Elements**
   * In both **Business** and **User Tabs**, you can add relevant **Tags** to each dataset element for better categorization and searchability.
