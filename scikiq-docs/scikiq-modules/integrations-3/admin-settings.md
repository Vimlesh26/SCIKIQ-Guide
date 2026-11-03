---
icon: gear
---

# Admin Settings

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page explains how to configure Admin Settings. After creating the data source connection, the next step is configuring the Admin Settings.&#x20;

The **Admin Settings** page in SCIKIQ acts as the control center for managing important administrative functions. It contains the below mentioned four main tabs including Admin Setting, Resource Approval, SMTP  Configuration, Scheduler Servers, and Company Profile.

Each tab plays a key role in ensuring the platform works smoothly, securely, and efficiently.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Only the users with admin privileges can access and configure the Admin Settings.
> * If the Admin Settings are not properly configured, many features of SCIKIQ may not function correctly or securely.

***

### **Admin Settings**

{% tabs %}
{% tab title="Setup Admin Settings" %}
**Overview**

The **Admin Settings** section in SCIKIQ acts as the control center for managing important administrative functions. As part of configuring the admin settings, you need to set up the activities outlined in the expandable panels below. Once you have completed the configuration, click the **Save** button.

**Procedure**

{% hint style="info" %}
**Tip:** Expand the below panels to view step-by-step instructions.
{% endhint %}

<details>

<summary>Configure File Storage</summary>

**Purpose:**

Configuring the file storage enables to specify the location where the file will be stored. As part of the configuration,  you need to configure the connection as well.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click the **Admin Settings** under **Asset Management**.

<figure><img src="../../.gitbook/assets/Admin Settings.png" alt=""><figcaption><p>Navigating to Admin Settings</p></figcaption></figure>

The Admin Settings page is opened with the Admin Setting tab displayed by default.&#x20;

2\. On the **Admin Setting** tab, in the **File Storage** section _(See the below example image)_:

* From the [<mark style="color:blue;">**Storage Location**</mark>](#user-content-fn-1)[^1] drop-down box, select the **storage type.** For example, AWS S3, Azure Blob, Google Cloud.
* From the **Connection Name** drop-down box, select the **Connection Name.**

> <mark style="color:red;">**Note:**</mark> If no connections are available, create one. To know how to create, refer to [Creating a Data Source Connection](/broken/pages/KYPJ1EeiYPq5HSdryccS).

* Enable  the [<mark style="color:blue;">**Replicate users, groups & policies on Cloud Identity Manager**</mark>](#user-content-fn-2)[^2] option if required.&#x20;

<figure><img src="../../.gitbook/assets/File Storage2.png" alt=""><figcaption><p>File Storage Section</p></figcaption></figure>

</details>

<details>

<summary>Configure Dataset Storage</summary>

**Purpose:**

Configuring the Dataset Storage enables to define how datasets are saved within the SCIKIQ application — either as serialized files (Pickle) or structured tables (Database). Based on the selected option, different configuration fields will appear.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1\. In the **Save Dataset To** section, select **Pickle** or **Database** to specify the **format** where the dataset is to be stored.

2\. If you wish to select the [<mark style="color:blue;">**Pickle**</mark>](#user-content-fn-3)[^3] option:

A. From the **Dataset Storage Location** drop-down box, select the **Storage Type.** For example, AWS S3, Azure Blob, GCP Storage, or Local File System.

The selected connection will be used to store the dataset as a **.pkl** file.

B. **If you wish the dataset uses the file storage same as the file**, then enable **Same As File** <img src="../../.gitbook/assets/image (179).png" alt="" data-size="original">option.

C. Do not make any more selections after the above steps.

3\. If you wish to select the [<mark style="color:blue;">**Database**</mark>](#user-content-fn-4)[^4] option:

A. From the **Dataset Storage Location** drop-down box, select the required **option**.

B. In the [<mark style="color:blue;">**Prefix Table Name**</mark>](#user-content-fn-5)[^5] field, enter the **prefix table name**. For example, qa4\_, sales\_, etc.

<figure><img src="../../.gitbook/assets/Save Dataset.png" alt=""><figcaption><p>Saving Dataset</p></figcaption></figure>

</details>

<details>

<summary>Configure Auto Gen Vector</summary>

**Purpose:**

Configuring [<mark style="color:blue;">**Auto Gen Vector**</mark>](#user-content-fn-6)[^6] allows you to select a database, such as Chroma DB, to store automatically generated vectors for AI/ML integrations. This is especially useful for machine learning workflows that rely on document embeddings and other vectorized data.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

* From the **Auto Gen Vector Storage Location** drop-down box, select a **vector database**. For example, Chroma DB. See the below image.

<figure><img src="../../.gitbook/assets/Save Auto.png" alt=""><figcaption><p>Configuring Auto Gen Vector </p></figcaption></figure>

</details>

<details>

<summary>Configure Reject Logs Location</summary>

**Purpose:**

Configuring the reject logs location allows you to capture and store all failed or rejected operations, such as invalid file uploads, failed validations, or unauthorized access attempts. The benefits of reject logs include:

* Recording the reasons for failures across the platform
* Supporting auditing, troubleshooting, and debugging

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. In the **Reject Logs** section, from the **Storage Location** drop-down box, select the **location**.
2. From the **Connection Name** drop-down box, select the **connection**.

<figure><img src="../../.gitbook/assets/Reject Logs.png" alt=""><figcaption><p>Configuring Reject Logs</p></figcaption></figure>

</details>

<details>

<summary>Configure Service Details</summary>

**Purpose:**

Configuring the service details allows you to set up service-related credentials, such as the Service ID and Application ID, which are required for internal and external system integrations.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. In the **Service Details** section, from the **Connection Details** drop-down box, select the required **connection**.

The connection data related to the selected connection appear in the adjacent Connection Data drop-down box.

2. Now, from the **Connection Data** drop-down box, select the applicable **connection data**.
3. From the **Service ID** drop-down box, select the applicable **service Id**.
4. From the **Application ID** drop-down box, select the applicable **application Id**.

{% hint style="info" %}
**Tip:** You can get the service details from your IT dept. or Platform team.
{% endhint %}

<figure><img src="../../.gitbook/assets/Service Details.png" alt=""><figcaption><p>Configuring Service Details</p></figcaption></figure>

</details>

<details>

<summary>Configure LLM API</summary>

**Purpose:**

Configuring the LLM API allows you to connect the SCIKIQ application with external LLMs (Large Language Models). As part of the process, you need to input the API credentials to enable advanced NLP and AI features like text summarization, document understanding, etc.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. In the **LLM API** section, from the **Save LLM API** drop-down box, select the required **connection**.
2. Input the **API key** or **Credentials**.

<figure><img src="../../.gitbook/assets/Save LLM.png" alt=""><figcaption><p>Cinfiguring LLM API</p></figcaption></figure>

</details>

<details>

<summary>Configure Password Expiry Settings</summary>

**Purpose:**

Configuring the password expiry settings allows you to define how long user passwords remain valid. You can also set reminder intervals to notify users before their passwords expire.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. In the **Password Expiry Setting** section, specify the **number of days** for **password expiry**.
2. In the **Password Change Reminder 1** field, specify the number of **days** before the password expiry when users should receive their **first** notification.
3. In the **Password Change Reminder 2** field, specify the number of **days** before the password expiry when users should receive their **last** notification.

<figure><img src="../../.gitbook/assets/Password Expiry.png" alt=""><figcaption><p>Configuring Password Expiry Settings</p></figcaption></figure>

</details>

<details>

<summary>Configure Allowed Domains</summary>

**Purpose:**

Configuring the allowed domain restricts user registration only to the domains that are configured in the Allowed Domain field. This ensures that only authorized users can access SCIKIQ.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

* In the **Domain** field of **Allowed Domains** section, enter the allowed **domains** for user registrations. For example, SCIKIQ.com

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> 1. Based on the requirement, you can configure multiple domains for user registration.
> 2. Domain checks are not case-sensitive.
> 3. Click **Update** after changing the domain settings.

<figure><img src="../../.gitbook/assets/Allowed Domain.png" alt=""><figcaption><p>Configuring Allowed Domains</p></figcaption></figure>

</details>

<details>

<summary>Configure Multiple Device Login</summary>

**Purpose**

Configuring Multiple Device Login allows multiple users to login using the same login credentials.

**Procedure**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

* In the **Multiple Device Login** section, from the **Multiple Device Login** drop-down box, select **Yes** if you wish to allow multiple users to login using the same login credentials.

<figure><img src="../../.gitbook/assets/Multiple Device.png" alt=""><figcaption><p>Configuring Multiple Device Login</p></figcaption></figure>

</details>
{% endtab %}

{% tab title="Resource Approval" %}
**Overview**

The **Resource Approval** tab in ScikIQ allows administrators to define approval workflows for various resources within the platform. This is essential for managing which resources (such as datasets, models, or integrations) require manual approval and for automating the approval process where needed. By setting approval rules, administrators can enforce structured workflows and ensure proper validation before resource utilization.

**Procedure**

The module consists of two main sections:

* **Auto Approval**
* **Manual Approval**

These sections help manage approvals efficiently while ensuring governance and control over resources.

<details>

<summary><strong>1.Auto Approval</strong></summary>

**Overview**

The **Auto Approval** feature automates the approval process for certain resources based on predefined rules or conditions. This allows resources to be automatically approved without requiring manual intervention, streamlining workflows and reducing the need for constant oversight.&#x20;

**Procedure**

* **Resource Type**: Select the type of resource for which automatic approval is enabled. This could include datasets, models, or other system integrations.
* **Auto Approval Toggle**: Use this toggle to enable or disable auto-approval for the selected resource type. When enabled, the resource will automatically be approved once it is submitted, bypassing the manual approval workflow.

1.  **Enable the Auto Approval Toggle Button**

    * Locate the **Auto Approval** toggle switch within the approval configuration section.
    * Set the toggle to **Enabled** to activate the auto approval functionality for the selected resource types.

    <figure><img src="../../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>
2. **Auto Approval Status**
   1. When **Auto Approval** is enabled, the resource will bypass the manual approval process, and the status will be automatically set as **Approved**.&#x20;
   2. This means the resource has been approved without requiring a manual intervention.
3. **Available Statuses for Auto Approval**
   1. **Approved:** The resource is automatically approved by the system, and no further approval steps are required.
   2. **Auto Approved:** Indicates that the resource was approved automatically, often due to predefined conditions or rules.
   3. **Created:** A new resource is created but hasn't yet been reviewed. It’s in the initial state of the approval process.
   4. **Draft:** The resource is still being worked on and is not yet ready for approval. It can be reviewed again before approval.
   5. **Recommended:** The resource is flagged as recommended for approval but requires a final decision.
   6. **Submitted:** The resource has been submitted for approval by a user or system, awaiting manual or automatic approval.
   7. **Under Modification:** If changes are made to a resource, it will require re-approval. This status indicates that the resource is being modified and needs revalidation.

<figure><img src="../../.gitbook/assets/image (453).png" alt=""><figcaption></figcaption></figure>

4. **Field Type Selection**
   1. Select the **Field Type** for which you wish to enable auto approval. The options available will depend on the types of resources in your system. Common resource types include:
      1. **Catalogue:** A collection or classification of data resources.
      2. **Domain:** Specific areas or categories of data, typically at a higher organizational level.
      3. **Entity:** Represents an individual resource, like a database or dataset.
      4. **Role:** Roles or responsibilities related to data access and management.
      5. **Sub-domain:** A subset of a domain, often representing more specific categories.
      6. **Users:** User accounts and associated permissions.

<figure><img src="../../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>

5. **Field Selection**
   1. Choose the **Field** on which the auto approval rule will be applied. The available options will depend on the selected **Fields Type**. For example:
      1. **Catalogue:** The auto approval rule could be based on a specific catalogue name.
      2. **Domain:** Select specific domains to apply auto approval for.
      3. **Entity:** Specify particular entities or resources that will be auto-approved.
   2. Once the **Resource Type** is selected, the **Field** options will automatically adjust to show relevant options that correspond to the resource type. For example, if **Catalogue** is selected, the field options might include a list of available catalogues.
6. **Operator Selection**
   1. Choose the **Operator** to define how the selected **Field** will be compared to the **Values**:
      1. **Equals:** The field value must exactly match the specified value (e.g., the catalogue name is exactly the one selected).
      2. **In:** The value must be one of a list of selected options (e.g., the resource must be in one of several selected domains).
      3. **Not Equal:** The value must not match the specified value.
      4. **Not In:** The value must not belong to any of the selected options.

<figure><img src="../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

7. **Value Selection**
   1. After selecting the **Field** and **Operator**, the **Values** field will populate based on the field you’ve chosen. The system will display the available options relevant to the field. For example:
      1. If **Catalogue** is selected as the field, the **Values** will display a list of available catalogues in your system.
      2. If **Domain** is selected, the values will show the different domains in your organization.
      3. If **Entity** is selected, the available entities will be displayed for you to choose from.

<figure><img src="../../.gitbook/assets/image (457).png" alt=""><figcaption><p>Choose the appropriate value(s) for the auto approval condition.</p></figcaption></figure>

</details>

<details>

<summary><strong>2.Manual Approval</strong></summary>

**Overview**

The **Manual Approval** section allows administrators to configure approval workflows, offering granular control over how resources are approved within the system. This ensures that only authorized users are able to approve or reject resources, based on predefined conditions and roles.

**Procedure**&#x20;

1. **Resource Type**
   1.  This defines the type of resource being requested for approval. Common resource types include.

       1. **Data source:** For database connections or data sources.
       2. **Dataset:** For data collections or datasets.
       3. **Dashboard:** For analytical or reporting dashboards.
       4. **Business Data Event:** Events related to business data operations.

       <figure><img src="../../.gitbook/assets/image (458).png" alt=""><figcaption></figcaption></figure>
2. **Role**
   1. Select the role that will be responsible for approving the resource request. The role chosen will have the authority to approve or reject the resource based on the workflow.
   2. Example roles could include:
      1. **Admin:** A top-level role with full approval rights.
      2. **Data Engineer:** Responsible for reviewing and approving technical resources.
      3. **Data Owner:** Person in charge of approving datasets, often a business owner or manager.

<figure><img src="../../.gitbook/assets/image (459).png" alt=""><figcaption></figcaption></figure>

3. **Action**
   1. Choose the action the selected role will take on the resource request. Available actions include.
      1. **Approve:** Grant approval for the resource, allowing it to proceed further in the workflow.
      2. **Concur:** A conditional approval, where the role agrees with the resource but requests further review or conditions.
      3. **Pending:** Marks the resource as awaiting action, no approval or rejection has been made yet.
      4. **Recommend:** Suggests approval or further review, but doesn't directly approve the resource.

<figure><img src="../../.gitbook/assets/image (460).png" alt=""><figcaption></figcaption></figure>

4. **Status**
   1. Define the status that triggers the approval rule. These are some of the common statuses that could initiate the workflow.
      1. **Approved:** Resource has been approved.
      2. **Auto Approved:** The resource was automatically approved, possibly via predefined rules or conditions.
      3. **Created:** A newly created resource awaiting approval.
      4. **Draft:** Resource in the initial draft phase, not yet ready for approval.
      5. **Recommended:** The resource has been marked as recommended for approval.
      6. **Submitted:** Resource has been submitted for approval.
      7. **Under Modification:** The resource is undergoing changes and requires reapproval after modification.

<figure><img src="../../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>

5. **Is Required**
   1. Select to this option to indicate if this approval step is mandatory. If marked as **Yes**, the resource cannot proceed to the next stage without the designated role’s approval.

<figure><img src="../../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>

6. **Priority**
   1. Set the priority for the approval step. This indicates the urgency level of the approval
      1. **Higher priority** means faster action is required to approve the resource, typically to avoid delays.
      2. **Lower priority** could allow for more time in the approval process before escalation.

<figure><img src="../../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>

7. **SLA Days/Hrs.**
   1. Specify the **Service Level Agreement (SLA)** for the approval time, expressed in **days or hours**. This defines the maximum allowable time within which the approval action must be completed.
   2. If the action isn't completed within the specified SLA, an escalation process may be triggered.

<figure><img src="../../.gitbook/assets/image (464).png" alt=""><figcaption></figcaption></figure>

8. **On Breach Action**
   1. Define what should happen if the SLA is breached, i.e., if the approval action isn't completed in the allotted time.
      1. **Move to next level:** The resource request is escalated to the next level or person in the approval hierarchy.
      2. **Auto-Approve:** Automatically approve the resource if the SLA is breached without any action.

<figure><img src="../../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

9. **Rule Check:** For different resource types, certain rule checks can be applied. For example.
   1. **Data source:** Rules like Connection Check, Catalogue Check, Domain Check, etc.
   2. **Dataset:** Rules like DQ Check, EDA Check, Dictionary Check, etc.

<figure><img src="../../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>

10. **Add Row Button**
    1. Use this button to add additional approval rules to create complex workflows with multiple approval steps. This is helpful when different roles are responsible for different stages in the approval process.

<figure><img src="../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>

11. **Delete Row Button**
    1. Use the **Delete Row** button to remove any approval rule if it is no longer needed or valid. This can be useful to streamline the approval workflow if changes in policy or process occur.

<figure><img src="../../.gitbook/assets/image (468).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Setup SMTP" %}
**Overview**

This section explain how to configure the SMTP settings in the SCIKIQ application. SMTP configuration refers to providing the necessary server details—such as the SMTP host, port, username, password, and security settings—to enable the application to send emails.&#x20;

Configuring SMTP is essential because:

* Applications cannot send emails without a properly set email server connection.
* It ensures email delivery through a secure and authenticated channel.
* You control the email-sending identity (From address, domain, branding).
* It prevents emails from landing in spam by using an authenticated mail server.
* It ensures compliance with email delivery standards and security policies

***

#### Procedure

As part of the SMTP configuration in the SCIKIQ application, you can add an email configuration by providing details such as the **Configuration Name, Host Number (SMTP server address), Port Number, From Email ID, Default Configuration selection, Use Authentication option, Username,** and **Password.** Based on your needs, you can also update or delete an existing email configuration.&#x20;

In addition, the SCIKIQ application allows you to **create, update,** and **delete** email templates as required.

Expand the below panels to understand how to add both email configurations and email templates in the SCIKIQ application along with the process of updating and deleting them.

<details>

<summary>1.Add Email Configuration</summary>

**Purpose:**

[<mark style="color:blue;">**SMTP**</mark>](#user-content-fn-7)[^7] is the standard protocol used to send emails over the internet. The **SMTP configuration** refers to setting up the required server details (such as SMTP host, port, username, and password, etc.) so that the application can send emails reliably. &#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click the **Admin Settings** under **Asset Management**.

<figure><img src="../../.gitbook/assets/Admin Settings.png" alt=""><figcaption><p>Admin Settings Menu Item</p></figcaption></figure>

The Admin Settings page is opened.&#x20;

2\. On the **Admin Settings** page, click the **SMTP Configuration** tab.

The Email Configuration List tab is displayed.

3\. On the **Email Configuration** **List** tab, click the **Add Configuration** button.

<figure><img src="../../.gitbook/assets/Add Configuration.png" alt=""><figcaption><p>Add Configuration Button</p></figcaption></figure>

The Email Configuration dialogue box is displayed.

4\. On the **Email Configuration dialogue box** (See the below example image)**:**

A. In the **Email Config Name** field,  enter a **name** for the **email configuration.** For example, Gmail SMTP, Production Email Server, etc.

B. In **Host** field,  enter the **SMTP server address.** For example, smtp.office365.com.

C. In the **Port** field, enter the **port number** used for SMTP connection.

{% hint style="info" %}
**Tip:**&#x20;

* 25 for standard (unencrypted) SMTP
* 465 for SMTP over SSL (secure)
* 587 for SMTP over TLS (secure and recommended)
{% endhint %}

D. In the **From Mail** field, enter the **default email address** used for **outgoing messages**.

E. Enable the **Default Configuration** option if you wish to **set this SMTP as the default server.**

{% hint style="info" %}
**Tip:** Only one SMTP can be made as default server.
{% endhint %}

F. Enable  the **Use Authentication** option if you wish to make the **SMTP authentication use secure login credentials.**

G. In the **Username** field, specify a **username for SMTP authentication.**

{% hint style="info" %}
**Tip:** The username is generally an email address.
{% endhint %}

&#x20;H. Click the save button.

<figure><img src="../../.gitbook/assets/Email Config dialogue box.png" alt="" width="369"><figcaption><p>Email Configuration</p></figcaption></figure>

The email configuration is created and displayed on the Email Configuration List tab. See the below image.

<figure><img src="../../.gitbook/assets/Email Config 1.png" alt=""><figcaption><p>Creation of Email Configuration</p></figcaption></figure>

</details>

<details>

<summary>2.Update Email Configuration</summary>

**Overview:**

If required, you can update an email configuration. As part of updating, you can modify the details including Email Config Name, Host, Port, From Email, and Default Configuration, etc.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. On the **Email Configuration** **List** tab, click the **Edit** icon ![](<../../.gitbook/assets/image (180).png>) corresponding to the required email config.

<figure><img src="../../.gitbook/assets/Email config Edit.png" alt=""><figcaption><p>Edit Icon</p></figcaption></figure>

The Email Configuration dialogue box is displayed.

2. On the **Email Configuration** dialogue box, make the required changes, and then click the **Save** button at the bottom.

The Email Config is updated.

</details>

<details>

<summary>3.Delete Email Configuration</summary>

**Overview:**

If required, you can delete an email configuration. Once deleted, it will be removed from the Email Configuration List.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

* On the **Email Configuration** **List** tab, click the **Delete**![](<../../.gitbook/assets/image (181).png>)  icon  corresponding to the required email config.

<figure><img src="../../.gitbook/assets/EMail Config Delete.png" alt=""><figcaption><p>Delete Icon</p></figcaption></figure>

The email config is removed from the Email Configuration List,

</details>

<details>

<summary>4.Add Email Template</summary>

**Purpose:**

The purpose of email templates is to deliver consistent, branded, and automated communication to users.  The templates work together with SMTP to streamline and standardize the entire email-sending process. &#x20;

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1\. On the **Left Navigation Bar** of the **SCIKIQ** application, click the **Admin Settings** under **Asset Management**.

<figure><img src="../../.gitbook/assets/Admin Settings.png" alt=""><figcaption><p>Admin Settings Menu Item</p></figcaption></figure>

The Admin Settings page is opened.&#x20;

2\. On the **Admin Settings** page, click the **SMTP Configuration** tab.

The Email Template List tab is displayed.

3\. On the **Email Template List** tab, click the **Add Template** button.

<figure><img src="../../.gitbook/assets/Add email template.png" alt=""><figcaption><p>Add Template Button</p></figcaption></figure>

The Email Template dialogue box is displayed.

4\. On the **Email Template** dialogue box (See the below example image):

A. In the **Title** field, enter an **appropriate name** for the **email template**. For example, Forgot Password communication.

B. In the **Caption** field,  enter a **unique identifier** for the email template. For example, Forgot\_Password\_communication.

C. In the Subject field, enter an **appropriate subject** for the email template.

D. In the **Body** box, enter the **content** of the email, including placeholders for dynamic data.

<figure><img src="../../.gitbook/assets/Email Temp dialogue box.png" alt=""><figcaption><p>Configuring Email Template Data</p></figcaption></figure>

The email template is created and displayed on the Email Template List tab.&#x20;

</details>

<details>

<summary>5.Update Email Template</summary>

**Overview:**

If required, you can update an email template. As part of updating, you can modify the details including title, caption, subject, and body text.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

1. On the **Email Template** **List** tab, click the **Edit** icon ![](<../../.gitbook/assets/image (180).png>) corresponding to the required email template.

<figure><img src="../../.gitbook/assets/Edit Email Temp.png" alt=""><figcaption><p>Email Template - Update Icon</p></figcaption></figure>

The Email Template dialogue box is displayed.

2. On the **Email Template** dialogue box, **make the required changes**, and then click the **Save** button at the bottom.

The email template is updated.

</details>

<details>

<summary>6.Delete Email Template</summary>

**Overview:**

If required, you can delete an email template. Once deleted, it will be removed from the Email Template List.

**Procedure:**

The below step-by-step instructions describe the procedure:

**Step-by-Step Instructions:**&#x20;

* On the **Email Template** **List** tab, click the **Delete**![](<../../.gitbook/assets/image (181).png>)  icon  corresponding to the required email template.

<figure><img src="../../.gitbook/assets/Delete Email Temp.png" alt=""><figcaption><p>Email Template - Delete Icon</p></figcaption></figure>

The email template is deleted and removed from the Email Template List.

</details>
{% endtab %}

{% tab title="Scheduler Servers" %}
**Overview**

The **Scheduler Server** in ScikIQ is designed to manage and execute scheduled jobs like data ingestion, transformation, and system tasks. It supports multiple instances, enabling distributed scheduling and efficient job execution across environments. This is a critical component in enabling automated workflows and ensuring precise control over task execution timing.

**Procedure**

<details>

<summary><strong>1.Scheduler Servers List</strong></summary>

The **Scheduler Servers List** provides administrators with an overview of all configured scheduler servers. It allows monitoring, management, and modification of these servers from a centralized interface.

1. **Functional Elements**
   1. **Show Entries**: Lets you control the number of servers displayed per page (e.g., 10, 25, 50)
   2. **Search Bar**: Enables quick filtering of servers using criteria such as name, host, or description.
   3. **Pagination Controls**: Helps navigate through multiple pages of server entries.
   4. **Add Configuration**: Opens the Scheduler Server Configuration form to add a new server.

<figure><img src="../../.gitbook/assets/image (1760).png" alt=""><figcaption></figcaption></figure>

2. **Scheduler Server List Fields**
   1. Each scheduler server entry displays the following fields.
      1. **Name**: Internal system reference (e.g., `scheduler-prod-01`)
      2. **Display Name**: Friendly name for UI identification (e.g., `Production Scheduler`)
      3. **Description**: Brief explanation of what the server is used for
      4. **Host**: Hostname or IP address (e.g., `scheduler.example.com`)
      5. **Created At**: Timestamp when the configuration was first created
      6. **Updated At**: Timestamp when it was last modified
      7. **Action**: Icons or buttons to edit or delete the server.

<figure><img src="../../.gitbook/assets/image (1761).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Add New Server</strong></summary>

1. **Add a New Scheduler Server**
   1. Click on the **Add Configuration** button to open the Scheduler Server Configuration form.

<figure><img src="../../.gitbook/assets/image (1762).png" alt=""><figcaption></figcaption></figure>

2. **Fill in the Required Fields**
   1. **Name**: Unique internal identifier (e.g., `scheduler-server7`)
   2. **Display Name**: Friendly name (e.g., `Server 7`)
   3. **Description**: Description of server function (e.g., “Handles nightly batch ETL jobs”)
   4. **Host**: Hostname or address (e.g., `scheduler7.example.com`)

> Make sure the **SERVER\_NAME** is unique, as it's used to create corresponding database tables.

<figure><img src="../../.gitbook/assets/image (1763).png" alt=""><figcaption></figcaption></figure>

3. **Save the Configuration**
   1. Once all fields are filled out, click **Save Configuration** to add the new scheduler server to the system.

<figure><img src="../../.gitbook/assets/image (1764).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Company Profile" %}
**Overview**

The **Company Profile** tab allows you to configure and manage your organization's profile information. It enables you to enter essential company details, such as the company name and other relevant information, to establish your organization's identity within the application. You can also upload your company logo, which is displayed across supported areas of the platform to provide a consistent organizational branding.

Procedure

1. On the Company Profile tab, enter **Company Name, Welcome Text,** and **Contact Details.**
2. In the **Company Logo** area, upload your **company logo**.

> <mark style="color:red;">**Note:**</mark> Only **PNG, JPG, WEBP,** and **SVG** image formats are supported. The maximum allowed file size for the logo is **1 MB**.

3. Click the **Save Changes** button at the bottom of the page.

<figure><img src="../../.gitbook/assets/image (2499).png" alt=""><figcaption></figcaption></figure>

The company logo is configured.
{% endtab %}
{% endtabs %}

***

### **Related Topics**

* [**User Activity**](../integrations-2/user-activity.md)

[^1]: The **Storage Location** refers to the type of storage.

[^2]: This setting makes sure that the **same users, roles, and permissions you manage in SCIKIQ are also applied in the connected cloud identity system**, so access remains secure and consistent.

[^3]: Selecting the **Pickle** option saves datasets as serialized `.pkl` files. This format is optimized for machine learning and data science, allowing for efficient reloading of data for modeling and analysis.

[^4]: Selecting the **Database** option exports datasets as tables within a connected database. This method is optimized for structured data workflows, facilitating SQL querying, reporting, and seamless integration with external data pipelines.

[^5]: Configuring the **Prefix Table Name** lets you add a tag or keyword at the beginning of table names so they stay organized, unique, and easy to identify

[^6]: The full form of Auto Gen Vector is Automatically Generated Vector Embeddings. In AI, **vectors** usually mean **vector embeddings**—numerical representations of text, images, audio, or other data. So the meaning of **Save Auto Gen Vector** is - automatically generate vector embeddings and save them for later use.

[^7]: Simple Mail Transfer Protocol
