---
icon: webhook
---

# API Pipeline

API Pipelines in SCIKIQ enable seamless data interaction through internal or external APIs, facilitating real-time data exchange. By supporting protocols such as GraphQL, these pipelines allow easy integration with cloud-based applications or platforms that expose API interfaces. They are designed to fetch, transform, and serve data via published endpoints, making them ideal for dynamic integrations with third-party platforms, internal services, or cloud applications.

A core element of API Pipelines is the API Schema Node, which provides a visual interface for mapping incoming data and applying field-level transformations.

<figure><img src="../../../../.gitbook/assets/image (625).png" alt=""><figcaption><p>This image shows the API Pipelines dashboard in SCIKIQ, where users can view and manage API-based data pipelines.</p></figcaption></figure>

### &#xD;**Mandatory Node**&#x20;

In SCIKIQ’s API Pipeline, the API Schema Node is mandatory. It provides a visual interface\
for mapping incoming API data and defining field-level transformations, ensuring structured\
and accurate data processing.

<figure><img src="../../../../.gitbook/assets/image (626).png" alt=""><figcaption><p>This image shows an API Pipeline in SCIKIQ, featuring the API Schema node and multiple input sources connected.</p></figcaption></figure>

\
Other input nodes such as Database Input, File Input, Query Input, GraphQL, SAP and NoSQL\
are available for flexible integration across a wide variety of data sources.

### **Input Node- API Schema**

* Open the application and navigate to the **API Schema** section.
* Locate and **select the API schema node** in the node tree.
* Once the node is selected, **drag the node** to the workspace or editor.

<figure><img src="../../../../.gitbook/assets/image (640).png" alt=""><figcaption></figcaption></figure>

* A prompt will appear asking for input format (either JSON or XML).

<figure><img src="../../../../.gitbook/assets/image (627).png" alt=""><figcaption></figcaption></figure>

**Select JSON** as the input format from the available options.

* Once JSON is selected, input a valid JSON object into the provided input field.
* Example: `{"key": "value", "field": "data"}`

<figure><img src="../../../../.gitbook/assets/image (641).png" alt=""><figcaption></figcaption></figure>

**Validate JSON:**

* After inputting the JSON, **click on the "Validate" button** to trigger the JSON validation.
* The system should validate the JSON and return an appropriate message (e.g., **valid JSON** or **invalid JSON**).
* If the JSON is invalid, verify the error message is displayed with specific details about the error.

<figure><img src="../../../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure>

**Extract Data:**

* **Click on the "Extract" button** after validation.
* The system should extract the data from the JSON input and display it in the UI.

<figure><img src="../../../../.gitbook/assets/image (629).png" alt=""><figcaption></figcaption></figure>

**Toggle Button Verification:**

* Locate the **toggle button** for data view options.
* **If the toggle is enabled**, verify that the system displays the extracted JSON data in **tabular format** in the data frame.
* **If the toggle is disabled**, verify that the system displays the extracted data in **JSON format**.

<figure><img src="../../../../.gitbook/assets/image (631).png" alt=""><figcaption></figcaption></figure>

The API Input feature in SCIKIQ allows users to bring in external data directly from APIs into\
their pipeline. Whether it is third-party services or internal endpoints, this input method\
enables seamless integration of real-time or static data sources.

<figure><img src="../../../../.gitbook/assets/image (632).png" alt=""><figcaption><p>This image shows the selection of the API Input node from the Input tab in SCIKIQ.</p></figcaption></figure>

### &#xD;Input Node- API

Navigate to the Input section from the left panel and select the API tile. Drag and drop it onto\
the pipeline canvas. This node allows users to fetch data from external APIs and incorporate\
it into their data workflows.\
Once the API Input node is placed:

* User will see the configuration panel titled Select API.
* Users can choose an existing API integration from the dropdown or configure a new  \
  one.
* Toggle DF Enable to allow the response data to be mapped into a dataframe format.

Additional options such as Pagination and Save Data on Failure help in handling\
large data and failure cases gracefully.

<figure><img src="../../../../.gitbook/assets/image (633).png" alt=""><figcaption><p>This image displays the API Input node placed on the canvas with initial configuration options</p></figcaption></figure>

\
In this step, users can select an existing API from the dropdown and define the endpoint,\
parameters, headers and payload. This flexibility enables integration with multiple third-party\
systems as needed.

<figure><img src="../../../../.gitbook/assets/image (637).png" alt=""><figcaption><p>This image shows the available API selection dropdown, including an option to create a new API.</p></figcaption></figure>

\
Here, the selected API is fully configured:

* Base URL and Endpoint are defined to target a specific API resource.
* Headers like Content-Type are added to define request format.
* If 'DF' is disabled, users can view the data in JSON format
* The Request Body (JSON) is prepared. This view helps ensure the API call structure  \
  is complete and ready to be sent.

<figure><img src="../../../../.gitbook/assets/image (635).png" alt=""><figcaption><p>This image shows the detailed configuration of a selected API, including base URL, endpoint, headers and JSON body.</p></figcaption></figure>

Once the API call is made the JSON Preview panel displays the response from the API.

* This ensures the connection is successful and data is being fetched as expected.
* Users can review raw JSON data before transforming or mapping it to downstream  \
  tasks.

<figure><img src="../../../../.gitbook/assets/image (638).png" alt=""><figcaption><p>This image shows the JSON Preview of the API response, enabling users to inspect incoming data.</p></figcaption></figure>

After previewing the data, the response JSON is parsed, and values are extracted into a\
structured data frame view.

* If 'DF' is enabled users can view the data in a tabular format.
* Users can now select the data frame and map the columns (e.g. name, email,  \
  username) to be used in the pipeline.
* The Preview section displays the final extracted rows, confirming that API data has  \
  been correctly ingested and structured.

<figure><img src="../../../../.gitbook/assets/image (639).png" alt=""><figcaption><p>This image shows the structured preview of parsed API data with two rows displayed in tabular format.</p></figcaption></figure>

> **For more information on the other input nodes, refer to the following section within the pipeline input node documentation-** &#x20;





