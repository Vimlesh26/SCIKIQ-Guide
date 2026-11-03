---
icon: circle-share-nodes
---

# Other  Common Nodes

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page explains how to use the other common nodes while creating a pipeline. These other common nodes include **Join, Variable, SQL Statement, Notify, ML Model, Group,** and **Unstructured**.

### Using Other Common Nodes

{% tabs %}
{% tab title="Join" %}
**Overview**

The **Join Node** is used to combine datasets from two or more sources into a single unified view based on specified join conditions. It enables you to enrich and correlate data by joining tables using common fields or defined conditions.

**Types of Join Nodes**

<table><thead><tr><th width="179">Type</th><th>Purpose</th></tr></thead><tbody><tr><td>Inner Join</td><td>Returns records that have matching values in both tables.</td></tr><tr><td>Left Join</td><td>Returns all records from the left table and matching records from the right table. If there's no match, NULLs are returned from the right.</td></tr><tr><td>Right Join</td><td>Returns all records from the right table and matching records from the left. If there's no match, NULLs are returned from the left.</td></tr><tr><td>Outer Join</td><td>Returns all records when there is a match in either left or right table.</td></tr></tbody></table>

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

<details>

<summary><strong>Add Variable Node</strong> </summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. On the **Right Pane**, add an **input node**. For example, Database input node.
3. Now, from the **Top Toolbar** drag the **Variable node** on to the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (462).png" alt=""><figcaption><p>Adding Variable Node</p></figcaption></figure>

The Define Variable section is displayed on the left pane.&#x20;

</details>

<details>

<summary><strong>Define Variable Name and Type</strong></summary>

**Purpose:**

The **purpose** of defining the Variable Name and Type when connecting the Variable node with a source node is to identify the stored data and specify the type of data that the variable will hold for reuse within the pipeline.

The **Variable Name** uniquely identifies the variable within the pipeline so that it can be easily referenced by other nodes.

The **Variable Type** specifies **what kind of data the variable will store**, such as a single value, a column, or an entire table.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, specify a **name** for the variable.
2. From the **Variable Type** drop-down box, select the **variable type** choosing from **Single value, Single Column,** or **Table.** For example, Single Column.

<figure><img src="../../../../.gitbook/assets/S (463).png" alt=""><figcaption><p>Defining Variable Name and Type</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* The **Single Value** option is used to store **one constant or scalar value** that can be reused in different parts of the pipeline.
* The **Single Column** option is used to store **values from a specific column of a dataset** so that they can be referenced or used in other nodes.
* The **Entire Table** option is used to store **a complete dataset or table** so that it can be reused by other nodes in the pipeline.
{% endhint %}

</details>

<details>

<summary><strong>Connect Variable Node to Source Node</strong></summary>

**Purpose:**

The **purpose** of connecting the Variable Node to a Source Node is to capture data from the source and store it in a variable so that it can be reused in other parts of the pipeline.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

* On the **Right Pane**, connect the **Variable Node** to **Source Node**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (464).png" alt=""><figcaption><p>Connecting Variable Node</p></figcaption></figure>

Once connected, the defined name is displayed on the Variable node.

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

The purpose of saving the pipeline while connecting the **Variable node** with input nodes is to store the configured pipeline structure and settings so that the variable configuration and node connections are preserved and can be executed later.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (465).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Overview:**

The purpose of previewing the result while connecting the **Variable node** with input nodes is to verify that the variable configuration is correct and that the data retrieved from the input dataset is captured as expected before running the entire pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Variable** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Variable** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (466).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The result is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (467).png" alt=""><figcaption><p>Preview Result</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Variable" %}
**Overview**

The **Variable** node is used to store reusable data that can be referenced across different stages of a pipeline. It enables to capture and reuse values such as constants, selected columns, or entire tables, making the pipeline more flexible and easier to manage.

The **Variable Node** allows storing and reuse the following types of data:

* **A single value** (for example, a constant or parameter used in transformations)
* **A single column** from a dataset
* **An entire table or dataset** that can be referenced in subsequent nodes

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

<details>

<summary><strong>Add Variable Node</strong> </summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. On the **Right Pane**, add an **input node**. For example, Database input node.
3. Now, from the **Top Toolbar** drag the **Variable node** on to the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (462).png" alt=""><figcaption><p>Adding Variable Node</p></figcaption></figure>

The Define Variable section is displayed on the left pane.&#x20;

</details>

<details>

<summary><strong>Define Variable Name and Type</strong></summary>

**Purpose:**

The **purpose** of defining the Variable Name and Type when connecting the Variable node with a source node is to identify the stored data and specify the type of data that the variable will hold for reuse within the pipeline.

The **Variable Name** uniquely identifies the variable within the pipeline so that it can be easily referenced by other nodes.

The **Variable Type** specifies **what kind of data the variable will store**, such as a single value, a column, or an entire table.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, specify a **name** for the variable.
2. From the **Variable Type** drop-down box, select the **variable type** choosing from **Single value, Single Column,** or **Table.** For example, Single Column.

<figure><img src="../../../../.gitbook/assets/S (463).png" alt=""><figcaption><p>Defining Variable Name and Type</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* The **Single Value** option is used to store **one constant or scalar value** that can be reused in different parts of the pipeline.
* The **Single Column** option is used to store **values from a specific column of a dataset** so that they can be referenced or used in other nodes.
* The **Entire Table** option is used to store **a complete dataset or table** so that it can be reused by other nodes in the pipeline.
{% endhint %}

</details>

<details>

<summary><strong>Connect Variable Node to Source Node</strong></summary>

**Purpose:**

The **purpose** of connecting the Variable Node to a Source Node is to capture data from the source and store it in a variable so that it can be reused in other parts of the pipeline.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

* On the **Right Pane**, connect the **Variable Node** to **Source Node**.&#x20;

<figure><img src="../../../../.gitbook/assets/S (464).png" alt=""><figcaption><p>Connecting Variable Node</p></figcaption></figure>

Once connected, the defined name is displayed on the Variable node.

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

The purpose of saving the pipeline while connecting the **Variable node** with input nodes is to store the configured pipeline structure and settings so that the variable configuration and node connections are preserved and can be executed later.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (465).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Overview:**

The purpose of previewing the result while connecting the **Variable node** with input nodes is to verify that the variable configuration is correct and that the data retrieved from the input dataset is captured as expected before running the entire pipeline.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Variable** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Variable** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (466).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The result is displayed on the Preview tab. See the example image below:

<figure><img src="../../../../.gitbook/assets/S (467).png" alt=""><figcaption><p>Preview Result</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="SQL Statement" %}
**Overview**

The **SQL Statement** node is used to run SQL queries on a connected database within the pipeline. It allows you to **retrieve, insert, update, or delete data** from database tables using SQL commands.

This node helps perform database operations directly within the pipeline workflow.

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

<details>

<summary><strong>Connect SQL Statement Node to Input Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. On the **Right Pane**, add an **input node**. For example, Database input node.
3. Now, from the **Top Toolbar** drag the **SQL Statement node** on to the **Main Workspace,** and connect it to the input nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (299).png" alt=""><figcaption><p>Connecting SQL Statement Node</p></figcaption></figure>

The Database Type and SQL Statement sections are displayed on the left pane.&#x20;

</details>

<details>

<summary><strong>Configure</strong> <strong>Database Type and Connection</strong></summary>

**Purpose:**

The purpose of configuring a **Database Type** (such as **Data Source** or **Asset**) is to define **how the database will be used within the pipeline**.&#x20;

**Procedure:**

As part of configuring, selecting the **Datasource** option connects to an external database whereas the **Assets** option use pre-configured datasets stored within SCIKIQ. Once the database type is selected, the tables pertaining to the selected data source or asset are available in the Schema Properties section on the Left Pane.

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the **Right Pane,** select the **SQL Statement Node.**
2. On the **Left Pane**, from the **Data Type** drop-down box, select either **Datasource** or **Assets.**

&#x20;3\. From the **Select Datasource** drop-down box, select a pre-configured **connection.**

<figure><img src="../../../../.gitbook/assets/S (300).png" alt=""><figcaption><p>Selecting Database Type and Connection</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure SQL Statement</strong></summary>

**Purpose:**

The The purpose of configuring the **SQL statement** while connecting the **SQL Statement Node** is to **define the exact database operation that the pipeline should perform**.

It specifies **what data needs to be retrieved or modified in the database** when the pipeline is executed.

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, in the **SQL Statement** section, enter the **SQL Statement**.&#x20;
2. Scroll down to the **SQL Statement** section, and then click the **OK** button.

<figure><img src="../../../../.gitbook/assets/S (301).png" alt=""><figcaption><p>Configuring SQL Statement</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Purpose**

The **purpose** of saving the pipeline while connecting the SQL Statement Node is to store the pipeline configuration and node settings so that the SQL query and node connections are preserved.

Saving ensures that the pipeline structure and the configured SQL statement are properly recorded and available for execution later.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (302).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Overview:**

The purpose of **previewing the result while connecting the SQL Statement Node** is to **verify that the SQL query is correctly configured and that it returns the expected data from the database** before running the entire pipeline.

Previewing helps ensure that the SQL statement works properly and retrieves or modifies the intended data.

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **SQL Statement** node.

<figure><img src="../../../../.gitbook/assets/S (303).png" alt=""><figcaption><p>Edit Icon</p></figcaption></figure>

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **SQL Statement** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (304).png" alt=""><figcaption><p>Preview Icon</p></figcaption></figure>

The Pipeline Preview message box is displayed.&#x20;

3. On the **Pipeline Preview** message box, click the **OK** button.

<figure><img src="../../../../.gitbook/assets/S (305).png" alt=""><figcaption><p>Pipeline Preview Message Box</p></figcaption></figure>

4. From the **Top Toolbar**, click Output, and then drag an **output node** from the **Output Node Palette**, and on to the **Main Workspace**.
5. Click the **Preview** icon on the top of **Output Node** and validate data post-update.

</details>
{% endtab %}

{% tab title="Notify" %}
**Overview**

The **Notify** is used to send automated alerts or messages when specific conditions in the data pipeline are met. This helps users monitor the pipeline, detect errors, and receive updates about important events during pipeline execution.

The **Notify Node** sends notifications based on conditions. The following are the different types of notifications:

* Email
* Webhook
* API Write

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Notify Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **Notify node** on to the **Main Workspace.**
3. Connect the **Notify node** to the node whose output triggers the notificatio&#x6E;**.**

<figure><img src="../../../../.gitbook/assets/S (306).png" alt=""><figcaption><p>Connecting Notify Node</p></figcaption></figure>

Once connected, the Notify section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure Notify Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the **Left Pane,** click the **Add** ![](<../../../../.gitbook/assets/image (2491).png>) .

The Notify expandable panel is displayed.

2. Expand the **Notify** **expandable panel**, and then from the **Notify drop-down box**, select the **notification channel** choosing from **Webhook, API Write,** or **Email.** For example, Email.

{% hint style="info" %}
**Tip:** The **notification channels** specify how the notification will be sent when the **Notify node** is triggered in the pipeline.

Here is the description of these channels:

* **Webhook:** This channel sends a notification to another application through an **HTTP request**.
* **API Write:** This channel  sends notification data to another system using an **API call**.
* **Email:** This channel sends a **notification email** to specified recipients.
{% endhint %}

&#x20;3\. From the **Email Config** drop-down box, select the **email config**. For example, Gmail SMTP.

4. From the **Email Template** drop-down box, select the **required template.**

{% hint style="info" %}
**Tip:** If required, you can create a new template by clicking the **Add Template** ![](<../../../../.gitbook/assets/image (2492).png>) link.
{% endhint %}

4. Click the **Email Config** tab, and then specify the To Email.
5. In the Subject field, change the subject if required.
6. Enable **Data Repeat, Attached Table,** and **From Column** based on the requirement. Refer to the below tip for the description of these.

{% hint style="info" %}
**Tip:**&#x20;

* **Data Repeat:** Enable this option repeats the email content for each record in the dataset.
* **Attached Table:** Enable this option adds the dataset as a table in the email.
* **From Column:** Enable this option uses email addresses from a data column as recipients.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (307).png" alt=""><figcaption><p>Configuring Notify Node Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (308).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Notify** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Notify** nod&#x65;**.**
3. Click the **Preview** icon on the top of **Notify** node.&#x20;

Once triggered, the notification is sent to the configured email address. See the example image below.

<figure><img src="../../../../.gitbook/assets/S (309).png" alt=""><figcaption><p>Notification Email</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="ML Model" %}
**Overview**

The **ML Model Node** integrates machine learning models into ETL pipelines to perform predictions, classifications, and other intelligent data operations. It enables the pipeline to process data using trained machine learning models and generate analytical outputs.

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

<details>

<summary><strong>Add and Connect ML Model Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **ML Model node** on to the **Main Workspace.**
3. Connect the **ML Model node** to the input nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (310).png" alt=""><figcaption><p>Connecting ML Model Node</p></figcaption></figure>

Once connected, the ML Model section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure ML Model Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the **Left Pane,** from the **Select Model** drop-down box, select the **required ML model.**

The **ML Model Columns** section is displayed.

2. In the **ML Model Columns** section, select the **Target Columns** and **Source Columns**.
3. Click the **Test** button.

<figure><img src="../../../../.gitbook/assets/S (311).png" alt=""><figcaption><p>Configure ML Model Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (312).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **ML Model** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **ML Model** nod&#x65;**.**

The preview is displayed.

</details>
{% endtab %}

{% tab title="Group" %}
**Overview**

The **Group node** aggregates data based on specified columns. It is also used to group records and apply aggregation functions to generate summarized results for analysis and reporting.

**Procedure**

The expandable panels below provide guided assistance for each step in the procedure.&#x20;

<details>

<summary><strong>Add Group Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **Group node** on to the **Main Workspace.**

<figure><img src="../../../../.gitbook/assets/S (313).png" alt=""><figcaption><p>Adding Group Node</p></figcaption></figure>

</details>

<details>

<summary><strong>Add and Connect Input Nodes</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. From the **Top Toolbar**, drag the required nodes, and place them inside the **Group Node**. For example, input nodes.
2. Inside the **Group Node**, connect **Input nodes.**

<figure><img src="../../../../.gitbook/assets/S (314).png" alt=""><figcaption><p>Adding and Connect  Input Nodes</p></figcaption></figure>



</details>

<details>

<summary><strong>Configure Group Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the top of **Group Node**, click the **Edit** icon.

<figure><img src="../../../../.gitbook/assets/S (315).png" alt="" width="514"><figcaption><p>Group Node - Edit Icon</p></figcaption></figure>

The Group section is displayed on the left pane.

2. On the left pane, from the **Select Group Type** drop-down box, select either **Flink Window Function** or **Other.**

{% hint style="info" %}
**Tip:**&#x20;

* Selecting the **Flink Window Function** group type groups streaming data within defined **time windows** using Apache Flink window functions.
* Selecting the  **Other** group type allows the use of **custom or advanced grouping configurations** that are not covered by the standard grouping or window functions
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (316).png" alt=""><figcaption><p>Selecting Group Type</p></figcaption></figure>

</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (317).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Group** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** Setup icon on the top right side of **Group** nod&#x65;**.**

<figure><img src="../../../../.gitbook/assets/S (318).png" alt=""><figcaption><p>Preview Setup</p></figcaption></figure>

The preview is displayed.

</details>
{% endtab %}
{% endtabs %}

## Related Topics

* [**Configuring Input Nodes**](configuring-input-nodes.md)
* [**Applying Transform Nodes**](applying-transform-nodes.md)
* [**Using Output Nodes**](../using-output-nodes/)
