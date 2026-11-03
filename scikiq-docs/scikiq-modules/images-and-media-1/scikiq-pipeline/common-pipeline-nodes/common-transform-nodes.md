# Common Transform Nodes

## Transformations in SCIKIQ Pipelines

The Transformation layer in SCIKIQ Pipelines allows users to reshape, clean, enrich, and prepare data before it moves to its next destination. Whether you are filtering rows, joining datasets, converting formats, or applying business logic, these transformation nodes provide a no-code interface to perform complex operations effortlessly.

* User can transform the data with the available 8 functions once the data is connected/loaded to the page as per below. This will apply to multiple nodes and tables.

**Key Transformation Nodes**

Here are some of the most commonly used transformation options:

* Filter By – Filter records based on specific conditions.
* Limit By – Restrict the number of rows passed to the next step.
* Calculated By / Calculated Field – Derive new values using formulas or expressions.
* Group By – Aggregate data based on one or more grouping columns.
* Order By – Sort records in ascending or descending order.
* Select – Choose specific columns from the dataset.
* Value Mapper – Replace or map values within columns.
* JSON/XML Converters – Seamlessly switch between structured formats (JSON ↔ XML ↔ DataFrame).
* Join / Merge / DF to JSON / JSON to DF / DQ Rules / Binning / Bulk Columns – Advanced data manipulation tools for combining, structuring, validating, and transforming content.

**Transformation Nodes**

**Calculated By** - It will apply mathematical or logical functions with the available table fields and give the output on a new column.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FHc2vZb6aZsVYre0dT0JA%2Fimage.png?alt=media\&token=9ade471f-a65f-4167-abb1-25415364c462)

**Filter By** - The user can apply AND or OR filter on table fields with the available functions.![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2F0AM4gHYp6Ig5ka6Vu7NK%2Fimage.png?alt=media\&token=ec373a86-4c0e-434a-a58b-03db057bfa15)



**Order By** - The user can arrange any column or table fields in ascending or descending order.![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FSNQYjXueS88qtvgQVd3N%2Fimage.png?alt=media\&token=528a0d34-96b8-4e63-b21b-2b4636a73694)

**Limit By** - The user can apply the limit either from the start or from the end of the table data.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2Fj5UgN30tPd68o3slou9G%2Fimage.png?alt=media&#x26;token=a420ee13-4638-4096-87e3-f6a09b67f1be" alt=""><figcaption></figcaption></figure>

**Group By** - The user can make a group of table fields as per the requirement.Comment

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FryL3dcIib6SK8MVcnqHJ%2Fimage.png?alt=media&#x26;token=feb4080b-d2e8-434c-9c08-d32223cbdef0" alt=""><figcaption></figcaption></figure>

**Value Mapper** - The user just cross-checks the field data to match as per user input and it will display the result in a new column field whether it matches or not matches. If not match then we will specify the value under Default upon Non-matching as in the window.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FO2PitIQXIdLgNReXSPPV%2Fimage.png?alt=media&#x26;token=d1d90d7f-e91c-423d-a489-3e3b4a2eaffa" alt=""><figcaption></figcaption></figure>

**Select** - It gives the final output on the selected columns only.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FTHjZHoWe56oWV0uK15Wl%2Fimage.png?alt=media&#x26;token=22560146-c68a-490b-aafb-4f626323239a" alt=""><figcaption></figcaption></figure>

**Calculated Field** - There is n number of functions under the categories such as statistical, logical, math, etc which can be applied on the table fields and give the result as a new column/field.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FFzvoTukIigExqHiDa8iS%2Fimage.png?alt=media&#x26;token=4a14e2cb-9297-4845-948c-28aba0eb9bda" alt=""><figcaption></figcaption></figure>

**JSON to DF**- A "JSON to DF" node is a tool or component that converts JSON data into a tabular format known as a DataFrame, making it easier to work with and analyze data.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2F8rp5yOSnNAPPGCAR5rkE%2Fimage.png?alt=media&#x26;token=7224fbf3-b1f5-4242-802e-52b5a4c903c4" alt=""><figcaption></figcaption></figure>

**JSON Splitter**- A "JSON splitter" is a tool or function that breaks down a JSON document into smaller pieces, typically individual records or elements, to simplify data extraction and analysis.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2Fx2wCZtFQb6CJx6xsMdwz%2Fimage.png?alt=media&#x26;token=ca1f42ff-1e6e-4426-82e7-77f54ab65d88" alt=""><figcaption></figcaption></figure>

**EDA-** An "EDA node" in data transformation is a tool for initial data exploration, visualization, and quality checks before in-depth analysis

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FhSJ51xRtXxbYrNfrKUHn%2Fimage.png?alt=media&#x26;token=4faf303b-cbd8-42b0-aabb-9425c042ba6e" alt=""><figcaption></figcaption></figure>

**Binning-** A "binning node" in ETL (Extract, Transform, Load) processes are used to group data into categories or bins based on specific criteria. This helps in data transformation and simplifies data analysis and loading into databases..

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FBEpBIegh8mQPespLxokc%2Fimage.png?alt=media&#x26;token=8ca869fb-2ac5-48de-abf1-25fbe8eae63e" alt=""><figcaption></figcaption></figure>

**Bulk Columns-**

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2F63mo0X4ByGbB2qwtzMJU%2Fimage.png?alt=media&#x26;token=7578555d-360a-4591-a1b6-1f84d227252f" alt=""><figcaption></figcaption></figure>

Transformations help ensure your data is accurate, relevant, and analytics-ready—right within the pipeline flow.

<figure><img src="../../../../.gitbook/assets/image (681).png" alt=""><figcaption></figcaption></figure>



### Transformation Node: Calculated Field

The Calculated Field transformation node in SCIKIQ allows users to derive new columns by applying custom expressions or logic on existing data fields. It enhances the dataset by adding computed values, enabling more meaningful analysis downstream.



<figure><img src="../../../../.gitbook/assets/image (682).png" alt=""><figcaption><p>Image displays the use of the Calculated Field node connected to the CUSTOMERS input for performing custom transformations</p></figcaption></figure>

#### Node Configuration:

The Calculated Field node is placed on the canvas and connected to the CUSTOMERS input. This sets up the transformation stage to compute new data fields using existing ones.

_Purpose:_ Prepares for defining custom logic or calculations based on input fields.

<figure><img src="../../../../.gitbook/assets/image (683).png" alt=""><figcaption><p>Image displays the Calculated Field configuration window, users can define expressions and select predefined functions by category.</p></figcaption></figure>

**Open Expression Editor**

Clicking “Open Calculated Field” launches the function editor. Here, users can:

·        Define the Field Name and Description.

·        Write custom expressions using field names and logic.

·        Access categorized functions on the right (Information, Compare, Date & Time, etc.).

_Purpose:_ This editor is where new derived fields are authored.

<figure><img src="../../../../.gitbook/assets/image (684).png" alt=""><figcaption><p>Image displays the Calculated Field node generating a new column "Today" using the TODAY() function for each row.</p></figcaption></figure>

Previewing Calculated Output

Once saved, the calculated field is processed and visible in the Preview tab. The new column appears alongside existing ones like NAME and WEBSITE\_01.

_Purpose:_ Validates that the logic was applied correctly and data transformation succeeded.

<figure><img src="../../../../.gitbook/assets/image (685).png" alt=""><figcaption><p>Image displays a Calculated By node using the date_A_plus_B_months function to derive future dates two months ahead.</p></figcaption></figure>

Here, a prebuilt function date\_a\_plus\_b\_months(Today, 2) is applied. The node takes the result of the Today field and adds 2 months to it, generating a new field called Test.

#### Transformation Node: Order By Node

The Order By transformation node in SCIKIQ allows users to sort incoming records based on selected columns to ensure data is organized before applying further transformations or loading into output systems.

<figure><img src="../../../../.gitbook/assets/image (686).png" alt=""><figcaption><p>Image displays the application of ascending order on the CREDIT_LIMIT column using the Order By transformation node.</p></figcaption></figure>

The user selects the CREDIT\_LIMIT column and sets the sort order to Ascending (ASC) using the dropdown menu. This sorts the dataset from the lowest to highest credit limit value. Users can add multiple sort rules if required by clicking the plus (+) icon.

<figure><img src="../../../../.gitbook/assets/image (687).png" alt=""><figcaption><p>Image shows the sorted dataset in descending order based on CREDIT_LIMIT, highlighting the updated preview results.</p></figcaption></figure>

As shown in the preview panel, the dataset is reordered in real time based on the selected sort criteria. This structured ordering is essential when preparing datasets for reporting, aggregations, or downstream integration.

#### Transformation Node: Limit By

The Limit By node allows users to restrict the number of rows processed in a pipeline. This feature is particularly useful when you are working with large datasets but want to test transformations or perform quick validations on a smaller subset of data. The node can be configured using predefined limits or a custom-defined value.

Below image shows the user interface of the Limit By node right after it is dragged into the pipeline and connected to an input node.

<figure><img src="../../../../.gitbook/assets/image (688).png" alt=""><figcaption><p>Image shows the Limit By transformation node configured with a selection of predefined row limits such as 10, 500, 1000 and 2000.</p></figcaption></figure>

**Process Steps:**

1. The Limit By node is connected to an input node named CUSTOMERS, which contains 200 rows.
2. On the left-hand panel under Limit By, users are presented with several predefined options to limit rows:

·        Limit By 10

·        Limit By 500

·        Limit By 1000

·        Limit By 2000

·        Limit By 20000

3. The user can also choose whether to limit rows from the start or from the end of the dataset, ensuring flexibility based on the dataset structure.
4. After applying any of these options, the preview panel will reflect the truncated dataset accordingly.

<figure><img src="../../../../.gitbook/assets/image (689).png" alt=""><figcaption><p>Image displays a custom row limit of 5 being applied to the dataset, with successful execution confirmation.</p></figcaption></figure>

This image illustrates the scenario where a user has chosen the Custom option to apply a specific row limit- set to 5.

Process Steps:

1\.       The user selects the Custom checkbox under the Limit By panel and inputs 5 as the number of records to fetch.

2\.       Upon clicking the arrow (submit) button, the limit is applied. A notification at the bottom right confirms:

·        ETL Job executed successfully!

·        Limit apply successfully!

3\.       The data preview panel now displays only the top 5 rows from the CUSTOMERS dataset, confirming the limit was enforced as expected.

4\.       The job log on the right also reflects successful transformation execution.



**Transformation Node: Group By**

The Group By transformation node allows users to aggregate data based on one or more selected columns. This is particularly useful for summarizing datasets, generating grouped insights, or preparing data for downstream reporting or loading.

<figure><img src="../../../../.gitbook/assets/image (690).png" alt=""><figcaption><p>Image shows the “Group By” node placed between the CUSTOMERS input source and downstream transformation.</p></figcaption></figure>

**Step-by-Step Instructions**

1.Drag and drop the Group By node from the Transform panel onto the canvas and connect it to the input node (in this case, the CUSTOMERS table).

<figure><img src="../../../../.gitbook/assets/image (691).png" alt=""><figcaption><p>Image displays the Group By panel where users begin by clicking “+ Group Column” to specify which column to group data by.</p></figcaption></figure>

2.In the configuration panel, click the Group tab. Choose the column(s) on which you want to group the data. For example, selecting CREDIT\_LIMIT will group all records based on credit limit values.

<figure><img src="../../../../.gitbook/assets/image (692).png" alt=""><figcaption><p>Image shows CREDIT_LIMIT selected as the group column.</p></figcaption></figure>

3.Switch to the Column tab to define how each column should be aggregated. You can apply functions like SUM, AVG, COUNT or MAX to columns and assign aliases to each result field for clarity.

<figure><img src="../../../../.gitbook/assets/image (693).png" alt=""><figcaption><p>Image displays additional columns being configured for aggregation alongside CREDIT_LIMIT</p></figcaption></figure>

Click the Preview button to review the grouped and aggregated results before proceeding. The transformation will execute and the output table will reflect the new grouped structure.

#### Transformation Node: Select

The Select node in SCIKIQ Pipelines allows users to refine the dataset by choosing specific columns from the source. This helps in focusing only on relevant fields, reducing data noise and optimizing downstream operations.

<figure><img src="../../../../.gitbook/assets/image (694).png" alt=""><figcaption><p>Image displays the Select node in action, filtering specific columns from the CUSTOMERS table for downstream processing.</p></figcaption></figure>

1.Drag and drop the Select node from the Transform panel and connect it to the data source node (in this case, the CUSTOMERS table).

2.In the left configuration panel, all columns from the source table will be listed.\
Use the checkboxes to select only the columns you want to pass downstream. For example:

·        ADDRESS

·        CREDIT\_LIMIT

·        CUSTOMER\_ID

3\. Each selected column allows for aliasing. You can rename columns directly in the "Alias" field if you want them to appear differently in the output.

4.If you want to remove duplicate rows based on selected columns, enable the Distinct option at the top of the column list.

5.Click the Preview button to validate the selected output. The data panel below will show only the chosen columns.

&#x20;**Transformation Node: Value Mapper**

The Value Mapper node in SCIKIQ is used to remap values from a source field to a new target field based on user-defined mappings. This transformation is especially useful when standardizing values, creating lookup mappings, or reformatting data for downstream analytics.

<figure><img src="../../../../.gitbook/assets/image (695).png" alt=""><figcaption><p>Displays the initial setup of the Value Mapper node with empty field configurations.</p></figcaption></figure>

**Step-by-Step Process**

1. Drag and drop the Value Mapper node from the “Transform” panel onto the canvas and connect it to your input source (in this case, the CUSTOMERS table).
2. In the left configuration panel, choose the field you want to map.\
   _&#x45;xample:_ Selected field is CREDIT\_LIMIT.
3. Enter a name for the new target field where the mapped values will be stored.

<figure><img src="../../../../.gitbook/assets/image (696).png" alt=""><figcaption><p>Shows mapping configuration where CREDIT_LIMIT = 3500 is mapped to 35, with default value 45 applied to unmatched.</p></figcaption></figure>

4. If a value does not match any source mappings, SCIKIQ allows you to define a default value that will be assigned.  _Example:_ 45 is entered as the default value.
5. Add the source and target value pairs to build your mapping.\
   _&#x45;xample:_  Source: 3500 → Target: 35
6. Once mappings are defined, click the Preview button to validate the transformation.\
   You will see the newly created field (Test) populated with mapped or default values alongside the original column.

&#x20;**Transformation Node: DF to JSON**

The DF to JSON transformation node in SCIKIQ Pipeline Interface enables the conversion of structured tabular data into nested JSON format, which is useful for API consumption, downstream processing or JSON file storage. Below is the step-by-step process of using the DF to JSON node effectively:

<figure><img src="../../../../.gitbook/assets/image (697).png" alt=""><figcaption><p>This image shows the initial step where the "DF to JSON" node is added to the pipeline and connected to the "CUSTOMERS" input.</p></figcaption></figure>

**Step 1: Drag and Drop the DF to JSON Node**

* From the "Transform" menu, select the DF to JSON node.
* Drag the node onto the canvas and connect it to the input node containing your dataset (e.g., CUSTOMERS).

**Step 2: Configure Grouping Parameters**

* In the left-side configuration panel, use the Group tab.
* Select one or more columns to define the grouping key (e.g., CUSTOMER\_ID, CREDIT\_LIMIT).
* These fields will form the top-level JSON structure, grouping other columns under each key.

<figure><img src="../../../../.gitbook/assets/image (698).png" alt=""><figcaption><p>This image displays grouping configured using CUSTOMER_ID and CREDIT_LIMIT and output is previewed in JSON format.</p></figcaption></figure>

Step 3: Define Column Nesting

* Click the Column tab.
* Choose the columns you want to include in the nested JSON object (e.g., ADDRESS, NAME, WEBSITE\_01).
* Optionally, use the "fx" option to apply transformations to selected fields before nesting.

<figure><img src="../../../../.gitbook/assets/image (699).png" alt=""><figcaption><p>Image highlights step where columns like ADDRESS, NAME etc are selected to be included in the JSON structure under nested key.</p></figcaption></figure>

**Step 4: Set the Nesting Properties**

* Nested Field Name: Provide a name for the nested JSON block (e.g. "details" or "Test").
* Orientation: Choose the layout of the JSON output. Default is set to records, which formats each row as an individual JSON object.

<figure><img src="../../../../.gitbook/assets/image (700).png" alt=""><figcaption><p>This image displays the complete transformed data in JSON format, showing grouped keys and nested details clearly rendered.</p></figcaption></figure>

**Step 5: Preview the JSON Outpu**t

* Click the Preview tab to view the generated JSON structure.
* Confirm that the nested fields are correctly placed and grouped under the specified keys.

**Step 6: Run the Transformation**

* Click Run on the top panel.
* A success message will appear once the transformation executes successfully.

This transformation node is especially powerful when preparing data for downstream systems that require nested JSON structure or when enabling integration with APIs that consume JSON-formatted payloads.

**Transformation Node: JSON Splitter and JSON to DF**

In SCIKIQ, transforming complex nested JSON into a structured format is essential for efficient downstream processing. The JSON Splitter and JSON to DF transformation nodes help users flatten and convert JSON objects into tabular data. This allows for better readability, filtering and further transformation within pipelines. Together, these nodes simplify the process of handling hierarchical data and make it ready for analytics or storage in structured systems.

<figure><img src="../../../../.gitbook/assets/image (701).png" alt=""><figcaption><p>Image shows the JSON Splitter node connected and ready to configure the splitting process.</p></figcaption></figure>

Step 1: Connecting JSON Splitter NodeOnce the dataset is transformed into JSON using the DF to JSON node, the next step is to break down the nested structure for granular access. For this, connect the JSON Splitter node to the DF to JSON output.

<figure><img src="../../../../.gitbook/assets/image (702).png" alt=""><figcaption><p>Image 2 displays the JSON response structure extracted from the data.</p></figcaption></figure>

Step 2: Click on the “Open JSON Splitter” button in the left panel.

·        Here, each JSON field (e.g. NAME, ADDRESS, CREDIT\_LIMIT) is auto-parsed.

·        For each field:

o   Choose the Path, Alias and Data Type

o   Set Repeat if the field is nested in an array.

<figure><img src="../../../../.gitbook/assets/image (703).png" alt=""><figcaption><p>Image captures the preview popup window.</p></figcaption></figure>

Step 3: Click “Preview & Save” to review the flattened structure.

Enter a mapping name (e.g. “Test”) and click Save.

<figure><img src="../../../../.gitbook/assets/image (704).png" alt=""><figcaption><p>Image displays a complete transformation flow connecting CUSTOMERS input to DF to JSON, JSON Splitter and JSON to DF nodes.</p></figcaption></figure>

Step 4: Once JSON has been split successfully, the final step is to convert the flattened JSON into tabular structure. Drag the JSON to DF node and connect it to the output of the JSON Splitter. The final output is now ready for further transformation, enrichment or output export.

### Calculated Fields: Key Functions Explained





* **Category (Date & Time) - Function - NOW()** - In this user can add a new column with the current date and time

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2F8nmMHYQHJ0hDbMmtHSQP%2Fimage.png?alt=media&#x26;token=1ebf6574-d663-4bd9-905e-ae9196012e5d" alt=""><figcaption></figcaption></figure>

* **Category (Date & Time) - Function - TODAY()** - In this user gets a new column with the current date only.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FwAzYEiqZ5N4qENuGt5Mq%2Fimage.png?alt=media&#x26;token=4e2affd0-8278-4b7d-bcd8-917516633a76" alt=""><figcaption></figcaption></figure>

* **Category (Logical) - Function - ISNULL()** - In this user gets output in the form of true/false (If NULL then true and if not then true).In the above bracket the user needs to give the column and the function will check whether the cells contain any data or not.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FfGVamVXYAIMNmy7CxF3w%2Fimage.png?alt=media&#x26;token=07f5187d-e9a7-4178-9ace-ba0b778e3560" alt=""><figcaption></figcaption></figure>

* **Category (Rows) - Function - COUNTROWS()** - In this user gets a total number of rows of the table in a new column.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FZ06IGFIu44Mzabp48462%2Fimage.png?alt=media&#x26;token=2f16f2a3-55fb-4729-bd15-a8922071822b" alt=""><figcaption></figcaption></figure>

* **Category (Rows) - Function - DROPDUPLICATE()** - If the table contains any duplicate rows, this function will drop those rows from the entire table.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FzRBJRhoM6aK3kBDZDAWZ%2Fimage.png?alt=media&#x26;token=96a0fa0b-4e4b-43bf-b812-1e52dc6b4cea" alt=""><figcaption></figcaption></figure>

* **Category (Math) - Function - ABS()** - The ABS function returns the absolute value of a number present in the cell. In the above bracket, the user needs to give the column on which this function needs to be applied.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FryfInuAHy3SE8rlpmByr%2Fimage.png?alt=media&#x26;token=ea5dc64f-9211-41aa-b952-8bc684479af1" alt=""><figcaption></figcaption></figure>



* **Category (Math) - Function - SQRT()** - The SQRT function provides the square root of a number. In the above bracket, the user needs to give the column on which this function needs to be applied.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FQJvV1cxKY42isLdIKkCL%2Fimage.png?alt=media&#x26;token=0e8239f7-bfc4-49dd-9b32-16b1d54ab1c9" alt=""><figcaption></figcaption></figure>

* **Category (Math) - Function - LOG()** - In the LOG function the power is raised to some numbers (usually, base numbers) to get some other number. It is an inverse function of exponential.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FphMHkoT5glD8NvbVteHO%2Fimage.png?alt=media&#x26;token=4fbb2eef-4681-4b2a-9f0e-09643eb2f718" alt=""><figcaption></figcaption></figure>

* **Category (Math) - Function - ROUND()** - The ROUND function rounds a number to a given number of places. In the above bracket, the user needs to give the column on which this function needs to be applied.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FOrITFc721W44EfeTHo6C%2Fimage.png?alt=media&#x26;token=bac4d8d1-de3d-40f8-ade2-a40808c26f36" alt=""><figcaption></figcaption></figure>

Category - Compare\
EQ
--

Compares is an equal column with value elementwise and returns values TRUE or FALSE.

*   Examples

    * Input:- The user has columns as below.
    * Expressions:-
    * The user applies the following function.

    ​![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQhYvT2j1bEsXOiPKB1os%2Fuploads%2FdjSV4hlrlpZlx9NSlO82%2Fimage.png?alt=media\&token=a6e6d356-4a19-48b4-b98e-addf184dc710)​
* **Output**:- The following is the output of the function.
*
