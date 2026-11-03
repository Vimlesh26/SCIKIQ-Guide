---
icon: list-radio
---

# Delta Pipelines List

### Introduction

This guide provides step-by-step instructions on how to interact with different features of the Delta Pipelines platform. It covers how to control column visibility, filter table data, run tasks, view logs, and manage permissions for sharing resources.

### 1. **Controlling Column Visibility**

Delta Pipelines allows you to toggle the visibility of columns to streamline your view. This can be helpful when you need to focus on specific pieces of data.

#### Step-by-Step Process:

1. **Locate the Column Visibility Button**\
   On the Delta Pipelines dashboard, find the button that controls column visibility. Typically, this will be at the top of your data table or in a settings icon.

<figure><img src="../../../../.gitbook/assets/image (1195).png" alt=""><figcaption></figcaption></figure>

1. **Click on the Visibility Button**\
   When you click this button, a menu will appear showing a list of all available columns in the table.



1. **Toggle Columns**
   * To **show** a hidden column, simply check the box next to the column name.
   * To **hide** a visible column, uncheck the box next to that column name.
2. **Apply Changes**\
   After making the necessary adjustments, the columns will either appear or disappear from the table immediately based on your selections.

***

### 2. **Using the Table Search Functionality**

The search bar in Delta Pipelines is designed to help you quickly filter through your data tables. It can be used to search by any text in specific columns, such as the **Name** or **Model** of the pipeline.

#### Step-by-Step Process:

1. **Locate the Search Bar**\
   The search bar is typically positioned at the top-right corner of the data table. It may also be positioned just above the header row.
2. **Enter Search Query**\
   Click inside the search box and type a keyword or phrase that you wish to search for. For example:
   * If you want to find pipelines related to a specific model, type the model's name in the search bar.
   * To search by the pipeline’s name, type the name of the pipeline.
3. **Filter Results**\
   As you type, the table will dynamically update to show only the rows that match your search criteria.
4. **Clear Search**\
   To clear the search and return to the full list of pipelines, click the **clear** button (usually an ‘X’ icon) in the search bar.



<figure><img src="../../../../.gitbook/assets/image (1196).png" alt=""><figcaption></figcaption></figure>

***

### 3. **Managing Node and Notify Actions**

Delta Pipelines enables users to perform various actions on tasks through the **Node** and **Notify** features, such as **Re-discover**, **Delete**, and **Run** tasks.

#### Step-by-Step Process:

1. **Identify Action Buttons**\
   In the data table, you will find action buttons in the **Action** column. These buttons control specific task operations for each pipeline. Common actions include:
   * **Re-discover**
   * **Delete**
   * **Run**
   * **Logs**
2. **Re-discover Pipeline**
   * Click the **Re-discover** button to refresh the pipeline and re-sync it with the system.

<figure><img src="../../../../.gitbook/assets/image (1197).png" alt=""><figcaption></figcaption></figure>

1. **Delete Pipeline**
   * Click the **Delete** button to permanently delete the selected pipeline. A confirmation pop-up will appear to ensure that you want to proceed with deletion.&#x20;

<figure><img src="../../../../.gitbook/assets/image (1201).png" alt=""><figcaption></figcaption></figure>

* Confirm by clicking **Yes**.

<figure><img src="../../../../.gitbook/assets/image (1199).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../../.gitbook/assets/image (1200).png" alt=""><figcaption></figcaption></figure>

1. **Run Pipeline**
   * Click the **Run** button to trigger the execution of the pipeline. Depending on the pipeline's task, this could initiate data processing or other automated actions.

<figure><img src="../../../../.gitbook/assets/image (1202).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../../.gitbook/assets/image (1203).png" alt=""><figcaption></figcaption></figure>

1.  **View Logs**

    * Clicking on **Logs** opens the **Logs Viewer** window.

    <figure><img src="../../../../.gitbook/assets/image (1204).png" alt=""><figcaption></figcaption></figure>

    * &#x20;Here, you can see detailed information about the pipeline execution, including error messages, runtime, and task progress.

***

### 4. **Viewing and Understanding Task Logs**

The **Logs Viewer** is essential for debugging and tracking the status of your pipelines. It provides a detailed log for each pipeline, which includes task names, status, timestamps, and more.

#### Step-by-Step Process:

1. **Open the Logs Viewer**\
   To open the logs for a specific pipeline, locate the **Logs** button in the Action column of the data table and click on it.

<figure><img src="../../../../.gitbook/assets/image (1205).png" alt=""><figcaption></figcaption></figure>

1.  **Analyze the Log Details**\
    The Logs Viewer will display the following key information:

    * **Task Name**: The name of the task being logged.
    * **Status**: The current status of the task (e.g., Running, Completed, Failed).
    * **Start Time**: The date and time when the task started.
    * **End Time**: The date and time when the task finished.
    * **Message**: Any messages related to the task execution (e.g., errors, warnings, or successful completion).
    * **SQL Query**: If the task involves SQL, this will show the SQL query executed.
    * **Rows**: The number of rows processed or affected during the task.

    Example Log:

    | **Task Name**        | **Status** | **Start Time**      | **End Time**        | **Message**      | **SQL Query**            | **Rows** |
    | -------------------- | ---------- | ------------------- | ------------------- | ---------------- | ------------------------ | -------- |
    | JOIN NODE and NOTIFY | Running    | 2025-04-29 12:16:11 | 2025-04-29 12:16:17 | ETL Task Running | `SELECT * FROM pipeline` | 500      |
2. **Use Logs for Troubleshooting**\
   Logs can help identify errors, performance issues, or problems during the pipeline execution. If there is an error, the message will often contain troubleshooting details.

***

### 5. **Sharing and Managing Resource Permissions**

You can share a pipeline with other users or groups and control the level of access (e.g., Contributor, Viewer). This is critical for collaborative environments.



<figure><img src="../../../../.gitbook/assets/image (1206).png" alt=""><figcaption></figcaption></figure>

#### Step-by-Step Process:

1. **Locate the Share Button**\
   Find the **Share** button in the **Action** column of the data table. It may be represented by a share icon or simply labeled **Share**.

<figure><img src="../../../../.gitbook/assets/image (1207).png" alt=""><figcaption></figcaption></figure>

1. **Click the Share Button**\
   After clicking **Share**, a pop-up window or dropdown will appear. Here you can define who the pipeline will be shared with.
2. **Select Share Options**\
   You will have the option to share the pipeline as:
   * **Public**: The pipeline is accessible to everyone in the system.
   * **Private**: Only the owner or creator of the pipeline has access.
   * **Shared**: The pipeline can be shared with specific users or groups (e.g., Contributor or Viewer).

<figure><img src="../../../../.gitbook/assets/image (1210).png" alt=""><figcaption></figcaption></figure>

1. **Choose the Group to Share With**\
   Select the group you want to share the pipeline with, such as **Contributor**, **Viewer**, or other roles that are available in your system.

<figure><img src="../../../../.gitbook/assets/image (1209).png" alt=""><figcaption></figcaption></figure>

1. **Confirm Sharing Settings**\
   After selecting the appropriate group and permissions, confirm your selection by clicking **Share** or **Save**.

<figure><img src="../../../../.gitbook/assets/image (1211).png" alt=""><figcaption></figcaption></figure>

1. **Adjust Permissions**\
   If you need to adjust permissions later, you can revisit the share button and modify the sharing settings as needed.
