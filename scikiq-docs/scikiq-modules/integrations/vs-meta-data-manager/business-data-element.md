# Business Data Element

### <mark style="color:blue;">**Business Data Element Overview**</mark>

In today’s data-driven world, the management of business data elements is critical for effective data governance. Business data elements are the core building blocks of any data management initiative, providing structure and consistency across an organization’s data systems. By standardizing the way data is defined, accessed, and used, businesses can streamline operations, enhance decision-making, and ensure regulatory compliance.

SCIKIQ’s Business Data Element Management Interface allows organizations to define, govern, and manage data elements in a centralized, user-friendly platform. It enables various teams to interact with data elements, promoting consistent data usage across departments like IT, finance, marketing, HR, and more.

### <mark style="color:blue;">**Why Data Governance Matters in Business Data Elements**</mark>

Effective data governance ensures that data elements are standardized, secure, and accessible across the organization. This is especially important when multiple systems or departments use the same data, as discrepancies or misinterpretations can lead to operational inefficiencies, compliance issues, and data quality problems.

SCIKIQ’s Business Data Elements Management Interface supports data governance by:

* **Consistency**: Ensuring data elements are defined uniformly across systems.
* **Transparency**: Tracking the lifecycle and ownership of each data element.
* **Regulatory Compliance**: Facilitating compliance by linking data elements to legal or regulatory standards.

### <mark style="color:blue;">**Why Choose SCIKIQ's Business Data Elements Management Interface?**</mark>

SCIKIQ offers several key advantages for managing business data elements:

* **Centralized Management**: All business data elements reside in a unified repository for easy access and modification.
* **Governance & Compliance**: Assign roles, statuses, and approvals to ensure that data elements meet regulatory and internal governance standards.
* **User-Friendly Interface**: The no-code platform makes it easy for non-technical users to add, manage, and search data elements.
* **Scalability & Flexibility**: The platform grows with your organization’s needs, handling large datasets with ease.

### <mark style="color:blue;">**Features of the Business Data Element Interface**</mark>

1. **Data Element Name**
   * **Purpose**: A unique name for the business data element.
   * **Key Features**:
     * **Unique Identification**: Ensures each data element has a distinct name.
     * **Clarity**: Names should be self-explanatory and aligned with business terminology.
     * **Consistency**: Promotes standardization across systems and teams.
2. **Data Element Description**
   * **Purpose**: A detailed explanation of the business data element.
   * **Key Features**:
     * **Clarity**: Provides a detailed description to avoid ambiguity.
     * **Contextual Explanation**: Helps users understand the meaning and usage of the data element.
3. **Status**
   * **Purpose**: Tracks the lifecycle stage of the business data element.
   * **Key Features**:
     * **Lifecycle States**: Draft, Active, Archived.
     * **Governance Control**: Ensures only approved elements are used in operational processes.
4. **Scope**
   * **Purpose**: Defines the operational scope of the data element.
   * **Key Features**:
     * **Catalog**: Organizes the data element within relevant business catalogs (e.g., Enterprise Data Catalog).
5. **Data Domain**
   * **Purpose**: Assigns a broad category to the data element (e.g., Financial, Operational).
   * **Key Features**:
     * **Classification**: Helps organize data elements based on business relevance.
6. **Sub Data Domain**
   * **Purpose**: A more granular classification within the data domain.
   * **Key Features**:
     * **Specificity**: Further categorizes data elements for better data management.
7. **Owner**
   * **Purpose**: Specifies the individual or team responsible for the data element.
   * **Key Features**:
     * **Clear Accountability**: Establishes ownership for data governance.
8. **Data Originating Platform**
   * **Purpose**: Identifies the platform where the data element originates from.
   * **Key Features**:
     * **Platform Selection**: Easily select from a predefined list of platforms, databases, or data sets.
9. **Critical**
   * **Purpose**: Flags whether the data element is critical to business operations.
   * **Key Features**:
     * **Flagging**: Helps prioritize and secure critical data elements.
10. **Sensitive**
    * **Purpose**: Marks whether the data element contains sensitive information.
    * **Key Features**:
      * **Tags**: Use tags like PII or GDPR to identify sensitive data elements.
      * **Access Control**: Restricts access to sensitive data elements.
11. **Regulatory Rule**
    * **Purpose**: Links the data element to relevant compliance standards (e.g., GDPR, HIPAA).
    * **Key Features**:
      * **Compliance**: Ensures data elements meet regulatory and industry standards.
12. **Industry Standard**
    * **Purpose**: Aligns the data element with recognized industry standards.
    * **Key Features**:
      * **Standardization**: Facilitates consistency with frameworks like FIBO, HL7, etc.

### <mark style="color:blue;">**Add Business Data Elements**</mark>

1.  **Locate the Business Data Element Panel**:

    * Go to the Business Data Elements interface in SCIKIQ.

    <figure><img src="../../../.gitbook/assets/image (311).png" alt=""><figcaption></figcaption></figure>
2.  **Click on "Add Data Element"**:

    * Start the process of adding a new data element.

    <figure><img src="../../../.gitbook/assets/image (312).png" alt=""><figcaption></figcaption></figure>
3.  **Fill in the Basic Data Element Information**:

    * **Name**: Enter the name of the business data element.
    * **Description**: Provide a concise description of the data element.
    * **Status**: Choose the current status (e.g., Draft, Submit).

    <figure><img src="../../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>
4.  **Select Additional Data Element Details**:

    * **Scope**: Choose the scope or catalog (e.g., Enterprise Data Catalog).
    * **Data Domain**: Choose the appropriate data domain (e.g., Enterprise Daat Domain).
    * **Sub Data Domain**: Select a more specific sub-domain if applicable.

    <figure><img src="../../../.gitbook/assets/image (319).png" alt=""><figcaption></figcaption></figure>
5.  **Set Data Element Ownership**:

    * **Owner**: Assign ownership to an individual or team.
    * **Critical?**: Indicate whether the data element is critical to the organization.
    * **Select Platform**: Choose the originating platform (e.g., Oracle database, Cloud storage).

    <figure><img src="../../../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure>
6.  **Authorized Data Store and Data Quality (DQ) Integration**

    #### **Selecting Data Source**

    1. **Select Data Source**: Choose from available platforms
    2. **Testing Connection**: SCIKIQ verifies connectivity
    3. **Select Table**: Example – `CUSTOMERS`
    4. **Select Column**: Example – `CUSTOMER_ID`

    <figure><img src="../../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

    *   #### **Handling Data Quality Rules**

        If no DQ rule is found:

        *   Click **“Apply DQ Rules”** → Redirects to DQ screen

            *   **Options**:

                * Add new DQ rules
                * Provide rationale for **DQ dispensation**
                * Use **Manual Measure**

                **Note: For the**&#x20;

            <figure><img src="../../../.gitbook/assets/image (322).png" alt=""><figcaption></figcaption></figure>




7. #### **Authorized Data Layer Information**
   1. **Select Data Set**: Example – `customer_ldm`
   2. **Select Column**: Example – `CREDIT_LIMIT`
   3. **Data Quality Rule**: If none found:
      * **Add Rule**, provide **justification**, or use **Manual Measure/Other Options**
8. **Review and Save**:
   * Ensure that all fields are completed correctly.
   * Click "Save" to finalize the addition of the data element.

### <mark style="color:blue;">**Bulk Upload Business Data Elements**</mark>

To manage large datasets efficiently, SCIKIQ offers a Bulk Upload feature for Business Data Elements. This feature allows users to upload multiple data elements at once, improving productivity and consistency.

**Steps to Use Bulk Upload**:

1. **Navigate to the Bulk Upload Tab**:
   * Open the Bulk Upload section within the Business Data Element interface.
2. **Download the Template**:
   * Click on the "Download Template" link to get the pre-configured Excel file.
3. **Fill in the Template**:
   * Enter your data element information in the provided fields, such as Name, Description, Owner, Status, etc.
4. **Upload the Template**:
   * Once filled, return to the Bulk Upload tab and click on the “Click to Browse” area to upload the template.
5. **Review and Submit**:
   * Verify the details and submit the bulk-uploaded data elements.

### <mark style="color:blue;">**Search Business Data Elements**</mark>

The **Search Business Data Elements** feature enables you to quickly find and manage business data elements within SCIKIQ. You can refine your search using various filters and locate data elements based on specific criteria.

**Steps for Search**:

1. **Access the Search Tab**:
   * Go to the "Search Data Element" tab within the Business Data Elements interface.
2. **Use Filters**:
   * Filter by attributes such as:
     * Data Domain
     * Owner
     * Status
     * Sensitive Data
     * Regulatory Compliance
3. **Search by Term Name**:
   * If needed, type the name of the specific data element and click "Search" to locate it.
4. **Export Results**:
   * Export search results to a CSV for reporting or sharing purposes.

### <mark style="color:blue;">**Viewing and Editing Data Elements**</mark>

* **View**: Click on a data element to view detailed information such as the name, description, owner, and status.
* **Edit**: Modify any attributes or details of a data element as needed.
  * **Save**: Ensure changes are saved before exiting.

### <mark style="color:blue;">**Delete Business Data Element**</mark>

Deleting a business data element helps remove outdated, incorrect, or redundant elements, ensuring that your data catalog remains clean and up-to-date. The **Delete** functionality is especially important in maintaining data accuracy and preventing confusion or misuse of obsolete data elements.

**Steps to Delete a Business Data Element:**

1.  **Access the Business Data Elements List**:

    * Navigate to the Business Data Elements interface within SCIKIQ.
    *   Browse the list of available data elements or use the search functionality to locate the specific data element you want to delete.



    <figure><img src="../../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>
2.  **Find the Data Element to Delete**:

    * Use the search bar or apply filters (e.g., status, owner) to find the data element you wish to delete.
    * Once located, look for the delete icon (typically represented by a trash bin symbol) next to the data element.


3.  **Click the Delete Icon**:

    * Click the **Delete** icon next to the relevant data element to initiate the deletion process.

    <figure><img src="../../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>
4.  **Confirm Deletion**:

    * A **confirmation popup** will appear, warning you that the selected data element will be permanently deleted.
    * The message will be something like:\
      “**Business Data Element ‘\[Data Element Name]’ will be deleted. Do you want to continue?**”

    <figure><img src="../../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

    * **Click Yes** to confirm deletion or **No** to cancel.
5.  **Verify the Deletion**:

    * After clicking **Yes**, the data element will be removed from the system.

    <figure><img src="../../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

    * Refresh the list to ensure that the data element no longer appears.

    <figure><img src="../../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>
6. **Audit Log**:
   * Deletions are logged in the audit trail for tracking purposes.
   * The system maintains a record of who deleted the data element and when, providing accountability.
