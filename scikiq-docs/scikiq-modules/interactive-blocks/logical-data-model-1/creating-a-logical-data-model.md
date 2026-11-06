---
icon: page
---

# Creating a Logical Data Model

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to create a logical data model. Creating a **Logical Data Model** helps organize business data into a clear and structured format. It provides a systematic way to identify entities, define their attributes, and establish relationships between them.

***

### Procedure

The process of creating a logical data model involves a series of steps. These steps include **Adding Tables to the Logical Data Model, Customizing and Managing Tables, Defining Relationship, Auto Arranging Layout,** and **Saving LDM**.

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Adding Tables to the Logical Data Model" %}
**Overview**

**Adding tables** helps break down business information into smaller, organized structures. Each table represents a business entity, its columns define the required attributes, and relationships connect the tables to represent how business data is associated.

**Procedure**

While creating a table, the first step is to **select the required data source/asset and then choose the appropriate connection**. From the list of available tables, **drag and drop the required tables onto the application canvas**.

The below step-by-step instructions help you understand how to add tables to the logical data model:

_**To add the tables**_

1. On the **SCIKIQ left menu**, go to **SCIKIQ CURATE**, and then click **Logical Data Model**.

<figure><img src="../../../.gitbook/assets/image (2704).png" alt=""><figcaption></figcaption></figure>

The **Logical Data Model** page is displayed.

2. On the **Logical Data Model** page:

A. From the **Select Source Type** drop-down box, select either **Datasource** or **Assets**. For example, Datasource.

B. From the **Source Category** drop-down box, select the required  category choosing from **RDBMS, Big Query, File Storage, Glue,** or **File Upload (CSV/Excel).**

C. From the **Select Connection** drop-down box, select the required **connection**.

The **Table List** is displayed.

3. From the **Table List,** drag the required **tables** onto to the **right pane (Canvas)**.&#x20;

<figure><img src="../../../.gitbook/assets/image (3222).png" alt=""><figcaption></figcaption></figure>

3. Next, click [**Customizing and Managing Tables**](creating-a-logical-data-model.md#customizing-and-managing-tables)**.**
{% endtab %}

{% tab title="Customizing and Managing Tables" %}
**Overview**

After adding the tables, you can **customize and enhance** them by adding an **alias name** to the table and its columns. You can also add **business descriptions, filters, and calculation fields** to individual columns as required. In addition, you can **preview the table details** to review and verify the available data and configurations.

> <mark style="color:red;">**Note:**</mark> Customizing and managing tables is optional. Depending on the requirements, you can customize and manage the tables as needed.

**Procedure**

The below step-by-step instructions help you understand how customize and enhance tables.&#x20;

_**To customize and enhance tables**_

{% stepper %}
{% step %}
**Adding Alias Name to a Table**

**Overview**

**Adding an alias name** to a table or column helps make the data model easier to understand and use, especially when the original technical names are unclear, abbreviated, or difficult for business users to interpret.

**Procedure**

1. On the **required table**, click the **Edit** icon.

<figure><img src="../../../.gitbook/assets/image (2706).png" alt=""><figcaption></figcaption></figure>

The **Edit** screen is displayed.

2. On the **Edit** screen, click the **Edit** icon under **table title**.

<figure><img src="../../../.gitbook/assets/image (2708).png" alt=""><figcaption></figcaption></figure>

The **Alias Name** field is activated.

3. In the **Alias Name** field, enter the required **alias name**.&#x20;

<figure><img src="../../../.gitbook/assets/image (2710).png" alt=""><figcaption></figcaption></figure>

The alias name is added to the table title.
{% endstep %}

{% step %}
**Adding Alias/Business Name and Business Description to a Table Column**

**Overview**

Adding an **alias name and business description** to a column helps make the data model **more understandable and meaningful**, especially for business users who may not be familiar with technical database terminology.

**Procedure**

1. On the **required table**, click the **Edit** icon.

The Edit screen is displayed.

2. On the **Edit** screen, enter the **Alias/Business Name** and **Business Description** corresponding to the required table.&#x20;

The **Alias/Business Name** and **Business Description**  are added. See the below example image.

<figure><img src="../../../.gitbook/assets/image (2711).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Adding Filters**

**Overview**

Adding **filters while creating a Logical Data Model (LDM)** helps you define **which records should be included in the logical view of the data**. Instead of exposing all the records from the underlying physical tables, you can apply conditions to present only the relevant data.

**Procedure**

1. On the **required table**, click the **Edit** icon.

The Edit screen is displayed.

2. On the **Edit** screen, click the **Filter** icon on the top.

<figure><img src="../../../.gitbook/assets/image (2717).png" alt=""><figcaption></figcaption></figure>

The **Add/Edit Filter** screen is displayed.

2. On the **Add/Edit Filter** screen, specify the required **column, operator, value**, and then click the **Save** button.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **To add filters to more columns**, click the **Add Filter** button.
> * **To add a filter group**, click the **Add Filter Group** button, and then add the required columns to the group.
>
>

<figure><img src="../../../.gitbook/assets/image (2718).png" alt=""><figcaption></figcaption></figure>

The filter is added.
{% endstep %}

{% step %}
**Adding Calculated Field**

**Overview**

**Adding a** **calculated field** while creating a Logical Data Model (LDM) helps you derive meaningful business values from existing fields without physically changing the underlying source data.

**Procedure**

1. On the **required table**, click the **Edit** icon.

The **Edit** screen is displayed.

2. On the **Edit** screen, click the **Add Calculated Field** icon on the top.

<figure><img src="../../../.gitbook/assets/image (2713).png" alt=""><figcaption></figcaption></figure>

The **Calculated Field** screen is displayed.

3. On the **Calculated Field** screen, enter **field name, expression**, and then click the **Save** button.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can enable the **Save for global use** option on the **Calculated Field** screen. This allows the calculated field to be saved as a reusable, standardized calculation so that it can be used in other relevant contexts without recreating the formula each time.

<figure><img src="../../../.gitbook/assets/image (2715).png" alt=""><figcaption></figcaption></figure>

The calculated field is created.
{% endstep %}

{% step %}
**Previewing Table Data**

**Overview**

**Preview Table Data** helps you see the actual records and values stored in a table before using the table in a Logical Data Model (LDM).  It gives you visibility into the table’s structure and data so that you can build the model correctly.

**Procedure**

1. On the **LDM** page, click the **Preview** **Data** icon on the **required table.**

<figure><img src="../../../.gitbook/assets/image (2719).png" alt=""><figcaption></figcaption></figure>

The **Data Preview** screen is displayed.

2. If you want to preview more data, increase the **record limit** on the **Data Preview** screen, and then click the **Fetch** button

<figure><img src="../../../.gitbook/assets/image (2736).png" alt=""><figcaption></figcaption></figure>

3. Next, click [**Defining Relationship**](creating-a-logical-data-model.md#defining-relationship)**.**
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Defining Relationship" %}
**Overview**

**Defining relationships** helps establish how different tables are connected and how data is associated across them. It provides a clear understanding of the connections between business entities and ensures that the data model accurately represents business requirements.

**Procedure**

As part of defining a relationship between tables, you need to select one table as the source table and another as the target table. You need to repeat this process to establish relationships between all relevant tables in the Logical Data Model.

While defining a relationship between tables, you can also specify it as either **Active** or **Inactive**. Additionally, you can use the **Cross-Filter Direction** feature to specify the data flow between the tables.

{% hint style="info" %}
#### Tip: Description of  **Active Relationship, Inactive Relationship, and Cross-Filter Direction**

**1. Active Relationship:** Charts use active relationships by default to connect related tables and retrieve data.

**2. Inactive Relationship:** Use an inactive relationship when the same table needs to serve different roles or when multiple relationship paths exist between the same tables.

**When to use an Inactive Relationship:**

The following examples illustrate when an inactive relationship is useful:

* **One Table Serving Two Roles:** A Sales table may contain both Order Date and Ship Date, with both columns connected to the Date table. In this case, keep the Order Date relationship active and the Ship Date relationship inactive.
* **Multiple Paths Between Tables:** Sales data may be connected to a Store table through two different paths: directly through the store where the sale occurred and indirectly through the salesperson's home store. In this case, keep the direct relationship active and the alternative relationship inactive.

**3. Cross-Filter Direction:**

* Single: Filters flow from the One side to the Many side.
* Both: Filters flow in both directions between the related tables.
{% endhint %}

For each relationship, you need to specify the **relationship type** based on how records in the two tables are associated. The available relationship types are **One-to-One, One-to-Many, Many-to-One, and Many-to-Many**.

Expand the below table to view step-by-step instructions for each of the relationship type.

<details>

<summary><strong>Defining</strong> <strong>One-to-One Relationship Type</strong></summary>

**Overview**

Select the **One-to-One** option if you want one record in one table is associated with only one record in another table, and vice versa.&#x20;

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * One-to-One relationship always filter both ways.
> * When **One-to-One** is selected as the relationship type, the **Both** option is automatically selected in the **Cross Filter** drop-down list, located below the Relationship drop-down list.
> * You can also make when one table plays two roles for another by using the **Inactive** option.

**Procedure**

1. On the **Logical Data Model** page, first select the required **table**.

The selected table is highlighted with a blue border on its top.

2. Next, on the **Top Menu**, click the **Relationship** button.

<figure><img src="../../../.gitbook/assets/image (3223).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

3. On the **Define Relationship LDM** screen (See the below image):

A. In the **Source** section, select the **Source Table** and **Columns**.

B. In the **Target** section, select the **Target Table** and **Columns**.

C. From the **Relationship** drop-down box, select **One-to-One.**&#x20;

D. Once completed, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3199).png" alt=""><figcaption></figcaption></figure>

The source and target tables are connected. See the below image.

<figure><img src="../../../.gitbook/assets/image (3200).png" alt=""><figcaption></figcaption></figure>

4. Once connected, click the **Relationship** button again.

The **Relations Properties** screen is displayed with the **Status** option displayed as Active by default.

5. I**f you want to make when one table plays two roles for another, or when two paths lead between the same tables**, then disable the **Status** option.

<figure><img src="../../../.gitbook/assets/image (3201).png" alt=""><figcaption></figcaption></figure>

The relationship is marked as **Inactive** and represented by **dotted arrows** between the tables.

<figure><img src="../../../.gitbook/assets/image (3202).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Defining</strong> <strong>One-to-Many Relationship Type</strong></summary>

**Overview**

Select the **One-to-Many** option if you want one record in the first table is associated with multiple records in the second table and each record in the second table is associated with one record in the first table.&#x20;

> <mark style="color:red;">**Note:**</mark> If you want to filter both ways, then select the **Both** option from the **Cross-Filter** drop-down box, located below the Relationship drop-down list.

**Procedure**

1. On the **Top Menu** of **Logical Data Model** page, click the **Relationship** button.

The **Relationship Properties** screen is displayed.

2. On the **Relationship Properties** screen, click the Add Relationship button.

<figure><img src="../../../.gitbook/assets/image (3203).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

3. On the **Define Relationship LDM** screen (See the below image):

A. In the **Source** section, select the **Source Table** and **Columns**.

B. In the **Target** section, select the **Target Table** and **Columns**.

C. From the **Relationship** drop-down box, select **One-to-Many**&#x20;

D. From the **Cross-Filter Direction** drop-down box, select either **Single** or **Both**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **Single**: Selecting the Single option allows the Source table to filter the Target table.
> * **Both:** Selecting the Both option allows the Source and Target tables to filter each other in both directions.

E. Once completed, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3199).png" alt=""><figcaption></figcaption></figure>

The source and target tables are connected. See the below image.

<figure><img src="../../../.gitbook/assets/image (3204).png" alt=""><figcaption></figcaption></figure>

4. I**f you want to make when one table plays two roles for another, or when two paths lead between the same tables**,  then:

A. Click the **Relationship** button again.

The **Relations Properties** screen is displayed with the **Status** option displayed as **Active** by default.

B. On the the **Relations Properties** screen, disable the **Status** option.

<figure><img src="../../../.gitbook/assets/image (3205).png" alt=""><figcaption></figcaption></figure>

The relationship is marked as **Inactive** and represented by **dotted arrows** between the tables.

<figure><img src="../../../.gitbook/assets/image (3206).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Defining Many-to-One Relationship Type</strong></summary>

**Overview**

Select the **One-to-Many** option if you want one record in the first table is associated with multiple records in the second table and each record in the second table is associated with one record in the first table.&#x20;

Select the **Many-to-One relationship** if you want many records in the first table can be associated with one record in the second table.

> <mark style="color:red;">**Note:**</mark> If you want to filter both ways, then select the **Both** option from the **Cross-Filter** drop-down box, located below the Relationship drop-down list.

**Procedure**

1. On the **Relationship Properties** screen, click the **Add Relationship** button.

<figure><img src="../../../.gitbook/assets/image (3207).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

3. On the **Define Relationship LDM** screen (See the below image):

A. In the **Source** section, select the **Source Table** and **Columns**.

B. In the **Target** section, select the **Target Table** and **Columns**.

C. From the **Relationship** drop-down box, select **One-to-Many**&#x20;

D. From the **Cross-Filter Direction** drop-down box, select either **Single** or **Both**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **Single**: Selecting the Single option allows the Source table to filter the Target table.
> * **Both:** Selecting the Both option allows the Source and Target tables to filter each other in both directions.

E. Once completed, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3208).png" alt=""><figcaption></figcaption></figure>

The source and target tables are connected. See the below image.

<figure><img src="../../../.gitbook/assets/image (3209).png" alt=""><figcaption></figcaption></figure>

4. I**f you want to make when one table plays two roles for another, or when two paths lead between the same tables**,  then:

A. Click the **Relationship** button again.

The **Relations Properties** screen is displayed with the **Status** option displayed as **Active** by default.

B. On the the **Relations Properties** screen, disable the **Status** option.

<figure><img src="../../../.gitbook/assets/image (3210).png" alt=""><figcaption></figcaption></figure>

The relationship is marked as **Inactive** and represented by **dotted arrows** between the tables.

<figure><img src="../../../.gitbook/assets/image (3211).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Defining Many-to-Many Relationship Type</strong></summary>

**Overview**

Select the **Many-to-Many** option if you want multiple records in one table can be associated with multiple records in another table.

> <mark style="color:red;">**Note:**</mark>
>
> * Many-to-Many relationship always filter both ways.
> * When **Many-to-Many** is selected as the relationship type, the **Both** option is automatically selected in the **Cross Filter** drop-down list, located below the Relationship drop-down list.

**Procedure**

1. On the **Relationship Properties** screen, click the **Add Relationship** button.

<figure><img src="../../../.gitbook/assets/image (3212).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

3. On the **Define Relationship LDM** screen (See the below image):

A. In the **Source** section, select the **Source Table** and **Columns**.

B. In the **Target** section, select the **Target Table** and **Columns**.

C. From the **Relationship** drop-down box, select **Many-to-Many.**&#x20;

D. From the **Cross-Filter Direction** drop-down box, select either **Single** or **Both**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **Single**: Selecting the Single option allows the Source table to filter the Target table.
> * **Both:** Selecting the Both option allows the Source and Target tables to filter each other in both directions.

E. Once completed, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3213).png" alt=""><figcaption></figcaption></figure>

The source and target tables are connected. See the below image.

<figure><img src="../../../.gitbook/assets/image (3214).png" alt=""><figcaption></figcaption></figure>

4. I**f you want to make when one table plays two roles for another, or when two paths lead between the same tables**,  then:

A. Click the **Relationship** button again.

The **Relations Properties** screen is displayed with the **Status** option displayed as **Active** by default.

B. On the the **Relations Properties** screen, disable the **Status** option.

<figure><img src="../../../.gitbook/assets/image (3215).png" alt=""><figcaption></figcaption></figure>

The relationship is marked as **Inactive** and represented by **dotted arrows** between the tables.

<figure><img src="../../../.gitbook/assets/image (3216).png" alt=""><figcaption></figcaption></figure>



</details>
{% endtab %}

{% tab title="Auto Arranging Layout" %}
**Overview**

**Auto Arrange Tables** helps automatically organize the tables on the Logical Data Model (LDM) canvas in a **clear and structured layout**. Instead of manually moving each table, the system positions the tables and their relationships in an appropriate arrangement.

**Procedure**

1. On the **Top Menu** of **Logical Data Model**, click the **Auto Arrange** button.

<figure><img src="../../../.gitbook/assets/image (3217).png" alt=""><figcaption></figcaption></figure>

The Auto Arrange message box is displayed.

2. On the **Auto Arrange** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (3218).png" alt=""><figcaption></figcaption></figure>

The layout is auto arranged.

<figure><img src="../../../.gitbook/assets/image (3219).png" alt=""><figcaption></figcaption></figure>

3. Next, click [**Saving LDM**](creating-a-logical-data-model.md#saving-ldm)**.**
{% endtab %}

{% tab title="Saving LDM" %}
**Overview**

**Saving a Logical Data Model (LDM)** details ensures that the logical data model and its configurations are preserved, allowing you to retain your work, review it, make further changes, and reuse the model without having to recreate it.

**Procedure**

The process of saving a Logical Data Model (LDM) involves three main steps: **Adding Metadata, Adding Governance Details, and Reviewing and Submitting** the model.

Follow the steps below to complete the saving process:

_**To save a LDM**_

{% stepper %}
{% step %}
**Adding Metadata**

1. On the **Top Menu** right corner, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3220).png" alt=""><figcaption></figcaption></figure>

The **Save LDM** dialogue box displayed.

2. On the **Save LDM** dialogue box:

A. in the **Add Metadata** tab, specify all the required details.

> <mark style="color:red;">**Note:**</mark> If required, you can modify the **Business Name** as required.

B. Click the **Next** button.

The **Add Governance** tab is opened.
{% endstep %}

{% step %}
**Adding Governance Details**

* On the **Add Governance** tab, specify the **Business Owner, Technical Owner**, and then click the **Next** button.

The **Review & Submit** tab is opened.
{% endstep %}

{% step %}
**Reviewing and Submitting the Model**

* On the **Review & Submit** tab, enter name and description for the LDM, and then click the Finish **button**.

<figure><img src="../../../.gitbook/assets/image (2735).png" alt=""><figcaption></figcaption></figure>

The logical data model is created and displayed on the **Business Data Models** page.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

### Related Topics

* [**Managing Logical Data Models**](managing-logical-data-models.md)
