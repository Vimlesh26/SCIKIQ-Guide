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

Creating a **Logical Data Model** involves identifying the data required by an organization and organizing it into **entities, attributes, and relationships**. It begins by understanding the **business requirements and processes** to determine what data is needed and how it is connected. The model is then reviewed to ensure it is **accurate, consistent, complete, and aligned with business needs**. It serves as a **blueprint for designing the physical database**..

***

### Procedure

The procedure of creating a logical data model involves a series of steps. These include **Adding Tables to the Logical Data Model, Customizing and Managing Tables, Defining Relationship, Auto Arranging Layout,** and **Saving LDM**.

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Adding Tables to the Logical Data Model" %}
**Overview**

While creating a table, the first step is to **select the required data source/asset and then choose the appropriate connection**. From the list of available tables, **drag and drop the required tables onto the application canvas**.

This allows you to **visually build and organize the data model**. Each table represents an **entity**, and arranging the tables on the canvas provides a clear visual representation of **what data exists, how it is structured, and how different data elements are related and connected**.

**Procedure**

The below step-by-step instructions help you understand how to add tables to the logical data model:

_**To add the tables**_

1. On the **SCIKIQ left menu**, go to **SCIKIQ CURATE**, and then click **Logical Data Model**.

<figure><img src="../../../.gitbook/assets/image (2704).png" alt=""><figcaption></figcaption></figure>

The **Logical Data Model** page is displayed.

2. On the **Logical Data Model** page:

A. From the **Select Source Type** drop-down box, select either **Datasource** or **Assets**. For example, Datasource.

B. From the **Select Connection** drop-down box, select the required **connection**.

The **Table List** is displayed.

3. From the **Table List,** drag the required **tables** onto to the **right pane (Canvas)**.&#x20;

<figure><img src="../../../.gitbook/assets/image (2705).png" alt=""><figcaption></figcaption></figure>

4. Next, click [**Customizing and Managing Tables**](creating-a-logical-data-model.md#customizing-and-managing-tables)**.**
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

Defining a relationship connects related source and target tables. As part of defining relationships, you need to specify one table as the **source table** and another table as the **target table**. You can repeat this process to define relationships between all relevant tables in the Logical Data Model. For example, one table can be designated as the **source table**, while the other related tables can be defined as **target tables**.&#x20;

While defining each relationship, you can also specify the **relationship type**, choosing from **One-to-One, One-to-Many, Many-to-One, or Many-to-Many**, based on how the records in the two tables are related.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> Defining a relationship connects related source and target tables, while defining the relationship type specifies how their records are associated. This enables the Logical Data Model to represent business relationships accurately and allows related data to be combined and consumed correctly for reporting, analytics, and other downstream use cases.

**Procedure**

1. On the **Logical Data Model** page, first select the required **table**.

The selected table is highlighted with a blue border on its top.

2. Next, on the **Top Menu**, click the **Relationship** button.

<figure><img src="../../../.gitbook/assets/image (2725).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

3. On the **Define Relationship LDM** screen (See the below image):

A. In the **Source** section, select the **Source Table** and **Columns**.

B. In the **Target** section, select the **Target Table** and **Columns**.

C. From the **Relationship** drop-down box, select the **relationship** choosing from **One-to-One, One-to-Many, Many-to-One,** and **Many-to-Many.** See the below table for the description of these relationships:

<table><thead><tr><th width="139.4444580078125" valign="top">Relationship</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top">One-to-One</td><td valign="top">A <strong>One-to-One relationship</strong> means that one record in one table is associated with only one record in another table, and vice versa.</td></tr><tr><td valign="top">One-to-Many</td><td valign="top">A <strong>One-to-Many relationship</strong> means that one record in the first table can be associated with multiple records in the second table, while each record in the second table is associated with one record in the first table.</td></tr><tr><td valign="top">Many-to-One</td><td valign="top">A <strong>Many-to-One relationship</strong> is essentially the reverse direction of a One-to-Many relationship. It means that many records in the first table can be associated with one record in the second table.</td></tr><tr><td valign="top">Many-to-Many</td><td valign="top">A <strong>Many-to-Many relationship</strong> means that multiple records in one table can be associated with multiple records in another table.</td></tr></tbody></table>

D. Once completed, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2722).png" alt=""><figcaption></figcaption></figure>

4. Now, click the other **required table**, and then click the **Relationship** button on the **Top Menu** again.

<figure><img src="../../../.gitbook/assets/image (2723).png" alt=""><figcaption></figcaption></figure>

The **Relationship Properties** screen is displayed.

5. On the **Relationship Properties** screen, click the **Add Relationship** button.

<figure><img src="../../../.gitbook/assets/image (2727).png" alt=""><figcaption></figcaption></figure>

The **Define Relationship LDM** screen is displayed.

6. On the **Define Relationship LDM** screen:

A. Select the **Source Table** and **Columns,** and **Target Table** and **Columns**.

B. From the **Relationship** drop-down box, select the **relationship** choosing from **One-to-One, One-to-Many, Many-to-One,** and **Many-to-Many.**

C. Once completed, click the **Save** button.

7. Select the **other tables**, and apply the same above mentioned procedure.
8. Next, click [**Auto Arranging Layout**](creating-a-logical-data-model.md#auto-arranging-layout)**.**
{% endtab %}

{% tab title="Auto Arranging Layout" %}
**Overview**

**Auto Arrange Tables** helps automatically organize the tables on the Logical Data Model (LDM) canvas in a **clear and structured layout**. Instead of manually moving each table, the system positions the tables and their relationships in an appropriate arrangement.

**Procedure**

1. On the **Top Menu** of **Logical Data Model**, click the **Auto Arrange** button.

<figure><img src="../../../.gitbook/assets/image (2729).png" alt=""><figcaption></figcaption></figure>

The Auto Arrange message box is displayed.

2. On the **Auto Arrange** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2733).png" alt=""><figcaption></figcaption></figure>

The layout is auto arranged.

<figure><img src="../../../.gitbook/assets/image (2732).png" alt=""><figcaption></figcaption></figure>

3. Next, click [**Saving LDM**](creating-a-logical-data-model.md#saving-ldm)**.**
{% endtab %}

{% tab title="Saving LDM" %}
**Overview**

**Saving the LDM** details ensures that the logical data model and its configurations are preserved, allowing you to retain your work, review it, make further changes, and reuse the model without having to recreate it.

**Procedure**

1. On the **Top Menu** right corner, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2734).png" alt=""><figcaption></figcaption></figure>

The **Save LDM** dialogue box is displayed.

2. On the **Save LDM** dialogue box:

A. On the **Add Metadata** tab, specify all the required details, and click the **Next** button.

The **Add Governance** tab is opened.

B. On the **Add Governance** tab, specify the **Business Owner, Technical Owner**, and then click the **Next** button.

The **Review & Submit** tab is opened.

3. On the **Review & Submit** tab, enter name and description for the LDM, and then click the Finish **button**.

<figure><img src="../../../.gitbook/assets/image (2735).png" alt=""><figcaption></figcaption></figure>

The logical data model is created and displayed on the **Business Data Models** page.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Managing Logical Data Models**](managing-logical-data-models.md)
