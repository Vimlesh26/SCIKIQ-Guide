# SQL Statement Node

**Contents**

* [**Instructions for Using this Page**](sql-statement-node.md#instructions-for-using-this-page)
* [**Overview**](sql-statement-node.md#overview)
* [**Procedure**](sql-statement-node.md#procedure)
* [**Related Topics**](sql-statement-node.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the **SQL Statement** node while creating a pipelin&#x65;**.** It is used to run SQL queries on a connected database within the pipeline. It allows you to **retrieve, insert, update, or delete data** from database tables using SQL commands.

This node helps perform database operations directly within the pipeline workflow.

## Procedure

The procedure to use the **SQL Statement** node involves the steps including [Connect SQL Statement Node to Input Node,](sql-statement-node.md#connect-sql-statement-node-to-input-node) [Configure Database Type and Connection,](sql-statement-node.md#configure-database-type-and-connection) [Configure SQL Statement,](sql-statement-node.md#configure-sql-statement) [Save Pipeline](sql-statement-node.md#save-pipeline), and [Preview Result](sql-statement-node.md#preview-result). The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

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

&#x20;

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

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
