# Version 3.2.8

### Configure Azure AD Application for SCIKIQ Access

**Prepare Azure Active Directory (Azure AD)**

Before you connect OneDrive and SharePoint to SCIKIQ, you first need to set up an application in **Azure Active Directory (Azure AD)**.&#x20;

This process involves creating an app and generating credentials that SCIKIQ will use to access your OneDrive and SharePoint data.

<mark style="color:blue;">**Register an Application in Azure AD**</mark>

1. **Log in to Azure Portal**:
   * Visit Azure Portal and sign in with your admin credentials.
2. **Register a New App**:
   * In the left sidebar, click **Azure Active Directory**.
   * Then, click on **App registrations** > **New registration**.
   * **Name**: Enter a name like "SCIKIQ Integration".
   * **Supported account types**: Choose **Accounts in this organizational directory only**.
   * **Redirect URI**: Leave this empty unless you need it for specific use cases.
   * Click **Register**.
3. **Configure API Permissions**
   1. Next, assign the correct permissions to allow SCIKIQ to access SharePoint and OneDrive data.
4. **Go to API Permissions**:
   1. Click on **API permissions** > **Add a permission**.
   2. Select **Microsoft Graph** and choose **Delegated permissions** (to access data on behalf of users).
5.  **Add SharePoint and OneDrive Permissions**:

    * For **OneDrive**, add:
      * `Files.Read`
      * `Files.ReadWrite`
    * For **SharePoint**, add:
      * `Sites.Read.All`
      * `Sites.FullControl.All`

    Click **Add permissions**.
6. **Grant Admin Consent**:
   * Click **Grant admin consent for \[Your Organization]** to ensure these permissions are applied.
7. **Generate Client Secret**
   1. A **Client Secret** is required to authenticate SCIKIQ to access your Azure AD data.
   2. In **Certificates & Secrets**, click **New client secret**.
   3. **Description**: Enter something like "SCIKIQ Integration Secret".
   4. Choose the **Expiration** period (e.g., 1 year).
   5. Click **Add** and **copy the secret** immediately. You’ll need this later.
8. **Obtain Client ID and Tenant ID**&#x20;
   1. You will need two IDs from Azure:
      1. **Tenant ID**: Go to **Azure Active Directory > Properties** to find the **Tenant ID**.
      2. **Client ID**: In the **Overview** section of your app registration, copy the **Application (client) ID**.

### <mark style="color:blue;">Connecting OneDrive to SCIKIQ</mark>

This document provides detailed instructions on how to connect OneDrive as a data source within SCIKIQ.

1. **Navigating to the Connect Module:**  Upon logging into SCIKIQ, users will land on the SCIKIQ Dashboard. The left-side navigation panel provides access to various modules, including SCIKIQ Connect.

<figure><img src="../.gitbook/assets/image (1522).png" alt=""><figcaption></figcaption></figure>

2. **Accessing the "SCIKIQ Connect" Module**
   1. From the main menu, navigate to SCIKIQ Connect.
   2. Choose Connect to Data Source and proceed to Manage Data Source.

<figure><img src="../.gitbook/assets/image (1523).png" alt=""><figcaption></figcaption></figure>

3. **Selecting OneDrive as the Data Source**
   1. In the "Connect to Data Source" dialog, select the files option.

<figure><img src="../.gitbook/assets/image (1524).png" alt=""><figcaption></figcaption></figure>

&#x20;   b. Choose OneDrive from the list of available cloud sources.

<figure><img src="../.gitbook/assets/image (1525).png" alt=""><figcaption></figcaption></figure>

4. In this setup for establishing a connection, decide whether you wish to create a new connection or select an existing one.

<figure><img src="../.gitbook/assets/image (1526).png" alt=""><figcaption></figcaption></figure>

5. **Connection Details Configuration**
   1. You will be required to provide the following information:
   2. When setting up the OneDrive connection in SCIKIQ, you will need to provide the following details:
      1. Client ID: A unique identifier for your registered OneDrive application in Azure AD.\
         _&#x46;ind it in the Azure portal under App registrations._
      2. Client Secret: A secure key used to authenticate the application.\
         _&#x47;enerate it in the Azure portal under Certificates & Secrets._
      3. Tenant ID: A unique identifier for your Azure AD organization.\
         _&#x46;ind it in the Azure portal under Azure Active Directory > Properties._
      4. Username: The OneDrive account’s email address (usually your work email).\
         _&#x55;se the account you wish to connect to OneDrive._
      5. Password: The password for the OneDrive account provided above.\
         _&#x55;se the login password for the specified OneDrive account._

<figure><img src="../.gitbook/assets/image (1527).png" alt=""><figcaption></figcaption></figure>

6. **Adding Metadata**
   1. Add metadata to categorize and enrich your OneDrive data. Metadata can help improve the organization and searchability of your data.

<figure><img src="../.gitbook/assets/image (1528).png" alt=""><figcaption></figcaption></figure>

7. **Testing the Connection**
   1. Click the Test Connection button to ensure that SCIKIQ can connect to your OneDrive account.
   2. If the connection is successful, a green confirmation message will appear.
   3. Click next

<figure><img src="../.gitbook/assets/image (1529).png" alt=""><figcaption></figcaption></figure>

8. **Select Files for Discovery**
   1. Click on the Search button.

<figure><img src="../.gitbook/assets/image (1530).png" alt=""><figcaption></figcaption></figure>

&#x20;b. select the file extension (e.g., CSV) and click the Search button again. This will display a list of available folders or document libraries (for OneDrive)

<figure><img src="../.gitbook/assets/image (1531).png" alt=""><figcaption></figcaption></figure>

c. It will show folders with matching files (e.g., Documents, Desktop).

d. Select the folder you want (e.g.csv File).

e. Optionally, apply filters like Include/Exclude Patterns or set Skip Row(s) if needed.

<figure><img src="../.gitbook/assets/image (1532).png" alt=""><figcaption></figcaption></figure>

f. Click "Save" to display all .csv files in the selected folder.

g. Select few files then Click Next to proceed.

<figure><img src="../.gitbook/assets/image (1533).png" alt=""><figcaption></figcaption></figure>

9. There are additional connection configuration settings as follows:
10. Connection Type:
    1. Owned
    2. Third-party
11. Service Managed
12. User Managed
13. Security Settings:
    1. Secured Connection: Yes/No
    2. Unsecured Connection: Yes/No
14. click "Next" to proceed with the connection setup.

<figure><img src="../.gitbook/assets/image (1534).png" alt=""><figcaption></figcaption></figure>

3. Provide a name for the database that will be displayed in the list of connected databases.

* Click Finish.

<figure><img src="../.gitbook/assets/image (1535).png" alt=""><figcaption></figcaption></figure>

Viewing the Connection

After completing the setup, navigate to the Data Sources List to confirm the OneDrive connection is successfully listed

<figure><img src="../.gitbook/assets/image (1536).png" alt=""><figcaption></figcaption></figure>

### Connecting SharePoint to SCIKIQ

1\. Navigating to the Connect Module

Upon logging into SCIKIQ, users will land on the SCIKIQ Dashboard. The left-side navigation panel provides access to various modules, including SCIKIQ Connect.

2\. Accessing the "SCIKIQ Connect" Module

* From the main menu, navigate to SCIKIQ Connect.
* Choose Connect to Data Source and proceed to Manage Data Source.

<figure><img src="../.gitbook/assets/image (1537).png" alt=""><figcaption></figcaption></figure>

Selecting SharePoint as the Data Source

* In the Connect to Data Source dialog, select the files option.
* Choose SharePoint from the list of available cloud sources.

<figure><img src="../.gitbook/assets/image (1538).png" alt=""><figcaption></figcaption></figure>

Deciding on the Connection Setup

* In this setup for establishing a connection, decide whether you wish to create a new connection or select an existing one.

<figure><img src="../.gitbook/assets/image (1539).png" alt=""><figcaption></figcaption></figure>

Connection Details Configuration

When setting up the SharePoint connection in SCIKIQ, please provide the following details:

1\.      URL: The full address for your SharePoint site.\
Example:\
https://example.sharepoint.com/sites/yoursitename

2. User ID: The email address associated with the SharePoint account you are connecting to.
3. Password: The login password for the SharePoint account provided above. Ensure that this is the correct password for the User ID you entered.

<figure><img src="../.gitbook/assets/image (1540).png" alt=""><figcaption></figcaption></figure>

Adding Metadata

* Add metadata to categorize and enrich your SharePoint data.\
  Metadata can help improve the organization and searchability of your data.

<figure><img src="../.gitbook/assets/image (1541).png" alt=""><figcaption></figcaption></figure>

Testing the Connection

* Click the Test Connection button to ensure that SCIKIQ can connect to your SharePoint account.
* If the connection is successful, a green confirmation message will appear.
* Click Next.

<figure><img src="../.gitbook/assets/image (1542).png" alt=""><figcaption></figcaption></figure>

Select Files for Discovery

* Click on the Search button.

<figure><img src="../.gitbook/assets/image (1543).png" alt=""><figcaption></figcaption></figure>

* Then, select the file extension (e.g., CSV) and click the Search button again. This will display a list of available folders or document libraries for SharePoint.

<figure><img src="../.gitbook/assets/image (1544).png" alt=""><figcaption></figcaption></figure>

* It will show folders with matching files (e.g., Documents, Shared Documents).
* Select the folder you want (e.g., Documents).
* Optionally, apply filters like Include/Exclude Patterns or set Skip Row(s) if needed.

<figure><img src="../.gitbook/assets/image (1545).png" alt=""><figcaption></figcaption></figure>

Click Save to display all .xls files in the selected folder.\
Select a few files, then click Next to proceed.

<figure><img src="../.gitbook/assets/image (1546).png" alt=""><figcaption></figcaption></figure>

Additional Connection Configuration Settings

There are additional connection configuration settings as follows:

1. Connection Type:
   1. Owned
   2. Third-party
   3. Service Managed
   4. User Managed
2. Security Settings:

* Secured Connection: Yes/No
* Unsecured Connection: Yes/No

Click Next to proceed with the connection setup.

<figure><img src="../.gitbook/assets/image (1547).png" alt=""><figcaption></figcaption></figure>

Finalizing the Connection

* Provide a name for the database that will be displayed in the list of connected databases.
* Click Finish.

<figure><img src="../.gitbook/assets/image (1548).png" alt=""><figcaption></figcaption></figure>

Viewing the Connection

* After completing the setup, navigate to the Data Sources List to confirm the SharePoint connection is successfully listed.
