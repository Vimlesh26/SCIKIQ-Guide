---
icon: page
---

# Managing Logical Data Models

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes the various activities that can be performed as part of **managing Logical Data Models (LDMs)**. These activities include **viewing the details of an LDM and updating it as required** to accommodate changing business or data requirements.

In addition, you can perform various management and maintenance activities, such as **viewing change history and dataset metadata, performing data profiling, rediscovering the underlying data structure, creating assets, viewing and modifying permissions, publishing and scheduling the LDM, viewing refresh history, and deleting an LDM** when it is no longer required.

These options help you **review, maintain, govern, and manage LDMs throughout their lifecycle**.

***

### Procedure

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Viewing an LDM Details" %}
**Overview**

After creating a **Logical Data Model (LDM)**, viewing its details helps you review, validate, and understand the structure of the data model before using it for further data-related activities.&#x20;

It also allows you to verify that all required components are included, the relationships between them are defined correctly, and the model accurately represents the intended business structure.

**Procedure**

The below step-by-step instructions help you understand how to view the details of a logical data model:

_**To view details of an LDM**_

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **View Details** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2753).png" alt=""><figcaption></figcaption></figure>

The logical model details page is displayed.

<figure><img src="../../../.gitbook/assets/image (2754).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Updating an LDM" %}
**Overview**

**Updating an LDM** is necessary whenever the underlying data or business requirements change. It keeps the logical data model accurate, current, and aligned with the organization's business and analytical needs.

**Procedure**

The below step-by-step instructions help you understand how to update an LDM:

_**To update an LDM**_

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Edit** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2755).png" alt=""><figcaption></figcaption></figure>

The **LDM** page is displayed.

3. On the **LDM** page, make the required modifications, and then click the **Save** button.

The LDM is updated.
{% endtab %}

{% tab title="Viewing Change History" %}
**Overview**

**Change history acts like a record of the LDM's evolution.** It helps you answer questions such as **“What was changed?”, “When was it changed?”, and “Who changed it?”** This makes the LDM easier to **track, troubleshoot, review, and govern**.

**Procedure**

The below step-by-step instructions help you understand how to view the change history of an LDM:

_**To view the change history**_

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Change History** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2756).png" alt=""><figcaption></figcaption></figure>

The **Resource Change Log** screen is displayed.

3. On the **Resource Change Log** screen:

A. From the **Date Range** drop-down box, select the required **data range** or select the required **period** choosing from **Last 7 Days,  Last 30 Days,  Last 3 Months,** or  **Last 6 Months** from **Quick Select** section.

B. From the **User** drop-down box, select either **All Users** or the **required user.**

C. From the **Action** drop-down box, select either **All Actions** or the required action choosing from **Update, Restored, Deleted,** or **Restored Version.**

{% hint style="info" %}
Here is the description for the above actions:

* **All Actions:** Selecting this option displays the complete change history, including all types of actions performed on the LDM.
* **Update:**  Selecting this option display changes made to the existing LDM, such as modifying tables, columns, relationships, aliases, or descriptions.
* **Restored:** Selecting this option displays instances where a previously deleted or changed LDM component or version was restored.
* **Deleted:** Selecting this option displays instances where an LDM component or version was deleted.
* **Restored Version:** Selecting this option displays instances where an earlier version of the LDM was restored as the current version.
{% endhint %}

D. Finally, click the **Refresh** button.

<figure><img src="../../../.gitbook/assets/image (2757).png" alt=""><figcaption></figcaption></figure>

The change history is displayed.
{% endtab %}

{% tab title="Viewing and Updating Dataset Metadata" %}
**Overview**

**Dataset Metadata** provides information about the **fields or columns in an LDM**, including their business meaning and technical characteristics.

* **Business Properties:** Include **Business Name, Business Terms, Definition, and Tags** to describe the business context of each field.
* **Technical Properties:** Include **Field Type, Data Classification, Column Length, Minimum Range, Maximum Range, and Is Nullable** to describe its technical characteristics and constraints.

It helps **business and technical users understand and manage the data effectively**. **Viewing** helps verify the metadata, while **updating** keeps it accurate and current.

**Procedure**

The below step-by-step instructions help you understand how to view and update the dataset metadata of an LDM:

_**To view and update dataset metadata**_

{% stepper %}
{% step %}
**Viewing Dataset Metadata**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Dataset Metadata** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

The **Dataset Metadata** page is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2829).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Updating Dataset Metadata**

As part of updating the dataset metadata, you can **define business names, find and replace values, upload excel file**, and **download dataset metadata.** Refer to [**Managing Dataset Metadata**](../../integrations/meta-data-manager/dataset-metadata/#managing-dataset-metadata) for detailed information.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Data Profiling" %}
**Overview**

**Data profiling** after creating an LDM helps to look beyond the logical structure of the model and examine the characteristics and quality of the underlying data.&#x20;

It helps determine whether the data is complete, consistent, accurate, and aligned with the model, and whether any data quality issues need to be addressed before the data is used for further analysis, reporting, or other downstream activities.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Data Profiling** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2760).png" alt=""><figcaption></figcaption></figure>

The Data Profiling page is displayed.

<figure><img src="../../../.gitbook/assets/image (2761).png" alt=""><figcaption></figcaption></figure>

For more information on data profiling, refer to [**Data Profiling**](../data-profiling-1/) pag&#x65;**.**
{% endtab %}

{% tab title="Rediscover" %}
**Overview**

The **Rediscover** option is used to **re-examine the underlying data source and identify the latest available data structures or changes** after the Logical Data Model (LDM) has been created.&#x20;

It helps ensure that the LDM can be reviewed against the current state of the source data and that any relevant changes can be identified.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Rediscover** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2764).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Creating Asset" %}
**Overview**

**Creating assets** as part of managing a Logical Data Model (LDM) helps to create reusable data-related objects or resources from the model so that the modeled data can be used more effectively for downstream business and analytical activities.

As part of creating an asset, you need to specify asset information, metadata, asset name and description. Once done, the asset is created.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Create Asset** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2744).png" alt=""><figcaption></figcaption></figure>

The **Add Asset** dislogue box is displayed.

3. On the **Add Asset** dislogue box:

{% stepper %}
{% step %}
**Specify Asset Information**

A. In the **Asset Information** section, if required, make any changes to the data displayed by default.

B. In the **Resource Approval Roles** section, specify the **Approver, Concurr** and **Recommender,** enter **Asset Path** of asset, and then click the **Next** button.

> <mark style="color:red;">**Note:**</mark> When creating an asset, specifying **Approver, Concurr, Recommender, and Asset Path** helps define the **governance, review workflow, and location** of the asset.
>
> Here is the description:
>
> * **Approver:** Specifies the person or role responsible for **formally approving the asset** before it is published or made available for use.
> * **Concurr:** Specifies the person or role whose **agreement or concurrence is required** as part of the asset review process, typically before final approval.
> * **Recommender:** Specifies the person or role responsible for **reviewing the asset and providing a recommendation** on whether it should be approved or published.
> * **Asset Path:** Specifies the **location or organizational hierarchy where the asset will be stored**, making it easier to organize, locate, access, and manage the asset.

Once the Next button is clicked, the Metadata section is displayed.
{% endstep %}

{% step %}
**Specify Metadata**

1. **Specifying Business Term**

* In the **Business Term** column, specify the **Business Term** for the elements.

> <mark style="color:red;">**Note:**</mark> Specifying a **business term** in the metadata section while creating an asset helps associate the asset with a **standardized business concept or terminology** used within the organization.

Once the **Business Term** is specified, the corresponding Business Definition is automatically  displayed.

2. **Specifying Classification**

* In the **Classification** column, specify the **classification** for each element choosing from **Internal, Confidential, Public,** and **Secret**.

> <mark style="color:red;">**Note:**</mark>  Specifying a **classification** such as **Internal, Confidential, Public, or Secret** for metadata elements such as **Customer, Customer ID, and Email** helps organizations **identify the sensitivity of the information and apply appropriate data governance and access controls**.

3. **Using Find and Replace**&#x20;

If you want to find and replace **Status, Classification,** or **Data Owner** either in all the rows or only in the selected rows, then:

* From the **Find and Replace** drop-down box, select **Status, Classification,** or **Data Owner.**

Once a value is selected, the options corresponding to it appears. For example, if the selected value is Status, then its corresponding options Draft and Submit options are are displayed.

* Select the required option choosing from the displayed options.
* From the **Selection Types**, select either **All Rows** or **Selected Rows.**
* Click the **Apply** button.

Once everything is done, click the **Next** button.

The **Description** section is displayed.
{% endstep %}

{% step %}
**Specify Asset Name and Description**

1. In the **Asset Name** field, enter a **name** for the **asset**.&#x20;
2. In the **Description** field, enter the **asset description**.
3. Click the **Submit** button.
{% endstep %}
{% endstepper %}

<figure><img src="../../../.gitbook/assets/image (2745).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Viewing and Changing Permissions" %}
**Overview**

The **Permission** feature on the **Business Data Models** page allows you to **view the existing permission settings and modify them as required**. For example, you can change the permission from **Private** to **Public** or **Shared** to control how the business data model can be accessed by other users.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Permission** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2746).png" alt=""><figcaption></figcaption></figure>

The **Resource Permission** screen is displayed with **Private** permission selected by default.

3. On the **Resource Permission** screen:

A. If you wish to change the permission to **Public**, then select the **Public** option.

B. If you wish to **share it to a group:**

* Select the **Shared** option, and click the **Add More** button.
* Next, select the required **Group**, specify the **Role** choosing from **Contributor** or **Viewer**, and then click the **Save** button.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * If required, you can delete a row containing **Group** and **Role** fields by clicking the **Delete** ![](<../../../.gitbook/assets/image (2748).png>) button corresponding to it.
> * Based on the requirement, you can share the permission to **multiple groups** by clicking the **Add More** button and specifying the required group and role.

<figure><img src="../../../.gitbook/assets/image (2747).png" alt=""><figcaption></figcaption></figure>

Once saved, the permission is changed as per the change made.
{% endtab %}

{% tab title="Publishing LDM" %}
**Overview**

The **Publish** option makes a finalized **Logical Data Model (LDM)** available to **authorized users and downstream activities**, indicating that the model has been reviewed and is ready for use. Publishing helps ensure that users work with the **approved and intended version of the data model** when performing activities such as data analysis, reporting, data preparation, or creating data assets.

**Procedure**

As part of publishing the logical data model, you need to configure **Basic Details** (Token name, Valid Date, Whitelist IP, and Permission Grou&#x70;**) , Request Parameters, Sorting Order,** and **Output Format .** Once done, the token is generated.

The below step-by-step instructions help you understand how to publish a logical data model:

_**To publish a logical data model:**_

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Publish** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

The **Publish API** dialogue box is displayed.

3. On the **Publish API** dialogue box:

A. **Enter Basic Information**

* Expand the **Basic Information** panel.

The **Basic Information**, **Request Parameter,** **Order by**, and **Output**  field panels are displayed.

* In the **Basic Information** fields section, specify [<mark style="color:$primary;">**Token Name**</mark>](#user-content-fn-1)[^1]**,** [<mark style="color:$primary;">**Valid Date**</mark>](#user-content-fn-2)[^2]**,** [<mark style="color:$primary;">**Whitelist IP**</mark>](#user-content-fn-3)[^3]**,** and [<mark style="color:$primary;">**Permission Group**</mark>](#user-content-fn-4)[^4].&#x20;

**B. Configure Request Parameter Information**

* In the **Request Parameter** fields section, specify the [<mark style="color:$primary;">**Key**</mark>](#user-content-fn-5)[^5], [<mark style="color:$primary;">**Value**</mark>](#user-content-fn-6)[^6], and **Operator**.

> <mark style="color:red;">**Note**</mark>:&#x20;
>
> * The **Request Parameter** specifies the **inputs or conditions** that are passed with the API request to control what data is retrieved.
> * If you want more **Request Parameter** fields, click the **Add** ![](<../../../.gitbook/assets/image (5).png>)button on the panel.

**C. Define Sorting**

* Expand the **Order By** Panel and then click the **Add** ![](<../../../.gitbook/assets/image (5).png>) button on the panel.

The Column Name and Order fields are displayed.

* From the **Column Name** drop-down box, select the required **column**.

> <mark style="color:red;">**Note**</mark>: Selecting the **column** specifies the **data field based on which the returned records should be sorted.**

* From the **Order** drop-down box, select **ASC** or **DSC**.

> <mark style="color:red;">**Note**</mark>:
>
> * **ASC (Ascending):** Sorts the records from **lowest to highest** for numbers, **A to Z** for text, or **earliest to latest** for dates.
> * **DESC (Descending):** Sorts the records from **highest to lowest** for numbers, **Z to A** for text, or **latest to earliest** for dates.

**D. Select Output Format**&#x20;

* From the **Output Format** options, select **Flat** or **Nested**.

> <mark style="color:red;">**Note**</mark>:
>
> * **Flat:** The **Flat** option returns data in a simple, single-level structure.&#x20;
> * **Nested:** The **Nested** option returns data in a hierarchical structure, grouping **related information together.**

* Finally, click the **Generate Token** button.

<figure><img src="../../../.gitbook/assets/image (2828).png" alt=""><figcaption></figcaption></figure>

The **Token generated successfully** message is displayed.

<figure><img src="../../../.gitbook/assets/image (2826).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Adhoc Refreshing" %}
**Overview**

**Ad hoc refreshing** allows you to **manually refresh a Logical Data Model (LDM) whenever required**, without waiting for its scheduled refresh. This is useful when you need the LDM to reflect the latest available information immediately.

**Procedure**

As part of performing adhoc refreshing, you can manually refresh a Logical Data Model either immediately or schedule it for a later date and time. The below step-by-step instructions help you understand how to perform adhoc refreshing.

**To perform adhoc refreshing:**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Adhoc Refresh** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2824).png" alt=""><figcaption></figcaption></figure>

The **Dataset Schedule Refresh** dialogue box is displayed with **Run Now** and **Run Later** options.

3. **If you want to run immediately:**

A. On the **Dataset Schedule Refresh** dialogue box, select the **Run Now** option, and enter relevant **comments**.

B. Click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The **Loading dataset in background** message is displayed.

4. **If you want to run later:**

A. On the **Dataset Schedule Refresh** dialogue box, select the **Run Later** option.

B. Specify the **Start Date, Start Time**, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

The **Schedule created successfully** message box is displayed.
{% endtab %}

{% tab title="Scheduling LDM" %}
**Overview**

The **Schedule Refresh** option helps automate the **refresh of a Logical Data Model (LDM) at a specified time or frequency**. This is useful when the underlying data or related information changes regularly and the LDM needs to be refreshed to reflect the latest available information.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Schedule Refresh** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2738).png" alt=""><figcaption></figcaption></figure>

The **Dataset Schedule Refresh** dialogue box is displayed.

2. On the **Dataset Schedule Refresh** dialogue box, specify the **Schedule Name, Description, Start Date, Start Time,** and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2739).png" alt=""><figcaption></figcaption></figure>

The **Schedule created successfully** message box is displayed.
{% endtab %}

{% tab title="Refreshing History " %}
**Overview**

The **Refresh History** option of a **Logical Data Model (LDM)** helps users **view and track the history of refresh operations performed on the model**. It provides visibility into when the LDM was refreshed and the outcome of each refresh, helping users monitor and troubleshoot the refresh process.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Refresh History** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2740).png" alt=""><figcaption></figcaption></figure>

The **Dataset Refresh History screen** is displayed.

3. On the **Dataset Refresh History** screen, view the **refresh history.**
4. If you wish to refresh the history, click the **Refresh** button.

<figure><img src="../../../.gitbook/assets/image (2741).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Deleting LDM" %}
**Overview**

The **Delete** option on the **Business Data Models** page helps users **remove a Logical Data Model (LDM) that is no longer required, relevant, or intended for further maintenance or use**. Deleting unnecessary or obsolete LDMs helps keep the data modeling environment **organized and easier to manage**, while also reducing the possibility of users inadvertently using an outdated or irrelevant data model.

**Procedure**

1. On the **SCIKIQ Left Menu**, click **Business Data Models** under **SCIKIQ Curate.**

The **Business Data Models** page is displayed.

2. On the **Business Data Models** page, click the **Delete** icon corresponding to the required logical data model.

<figure><img src="../../../.gitbook/assets/image (2742).png" alt=""><figcaption></figcaption></figure>

The **Delete** message is displayed.

2. On the **Delete** message, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (2743).png" alt=""><figcaption></figcaption></figure>

The LDM is deleted.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating a Logical Data Model**](creating-a-logical-data-model.md)

[^1]: Token Name identifies the access token

[^2]: Valid Date controls how long the token remains valid

[^3]: Whitelist IP controls where the API can be accessed from

[^4]: Permission Group controls which group is authorized to access or perform

[^5]: Specifies the **name of the request parameter** that the API expects

[^6]: Specifies the value to be passed for the corresponding parameter
