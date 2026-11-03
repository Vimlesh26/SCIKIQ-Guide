---
icon: list
---

# Data Source List

Once you've selected the **"Data source List"**, you'll see a comprehensive list of all the data sources that are currently connected to ScikIQ. Each entry in the list provides key details about the data source, such as its name, type, and status. This view allows you to quickly verify connections, manage data sources, and troubleshoot any issues with connectivity.

<mark style="color:orange;">Once a connection is created, navigate to the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**"Data Sources List"**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">section to view all connected data source connections.</mark>

1. Open ScikIQ and navigate to the main menu.
2. Click on **"SCIKIQ Connect"**.
   * Choose **"Connect to Data Source"**.
   * Select **"Data source List"** to view all connected data sources.

<figure><img src="../../../.gitbook/assets/image (727).png" alt=""><figcaption></figcaption></figure>

3. When you click on the **Data Sources List** section, it displays a **complete list** of all connected data sources.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F8p31cjkiUltEhwLRHBIf%2Fuploads%2FvMf9JPMu8JCJTak9GVis%2Fimage.png?alt=media&#x26;token=892e04c7-f1e3-4415-b0bf-0b4460e0dae6" alt=""><figcaption></figcaption></figure>

4. **Displayed Columns**: The list includes the following attributes for each connected data source:
   1. **Data Source Name**: The name assigned to the data source.
   2. **DB Name**: The specific database associated with the data source.
   3. **Endpoint**: The connection endpoint (e.g., server or IP address).
   4. **Owner**: The individual or team who owns the data source.
   5. **Catalogue**: The associated data catalogue.
   6. **Updated Date**: The last date the connection or data source details were updated.
   7. **Discovery**: Information on data source discovery status (e.g., new or re-discovered).
   8. **Usage**: Indicates how the data source is being utilized.
   9. **Actions**: Options such as **Edit**, **Delete**, **View**, **Create Asset**, and **Re-discover**.

<figure><img src="../../../.gitbook/assets/image (1130).png" alt=""><figcaption></figcaption></figure>

5. **Hide/Unhide Columns**
   1. Use the **Visible Column** and **Hidden Column** settings to customize the displayed columns.
   2. **Visible Column:** Shows selected columns.
   3. **Hidden Column:** Hides selected columns.
   4. Example:
      1. If the column **"DB Name"** is deselected in **Hidden Column**, it will no longer be displayed in the list for all data sources.
      2. Similarly, selecting it will make it visible again.

<figure><img src="../../../.gitbook/assets/image (1114).png" alt=""><figcaption></figcaption></figure>

6. **Search Bar**
   1. A **search bar** is provided at the top of the **Data Sources List** section, which you can use to filter and search for specific data sources quickly.

<figure><img src="../../../.gitbook/assets/image (1119).png" alt=""><figcaption></figcaption></figure>

7. **Actions in the Data Sources List**
   1. From this list, you can choose actions like **Edit**, **Delete**, **View**, or **Create Asset** for each data source.

<figure><img src="../../../.gitbook/assets/image (1131).png" alt=""><figcaption></figcaption></figure>

1. **Edit**&#x20;
   1. Clicking the **Edit** button for a selected data source opens the connection details in **edit mode**

<figure><img src="../../../.gitbook/assets/image (1125).png" alt=""><figcaption></figcaption></figure>

1. **Modify Credentials**: Change **hostname**, **port**, **database name**, and **password**.
2. **Update Metadata**: Modify **name**, **catalog**, **owner**, and other metadata.
3. **Save Changes**: After editing, save the changes to apply the updates.
4. This lets you easily update connection details and metadata for an existing data source.

<figure><img src="../../../.gitbook/assets/image (1124).png" alt=""><figcaption></figcaption></figure>

2. **Delete**
   1. Removes the data source connection from the list.

<figure><img src="../../../.gitbook/assets/image (1126).png" alt=""><figcaption></figcaption></figure>

3. **View**
   1. In **View Mode**, you can **view** the data source details but **cannot make any changes** to the connection credentials or metadata.

<figure><img src="../../../.gitbook/assets/image (1127).png" alt=""><figcaption></figcaption></figure>

b. This mode is for **viewing** only, allowing you to check the details without editing.

<figure><img src="../../../.gitbook/assets/image (1128).png" alt=""><figcaption></figcaption></figure>

4. **Re-discover**
   1. Click **Re-discover** to update and refresh the metadata of tables and fields associated with the data source.

<figure><img src="../../../.gitbook/assets/image (1129).png" alt=""><figcaption></figcaption></figure>

5. **Share (Resource Permission)**
   1. Opens a dialog box to share the data source with specific groups and roles.

<figure><img src="../../../.gitbook/assets/image (1115).png" alt=""><figcaption></figcaption></figure>

&#x20;  b. Sharing a Data Source

&#x20;      **Public**: The data source is **visible to all users** and entities.

&#x20;    **Private**: The data source is **restricted** to specific users or roles.

&#x20;    **Shared**: The data source is **shared** with defined groups or roles.

<figure><img src="../../../.gitbook/assets/image (1133).png" alt=""><figcaption></figcaption></figure>

3. **Select a Group**: Choose the group you want to share the data source with.
4. **Assign a Role**:
   * **Contributor**: Can **update**, **delete**, and **view** the data source connection details.
   * **Viewer**: Can **only view** the connection credentials.

This functionality helps manage access and permissions for different users and groups.

<figure><img src="../../../.gitbook/assets/image (1120).png" alt=""><figcaption></figcaption></figure>

**9.6. Create Asset**

1. From the **Data Sources List**, click on the **Create Asset** button next to the desired data source.
2. Redirects directly to the **Create Asset** screen, allowing the user to create an asset from the selected data source.

<figure><img src="../../../.gitbook/assets/image (1121).png" alt=""><figcaption></figcaption></figure>

3. On the **Create Asset** screen, fill in the required details for the asset, ensuring all mandatory fields are completed correctly.&#x20;
4. Once done, click **Save** to create the asset using the selected data source.

<figure><img src="../../../.gitbook/assets/image (1122).png" alt=""><figcaption></figcaption></figure>

9.7. Admin DataSource Options

1. Enable the **Admin DataSource** toggle button to filter the list to only display data sources used in the **admin settings** for saving log files and datasets.
2. This option ensures that administrative connections are highlighted for specific use cases.

<figure><img src="../../../.gitbook/assets/image (1117).png" alt=""><figcaption></figcaption></figure>

9.8. Creating a New Datasource

1. Click on the **Create Datasource** button.

<figure><img src="../../../.gitbook/assets/image (1118).png" alt=""><figcaption></figcaption></figure>

2. It will be redirected to the **All Datasources** screen.
3. it displays  the list of available data sources.
4. Select the desired Datasource.
5. Click on **Create Connection** to set it up.

<figure><img src="../../../.gitbook/assets/image (1135).png" alt=""><figcaption></figcaption></figure>

