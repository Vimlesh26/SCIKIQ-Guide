---
hidden: true
icon: list
---

# Business Data Models

The **Dataset/LDM List** in ScikIQ displays a comprehensive list of all the datasets and Logical Data Models (LDMs) currently connected to the platform. It provides key information about each dataset or LDM, including its name, type, status, and metadata, allowing users to efficiently manage, verify connections, and troubleshoot any issues.

Once a dataset or LDM is created, navigate to the **Dataset/LDM List** section to view all connected datasets and LDMs.

To access the **Dataset/LDM List**:

1. Open **ScikIQ** and navigate to the main menu.
2. Click on **SCIKIQ Connect**.
3. Choose **Connect to Dataset/LDM**.
4. Select **Dataset/LDM List** to view all connected datasets and LDMs.

<figure><img src="../../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>

When you click on the **Dataset/LDM List** section, it will display a complete list of all the created datasets and Logical Data Models.

<figure><img src="../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

#### **Displayed Columns:**

The list includes the following attributes for each connected dataset or LDM:

* **Data Model Name:** The name assigned to the dataset or LDM.
* **Business Owner:** The individual or team responsible for the dataset or LDM.
* **Technical Owner:** The individual or team responsible for the technical aspects of the dataset or LDM.
* **Catalogue:** The associated data catalogue for the dataset or LDM.
* **Data Domain:** The primary data domain the dataset or LDM belongs to (e.g., Sales, Marketing).
* **Sub Data Domain:** The subcategory within the data domain (e.g., Customer Data, Product Data).
* **Discovery:** Information about the dataset or LDM's discovery status (e.g., new or re-discovered).
* **Actions:** Options such as Edit, Delete, View, and Dataset Metadata.

<figure><img src="../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

#### **Hide/Unhide Columns:**

Use the **Visible Column** and **Hidden Column** settings to customize which columns are displayed in the list.

* **Visible Column:** Displays the selected columns.
* **Hidden Column:** Hides the selected columns.

<figure><img src="../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>

For example, if the **"Catalogue"** column is deselected in the **Hidden Column** section, it will no longer appear in the list for all datasets or LDMs. Similarly, selecting it will make it visible again.

<figure><img src="../../.gitbook/assets/image (302).png" alt=""><figcaption></figcaption></figure>

#### **Search Bar:**

A search bar is provided at the top of the **Dataset/LDM List** section, allowing you to quickly filter and search for specific datasets or LDMs based on keywords like their name, owner, or domain.

<figure><img src="../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

### **Actions in the Dataset/LDM List**

From the **Dataset/LDM List**, you can choose actions like **Edit**, **Delete**, **View**, and **Dataset Metadata** for each entry.

<figure><img src="../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

#### **Edit:**

Clicking the **Edit** button for a selected dataset or LDM opens the connection details in edit mode.

<figure><img src="../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>

* **Modify Metadata:** Update key information such as name, owner, data domain, subdomain, and associated catalogue.
* **Save Changes:** After making edits, click **Save** to apply the changes.

This allows you to easily update the details for an existing dataset or LDM.

<figure><img src="../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>

#### **Delete:**

Clicking **Delete** removes the selected dataset or LDM from the list.

<figure><img src="../../.gitbook/assets/image (307).png" alt=""><figcaption></figcaption></figure>

#### **View:**

In **View Mode**, you can see the dataset or LDM details but cannot modify any of the information.&#x20;

<figure><img src="../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>

This is for reference purposes only.

<figure><img src="../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure>

#### **Dataset Metadata:**

Clicking on the **Dataset Metadata** button will redirect you to the **Dataset Metadata Screen**.&#x20;

<figure><img src="../../.gitbook/assets/image (310).png" alt=""><figcaption></figcaption></figure>

Here, you can:

* Modify metadata for the selected dataset or LDM.
* Update descriptions, data domains, and subdomains as needed.

#### **Re-discover:**

Click **Re-discover** to refresh and update the metadata associated with the dataset or LDM. This helps ensure the data model is fully synchronized with the latest updates.

### **Create Asset from Dataset/LDM**

From the **Dataset/LDM List**, you can create an asset directly from any of the listed datasets or LDMs.

1. Click the **Create Asset** button next to the desired dataset or LDM.
2. You’ll be redirected to the **Create Asset** screen.
3. On the **Create Asset** screen, fill in the necessary details for the asset, making sure to complete all required fields.
4. Once done, click **Save** to create the asset using the selected dataset or LDM.

### **Dataset Schedule and Refresh**

You can schedule a refresh for any dataset or LDM. This ensures that your data models are automatically updated at specified intervals.

#### **Schedule Refresh:**

To set up a refresh schedule, you can:

1. **Run Now:** Start the refresh process immediately.
2. **Run Later:** Set the refresh to run at a specific future time.

#### **Schedule Details:**

When configuring a refresh schedule, provide the following information:

* **Schedule Name:** Name the refresh schedule.
* **Schedule Description:** Optionally, provide a description of the refresh schedule.
* **Start Date:** Select the start date for the schedule.
* **Start Time:** Choose the time when the refresh should begin.
* **End Date (Optional):** Set an end date for recurring refreshes.
* **End Time (Optional):** Define the end time for the refresh.

### **Admin Dataset/LDM Options**

Enable the **Admin Dataset/LDM** toggle button to filter the list and display only those datasets or LDMs that are used for administrative purposes, such as saving log files or system datasets.

This feature ensures that administrative connections are easily identifiable.

### **Creating a New Dataset/LDM**

To create a new dataset or LDM:

1. Click the **Create Dataset/LDM** button.
2. You will be redirected to the **All Datasets/LDMs** screen, which displays a list of available datasets or LDMs.
3. Select the desired dataset or LDM.
4. Click **Create Connection** to establish a connection with the selected dataset or LDM.
