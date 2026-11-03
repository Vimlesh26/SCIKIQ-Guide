# Using Put API Output Node

This page explains how to use the **Put API Output node** with an input node. The **Put API Output node** can be connected to an **input node** when the pipeline needs to **send incoming or processed data to an external or internal system through a REST API using the PUT method**. It is typically used when the pipeline must update resources or push data to another application or service.

This node supports sending **JSON data through HTTP PUT requests**, with capabilities for **dynamic field mapping, authentication, and support for multiple payload formats**.

**Key Concepts:**

<details>

<summary><strong>How Put API Output node works with an input node</strong></summary>

* The **input node** retrieves data from the configured source (such as a database, file, API, or event stream).
* The data flows through the pipeline and may optionally pass through **transform nodes** if any modifications or formatting are required.
* The **Put API Output Node** formats the incoming data according to the API request structure.
* The node then sends the data as a **PUT request** to the configured API endpoint.

In simple terms, the input node supplies the data and the Put API node sends that data to another system through an API call.

</details>

<details>

<summary><strong>Applicable input nodes</strong></summary>

The Put API Output Node can be connected to input nodes that produce **structured datasets**.

**Applicable input nodes include:**

* **Database Input**
* **File Input**
* **API Input**
* **Kafka Topic (Event Input)**

</details>

<details>

<summary><strong>Applicable Transform nodes (Optional)</strong></summary>

Transform nodes can be used between the input node and the Put API node when the data must be prepared before sending it to the API.

Applicable transform nodes include:

* Mapping / Data Transform
* Filter
* Join
* Aggregation
* EDA Transform

</details>

<details>

<summary><strong>Non-applicable nodes</strong></summary>

The **Put API Output Node** cannot be connected directly to nodes that **do not produce data records**.

**Non-applicable nodes include:**

* **API Schema Node**
* **Execution Settings**
* **Parameters**
* Any **utility or control nodes** that do not output datasets

</details>

Connecting the **Put API Output Node** to an **input node** involves a sequence of steps. The table below provides a brief overview of each step in the process.

<table><thead><tr><th width="221">Step</th><th valign="top">Description</th></tr></thead><tbody><tr><td><a href="using-put-api-output-node.md#connect-put-api-output-node-to-input-node-transform-node">Connect Put API Output Node to Input Node/Transform Node</a></td><td valign="top"><p>As part of this step, you will drag the <strong>Put API Output node</strong> from the  <a data-footnote-ref href="#user-content-fn-1"><mark style="color:blue;"><strong>Output Node Palette</strong></mark></a> and then place it on the <strong>Main Workspace</strong>. Once done, you can connect both the <strong>Input or Transform</strong> and  <strong>Put API Output node</strong> nodes. </p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Connecting <strong>Transform</strong> node is optional.</p></td></tr><tr><td><a href="using-put-api-output-node.md#select-output-type-and-api-connection">Select Output Type and API Connection</a></td><td valign="top"><p>Subsequent to connecting the Put API Output Node to the <strong>Input or Transform</strong> node, you need to Select <strong>Output Type</strong> and <strong>API Connection.</strong>  </p><p></p><p>Selecting the <strong>Output Type</strong> defines the <strong>format or structure of the data</strong> that will be sent in the API request. Whereas Selecting the API connection specifies the <strong>API endpoint and authentication details</strong> required to send the request. </p><p></p></td></tr><tr><td><a href="using-put-api-output-node.md#configure-conditions">Configure Conditions</a> </td><td valign="top">Setting a <strong>condition</strong> ensures that the API call is triggered only for records that satisfy the specified criteria. This helps filter the data and send only the necessary records to the API, reducing unnecessary requests.</td></tr><tr><td><a href="using-put-api-output-node.md#map-fields">Map Fields</a></td><td valign="top"><strong>Mapping</strong> specifies how fields from the pipeline dataset are linked to the fields in the API request payload. It ensures that the correct input columns are included and properly structured in the API request.</td></tr><tr><td><a href="using-put-api-output-node.md#advanced-configurations">Advanced Configurations</a></td><td valign="top">In the advanced configuration step, you will verify or update the <strong>API endpoint</strong> according to the API being invoked. Also, you can add any required <strong>HTTP headers</strong> based on the API specifications. Additionally, you can configure the <strong>Response Settings</strong> by selecting the appropriate option such as <strong>Request Payload</strong>, <strong>Request Header</strong>, <strong>Previous Data</strong>, or <strong>Multiple Response</strong>.</td></tr><tr><td><a href="using-put-api-output-node.md#save-etl-job">Save ETL Job</a></td><td valign="top">After selecting the columns, you will save the <strong>ETL job</strong> to confirm the pipeline setup. This ensures that the <strong>Write</strong> <strong>No SQL output</strong> node is configured correctly and can be used effectively during execution. Once saved, the pipeline is displayed on the <strong>Data Pipelines</strong> page.</td></tr><tr><td><a href="using-put-api-output-node.md#preview-response">Preview Response</a></td><td valign="top">Viewing the <strong>response preview</strong> helps confirm that the API call is functioning as expected and that the returned data is correct. It also provides an opportunity to verify the API setup before running the pipeline.</td></tr></tbody></table>

***

## Procedure

The expandable panels below provide guided assistance for each step in the procedure. Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Connect Put API Output Node to Input Node/Transform Node</strong></summary>

**Purpose:**

The purpose of connecting a **Put API Output Node** to an **Input Node** is to send the data retrieved by the input node to an external or internal system through an HTTP PUT API request. This enables the pipeline to update or transmit data to another application or service via an API endpoint.

**Procedure:**

As part of connecting the **Put API Output Node** with the input node, you need to first drag it from the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-1)[^1] on to the **Mainwork space**, and then connect it with the input node.

> <mark style="color:red;">**Note:**</mark> Based on requirement, you can add the necessary transform node in between **input node** and **Write to NoSQL node.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Top Toolbar**, click the **Output Nodes** menu item.

The [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-1)[^1] is dispalette is displayed.

2. From the [<mark style="color:blue;">**Output Node Palette**</mark>](#user-content-fn-1)[^1]<mark style="color:blue;">**,**</mark> drag the **Put API Output Node** on to the **Main Workspace**, and then connect it to the input node.&#x20;

<figure><img src="../../../../.gitbook/assets/S (449).png" alt=""><figcaption><p>Connetinging Put API Node to Input Node</p></figcaption></figure>

Once the **Put API Output Node** is connected with the input node, the Put API section is displayed on the left pane.

</details>

<details>

<summary><strong>Select Output Type and API Connection</strong></summary>

**Purpose:**

* **Output Type** – Selecting the output type defines the **format or structure of the data** that will be sent in the API request. It ensures that the data from the input node is properly formatted before being transmitted to the API endpoint.
* **API Connection** – Selecting the API connection specifies the **API endpoint and authentication details** required to send the request. It establishes the connection between the pipeline and the target system where the data will be delivered.

**Procedure:**

As part of selecting the output type, you can choose from either Webhook or API Write. Once selected, the Select drop-down box is displayed. From this Select drop-down box, you can select the API connection.

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions:**

1. On the **Left Pane**, in the **Put API** section, click **Add**.

<figure><img src="../../../../.gitbook/assets/S (450).png" alt="" width="505"><figcaption><p>Add Link</p></figcaption></figure>

The Put API Collapsible Panel is displayed.

2. Expand the **Put API Collapsible Panel**, and then select the **Output Type** choosing from **Webhook** or **API Write**. For example, API Write.

{% hint style="info" %}
**Tip:** You can choose the **API Type** as **Webhook** for simple POST or PUT API requests, or **API Write** for advanced API requests that require headers, tokens, or additional configurations.
{% endhint %}

The Select drop-down box is displayed.

3. From the **Select** drop-down box, select an **API Connection**.

<figure><img src="../../../../.gitbook/assets/S (451).png" alt=""><figcaption><p>Selecting Output Type and API Connection</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Conditions</strong> </summary>

**Purpose:**

Configuring a **condition** allows the pipeline to send data through the API only when it meets defined criteria. This ensures that only relevant records are transmitted, avoiding unnecessary requests and improving efficiency.

**Procedure:**

The below step-by-step instructions describe the procedure:&#x20;

1. On the **Left Pane,** in the **Put API** section, click the **Add/Edit Condition** button.

The Add/Edit Filter dialogue box is displayed.

2. On the **Add/Edit Filter** dialogue box, **configure the condition** as shown in the below example image, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (452).png" alt=""><figcaption><p>Configuring Condition</p></figcaption></figure>

</details>

<details>

<summary><strong>Map Fields</strong></summary>

**Purpose**

The purpose of **mapping** is to define how data fields from the pipeline are assigned to the API request payload. It allows you to control which columns from the input dataset are sent to the API and how they are structured in the request.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the **Left Pane**, in the **Put API** section, click the **Mapper** tab.
2. Enter the **inputs** as described in the table below:

<table><thead><tr><th width="170">Field</th><th>Description</th></tr></thead><tbody><tr><td>Interval</td><td>Enter the time interval (in seconds) between consecutive API requests. This setting helps control the request rate and prevents API throttling or overload.</td></tr><tr><td>Append All Row in One Request</td><td>Enable this option to include all rows in a single API request payload. Disable it to send each row as a separate API request.</td></tr><tr><td>Search Column</td><td>Use this field to quickly locate a specific column when the dataset contains many fields</td></tr><tr><td>Mapper Column</td><td>From this, specify the API payload field name or request parameter to which the data should be mapped.</td></tr><tr><td>Column</td><td>From this, select the source column from the pipeline dataset that provides the value for the mapped API field.</td></tr></tbody></table>

<figure><img src="../../../../.gitbook/assets/S (453).png" alt="" width="512"><figcaption><p>Mapping Fields</p></figcaption></figure>

</details>

<details>

<summary><strong>Advanced Configurations</strong></summary>

**Overview**

The advanced configuration allows you to review and update the API endpoint based on the API being used, add any required headers according to the API specifications, and configure the response settings. The response configuration can be set by selecting options such as **Request Payload**, **Request Header**, **Previous Data**, or **Multiple Response**.

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. **Base URL:** It is displayed by default since it is defined in the API connection.
2. **End Point:** In the **End Point** field, **update or confirm** the endpoint value based on the API you are calling.

{% hint style="info" %}
**Tip:** The endpoint specifies the **API resource path** where the PUT request will be sent. The base URL is defined in the API connection.
{% endhint %}

3. **API Header:** You may need to add additional headers **depending on the API requirements.**

{% hint style="info" %}
Tip: Only add headers if the **API documentation requires them**.
{% endhint %}

4. **API Params:** The API Params are used to send **query parameters** along with the API request.&#x20;

{% hint style="info" %}
**Tip: API Params are optional** and are used only when the API requires **query parameters** to filter, identify, or modify the request. If the API endpoint works without query parameters, you can leave the **API Params** section empty.
{% endhint %}

5. **Response Config:** Select the **Response Configuration** choosing from **Request Payload, Request Header, Previous Data,** or **Multiple Response.**

{% hint style="info" %}
**Tip:** **Description of Response Config. Options**&#x20;

* **Request Payload** – Displays the data sent in the API request body. It helps verify that the correct data from the pipeline is being transmitted to the API.
* **Request Header** – Shows the HTTP headers included in the API request, such as authentication tokens, content type, or other metadata required by the API.
* **Previous Data** – Provides access to the data generated in earlier stages of the pipeline, allowing it to be referenced or used when handling the API response.
* **Multiple Response** – Handles scenarios where the API returns multiple responses or records, enabling the pipeline to process each response item appropriately.
{% endhint %}

</details>

<details>

<summary><strong>Save ETL Job</strong></summary>

**Purpose**

Saving the ETL job confirms the pipeline setup so the **Write** **No SQL** **Output Node** can be configured correctly and used during execution.

**Procedure**

As part of saving the ETL job, you need to input a **name** and **description** for the pipeline along with specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption><p>Save Button</p></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (454).png" alt="" width="531"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved and displayed on the Delta Pipelines page.

</details>

<details>

<summary><strong>Preview Response</strong></summary>

**Purpose:**

Previewing the response allows you to check whether the API request was processed correctly and whether the returned response matches the expected output. It helps validate the API configuration and request structure before executing the pipeline fully. &#x20;

**Procedure:**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step instructions:**

1. On the **Right Pane**, click the **Preview** icon on the top of **Put API Output** Node.

<figure><img src="../../../../.gitbook/assets/S (455).png" alt=""><figcaption><p>Previewing</p></figcaption></figure>

After successful execution, the response is displayed as shown below:

<figure><img src="../../../../.gitbook/assets/S (456).png" alt=""><figcaption><p>Response Preview</p></figcaption></figure>

</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Output Nodes:**



    * **Table Output** – Writes processed data into a database table.
    * **File Output** – Saves processed data to files in a specified file format and location.
    * **GraphQL Write** – Sends processed data to a GraphQL endpoint for consumption by applications.
    * **Table Update** – Updates existing records in a database table using incoming data.
    * **Merge** – Synchronizes source data with a target table by inserting new records and updating existing ones.
    * **Put API** – Pushes processed data to an external or internal system through an API call.
    * **Kafka Producer** – Publishes processed data as events to a Kafka topic.
    * **Files to Tables** – Loads data from files directly into database tables.
    * **Write NoSQL** – Writes processed data into a NoSQL database.
