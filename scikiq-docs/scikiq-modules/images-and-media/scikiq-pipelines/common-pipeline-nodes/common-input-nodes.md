# Common Input Nodes

## Using Input Nodes in SCIKIQ’s Pipeline Editor <a href="#inputnode" id="inputnode"></a>

### **Database Input**

Drag and drop the selected input source onto the workspace and once placed, the database connection settings panel will appear on the left.

<figure><img src="../../../../.gitbook/assets/image (1166).png" alt=""><figcaption><p>Image displaying the process of adding an input source by dragging and dropping it onto the pipeline workspace.</p></figcaption></figure>

After adding a Database Input node to the Pipeline, users must select either:

**Data source** – Connect to an external database.

**Assets** – Use pre-configured datasets stored within SCIKIQ.

<figure><img src="../../../../.gitbook/assets/image (1167).png" alt=""><figcaption><p>This ensures that users can integrate data from various structured sources, making it ready for transformation.</p></figcaption></figure>

**Click on the Database Input Node** – This opens the Database Type selection panel on the left. Choose between Data source or **Assets** – Based on whether data is coming from an external system or pre-loaded datasets.

If users select Data Source, the next step is to click on the dropdown under Select Data source.

<figure><img src="../../../../.gitbook/assets/image (1168).png" alt=""><figcaption><p>This image displays a list of available databases, such as Oracle EBS and the Salesforce Master database, in the data sources.</p></figcaption></figure>

Choose from available databases, such as:

1. SCIKIQ BUS DWH
2. Oracle EBS AP
3. Master Data File
4. Trade Orders
5. Salesforce Master Database

\
If users select Assets the next step is to click on the dropdown under Select Asset.

<figure><img src="../../../../.gitbook/assets/image (1169).png" alt=""><figcaption><p>This image displays a list of available assets in the data sources.</p></figcaption></figure>

Choose from available pre-configured datasets, such as Asset Customer Master Connection and Asset Customer Master. Once an asset is selected, its schema properties will be displayed for use.

### Schema Properties for Database Input

Once a Data source is selected, users must configure the Schema Properties for the selected table. This ensures that only the necessary columns filters and transformations are applied before the data moves forward in the pipeline.

<figure><img src="../../../../.gitbook/assets/image (1170).png" alt=""><figcaption><p>This image shows the Schema Properties Panel with table and column settings in the SCIKIQ’s Pipeline.</p></figcaption></figure>

#### Schema Properties Panel Displays

**Database Type** – Displays the selected database type (Data source or Asset).

**Data source** – Shows the connected database (e.g. Trade Orders).

**Create New Connection** – Allows users to configure a new database connection if needed.

#### **Schema Properties –**

1. **Table Name** – These are default existed tables in the connected database. (e.g. EMPLOYEES).
2. **Alias Name** – We can modify the table name with this otherwise it will take default table name.
3. **Column Selection** – Displays all available columns in the selected table.
   1. Users can choose which columns to include in the pipeline.
   2. Each column can be renamed using aliases.
4. **Table column Search box** - There is a search box available under table option (as shown above). As per the input level, user can filter few columns out of the list.

#### **Applying Schema Operations**

Once the Data source and Schema Properties are selected, users can refine data selection by applying additional operations such as:

<figure><img src="../../../../.gitbook/assets/image (1171).png" alt=""><figcaption><p>This image displays schema view and configuration options in the SCIKIQ Pipeline.</p></figcaption></figure>

#### Column Selection Feature

When working with large datasets, it is often unnecessary to retrieve all available columns. The Column Selection Feature in the SCIKIQ Pipeline allows users to shortlist only the required columns from a table, reducing data processing overhead and improving pipeline efficiency.

This feature ensures that only essential fields are selected for further transformation, filtering or export.

For Accessing the Table and Schema Panel

1\.       Navigate to the Schema Properties Panel.

2\.       Click on the Table Icon to view the available database tables.

3\.       Select the desired table (e.g. EMPLOYEES).

4\.       The entire table schema, including all columns, will be displayed.

Shortlisting Required Columns

1\.       By default, all columns from the table may be selected.

2\.       Uncheck the columns that are not required.

3\.       Keep only the relevant columns checked (as shown in the image).

4\.       Ensure that only the necessary data fields remain for further processing.

<figure><img src="../../../../.gitbook/assets/image (1174).png" alt=""><figcaption><p>This image displays the table selection with column filtering and alias assignment in the SCIKIQ Pipeline.</p></figcaption></figure>

Previewing the Selected Columns

1\.       Click the "Preview" button to see how the data looks with only the selected columns.

2\.       Verify that unwanted columns have been excluded.

3\.       Ensure that required data fields appear correctly in the preview.

**Applying Filters on Database input Node**

The Filter feature in the SCIKIQ Pipeline allows users to refine and extract specific subsets of data before processing. By applying filters, users can control which records are retrieved, ensuring that only relevant data is processed in subsequent transformations.

<figure><img src="../../../../.gitbook/assets/image (1175).png" alt=""><figcaption><p>This image displays the filter feature allowing users to apply conditions to refine dataset selection in the SCIKIQ Pipeline.</p></figcaption></figure>

#### Accessing the Filter Option

&#x20;This step enables users to define conditions that restrict data selection based on specific criteria.

1\.       Click the Filter Icon in the Schema Properties Panel.

2\.       Click "Add/Edit Filter" to open the filter configuration panel.

#### Configuring the Filter Condition

This step helps users refine data selection by defining conditions that restrict the retrieved dataset.

Select a Column – Choose the column on which the filter will be applied (e.g. EMPLOYEE\_ID).

#### Choose an Operator – Define the filter condition, such as:

* Equal To (=)
* Less Than (<) / Greater Than (>)
* Less Than or Equal To (<=) / Greater Than or Equal To (>=)
* Not Equal To (!=)

Enter a Value – Specify the value to filter (e.g. EMPLOYEE\_ID ≤ 10).

Add More Conditions – Click "Add Filter" to apply multiple conditions.

Use Parameters or Variables – Advanced users can use dynamic filters with predefined parameters or variables.

<figure><img src="../../../../.gitbook/assets/image (1176).png" alt=""><figcaption><p>This image displays the Add/Edit Filter feature, allowing users to define conditions for dataset filtering in the SCIKIQ Pipeline</p></figcaption></figure>

Saving and Applying the Filter- This ensures that only relevant data is selected before transformation, improving processing efficiency.

1\.       Click "Save" to apply the filter.

2\.       The filtered dataset will be displayed in the Preview Panel

3\.       Users can verify that only records meeting the filter condition are displayed.

<figure><img src="../../../../.gitbook/assets/image (1177).png" alt=""><figcaption><p>This image displays the Filter feature, allowing users to add conditions to refine dataset selection.</p></figcaption></figure>

#### Limit By&#x20;

The "Limit By" feature in the Pipeline allows users to restrict the number of records retrieved from a dataset. This feature is particularly useful for performance optimization, testing and controlling data processing volume before applying transformations.

<figure><img src="../../../../.gitbook/assets/image (1178).png" alt=""><figcaption><p>This image shows the Limit By feature, enabling users to restrict the number of records retrieved from the dataset.</p></figcaption></figure>

**Accessing the "Limit By" Option**

Users can access the "Limit By" option by navigating to the Schema Properties Panel.

1\.       Click the Limit Icon under the Limit By section.

2\.       A dropdown menu will appear with predefined options to limit the dataset.

Available Limit Options:

Users can choose from predefined limits or set a custom limit:

·        Limit by 10 – Retrieves the first 10 records.

·        Limit by 500 – Restricts the dataset to 500 records.

·        Limit by 1000 – Retrieves up to 1000 records.

·        Limit by 2000 – Retrieves up to 2000 records.

Custom Limit:

Users can manually set a custom record limit:

·        Select a predefined limit or enter a specific number in the Custom field.

·        Click the arrow button to apply the limit.

This feature provides flexibility in selecting the number of records retrieved.

**Users can preview** the limited dataset by clicking the "Preview" button on the Database Input Node. The Preview Panel will display only the specified number of records, ensuring that only the required data is retrieved for further processing.

<figure><img src="../../../../.gitbook/assets/image (1179).png" alt=""><figcaption><p>The image displays the Preview feature after applying the Limit By function showing a restricted dataset.</p></figcaption></figure>

#### **Order By**

The "Order By" feature in the Pipeline allows users to sort records based on specific columns in ascending or descending order. This helps structure data before transformation, ensuring that the dataset follows a meaningful sequence for analysis and processing.

Accessing the "Order By" Option

Users can access the "Order By" option from the Schema Properties Panel by following these steps:

1\.       Click the Order Icon under the Order By section.

2\.       The ordering options panel will be displayed.

<figure><img src="../../../../.gitbook/assets/image (1180).png" alt=""><figcaption><p>The image displays the "Order By" feature allowing users to sort data by a specific column in ascending or descending order.</p></figcaption></figure>

#### **Selecting Sorting Preferences**

Users can define sorting conditions using the following options:

* Column Name – Select the column by which records should be sorted (e.g., FIRST\_NAME).
* Order By – Choose the sorting order:

o   Ascending (ASC) – Sorts data in increasing order (e.g. A-Z, smallest to largest).

o   Descending (DESC) – Sorts data in decreasing order (e.g. Z-A, largest to smallest).

**Applying Sorting Preferences**

To apply sorting:

1\.       Select the desired Column Name for sorting.

2\.       Choose either ASC (Ascending) or DESC (Descending) from the dropdown menu.

3\.       Click the plus button to apply multiple sorting conditions if needed.

**Previewing the Sorted Data**

Users can preview the sorted data by clicking the "Preview" button on the Database Input Node. The dataset displayed in the Preview Panel will be sorted based on the specified conditions.

<figure><img src="../../../../.gitbook/assets/image (1181).png" alt=""><figcaption><p>The image shows the dataset sorted by "FIRST_NAME" in ascending order as per the applied sorting condition.</p></figcaption></figure>

This feature allows users to verify that sorting has been correctly applied before proceeding with transformations.

**Group By**

The Group By feature in the Pipeline allows users to aggregate data based on specific columns, summarizing large datasets for better insights. This feature is essential when performing operations like summing sales, counting records, finding averages or retrieving the maximum and minimum values for grouped data.

Grouping ensures that the dataset is structured logically, reducing redundancy and improving reporting efficiency.

<figure><img src="../../../../.gitbook/assets/image (1182).png" alt=""><figcaption><p>The image displays the "Group By" option being selected in the schema properties panel.</p></figcaption></figure>

**Accessing the "Group By" Option**

1\.       Navigate to the Schema Properties Panel.

2\.       Click on the Group Icon under the Group By section.

3\.       A configuration panel will open displaying available columns.

**Selecting Columns for Grouping**

1\.       Choose the columns that define the grouping criteria (e.g. Customer ID, Country or Region).

2\.       Select the aggregation function for numeric fields such as:

Sum – Calculates the total sum of a numeric column (e.g. total units sold).

Count – Counts the number of records within each group.

Avg – Computes the average value for grouped records.

Max/Min – Finds the highest or lowest value in the group.

<figure><img src="../../../../.gitbook/assets/image (1183).png" alt=""><figcaption><p>The image shows the selection of aggregate functions like Sum, Count, Avg, Max and Min for grouping data.</p></figcaption></figure>

1\.       Click "Save" to apply the Group By operation.

2\.       Click "Preview" to verify the transformed dataset.

This Ensure that the grouped dataset correctly reflects the chosen aggregations.

<figure><img src="../../../../.gitbook/assets/image (1184).png" alt=""><figcaption><p>The image displays the final grouped dataset after applying the "Group By" operation.</p></figcaption></figure>

**Apply Expand**

The Expand Schema Panel feature in the Pipeline allows users to toggle between a compact and expanded view of the Schema Properties Panel. This enhances usability by optimizing workspace and providing quick access to column configurations, aliases and transformation settings.

<figure><img src="../../../../.gitbook/assets/image (1185).png" alt=""><figcaption><p>The image shows the schema properties panel with an expand button to view more details.</p></figcaption></figure>

Expanding the Schema Panel

1\.       Locate the Schema Properties Panel on the left side of the interface.

2\.       Click the Expand button.

3\.       The panel will collapse, hiding detailed schema configurations while keeping the table name visible.

<figure><img src="../../../../.gitbook/assets/image (1186).png" alt=""><figcaption><p>This image displays the expanded panel for column configuration and transformations.</p></figcaption></figure>

#### Data Preview and Editing Options-

The Data Preview and Validation feature helps users confirm that the selected data is accurate before proceeding with transformations and output mapping. This step ensures that any modifications applied to the schema, such as column selection, aliases and filters are correctly reflected in the dataset.

<figure><img src="../../../../.gitbook/assets/image (1173).png" alt=""><figcaption><p>This image displays the Preview Feature, showing a sample dataset from the selected table in the SCIKIQ Pipeline.</p></figcaption></figure>

The Preview Feature allows users to click "Preview" to display a sample dataset from the selected table, ensuring data accuracy before proceeding. It helps verify column selection, data accuracy and record availability before applying transformations. Additionally, it ensures that schema modifications, such as renaming columns or applying filters are correctly reflected in the dataset.

Users also have the ability to edit or delete columns before processing:\
Edit – Modify column aliases, change data types or apply transformations as needed.\
Delete – Remove unwanted columns to streamline data processing and improve efficiency.

### Saving a Delta Pipeline

Saving a Delta Pipeline ensures that all configurations, transformations and metadata are stored securely for future execution, modifications or reference. The save functionality provides multiple options based on user needs.

<figure><img src="../../../../.gitbook/assets/image (705).png" alt=""><figcaption><p>This image displays the structured documentation of pipeline ownership</p></figcaption></figure>

**Steps to Save a Delta Pipeline**

1. Enter Pipeline Details:

·        Name: Define a unique name for the Delta Pipeline.

·        Description: Provide a summary of the pipeline.

2. Configure Metadata:

·        Catalogue: Select the appropriate data catalogue (e.g. Enterprise Data Catalogue).

·        Data Domain: Choose the relevant data domain and sub-data domain.

·        Business Owner: Assign the responsible business unit or organization.

·        Creator & Technical Owner: Specify ownership details.

3. Save Options:

·        Save as Draft: Stores the pipeline for future edits without submitting it.

·        Save & Submit: Finalizes the pipeline, making it ready for execution.

·        Save as Copy: Creates a duplicate of the pipeline for modifications or parallel workflows.

4. Finalize and Confirm:

·        Click Cancel to discard changes.

·        Click the appropriate save option to proceed.

### File Input

The File Input feature enables users to ingest data from various file-based sources into the pipeline. This feature supports structured data ingestion from different file formats and storage locations. This feature facilitates seamless data ingestion from local files and external storage sources into the pipeline.

<figure><img src="../../../../.gitbook/assets/image (706).png" alt=""><figcaption><p>This image displays the selection of the File Input node under the Input tab in SCIKIQ’s Pipeline Editor.</p></figcaption></figure>

Accessing File Input

1\.       Navigate to the Input tab in the pipeline editor.

2\.       Select File Input from the available input source options.

3\.       Drag and drop the File Input component into the pipeline workspace.

Selecting File Type: Once the File Input component is placed in the workspace:

1\.       Click on the File Input node to open the configuration panel.

2\.       In the Select File Type dropdown, choose one of the following options:

·        File Upload- Upload files directly from the local system (CSV, XLS, etc.).

·        File Storage- Connect to external file storage locations like Hadoop (HDFS), SFTP or cloud storage.

<figure><img src="../../../../.gitbook/assets/image (707).png" alt=""><figcaption><p>This image shows the File Input node with options to select input type File Upload or File Storage.</p></figcaption></figure>

If connecting to File Storage; user must specify File Details

1\.       Choose the file storage provider (e.g. Scikiq File Store).

2\.       Select the folder or file location.

3\.       Select the required Client/Directory from the dropdown.

4\.       Choose the desired File Format (e.g. CSV, JSON, Parquet, etc.).

5\.       Select the File Structure (Structured or Unstructured).

<figure><img src="../../../../.gitbook/assets/image (708).png" alt=""><figcaption><p>This image shows the File Storage input type selected with configuration options for storage location, file name, format structure.</p></figcaption></figure>

Establish Connection

1\.       Click on the Connect button to access the storage system.

2\.       A file browser window opens, displaying available folders and files.

3\.       Navigate to the ROOT/ directory or the required folder where the dataset is stored.

<figure><img src="../../../../.gitbook/assets/image (709).png" alt=""><figcaption><p>This image shows the File Storage directory view after clicking Connect, displaying the root folder and available files for selection.</p></figcaption></figure>

Select a File

1\.       Browse the directory to locate the target file.

2\.       Click on the required file (e.g. Orders.csv).

3\.       Confirm the file selection by ensuring its File Path is displayed in the properties panel.

<figure><img src="../../../../.gitbook/assets/image (710).png" alt=""><figcaption><p>This image shows a selected file (Orders.csv) from the File Storage, along with encoding and preview options.</p></figcaption></figure>

Configure File Parameters

1\.       Set the appropriate Encoding Format (e.g. ASCII, UTF-8).

2\.       Enable or disable the First Row as Column Header option.

3\.       Choose additional settings such as:

·        Skip Rows

·        Limit By (number of rows to load)

·        Delimited Text File options (Comma, Tab, Semicolon etc.)

·        Enable Password Protection if necessary.

<figure><img src="../../../../.gitbook/assets/image (711).png" alt=""><figcaption><p>This image shows file parsing options for Orders.csv, including encoding, delimiters, file format and preview to load sample data.</p></figcaption></figure>

Confirm and Preview Data

1\.       Click on Click Here to Preview to load a sample dataset.

2\.       Verify the file content, column headers and data structure.

3\.       If required, modify configurations before proceeding.

The file storage system is successfully connected. The required dataset is accessible and ready for transformation. Users can proceed with further operations like data mapping, validation and processing.

<figure><img src="../../../../.gitbook/assets/image (712).png" alt=""><figcaption><p>This image shows the File Input node with data from <em>Orders.csv</em> successfully loaded and previewed in the workspace.</p></figcaption></figure>

**Query Input**

The Query Input feature allows users to extract specific data from a connected database by executing SQL queries. Users can either manually write queries or use the one-click query generation feature for automatic SQL query creation.

Applying Query Input Node

·        Navigate to the Input section in the pipeline.

·        Select Query Input and drag it to the workspace.

<figure><img src="../../../../.gitbook/assets/image (713).png" alt=""><figcaption><p>This image shows the selection of the Query Input node under the Input tab in SCIKIQ Pipeline.</p></figcaption></figure>

**Configure Data Source**

·        In the Schema Properties panel, choose the Data Source from the dropdown.

·        If needed, click Create New Connection to add a new source.

·        Select the required database from the connected sources.

<figure><img src="../../../../.gitbook/assets/image (714).png" alt=""><figcaption><p>This image displays the Query Editor where users can manually write SQL queries or fetch SQL using the Get SQL button.</p></figcaption></figure>

**Manually Writing Queries**

·        Users can type custom SQL queries in the Query Editor to fetch the required data.

·        The Limit option can be applied to restrict the number of records retrieved, improving query performance.

·        The Preview Panel displays the fetched dataset for validation before proceeding with transformations.

<figure><img src="../../../../.gitbook/assets/image (715).png" alt=""><figcaption><p>This image shows the Query Input node in action with a preview of sample results based on the entered SQL query.</p></figcaption></figure>

Click Get Columns to execute the query.

Once the query is executed, the resulting dataset is displayed in the Preview Panel, allowing users to validate the fetched records before proceeding with transformations or further processing.

<figure><img src="../../../../.gitbook/assets/image (716).png" alt=""><figcaption><p>This image highlights the Limit option in the Query Editor to restrict the number of previewed rows.</p></figcaption></figure>

**For Auto-Generated Queries**

For users unfamiliar with SQL or looking to speed up the process our one-click query generation feature can automatically write queries, making data retrieval effortless.

Use the Query Editor and Select a desired column.

Click Get SQL to execute the query.

<figure><img src="../../../../.gitbook/assets/image (717).png" alt=""><figcaption><p>This image shows a selected table (EMPLOYEES) with a basic query generated using Get SQL and its preview data.</p></figcaption></figure>

A SQL query will be generated, and the user may modify it if needed. This feature allows the user to delete existing fields but does not permit adding new fields.

<figure><img src="../../../../.gitbook/assets/image (718).png" alt=""><figcaption><p>This image displays a SQL query for the EMPLOYEES table with selected fields and the resulting data preview.</p></figcaption></figure>

Now, users can apply a Limit to restrict the number of records fetched and click Get Columns to execute the query.

This feature provides full control over the dataset being fetched.

<figure><img src="../../../../.gitbook/assets/image (719).png" alt=""><figcaption><p>This image shows an expanded data preview with the row limit set to 22 for the EMPLOYEES table.</p></figcaption></figure>

### API Input

The API Input feature in SCIKIQ allows users to bring in external data directly from APIs into their pipeline. Whether it is third-party services or internal endpoints, this input method enables seamless integration of real-time or static data sources.

<figure><img src="../../../../.gitbook/assets/image (720).png" alt=""><figcaption><p>This image shows the selection of the API Input node from the Input tab in SCIKIQ.</p></figcaption></figure>

Navigate to the Input section from the left panel and select the API tile. Drag and drop it onto the pipeline canvas. This node allows users to fetch data from external APIs and incorporate it into their data workflows.

Once the API Input node is placed:

·        User will see the configuration panel titled Select API.

·        Users can choose an existing API integration from the dropdown or configure a new one.

·        Toggle DF Enable to allow the response data to be mapped into a dataframe format.

·        Additional options such as Pagination and Save Data on Failure help in handling large data and failure cases gracefully.

<figure><img src="../../../../.gitbook/assets/image (721).png" alt=""><figcaption><p>This image displays the API Input node placed on the canvas with initial configuration options.</p></figcaption></figure>

In this step, users can select an existing API from the dropdown and define the endpoint, parameters, headers and payload. This flexibility enables integration with multiple third-party systems as needed.

<figure><img src="../../../../.gitbook/assets/image (722).png" alt=""><figcaption><p>This image shows the available API selection dropdown, including an option to create a new API.</p></figcaption></figure>

Here, the selected API is fully configured:

·        Base URL and Endpoint are defined to target a specific API resource.

·        Headers like Content-Type are added to define request format.

·        If 'DF' is disabled, users can view the data in JSON format

·        The Request Body (JSON) is prepared. This view helps ensure the API call structure is complete and ready to be sent.

<figure><img src="../../../../.gitbook/assets/image (723).png" alt=""><figcaption><p>This image shows the detailed configuration of a selected API, including base URL, endpoint, headers and JSON body.</p></figcaption></figure>

Once the API call is made the JSON Preview panel displays the response from the API.

·        This ensures the connection is successful and data is being fetched as expected.

·        Users can review raw JSON data before transforming or mapping it to downstream tasks.

<figure><img src="../../../../.gitbook/assets/image (724).png" alt=""><figcaption><p>This image shows the JSON Preview of the API response, enabling users to inspect incoming data.</p></figcaption></figure>

After previewing the data, the response JSON is parsed, and values are extracted into a structured dataframe view.

·        If 'DF' is enabled users can view the data in a tabular format.

·        Users can now select the data frame and map the columns (e.g. name, email, username) to be used in the pipeline.

·        The Preview section displays the final extracted rows, confirming that API data has been correctly ingested and structured.

<figure><img src="../../../../.gitbook/assets/image (725).png" alt=""><figcaption><p>This image shows the structured preview of parsed API data with two rows displayed in tabular format.</p></figcaption></figure>

### GRAPHQL Input

To begin the process, navigate to the Input panel on the left. From the list of available input types, select GraphQL. Drag and drop the GraphQL node onto the workspace to start configuring the connection.

<figure><img src="../../../../.gitbook/assets/image (647).png" alt=""><figcaption><p>This image shows the selection of the GraphQL Input node from the Input tab in SCIKIQ.</p></figcaption></figure>



Once the GraphQL node is placed in the pipeline, it opens the configuration panel. Here you will configure connection details like:

·        API endpoint

·        Headers

·        Parameters

·        GraphQL query

This is where the setup for your data fetch begins.

<figure><img src="../../../../.gitbook/assets/image (648).png" alt=""><figcaption><p>This image displays the GraphQL node placed on the canvas with fields for connection, headers and query input.</p></figcaption></figure>

From the Select GraphQL API dropdown, choose an existing connection like Toolsense List Sites. Upon selection, the associated endpoint (https://api.toolsense.dev/graphql?list=sites) and parameters are auto populated. This simplifies the connection process with reusable APIs.

<figure><img src="../../../../.gitbook/assets/image (649).png" alt=""><figcaption><p>This image shows a selected GraphQL API connection with URL, header key and token input.</p></figcaption></figure>

In this step, the user fills in:

·        GraphQL Parameters (if any)

·        Header (e.g. api-key)

·        GraphQL Query

This defines what data will be fetched and how the API will authenticate the request.

<figure><img src="../../../../.gitbook/assets/image (650).png" alt=""><figcaption><p>This image presents the full API setup, including GraphQL query, variables, headers and endpoint.</p></figcaption></figure>

After entering the query, the JSON Preview allows the user to validate the API response in real-time before processing. Users can confirm the structure and values to ensure the query returns the expected results. If the 'DF' toggle is disabled, users can preview the response in JSON format.

<figure><img src="../../../../.gitbook/assets/image (651).png" alt=""><figcaption><p>This image shows the JSON Preview of the GraphQL response after executing the configured query.</p></figcaption></figure>

Toggle DF Enable to parse the JSON response into a structured DataFrame. This enables the platform to render the response in tabular form under the Preview tab, displaying rows and columns for further transformation or mapping.

<figure><img src="../../../../.gitbook/assets/image (652).png" alt=""><figcaption><p>This image displays the parsed preview of GraphQL data in a tabular format with the Data Frame enabled.</p></figcaption></figure>

### SAP APP Input

SAP APP Input allows users to seamlessly connect to SAP systems like S/4HANA and extract data directly from tables or CDS views. It enables secure access to enterprise-grade SAP data within your pipelines. To start using SAP APP as a data source in your pipeline:

·        Navigate to the Input section on the left panel.

·        Click on SAP APP from the available input options.

·        Drag and drop the SAP APP node onto the workspace.

<figure><img src="../../../../.gitbook/assets/image (653).png" alt=""><figcaption><p>This image shows the selection of the SAP APP Input node from the Input tab in SCIKIQ.</p></figcaption></figure>

After placing the SAP APP node on the canvas:

·        The configuration panel opens on the left.

·        You will see options to Select Connection, Source Type and Search for available tables.

·        This is where you begin linking your SAP system.

<figure><img src="../../../../.gitbook/assets/image (654).png" alt=""><figcaption><p>This image displays the SAP APP node on the canvas with connection and table selection options.</p></figcaption></figure>

Selecting an SAP Connection

·        From the Select Connection dropdown, choose an existing SAP connection (e.g. _S4 Hana Connection_).

·        This establishes the link between SCIKIQ and your SAP instance.

<figure><img src="../../../../.gitbook/assets/image (655).png" alt=""><figcaption><p>This image shows an established S4 Hana connection selected for SAP data access.</p></figcaption></figure>

Choosing Source Type

·        From the Source Type dropdown, choose whether you want to extract data from Table or CDS views.

·        For this example, we proceed with Table as the source type.

<figure><img src="../../../../.gitbook/assets/image (656).png" alt=""><figcaption><p>This image displays the selection between available SAP source types, Table or CDS.</p></figcaption></figure>

·        In the Search box, type the name of the SAP table you want to work with. For example: TCURR.

·        Click on the Search button to fetch matching tables.

<figure><img src="../../../../.gitbook/assets/image (657).png" alt=""><figcaption><p>This image shows a table search within the SAP connection, filtering for "TCURR."</p></figcaption></figure>

·        Once search results are populated, choose the required table from the Select Table dropdown.

·        In this case, TCURR is selected, which contains currency-related data.

<figure><img src="../../../../.gitbook/assets/image (658).png" alt=""><figcaption><p>This image displays the selected SAP table TCURR along with its available columns.</p></figcaption></figure>

·        After selecting the table, column metadata will be displayed below.

·        You can select or deselect specific columns you want to include in the pipeline.

·        A Preview of the data is shown on the bottom panel (e.g. MANDT, KURST, FCURR), confirming the SAP data has been successfully pulled into SCIKIQ.

<figure><img src="../../../../.gitbook/assets/image (659).png" alt=""><figcaption><p>This image shows the data preview of the TCURR table with 200 rows retrieved from the SAP APP input.</p></figcaption></figure>

### NoSQL Input

The NoSQL Input node in SCIKIQ allows users to connect to NoSQL databases (e.g. MongoDB) and ingest unstructured or semi-structured data directly into the pipeline for transformation and processing.

Navigate to the Input section and select the NoSQL tile. Drag and drop it onto the canvas to begin configuring a NoSQL data source.

<figure><img src="../../../../.gitbook/assets/image (660).png" alt=""><figcaption><p>This image shows the NoSQL Input node added to the canvas with data source and properties panel.</p></figcaption></figure>

Once the NoSQL node is placed, the configuration panel opens on the left. Users must:

·        Select Datasource type- Datasource

·        Choose or create a New Connection (e.g. MongoDB)

<figure><img src="../../../../.gitbook/assets/image (661).png" alt=""><figcaption><p>This image displays the selection of an existing Mongo Database Connection for the NoSQL source.</p></figcaption></figure>

From the Datasource dropdown, users can pick from pre-configured NoSQL connections (e.g. MongoDatabase Connection, MongoDBAuth, etc.) to proceed

<figure><img src="../../../../.gitbook/assets/image (662).png" alt=""><figcaption><p>This image shows multiple MongoDB connections available for selection under the Data source dropdown.</p></figcaption></figure>

After establishing a connection:

·        Use the Table dropdown to pick a NoSQL collection to fetch data from (e.g. Customer\_Information, Order\_details)

·        Alias can be set for easy identification of the dataset

<figure><img src="../../../../.gitbook/assets/image (663).png" alt=""><figcaption><p>This image displays the table selection dropdown listing available MongoDB collections.</p></figcaption></figure>

Once a collection is selected, JSON data structure is parsed and displayed in the Preview Panel

Columns are auto-detected, and users can apply filters, DQ rules and column-level transformations as needed.

<figure><img src="../../../../.gitbook/assets/image (664).png" alt=""><figcaption><p>This image shows the selected Customer_Information collection with a JSON preview of the document data.</p></figcaption></figure>

If the user wants to convert JSON into tabular form, they need to go to the Transformation section and click on 'JSON to DF'. We will cover this later in the document.

### UCM File Loader Input

Oracle Universal Content Management (UCM), now known as Oracle WebCenter Content, is an enterprise content management (ECM) platform used to manage the complete lifecycle of content- from creation to archival.

·        It offers a unified repository to securely store, access and collaborate on diverse content types across the organization.

·        UCM is built to handle large volumes of content efficiently while ensuring security and compliance.

·        Supported content types include documents, emails, images, web content and rich media.

Navigate to the Input tab and drag the UCM File Loader node into the canvas.

<figure><img src="../../../../.gitbook/assets/image (665).png" alt=""><figcaption><p>This image shows the selection of the UCM File Loader node from the Input tab in SCIKIQ.</p></figcaption></figure>



In the UCM File Loader configuration:

\-           Connection: Select the Oracle UCM connection.

\-           File Storage: Choose the S3 connection for storing retrieved files.

\-           Bucket: Select the appropriate S3 bucket.

\-           Process: Choose the UCM process which governs workflows like ingestion, approval or lifecycle management.

\-           Tables: Select the relevant Oracle UCM tables containing metadata, permissions, logs and configurations.

\-           Click Preview to validate successful data transfer to S3.

<figure><img src="../../../../.gitbook/assets/image (675).png" alt=""><figcaption><p>UCM File Loader node allows selecting Oracle UCM connection, file storage location and specific process tables.</p></figcaption></figure>

