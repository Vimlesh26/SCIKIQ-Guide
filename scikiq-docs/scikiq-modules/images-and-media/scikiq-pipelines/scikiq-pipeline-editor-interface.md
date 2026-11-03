# ScikIQ Pipeline Editor Interface

S**cikIQ Pipeline Editor** provides a rich, intuitive, and flexible visual interface that empowers users to build, configure, and execute data processing workflows. Through its drag-and-drop functionality and structured panels, users can manage complex data pipelines with ease. This section will guide you through each component of the editor, ensuring you understand how to fully utilize it.

### **Main Workspace (Center Grid)**

The **Main Workspace** is the central area of the Pipeline Editor, where users can design the entire data workflow. Here, users can **drag and drop components** such as data input sources, transformation nodes, and output destinations.

#### Features of the Main Workspace:

* **Drag-and-Drop Interface**: Easily move and arrange nodes to create logical workflows.
* **Visual Connections**: Draw edges between nodes to define data flow and processing order.
* **Workflow Visualization**: View all connected components and their relationships to maintain a clear overview of your data pipeline.

#### Example:

1. You might drag an **API Input** node, followed by a **Transform** node, and then an **Output** node that writes to a database or a file.
2. After creating these nodes, you can connect them by drawing edges from the **Output** of the **API Input** node to the **Input** of the **Transform** node and so on.

<figure><img src="../../../.gitbook/assets/image (582).png" alt=""><figcaption><p>This image shows the pipeline design area, where users can drag and drop input, transform &#x26; output components to build workflows.</p></figcaption></figure>

### **Toolbar – Top Left**

The toolbar on the **Top Left** provides essential tools for building and enhancing your data pipeline. It contains several node categories that are central to constructing workflows. These include input nodes, transformation nodes, unstructured data processing, and output destinations.

#### Key Node Categories in the Toolbar:

* **Input Nodes**:\
  These nodes allow you to integrate various data sources, such as:
  * **Databases**: Connect to relational or NoSQL databases (e.g., MySQL, MongoDB).
  * **APIs**: Fetch data from external APIs.
  * **Files**: Import data from flat files (e.g., CSV, Excel, JSON).
* **Transform Nodes**:\
  These nodes apply critical business logic and data transformations such as:
  * **Mapping**: Transform data formats or map fields.
  * **Enrichment**: Add additional information to the data.
  * **Filtering**: Apply conditions to clean or refine the data.
* **Unstructured Data Nodes**:\
  These nodes help handle semi-structured or unstructured data such as JSON, XML, or text documents.
  * Useful for integrating data that doesn't fit neatly into traditional tables.
* **Output Nodes**:\
  These nodes define where the processed data should be sent. You can output to:
  * **Databases**: Write transformed data back into a database.
  * **APIs**: Send the data to an external API.
  * **Files**: Export the data into a file format (e.g., CSV, Excel).
* **SQL Statement**:\
  Use this feature to execute SQL-based transformations, enabling you to directly apply SQL queries within your workflow.
* **Variable**:\
  Allows users to create and manage variables within the pipeline, which can be used to dynamically control parameters across the workflow.

<figure><img src="../../../.gitbook/assets/image (583).png" alt=""><figcaption></figcaption></figure>

#### Advanced Nodes:

* **Join**: Combine data from multiple sources or datasets based on common keys or conditions.
* **Glue**: Merge datasets vertically or horizontally (appending rows or columns).
* **Notify**: Set up alerts or notifications to trigger based on certain conditions during the pipeline's execution.
* **Group**: Aggregate data, such as grouping by certain fields for summing, averaging, or counting.
* **ML Model**: Integrate machine learning models to apply predictions or classifications on the data.

<figure><img src="../../../.gitbook/assets/image (584).png" alt=""><figcaption></figcaption></figure>

### Toolbar (Top Right)- Action & Control Tools

The **Top Right Toolbar** contains management tools to control the layout, execution, and scheduling of the pipeline.

#### Key Features:

* **Full-Screen Mode**:\
  Expand the editor to full-screen for better visibility when working on complex pipelines or viewing large datasets.
* **Delete**:\
  Removes selected nodes or components from the workflow, helping you clean up or adjust the pipeline structure.
* **Clear**:\
  Clears all selections from the workspace without affecting saved or loaded configurations.
* **Preview Step**:\
  This feature allows users to preview the results of intermediate data processing steps before running the entire pipeline. It helps ensure that transformations are being applied correctly.
* **Run**:\
  Executes the entire pipeline workflow based on the defined configuration and connected nodes. You can test the data processing in real-time.
* **Save**:\
  Saves the current configuration of the pipeline for future use. This is essential for saving progress or sharing workflows between users.
* **Schedule Job**:\
  Automates the execution of the pipeline by setting a schedule for when the workflow should run (e.g., at specific intervals like hourly, daily, or weekly).

<figure><img src="../../../.gitbook/assets/image (585).png" alt=""><figcaption></figcaption></figure>

### **Toolbar – Right Panel**

This panel provides advanced configuration and control settings to optimize data processing tasks.

<figure><img src="../../../.gitbook/assets/image (586).png" alt=""><figcaption></figcaption></figure>

**Execution Settings**:

Here, users can fine-tune execution parameters to optimize performance, handle errors, and ensure smooth workflow processing.

<figure><img src="../../../.gitbook/assets/image (595).png" alt=""><figcaption></figcaption></figure>

* **Execute Tasks in Parallel**:\
  This option enables the parallel execution of tasks, leveraging multi-threading to speed up processing, especially for large datasets.
* **Continue Job on Error**:\
  When enabled, minor errors will not interrupt the overall pipeline execution, ensuring that the workflow continues even if some tasks encounter issues.
* **Stop Job on Empty**:\
  Automatically halts the pipeline when no data is found to process, preventing unnecessary computations on empty datasets.
* **Hide SCIKIQ Audit Fields**:\
  Hides system-generated metadata (e.g., timestamps, execution logs) to give a cleaner and more user-friendly view of the data.
* **Batch Size**:\
  Defines the number of records to be processed in each batch. Optimizing this can help improve both performance and resource usage.
* **File Batch Size**:\
  For file-based data ingestion, this setting defines the size (in MB) of each file batch that will be processed.
* **Preview Limit**:\
  Limits the number of records shown during the preview step, enabling you to check a subset of the data before execution.
* **Dark Mode & Optimize Execution**:\
  Dark Mode enhances user interface comfort, while optimizing execution settings improve processing performance.

#### **Node Information Panel**

The **Node Information** panel provides key details about the currently selected node. This panel allows users to quickly assess the attributes and configuration of any node within the pipeline.

<figure><img src="../../../.gitbook/assets/image (588).png" alt=""><figcaption></figcaption></figure>

#### Key Components:

* **Task Type**: Specifies the operation being performed (e.g., SELECT, JOIN, TRANSFORM).
* **Node Name**: The name assigned to the node, helping you identify its purpose within the workflow.
* **Notes**: A section for adding descriptions, comments, or explanations about the node’s function.
* **Total Columns**: Displays the total number of columns in the dataset at this point in the pipeline.
* **Selected Columns**: Shows how many columns are actively being processed.
* **Unselected Columns**: Lists the number of columns excluded from processing.
* **Changed Alias**: Indicates the number of columns whose names have been altered for better readability or mapping.

#### Set Parameters Panel:&#xD;

The Set Parameters panel allows users to define dynamic parameters that control how the pipeline behaves during execution.

<figure><img src="../../../.gitbook/assets/image (589).png" alt=""><figcaption></figcaption></figure>

#### Key Components:

**Set Paramete**r: A list of customizable parameters that can be passed dynamically during execution.

**Default Value**: Shows the initial default value assigned to each parameter, which can be modified as needed.

Common Parameters:\
**resource\_key**: A unique identifier for the resource being used in the workflow.

**scheduler\_run\_id**: The ID that tracks scheduled runs of the pipeline.

**run\_time**: Captures the exact time the process is executed.

**run\_by**: The user or system triggering the execution.

**run\_on**: Specifies the execution date of the process.

#### **Job Log**

The **Job Logs** panel displays detailed execution status, making it easy to monitor, debug, and track the progress of tasks within the pipeline.

<figure><img src="../../../.gitbook/assets/image (590).png" alt=""><figcaption></figcaption></figure>

Key Features:

* **Task List**: Shows individual tasks that were executed, including SQL queries and custom processes.
* **Execution Status**: Displays whether each task was successful or encountered errors. Green highlights indicate success, and error counts are shown for troubleshooting.
* **Expand Task Details**: Clicking the (+) icon next to each task provides additional details, including execution time, parameters used, and error logs.
* **Error Monitoring**: Logs errors during task execution to help users quickly identify and fix issues.

#### **Database Input Suggestions**

This feature provides intelligent recommendations for selecting the right database table when integrating data.

<figure><img src="../../../.gitbook/assets/image (591).png" alt=""><figcaption></figcaption></figure>

#### Features:

* **Relevance**: Suggests database tables based on structure, usage history, or schema compatibility.
* **Efficiency**: Reduces manual effort in selecting the right table and minimizes errors.
* **Speed**: Helps users quickly locate the correct data source.

#### **Node Validation**

Node validation ensures that each node in the pipeline is configured correctly before execution.

<figure><img src="../../../.gitbook/assets/image (592).png" alt=""><figcaption></figcaption></figure>

#### Key Features:

* **Configuration Check**: Verifies the setup of the node to ensure it's ready for execution.
* **Error Detection**: Identifies issues like missing columns or invalid data types.
* **Validation Results**: Displays success (✓) or failure (❌) with detailed feedback on the issues.

#### SQL & Preview Panel (Bottom Panel)

The **SQL & Preview** section is essential for users to inspect their pipeline’s SQL queries and preview intermediate data transformations.

SQL Tab:

Displays the SQL query generated by the pipeline for review and modification. This tab helps ensure correctness and transparency in the data transformations.

<figure><img src="../../../.gitbook/assets/image (594).png" alt=""><figcaption></figcaption></figure>

Preview Tab:

Provides a preview of the data that will be processed by the selected node. This feature helps users verify data accuracy and transformation correctness before executing the full pipeline.

<figure><img src="../../../.gitbook/assets/image (593).png" alt=""><figcaption></figcaption></figure>

