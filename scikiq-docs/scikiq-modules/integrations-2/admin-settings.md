---
icon: gear
---

# Admin Settings

The Admin Settings section in ScikIQ is the control center for configuring core administrative operations. It includes four important tabs: **Admin Settings**, **Resource Approval**, **SMTP Configuration**, and **Scheduler Server**. Each of these tabs helps platform administrators manage system behaviors, data storage, user identity replication, scheduled jobs, and communication settings.

This guide walks you through each tab from scratch, starting with the **Admin Settings** tab. All sections are explained in simple language and organized so you can follow along with screenshots and actions in the UI.

It consists of four primary tabs:

<table data-view="cards"><thead><tr><th align="center"></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td align="center"><strong>Admin Setting</strong></td><td><a href="admin-settings.md#admin-setting-tab">#admin-setting-tab</a></td><td><a href="../../.gitbook/assets/download (2).png">download (2).png</a></td></tr><tr><td align="center"><strong>Resource Approval</strong></td><td><a href="admin-settings.md#resource-approval-tab">#resource-approval-tab</a></td><td><a href="../../.gitbook/assets/download (3).png">download (3).png</a></td></tr><tr><td align="center"><strong>SMTP Configuration</strong></td><td><a href="admin-settings.md#smtp-configurations">#smtp-configurations</a></td><td><a href="../../.gitbook/assets/images.jfif">images.jfif</a></td></tr><tr><td align="center"><strong>Scheduler Server</strong></td><td><a href="admin-settings.md#scheduler-server-in-scikiq">#scheduler-server-in-scikiq</a></td><td><a href="../../.gitbook/assets/images (1).jfif">images (1).jfif</a></td></tr></tbody></table>

### Admin Settings Tab <a href="#admin-setting-tab" id="admin-setting-tab"></a>

The Admin Settings tab is used to manage storage connections, user replication settings, DQ reject logs handling, password policy configurations, and integration with LLM (Large Language Model) services and vector databases.

Why Configure Admin Settings?

You need to configure Admin Settings in ScikIQ to:

* Define where data (datasets, logs, vectors) is stored.
* Enable user and group replication with cloud identity managers like AWS IAM or Azure AD.
* Store rejected data for review and audit.
* Use intelligent features powered by LLMs and vector databases.
* Control password expiry and restrict domain access.
* Configure communication via SMTP.
* Manage automated and scheduled background jobs.

> <mark style="color:orange;">**Note**</mark><mark style="color:orange;">: Without proper configuration of these settings, many ScikIQ features will not function correctly or securely.</mark>

### Configure Admin Settings in ScikIQ

Here is how you can configure the Admin Settings tab in ScikIQ from scratch:

1. **Log in to ScikIQ with an Admin Account**\
   Only users with admin privileges can access and configure admin settings.
2. **Navigate to Admin Settings Module**\
   From the left navigation panel, go to Access management **Module** and click on the **Admin Settings** menu.

<figure><img src="../../.gitbook/assets/image (1331).png" alt=""><figcaption></figcaption></figure>

1. **File Storage Connection**
   1. This section defines where ScikIQ stores all files such as datasets, rejections, logs, and vector data. ScikIQ supports **AWS S3**, **Google Cloud**, and **Azure**. After selecting the cloud provider, administrators link a pre-configured connection name to define where the data will be stored.

#### Steps to Configure:

1. In **Storage Location**, choose your preferred storage provider (e.g., AWS S3, Azure Blob, Google Cloud).

<figure><img src="../../.gitbook/assets/image (504).png" alt=""><figcaption></figcaption></figure>

2. From **Connection Name**, select an existing storage connection.

{% hint style="warning" %}
**If none are available, go to the** [**Data Source Connection**](../images-and-media/scikiq-connect-module/) **module and create a connection first.**
{% endhint %}

1. This connection will be used as the default for file-based operations.

<figure><img src="../../.gitbook/assets/image (505).png" alt=""><figcaption></figcaption></figure>

### **Use Case: Store Delta Pipeline Output in AWS S3**

**Purpose-** You want to create a **Delta Pipeline** in ScikIQ to process Employees data and **write the output to AWS S3** in **CSV format** for distributed access and regulatory tracking.

* **Navigate to Delta Hub and Build Pipeline**
  * Go to Delta Hub in ScikIQ, click "Create New Pipeline" (e.g., Employees\_Data\_Processing\_Delta), then add an Input Node (e.g., Database or File) and a Transformation Node for data logic.
*   In the **Output Node settings**:

    * Select the **Output Format**: CSV, Parquet, or JSON.
    * Choose the **S3 connection** (e.g., `S3-filestore Connection`) configured under Admin Settings > File Storage Connection.
    * Specify the **target folder/path** in the S3 bucket (e.g., Vimlesh43/demo1).

    <figure><img src="../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure>

#### Outcome:

* Log in to your AWS S3 console.
* Navigate to the target bucket and folder (e.g., `s3://scikiq-storage/customer_data/processed/`).
* Confirm that the output CSV files have been successfully written.

<figure><img src="../../.gitbook/assets/image (1333).png" alt=""><figcaption></figcaption></figure>

### User, Group & Policy Replication (IAM Integration)

1. This feature allows ScikIQ to replicate user, group, and policy creation to a connected cloud identity manager like AWS IAM.&#x20;
2. this toggle button syncs users, groups, and policies in ScikIQ with cloud identity managers. If enabled, every time a user or policy is created in ScikIQ, it is replicated in the cloud identity system (e.g., AWS IAM).

<figure><img src="../../.gitbook/assets/image (492).png" alt=""><figcaption></figcaption></figure>

#### Steps to Enable:

1. Toggle **Replicate users, groups & policies on Cloud Identity Manager** to ON.
2. When new users/groups are created in ScikIQ:
   * An **IAM user** is automatically created in AWS IAM.
   * An **IAM group** is created with a corresponding **resource key**.

### Use Case: User and Group Creation with Automatic Replication in AWS IAM and S3 Bucket Configuration in ScikIQ

#### **Purpose**:

This use case covers the process of creating users and groups in ScikIQ, automatically replicating them into AWS IAM, and configuring S3 bucket access with the appropriate read-only or read-write policies. The goal is to streamline user and group management across both platforms and automate the access control process for S3 buckets.

#### **Steps**:

1. **Create User in ScikIQ and Replicate to AWS IAM**
   1. **Log in to ScikIQ** as an Admin user.

<figure><img src="../../.gitbook/assets/image (493).png" alt=""><figcaption></figcaption></figure>

2. Navigate to the **Access Management** section and click on **Users**.
   1. Click **Create New User**.
   2. Fill in the user details:
      1. **User Name** (e.g., IAM User)
      2. **Email Address** (e.g., <mark style="color:blue;">**`iamuser40@scikiq.com`**</mark>)
      3. **Role** (e.g., <mark style="color:blue;">`Data Engineer, Data Analyst, Viewer`</mark>)
      4. **Password** (set a password)
   3. Click **Save** to create the user.

<figure><img src="../../.gitbook/assets/image (494).png" alt=""><figcaption></figcaption></figure>

* A new user,<mark style="color:blue;">**`iamuser40@scikiq.com`**</mark>**,** is created in ScikIQ.
* **AWS IAM User Creation**: This user is automatically replicated into AWS IAM with the same credentials, allowing seamless synchronization of user accounts.

<figure><img src="../../.gitbook/assets/image (495).png" alt=""><figcaption></figcaption></figure>

2. **Create Group in ScikIQ and Replicate to AWS IAM**
   1. In the **Access Management** section, go to **User Groups** and click on **Create New Group**.
   2. Enter a **Group Name** (e.g.,<mark style="color:blue;background-color:yellow;">**`IAM Users Group`**</mark><mark style="background-color:blue;">)</mark>.
   3. Assign the group appropriate permissions (e.g., access to datasets, read-write permissions).
   4. Click **Save** to create the group.

<figure><img src="../../.gitbook/assets/image (496).png" alt=""><figcaption></figcaption></figure>

**2.1. Outcome**:

* A new group,  IAM Users Group is created in ScikIQ.
* This group is **automatically replicated into AWS IAM** with the same name and permissions, ensuring consistency across both systems.

<figure><img src="../../.gitbook/assets/image (497).png" alt=""><figcaption></figcaption></figure>

3. **Create S3 Bucket Connection in ScikIQ**
   1. Navigate to **Admin Settings** > **File Storage**.
   2. Click **Create New S3 Connection** and enter the necessary details:
      1. **Connection Name** (e.g., <mark style="color:blue;">`DataScikIQ Bucket S3`</mark>).
      2. **AWS Region** (e.g., <mark style="color:blue;background-color:yellow;">`Asia Pacific(Mumbai))`</mark>.
      3. **Access Key** and **Secret Key** for AWS IAM.
   3. Click **Save** to create the S3 connection.

**Outcome**:

* An S3 bucket connection is created in ScikIQ, linking it to AWS IAM credentials.

<figure><img src="../../.gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure>

4. **Grant Read-Only Access to S3 Bucket for ScikIQ Group**
   1. In the **S3 Connection Settings** for the selected bucket, enable the **Read-Only Access** toggle for the ScikIQ group (e.g., <mark style="color:blue;background-color:yellow;">**`IAM Users Group`**</mark>).
   2. **Automatically generate a Read-Only IAM policy** in AWS IAM. The policy is named using the pattern <mark style="color:blue;">`PLCY-{data source key}R`</mark> (e.g., <mark style="color:blue;">`PLCY-DSRCCLNT0052000019R`</mark><mark style="color:blue;">)</mark>.

<figure><img src="../../.gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure>

**Outcome**:

* The <mark style="color:blue;background-color:yellow;">**`IAM Users Group`**</mark> group in AWS IAM is granted **read-only access** to the S3 bucket.
* The **IAM policy** is automatically created in AWS IAM with the appropriate permissions.

<figure><img src="../../.gitbook/assets/image (501).png" alt=""><figcaption></figcaption></figure>

5. **Grant Read-Write Access to S3 Bucket for ScikIQ Group**
   1. In the **S3 Connection Settings**, enable the **Read-Write Access** toggle for the ScikIQ group (e.g., <mark style="color:blue;background-color:yellow;">**`IAM Users Group`**</mark>).
   2. **Automatically generate a Read-Write IAM policy** in AWS IAM. The policy is named using the pattern <mark style="color:blue;">`PLCY-{data source key}RW`</mark> (e.g., <mark style="color:blue;">`PLCY-DSRCCLNT0052000019RW`</mark>).

<figure><img src="../../.gitbook/assets/image (503).png" alt=""><figcaption></figcaption></figure>

**Outcome**:

* The <mark style="color:blue;background-color:yellow;">**`IAM Users Group`**</mark> group in AWS IAM is granted **read-write access** to the S3 bucket.
* The **IAM policy** is automatically created in AWS IAM with the appropriate permissions for read and write access.

<figure><img src="../../.gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure>

1.  **Rejects Log**

    Reject Logs capture and store all failed or rejected operations, such as invalid file uploads, failed validations, or unauthorized access attempts.

    **Key Points:**

    * Logs reasons for failures across the platform.
    * Helps in auditing and debugging.
    * Requires a defined **Storage Location** to save the logs.

    <figure><img src="../../.gitbook/assets/image (506).png" alt=""><figcaption></figcaption></figure>
2.  **Save Dataset To**:

    The **"Save Dataset To"** setting allows administrators to define how datasets are saved within ScikIQ — either as serialized files (Pickle) or structured tables (Database). Depending on the selected option, different configuration fields will appear.\
    Choose one of the two options:

<figure><img src="../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>

**Option 1: Pickle**

When the **Pickle** option is selected, datasets are saved as serialized `.pkl` files. This format is particularly useful for machine learning and data science applications where data needs to be loaded back into memory for modeling or analysis.

#### **Steps to Configure:**

1. Navigate to the **Save Dataset To** section in Admin Settings.
2. Select the option **Pickle**.
3. A list of file storage connections will be displayed for selection.

<figure><img src="../../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

1. Admin selects one **File Connection Name** (e.g., AWS S3, Azure Blob, GCP Storage, or Local File System).
2. The selected connection will be used to store the dataset as a `.pkl` file.
3.  Choose a **File Connection Name** from the available file storage connections.

    Enable or disable the **Same As File** toggle:

    * **Enabled**: No further selection needed; dataset uses the file storage connection from the **File Storage** section.
    * **Disabled**: A new field, **Dataset Storage Location**, will appear. Select a specific file connection for dataset saving.

<figure><img src="../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>

**Option 2: Database**

When the **Database** option is selected, datasets are saved as tables in a connected database. This option is recommended for structured data workflows that require reporting, querying, or integration with other data pipelines.

#### **Steps to Configure:**

1. Navigate to the **Save Dataset To** section in Admin Settings.
2. Select the option **Database then a** list of database connections will be displayed. Choose a valid **Database Connection Name** from the list.

<figure><img src="../../.gitbook/assets/image (508).png" alt=""><figcaption></figcaption></figure>

1. A **Prefix Table Name** field will be shown. This prefix is prepended to the dataset's actual table name during creation. Enter a desired **Prefix Table Name** (e.g., `vs__projectX_`), which will be added to all dataset tables stored in the database.

<figure><img src="../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>

#### Advanced Configuration

1.  **Service Details**&#x20;

    The **Service Details** section is used to configure service-related credentials, such as **Service ID** and **Application ID**, required for internal and external system integrations.

    1. **Enter Service Details**  Provide any required connection data, service ID, and application ID as given by your IT or platform team.

    <figure><img src="../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>



### Allow Domain

A **domain** is the part of an email address that comes **after the "@" symbol**. It identifies the email service provider or the organization to which the email belongs.

**Examples:**

* In `test.user@scikiq.com`, the domain is **`scikiq.com`**
* In `john.doe@gmail.com`, the domain is **`gmail.com`**

**Why It Matters:**

In many systems, administrators restrict account creation to specific domains (e.g., only company emails). This improves security and ensures that only authorized users can access the system.

#### **Step 1: Navigate to Admin Settings**

1. Log in to the system as **Client Admin Role (only client admin has access of admin setting menu).**
2. Go to the **Access Management** module.
3. Click on **Admin Settings**.

<figure><img src="../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

#### **Step 2: Access the Allowed Domain section.**

<figure><img src="../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>

#### **Step 3: Add Allowed Domain**

1.  In the **domain configuration** section, enter the domain:

    ```
    scikiq.com
    ```
2. Click the **Update** button.
3.  A confirmation message should appear:

    ```
    SCIK-0125: Success
    ```

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

#### Creating Users Based on Allowed Domains

**Scenario 1: Email Not in Allowed Domain**

**Steps:**

1. Navigate to the **Users & Groups** screen.
2. Click on **Create User**.
3.  Enter the email:

    ```
    test.user41@gmail.com
    ```
4. Click the **Create User** button.
5.  An error message is shown:

    ```
    SCIK-0337: test.user41@gmail.com not in allowed domains.
    ```



<figure><img src="../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

#### Scenario 2: Email in Allowed Domain

**Steps:**

1. Go to the **Users & Groups** screen.
2. Click on **Create User**.
3.  Enter the email:

    ```
    test.user41@scikiq.com
    ```
4. Click the **Create User** button.

<figure><img src="../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

5. Newly created user will now appear in the **User List** under the **Users & Groups** section.

<figure><img src="../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Notes**

* You can configure multiple allowed domains if needed (e.g., `scikiq.com`, `example.com`).
* Domain checks are not case-sensitive.
* Always click **Update** after changing the domain settings.
{% endhint %}

1. **Save Auto Gen Vector**
   1. For AI/ML-based integrations, the **Auto Gen Vector** section allows admins to select a database (e.g., **Chroma DB**) to store generated vectors. This is especially useful for machine learning workflows that use document embeddings and other vectorized data.
   2. **Set Up Auto Gen Vector Storage**\
      If you are using vector-based features, select the vector database (e.g., Chroma DB), choose a connection ID, and define where the vectors will be saved

<figure><img src="../../.gitbook/assets/image (446).png" alt=""><figcaption></figcaption></figure>

3. **Save LLM API**
   1. This section connects ScikIQ with external LLMs (Large Language Models). Administrators input the API credentials to enable advanced NLP and AI features like text summarization, document understanding, and more.
   2. **Configure LLM API Access**\
      Input the API key or credentials to connect to your preferred LLM provider, such as OpenAI.

<figure><img src="../../.gitbook/assets/image (447).png" alt=""><figcaption></figcaption></figure>

4. **Password Expiry Settings**
   1. The **Password Expiry** settings allow administrators to define the validity period of user passwords. Additionally, administrators can set reminder intervals to notify users about upcoming password expirations.
   2. **Define Password Policy**\
      Set the number of days before a password expires and when reminders should be sent to users.
5. **Domain Restriction**
   1. This feature restricts user registration to certain email domains, ensuring that only authorized users (e.g., `@scikiq.com`) can access ScikIQ.
   2. **Restrict User Domain Access (Optional)**\
      Specify email domains (e.g., `@company.com`) to restrict who can register or access ScikIQ.
6. **Save All Configurations**\
   After filling in each section, click the **Save** button to apply the settings. It is recommended to test each connection (e.g., storage, SMTP) after saving.

<figure><img src="../../.gitbook/assets/image (449).png" alt=""><figcaption></figcaption></figure>

1. **Repeat for Other Tabs (SMTP, Scheduler, etc.)**\
   Use the remaining tabs to configure communication settings, approval workflows, and scheduler servers as needed.

### Resource Approval Tab

The **Resource Approval** tab in ScikIQ allows administrators to define approval workflows for various resources within the platform. This is essential for managing which resources (such as datasets, models, or integrations) require manual approval and for automating the approval process where needed. By setting approval rules, administrators can enforce structured workflows and ensure proper validation before resource utilization.

This guide will walk you through how to configure the **Resource Approval Tab**, focusing on both **Auto Approval** and **Manual Approval** settings, and explaining each configuration field.

<figure><img src="../../.gitbook/assets/image (450).png" alt=""><figcaption></figcaption></figure>

#### **Resource Approval Settings Overview**

The **Resource Approval Tab** consists of two main sections:

1. **Auto Approval Section**
2. **Manual Approval Section**

Both sections help manage how resources are approved and controlled, but they differ in how approvals are handled.

<figure><img src="../../.gitbook/assets/image (451).png" alt=""><figcaption></figcaption></figure>

1. Auto Approval Section

The **Auto Approval** feature automates the approval process for certain resources based on predefined rules or conditions. This allows resources to be automatically approved without requiring manual intervention, streamlining workflows and reducing the need for constant oversight.

#### **Configuration Options for Auto Approval:**

* **Resource Type**: Select the type of resource for which automatic approval is enabled. This could include datasets, models, or other system integrations.
* **Auto Approval Toggle**: Use this toggle to enable or disable auto-approval for the selected resource type. When enabled, the resource will automatically be approved once it is submitted, bypassing the manual approval workflow.

**Steps to Enable Auto Approval:**

1.  **Enable the Auto Approval Toggle Button:**

    * Locate the **Auto Approval** toggle switch within the approval configuration section.
    * Set the toggle to **Enabled** to activate the auto approval functionality for the selected resource types.

    <figure><img src="../../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>
2.  **Auto Approval Status:**

    * When **Auto Approval** is enabled, the resource will bypass the manual approval process, and the status will be automatically set as **Approved**. This means the resource has been approved without requiring a manual intervention.

    **Available Statuses for Auto Approval:**

    * **Approved:** The resource is automatically approved by the system, and no further approval steps are required.
    * **Auto Approved:** Indicates that the resource was approved automatically, often due to predefined conditions or rules.
    * **Created:** A new resource is created but hasn't yet been reviewed. It’s in the initial state of the approval process.
    * **Draft:** The resource is still being worked on and is not yet ready for approval. It can be reviewed again before approval.
    * **Recommended:** The resource is flagged as recommended for approval but requires a final decision.
    * **Submitted:** The resource has been submitted for approval by a user or system, awaiting manual or automatic approval.
    * **Under Modification:** If changes are made to a resource, it will require re-approval. This status indicates that the resource is being modified and needs revalidation.

    <figure><img src="../../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>

**Field Type Selection:**

*   Select the **Field Type** for which you wish to enable auto approval. The options available will depend on the types of resources in your system. Common resource types include:

    * **Catalogue:** A collection or classification of data resources.
    * **Domain:** Specific areas or categories of data, typically at a higher organizational level.
    * **Entity:** Represents an individual resource, like a database or dataset.
    * **Role:** Roles or responsibilities related to data access and management.
    * **Sub-domain:** A subset of a domain, often representing more specific categories.
    * **Users:** User accounts and associated permissions.

    <figure><img src="../../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>

1.  **Field Selection:**

    * Choose the **Field** on which the auto approval rule will be applied. The available options will depend on the selected **Fields Type**. For example:
      * **Catalogue:** The auto approval rule could be based on a specific catalogue name.
      * **Domain:** Select specific domains to apply auto approval for.
      * **Entity:** Specify particular entities or resources that will be auto-approved.

    Once the **Resource Type** is selected, the **Field** options will automatically adjust to show relevant options that correspond to the resource type. For example, if **Catalogue** is selected, the field options might include a list of available catalogues.
2. **Operator Selection:**
   *   Choose the **Operator** to define how the selected **Field** will be compared to the **Values**:

       * **Equals:** The field value must exactly match the specified value (e.g., the catalogue name is exactly the one selected).
       * **In:** The value must be one of a list of selected options (e.g., the resource must be in one of several selected domains).
       * **Not Equal:** The value must not match the specified value.
       * **Not In:** The value must not belong to any of the selected options.

       <figure><img src="../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>


3.  **Value Selection:**

    * After selecting the **Field** and **Operator**, the **Values** field will populate based on the field you’ve chosen. The system will display the available options relevant to the field. For example:
      * If **Catalogue** is selected as the field, the **Values** will display a list of available catalogues in your system.
      * If **Domain** is selected, the values will show the different domains in your organization.
      * If **Entity** is selected, the available entities will be displayed for you to choose from.

    <figure><img src="../../.gitbook/assets/image (457).png" alt=""><figcaption><p>Choose the appropriate value(s) for the auto approval condition.</p></figcaption></figure>



#### 2. Manual Approval Configuration Section

The **Manual Approval** section allows administrators to configure approval workflows, offering granular control over how resources are approved within the system. This ensures that only authorized users are able to approve or reject resources, based on predefined conditions and roles.

#### Configuration Fields for Manual Approval:

1. **Resource Type:**
   *   This defines the type of resource being requested for approval. Common resource types include:

       * **Data source:** For database connections or data sources.
       * **Dataset:** For data collections or datasets.
       * **Dashboard:** For analytical or reporting dashboards.
       * **Business Data Event:** Events related to business data operations.

       <figure><img src="../../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure>
2. **Role:**
   * Select the role that will be responsible for approving the resource request. The role chosen will have the authority to approve or reject the resource based on the workflow.
     *   Example roles could include:

         * **Admin:** A top-level role with full approval rights.
         * **Data Engineer:** Responsible for reviewing and approving technical resources.
         * **Data Owner:** Person in charge of approving datasets, often a business owner or manager.

         <figure><img src="../../.gitbook/assets/image (459).png" alt=""><figcaption></figcaption></figure>
3. **Action:**
   *   Choose the action the selected role will take on the resource request. Available actions include:

       * **Approve:** Grant approval for the resource, allowing it to proceed further in the workflow.
       * **Concur:** A conditional approval, where the role agrees with the resource but requests further review or conditions.
       * **Pending:** Marks the resource as awaiting action, no approval or rejection has been made yet.
       * **Recommend:** Suggests approval or further review, but doesn't directly approve the resource.

       <figure><img src="../../.gitbook/assets/image (460).png" alt=""><figcaption></figcaption></figure>
4. **Status:**
   *   Define the status that triggers the approval rule. These are some of the common statuses that could initiate the workflow:

       * **Approved:** Resource has been approved.
       * **Auto Approved:** The resource was automatically approved, possibly via predefined rules or conditions.
       * **Created:** A newly created resource awaiting approval.
       * **Draft:** Resource in the initial draft phase, not yet ready for approval.
       * **Recommended:** The resource has been marked as recommended for approval.
       * **Submitted:** Resource has been submitted for approval.
       * **Under Modification:** The resource is undergoing changes and requires reapproval after modification.

       <figure><img src="../../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>
5.  **Is Required:**

    * Select to this option to indicate if this approval step is mandatory. If marked as **Yes**, the resource cannot proceed to the next stage without the designated role’s approval.

    <figure><img src="../../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>
6. **Priority:**
   *   Set the priority for the approval step. This indicates the urgency level of the approval:

       * **Higher priority** means faster action is required to approve the resource, typically to avoid delays.
       * **Lower priority** could allow for more time in the approval process before escalation.

       <figure><img src="../../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>
7. **SLA Days/Hrs:**
   *   Specify the **Service Level Agreement (SLA)** for the approval time, expressed in **days or hours**. This defines the maximum allowable time within which the approval action must be completed.

       * If the action isn't completed within the specified SLA, an escalation process may be triggered.

       <figure><img src="../../.gitbook/assets/image (464).png" alt=""><figcaption></figcaption></figure>
8. **On Breach Action:**
   *   Define what should happen if the SLA is breached, i.e., if the approval action isn't completed in the allotted time:

       * **Move to next level:** The resource request is escalated to the next level or person in the approval hierarchy.
       * **Auto-Approve:** Automatically approve the resource if the SLA is breached without any action.

       <figure><img src="../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>
9.  **Rule Check:** For different resource types, certain rule checks can be applied. For example:

    * **Data source:** Rules like Connection Check, Catalogue Check, Domain Check, etc.
    * **Dataset:** Rules like DQ Check, EDA Check, Dictionary Check, etc.

    <figure><img src="../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>
10. **Add Row Button:**

    * Use this button to add additional approval rules to create complex workflows with multiple approval steps. This is helpful when different roles are responsible for different stages in the approval process.

    <figure><img src="../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>
11. **Delete Row Button:**

* Use the **Delete Row** button to remove any approval rule if it is no longer needed or valid. This can be useful to streamline the approval workflow if changes in policy or process occur.

<figure><img src="../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>

#### **Steps to Configure Resource Approval Settings**

1.  **Select Resource Type**

    Choose the type of resource for which you are setting up the approval workflow (e.g., **Datasource**,**Dataset**, **Model**, etc.).

<figure><img src="../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure>

2.  **Enable Auto Approval (Optional)**

    If you want to automate the approval process, toggle the **Auto Approval** button to "ON." This will automatically approve resources of the selected type without manual intervention.
3.  **Configure Manual Approval Workflow**

    If you choose not to use auto-approval, configure the manual approval workflow:

    1. Select the **Role** responsible for approval.
    2. Choose the **Action** (Approve, Reject, or Review).
    3. Set the **Status** that triggers this approval rule.
    4. Indicate whether the approval is **Required**.
    5. Assign the **Priority** of the approval.
    6. Set the **SLA Days/Hrs** to define the time window for approval.
    7. Define the **On Breach Action** to specify the action to take if the SLA is breached.

<figure><img src="../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure>

4.  **Add More Rules (Optional)**

    If necessary, click **Add Row** to create additional approval rules, specifying different roles, actions, or priorities.

<figure><img src="../../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure>

5.  **Save Configurations**

    Once all the approval rules are configured, make sure to save the changes to apply the new approval workflow.

<figure><img src="../../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure>

### **SMTP Configurations**

The SMTP Configuration in ScikIQ enables seamless email communication by setting up the email server through which notifications, alerts, and user communications are sent. Proper configuration is essential for ensuring reliable delivery of system-generated emails and for maintaining communication between users and the platform.

**Overview**

The SMTP Configuration in ScikIQ allows administrators to set up and manage the email system used for notifications, alerts, and other automated communications. Proper configuration ensures that ScikIQ can send emails reliably and securely.

**SMTP Configuration Components Overview**

When setting up SMTP configurations, administrators can define various parameters to ensure seamless email delivery. The following sections explain each component and the actions available in the email configuration interface.

#### **Email Configuration List Overview**

The Email Configuration List displays the various SMTP configurations that have been set up within ScikIQ. It allows administrators to view, manage, and edit existing configurations.

1. **Page Elements**
   1. **Show Entries**: A dropdown menu that allows users to select the number of entries displayed per page (e.g., 10, 25, or 50).
   2. **Search**: An input field that allows users to quickly search configurations by config name, host, port, or other related fields.
   3. **Add Configuration**: A button that opens the Email Settings Modal, where administrators can add a new SMTP configuration.
   4. **Pagination Controls**: Navigation to browse through multiple pages of email configurations when the list exceeds the displayed number of entries.

<figure><img src="../../.gitbook/assets/image (474).png" alt=""><figcaption></figcaption></figure>

**SMTP List Overview**

* **Config Name**: The display name for easy identification (e.g., Gmail SMTP, Production Email Server).
* **Host**: The SMTP server address (e.g., smtp.gmail.com).
* **Port**: The port used for SMTP connection:
* **From Mail**: The default email address used for outgoing messages.
* **Default Configuration**: Option to set this SMTP as the default server (only one can be default).
* **Username**: The username for SMTP authentication, typically an email address.
* **Created Date**: Date when the configuration was created.
* **Updated Date**: Date when the configuration was last modified.

**Actions**:

* **Edit**: Modify existing SMTP configuration.
* **Delete**: Remove configuration from the list.

<figure><img src="../../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

3.  **Add Configuration – Email Settings Modal**

    The Add Configuration modal is used to add a new SMTP configuration. Administrators can input the necessary details for the SMTP server and other settings

    1. **Config Name**: The display name for easy identification (e.g., Gmail SMTP, Production Email Server).

* **Host**: The SMTP server address (e.g., smtp.gmail.com).
* **Port**: The port used for SMTP connection:
  * 25 for standard (unencrypted) SMTP
  * 465 for SMTP over SSL (secure)
  * 587 for SMTP over TLS (secure and recommended)
* **From Mail**: The default email address used for outgoing messages.
* **Default Configuration**: Option to set this SMTP as the default server (only one can be default).
* **Use Authentication**: Checkbox to enable SMTP authentication.
* **Username**: The username for SMTP authentication, typically an email address.
* **Password**: The password for SMTP authentication.
* **Created Date**: Date when the configuration was created.
* **Updated Date**: Date when the configuration was last modified.

**Actions**:

* **Edit**: Modify existing SMTP configuration.
* **Delete**: Remove configuration from the list.
* **Save**: Save the new or edited configuration.
* **Close**: Cancel changes and close the configuration form.

<figure><img src="../../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>

#### **Email Template List Overview**

The Email Template List allows administrators to view and manage the templates used for various notifications and alerts in ScikIQ.

**Page Elements for the Email Template List**

* **Show Entries**: A dropdown to select how many templates to display.
* **Search**: A search field to find templates by title, caption, or subject.
* **Add Template**: A button to create a new email template.
* **Pagination Controls**: Navigation to browse through multiple pages of email templates.

<figure><img src="../../.gitbook/assets/image (478).png" alt=""><figcaption></figcaption></figure>

**Email Template List Columns**

* **Title**: The name of the email template (e.g., Asset Access Approval).
* **Caption**: A unique identifier for the email template (e.g., asset\_access\_approval).
* **Subject**: The subject line of the email.
* **Created Date**: The date when the template was created.
* **Updated Date**: The date when the template was last modified.
*   **Action**:

    * **Edit**: Allows editing the email template.
    * **Delete**: Removes the template if no longer needed.

    <figure><img src="../../.gitbook/assets/image (479).png" alt=""><figcaption></figcaption></figure>

***

#### **Example: How to Create a New Email Template in ScikIQ**

**Step 1: Access the Email Template Section**

* Navigate to the Admin Settings in the ScikIQ dashboard.
* Under Email Configuration, click on **Email Template List**.
* Click **Add Template** to open the Add New Template modal.

<figure><img src="../../.gitbook/assets/image (481).png" alt=""><figcaption></figcaption></figure>

**Step 2: Fill in Template Details**

* **Title** (Required): The name of your template (e.g., Policy Assignment Alert).
* **Caption** (Required): A unique identifier for internal reference (e.g., policy\_assignment).
* **Subject** (Required): The subject line (e.g., New Policy Assigned:New Policy Assigned: Data Curator).
* **Body** (Required): The content of the email, including placeholders for dynamic data&#x20;

<figure><img src="../../.gitbook/assets/image (482).png" alt=""><figcaption></figcaption></figure>

**Step 4: Save the Template**

Once all fields are completed, click **Save** to add the template. The template will appear in the Email Template List for management.

<figure><img src="../../.gitbook/assets/image (483).png" alt=""><figcaption></figcaption></figure>

### **Scheduler Server in ScikIQ**

The **Scheduler Server** in ScikIQ is designed to manage and execute scheduled jobs like data ingestion, transformation, and system tasks. It supports multiple instances, enabling distributed scheduling and efficient job execution across environments. This is a critical component in enabling automated workflows and ensuring precise control over task execution timing.

#### Scheduler Servers List

The **Scheduler Servers List** provides administrators with an overview of all configured scheduler servers. It allows monitoring, management, and modification of these servers from a centralized interface.

#### Functional Elements:

* **Show Entries**: Lets you control the number of servers displayed per page (e.g., 10, 25, 50).
* **Search Bar**: Enables quick filtering of servers using criteria such as name, host, or description.
* **Pagination Controls**: Helps navigate through multiple pages of server entries.
* **Add Configuration**: Opens the Scheduler Server Configuration form to add a new server.

<figure><img src="../../.gitbook/assets/image (484).png" alt=""><figcaption></figcaption></figure>

#### Scheduler Server List Fields

Each scheduler server entry displays the following fields:

1. **Name**: Internal system reference (e.g., `scheduler-prod-01`)
2. **Display Name**: Friendly name for UI identification (e.g., `Production Scheduler`)
3. **Description**: Brief explanation of what the server is used for
4. **Host**: Hostname or IP address (e.g., `scheduler.example.com`)
5. **Created At**: Timestamp when the configuration was first created
6. **Updated At**: Timestamp when it was last modified
7. **Action**: Icons or buttons to edit or delete the server.

<figure><img src="../../.gitbook/assets/image (485).png" alt=""><figcaption></figcaption></figure>

#### Adding a Scheduler Server: Step-by-Step

**Add a New Scheduler Server**

* Click on the **Add Configuration** button to open the Scheduler Server Configuration form.

<figure><img src="../../.gitbook/assets/image (486).png" alt=""><figcaption></figcaption></figure>

#### Fill in the Required Fields

* **Name**: Unique internal identifier (e.g., `scheduler-server7`)
* **Display Name**: Friendly name (e.g., `Server 7`)
* **Description**: Description of server function (e.g., “Handles nightly batch ETL jobs”)
* **Host**: Hostname or address (e.g., `scheduler7.example.com`)

> Make sure the **SERVER\_NAME** is unique, as it's used to create corresponding database tables.

<figure><img src="../../.gitbook/assets/image (488).png" alt=""><figcaption></figcaption></figure>

**Step 4: Save the Configuration**

Once all fields are filled out, click **Save Configuration** to add the new scheduler server to the system.

<figure><img src="../../.gitbook/assets/image (489).png" alt=""><figcaption></figcaption></figure>

#### Use Case: **Scheduling Data Processing Tasks Using a Scheduler Server**

**Purpose** - To automate the execution of data ingestion and processing tasks by scheduling them through ScikIQ Orchestrator using a designated Scheduler Server.

#### **Steps to Schedule a Data Processing Task**

1. **Create a Delta Pipeline**
   * Navigate to the **"Create Delta Pipeline"** submenu in ScikIQ Curate.
   * Design your pipeline using available nodes.
   * Click **"Save"** to submit the pipeline.

<figure><img src="../../.gitbook/assets/image (490).png" alt=""><figcaption></figcaption></figure>



* **Navigate to ScikIQ Orchestrator**
  * Go to **ScikIQ Curate** → **ScikIQ Orchestrator**.
  * Click the **"Create"** button to initiate a new scheduler job.

<figure><img src="../../.gitbook/assets/image (491).png" alt=""><figcaption></figcaption></figure>

* **Add a New Scheduler Job**
  * Drag and drop the **ETL Job node** onto the canvas.
  * In the **Action** dropdown, select the required ETL job(s).
  * Multiple ETL jobs can be selected and scheduled together.
* **Configure Frequency**
  * Choose the trigger type: **Run Once**, **Daily**, **Weekly**, or **Monthly**.
  * Example: Select **"Daily"**, then set the desired **date and time**.
  * Click **"Next"** to continue.

<figure><img src="../../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure>

* **Enter Job Details**
  * **Job Name**: `Daily Data Ingestion`
  * **Description**: `Ingests raw data from external sources for processing`
  * **Task Type**: `Data Processing`
  * **Execution Time**: `Daily at 2:00 PM`
* **Select Scheduler Server**
  * From the dropdown list, select a server (e.g., **Server 1** or **Production Scheduler**).
  * Choose other necessary scheduler settings.
  * Click **"Finish"** to finalize the job setup.

<figure><img src="../../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>



* **Verify the Job**
  * Ensure the job appears in the **Scheduler List**.
  * Confirm that the selected **server name** (e.g., `Server 1`) is correctly displayed.
  * Verify the job frequency is shown as **Daily**

<figure><img src="../../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure>









