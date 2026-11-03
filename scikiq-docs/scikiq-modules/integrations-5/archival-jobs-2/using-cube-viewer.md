---
icon: page
---

# Using Cube Viewer

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Cube Viewer** enables to explore and analyze data associated with a configured cube. It consists of three tabs:&#x20;

* **Pivot**: This tab supports interactive analysis by allowing users to rearrange dimensions and measures.&#x20;
* **Source Data** and **Archived Data:** These tabs provide access to the underlying source data and archived data, respectively.

This page provides step-by-step instructions for **analyzing cube data, viewing source and archived data,** and **saving and downloading data.**

***

### Procedure

Click the below tabs to view the procedure.

{% tabs %}
{% tab title="Analyzing Cube Data" %}
**Overview**

The **Pivot** tab is typically used to **analyze cube data interactively by arranging dimensions and measures in different ways**.

Using the **Pivot** tab, you may:

* Select dimensions to display as rows or columns.
* Apply filters to focus on specific data.
* Change the arrangement of the data to view it from different perspectives.

**Procedure**

As part of **analyzing cube data**, you can **view the** **required account details**, **use filters,** and **configure display settings** to customize the data view.

The below step-by-step instructions describe the procedure:&#x20;

{% stepper %}
{% step %}
**Viewing account details**

1. On the **SCIKIQ left menu**, expand **Archival Jobs** under **SCIKIQ Archival**, and then click **Cube Viewer**.

<figure><img src="../../../.gitbook/assets/image (2913).png" alt=""><figcaption></figcaption></figure>

The **Cube Viewer** page is displayed with the **Pivot** tab selected by default.

2. On the **Pivot** tab, from the **Select a Cube** drop-down box, select the required **cube**.&#x20;

<figure><img src="../../../.gitbook/assets/image (2914).png" alt=""><figcaption></figcaption></figure>

The cube data is displayed.

3. On the **Cube Viewer Left Pane**, select the **required account** (For example, ACRV - Unbilled Revenue), and then click the **Apply** button.

> <mark style="color:red;">**Note:**</mark> Alternatively, you can do one of the below to view the details of the required account.
>
> * On the top of **Cube Viewer Right Pane**, in the **Search Accounts** field, enter the **required account**.
> * On the **Right Pane**, locate the **required account**, and then expand it.&#x20;

<figure><img src="../../../.gitbook/assets/image (2915).png" alt=""><figcaption></figcaption></figure>

4. After locating the required account, click the **Run** button on the top of **Cube Viewer** page. &#x20;

<figure><img src="../../../.gitbook/assets/image (2916).png" alt=""><figcaption></figcaption></figure>

The required information is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2917).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Viewing Account Details for a Specific Period**

1. On the **Left Pane**, select the **Period**.

The **Select - Period** dialogue box is displayed.

2. On the **Select - Period** dialogue box, select the **required period**, and then click the **Apply** button.

> <mark style="color:red;">**Note:**</mark> If you wish to copy the selected member along with all its child members in the cube hierarchy, click the **Copy with Children** button.

<figure><img src="../../../.gitbook/assets/image (2918).png" alt=""><figcaption></figcaption></figure>

3. Now, click the **Run** button on the top of **Cube Viewer** page.

The account details for the specific period is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (2919).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Using Filters**

You can also view the cube data using filters such as **Scenario, Year,** **View, Entity, Value, ICP, Flow,** and **Segment**. You can apply any one of these filters or use multiple filters together to narrow down the data.

See the below table for the description of these filters:

| Filter       | Description                                                                                          |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| **Scenario** | Filters data based on the selected business scenario, such as Actual, Budget, or Forecast.           |
| **Year**     | Filters data based on the selected calendar or fiscal year.                                          |
| **View**     | Filters or displays data based on the selected view or perspective configured in the cube.           |
| **Entity**   | Filters data based on the selected entity, such as a company, business unit, or organizational unit. |
| **Value**    | Filters data based on the selected value or measure category available in the cube.                  |
| **ICP**      | Filters data based on the selected Intercompany Partner associated with the transaction or balance.  |
| **Flow**     | Filters data based on the selected movement or change in an account balance during a period.         |
| **Segment**  | Filters data based on the selected business or organizational segment.                               |

The below information describes how to use **Scenario, Year, and View.**&#x20;

> <mark style="color:red;">**Note:**</mark> The procedure for applying the other filters including **Value, ICP, Flow,** and **Segment** is similar to that for applying the **Scenario, Year,** and **View** filters described below.

1. **Using Scenario**

* On the **Cube Viewer Left Pane**, from the **Filters** groups, select the **Scenario**.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Scenario represents the business context or version of the data, such as Actual, PMActual-Actual @ Prior Month Rates, or PYActual-Actual @ Prior Year Rates.
> * You can select **one, multiple**, or **all** the scenarios depending on your requirement.

The **Select-Scenario** dialogue box is displayed.

* From the **Select-Scenario** dialogue box, select the **required scenario.**
* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2939).png" alt=""><figcaption></figcaption></figure>

2. **Using Year**

* From the **Filters** groups, select the **Year**.

The **Select-Year** dialogue box is displayed.

* From the **Select-Year** dialogue box, select the required year.

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the years.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2940).png" alt=""><figcaption></figcaption></figure>

3. **Using View**

* From the **Filters** groups, select **View**.

The **Select-View** dialogue box is displayed.

* From the **Select-View** dialogue box, select the required option.

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the options.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2921).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Configuring Display Settings**

The **Display Settings** in Cube Viewer allow to customize how cube data is presented, making the data easier to read, interpret, and analyze. See the below table for the purpose of  of these display settings.

<figure><img src="../../../.gitbook/assets/image (2922).png" alt=""><figcaption></figcaption></figure>

| Display Setting         | Purpose                                                                                                                                                                                                          |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hide Empty Rows**     | Hides rows that do not contain any data, making the view more concise and easier to read.                                                                                                                        |
| **Show System Members** | Displays system-generated or technical members that may otherwise be hidden from the view. This can help when users need to inspect the complete cube hierarchy.                                                 |
| **Heatmap**             | Uses color-based formatting to visually highlight variations or patterns in values, helping users identify higher, lower, or significant values quickly.                                                         |
| **Show Descriptions**   | Displays the descriptive name or explanation of a member in addition to, or instead of, its code or identifier, depending on the cube configuration.                                                             |
| **Year Starts**         | Specifies the starting month of the year used by the cube, particularly where a fiscal year differs from the calendar year. This can affect how periods and year-based calculations, such as YTD, are displayed. |
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing Source Data" %}
**Overview**

The **Source Data** tab in Cube Viewer enables to view and examine the **original data associated with the cube** before or as it was processed for archival and cube ingestion.

It helps to:

* **Verify the source records** associated with the cube.
* Compare source data with the **cube or archived data**.
* Investigate **missing, inconsistent, or unexpected data**.
* Understand the underlying data used to populate the cube.

**Procedure**

As part of the procedure, you can **view the complete source data** and also **filter the data based on specific criteria**.

The below step-by-step instructions describe the procedure:

{% stepper %}
{% step %}
**Viewing** **complete source data**

1. Navigate to **Cube Viewer** page. (**SCIKIQ left menu>>Archival Jobs>>** **Cube Viewer).**

The **Cube Viewer** page is displayed.

2. On the **Cube Viewer** page, click the **Source Data** tab.

<figure><img src="../../../.gitbook/assets/image (2923).png" alt=""><figcaption></figcaption></figure>

The Source Data is displayed. See the below image.&#x20;

<figure><img src="../../../.gitbook/assets/image (2924).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Viewing source data using filters**

You can also view the source data using filters such as **Scenario, Year,** **View, Entity, Value, ICP, Flow,** and **Segment**. You can apply any one of these filters or use multiple filters together to narrow down the data.

See the below table for the description of these filters:

| Filter       | Description                                                                                          |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| **Scenario** | Filters data based on the selected business scenario, such as Actual, Budget, or Forecast.           |
| **Year**     | Filters data based on the selected calendar or fiscal year.                                          |
| **View**     | Filters or displays data based on the selected view or perspective configured in the cube.           |
| **Entity**   | Filters data based on the selected entity, such as a company, business unit, or organizational unit. |
| **Value**    | Filters data based on the selected value or measure category available in the cube.                  |
| **ICP**      | Filters data based on the selected Intercompany Partner associated with the transaction or balance.  |
| **Flow**     | Filters data based on the selected movement or change in an account balance during a period.         |
| **Segment**  | Filters data based on the selected business or organizational segment.                               |

The below information describes how to use **Scenario, Year, and Period.**&#x20;

> <mark style="color:red;">**Note:**</mark> The procedure for applying the other filters including **Value, ICP, Flow,** and **Segment** filters is similar to that for applying the **Scenario, Year,** and **Period** filters described below.

1. **Using Scenario**

> <mark style="color:red;">**Note:**</mark> Scenario represents the business context or version of the data, such as Actual, PM Actual, or PY Actual.

* On the **Cube Viewer Left Pane**, from the **Filters** groups, select the **Scenario**.

The **Select-Scenario** dialogue box is displayed.

* From the **Select-Scenario** dialogue box, select the **required scenario.**

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the scenarios.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2926).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the options.

2. **Using Year**

* From the **Filters** groups, select the **Year**.

The **Select-Year** dialogue box is displayed.

* From the **Select-Year** dialogue box, select the required year.

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the years.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2927).png" alt=""><figcaption></figcaption></figure>

3. **Using Period**

* From the **Filters** group, select **Period**.

The **Select-Period** dialogue box is displayed.

* On the **Select-Period** dialogue box, select the required **year**.

> <mark style="color:red;">**Note:**</mark> You can select one, multiple, or all the years depending on your requirement.

<figure><img src="../../../.gitbook/assets/image (2928).png" alt=""><figcaption></figcaption></figure>

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.
* Finally, click the **Run** button on the top of the page.

The required source data based on the applied filter is displayed.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing Archived Data" %}
**Overview**

The **Archived Data** tab is used to **view the data that has been archived and is represented through the cube**. It helps users access and analyze information that has been moved from the operational environment to archival storage.

It can be useful for:

* Searching or filtering archived records.
* Viewing historical information.
* Analyzing archived data through the cube structure.
* Comparing archived information with the corresponding source data.

**Procedure**

As part of the procedure, you can **view the complete archived data and filter the data based on specific criteria**.

The below step-by-step instructions describe the procedure:

{% stepper %}
{% step %}
**Viewing** **complete archived data**

1. Navigate to **Cube Viewer** page. (**SCIKIQ left menu>>Archival Jobs>>** **Cube Viewer),**

The **Cube Viewer** page is displayed.

2. On the **Cube Viewer** page, click the **Archived Data** tab.

<figure><img src="../../../.gitbook/assets/image (2929).png" alt=""><figcaption></figcaption></figure>

The Archived Data is displayed.

<figure><img src="../../../.gitbook/assets/image (2924).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Viewing archived data using filters**

You can also view the archived data using filters such as **Scenario, Year,** **View, Entity, Value, ICP, Flow,** and **Segment**. You can apply any one of these filters or use multiple filters together to narrow down the data.

See the below table for the description of these filters:

| Filter       | Description                                                                                          |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| **Scenario** | Filters data based on the selected business scenario, such as Actual, Budget, or Forecast.           |
| **Year**     | Filters data based on the selected calendar or fiscal year.                                          |
| **View**     | Filters or displays data based on the selected view or perspective configured in the cube.           |
| **Entity**   | Filters data based on the selected entity, such as a company, business unit, or organizational unit. |
| **Value**    | Filters data based on the selected value or measure category available in the cube.                  |
| **ICP**      | Filters data based on the selected Intercompany Partner associated with the transaction or balance.  |
| **Flow**     | Filters data based on the selected movement or change in an account balance during a period.         |
| **Segment**  | Filters data based on the selected business or organizational segment.                               |

The below information describes how to use **Scenario, Year, and Period.**&#x20;

> <mark style="color:red;">**Note:**</mark> The procedure for applying the other filters including **Value, ICP, Flow,** and **Segment** filters is similar to that for applying the **Scenario, Year,** and **Period** filters described below.

1. **Using Scenario**

> <mark style="color:red;">**Note:**</mark> Scenario represents the business context or version of the data, such as Actual, PM Actual, or PY Actual.

* On the **Cube Viewer Left Pane**, from the **Filters** groups, select the **Scenario**.

The **Select-Scenario** dialogue box is displayed.

* From the **Select-Scenario** dialogue box, select the **required scenario.**

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the scenarios.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2926).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the options.

2. **Using Year**

* From the **Filters** groups, select the **Year**.

The **Select-Year** dialogue box is displayed.

* From the **Select-Year** dialogue box, select the required year.

> <mark style="color:red;">**Note:**</mark> You can select **one, multiple**, or **all** the years.

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2927).png" alt=""><figcaption></figcaption></figure>

3. **Using Period**

* From the **Filters** group, select **Period**.

The **Select-Period** dialogue box is displayed.

* On the **Select-Period** dialogue box, select the required **year**.

> <mark style="color:red;">**Note:**</mark> You can select one, multiple, or all the years depending on your requirement.

<figure><img src="../../../.gitbook/assets/image (2928).png" alt=""><figcaption></figcaption></figure>

* Click the **Copy with Children** button if you wish to include the selected parent member and its child members when applying or copying a filter selection.&#x20;
* Click the **Apply** button.
* Finally, click the **Run** button on the top of the page.

The required archived data based on the applied filter is displayed.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Saving Views" %}
**Overview**

The **Save Views** option in Cube Viewer allows to **save a customized view of cube data for future use**. A saved view can retain the user's selected filters, dimensions, measures, and display settings, eliminating the need to configure the same view repeatedly.

It helps to:

* Quickly return to a **frequently used data view**.
* Preserve specific **filter and display configurations**.
* Maintain consistent views for **regular analysis and reporting**.
* Reduce the time required to recreate commonly used data views.

**Procedure**

1. Navigate to **Cube Viewer** page. (**SCIKIQ left menu>>Archival Jobs>>** **Cube Viewer).**

The **Cube Viewer** page is displayed.

2. After analyzing or viewing the required source or archived data, click the **Save** button at the top of the **Cube Viewer** page to save the current view.

<figure><img src="../../../.gitbook/assets/image (2930).png" alt=""><figcaption></figcaption></figure>

The **Save View** dialogue box is displayed.

3. On the **Save View** dialogue box, enter a **name, description** for the current view, and then click the **Save View** button.

<figure><img src="../../../.gitbook/assets/image (2931).png" alt=""><figcaption></figcaption></figure>

The saved view is displayed with the **entered name** at the top of the **Cube Viewer** page.

<figure><img src="../../../.gitbook/assets/image (2932).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * You can save **multiple views** for future use.
> * To delete a saved view, click the **Delete** ![](<../../../.gitbook/assets/image (2934).png>) icon next to the saved view.
> * To edit a saved review, click the **Edit** ![](<../../../.gitbook/assets/image (2933).png>) icon next to the saved review.
{% endtab %}

{% tab title="Downloading Data" %}
**Overview**

The **Export** option in Cube Viewer enables users to **download the displayed source or archived data for offline use**. It is useful when there is a need to retain a copy of the data, perform further analysis, share the data with others, or use it for reporting.

The downloaded data generally reflects the **current view and applied filters**.

**Procedure**

1. Navigate to **Cube Viewer** page. (**SCIKIQ left menu>>Archival Jobs>>** **Cube Viewer),**

The **Cube Viewer** page is displayed.

2. On the **Cube Viewer** page, click the **Export** button on the top of the page.

<figure><img src="../../../.gitbook/assets/image (2935).png" alt=""><figcaption></figcaption></figure>

The data is downloaded in CSV format in the local system. See the below image.

<figure><img src="../../../.gitbook/assets/image (2936).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Validating Data**](validating-data.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
