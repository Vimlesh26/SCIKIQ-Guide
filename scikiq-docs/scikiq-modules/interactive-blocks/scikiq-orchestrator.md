---
icon: calendar-circle-exclamation
---

# SCIKIQ Orchestrator

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview <a href="#aiyjzqcxbeam" id="aiyjzqcxbeam"></a>

The **Orchestrator** module enables you to create and manage schedulers that automatically run jobs or pipelines at predefined times or based on specific conditions. It helps automate tasks such as ETL jobs, data refreshes, and report generation without manual intervention. You can create, modify, pause, resume, or delete schedulers as needed.&#x20;

The module also provides access to change history, SLA history, and execution logs for monitoring and auditing scheduler activities.

***

### Procedure <a href="#br8cm8epmiq" id="br8cm8epmiq"></a>

Creating a scheduler involves a series of steps, including selecting the job, defining the frequency, specifying external dependency, and completing the configuration. As part of job selection, a pipeline is created by adding an ETL Job node, Metadata Refresh node, and Connection Refresh node. This ensures the correct execution order, manages dependencies, enables centralized scheduling, and improves overall reliability.

Subsequently, the frequency is defined to determine how often and when the pipeline should run automatically (for example, hourly, daily, or weekly). As part of the scheduler configuration, it is also specified whether the pipeline should run independently or depend on another schedule or job before execution.

In the final step, details such as Scheduler Name, Description, Server, Catalogue, Business Owner, and Technical Owner are provided. Once the configuration is completed, the scheduler is created and displayed on the SCIKIQ Schedules page.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Access SCIKIQ Orchestrator</strong></summary>

1. On the SCIKIQ left navigation bar, click **SCIKIQ Orchestrator** under **SCIKIQ CURATE.**

<figure><img src="../../.gitbook/assets/unknown (2).png" alt=""><figcaption><p align="center">SCIKIQ Orchestrator Menu Item</p></figcaption></figure>

The Scheduler page is displayed.

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

2. On the **Scheduler** page, click **Create Scheduler**.&#x20;

nel is expanded.

1. On the Schedule SLA panel, select the Active checkbox.
2. In the SLA Definition section, specify the SLA duration.

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> SLA Duration specifies the maximum time allowed for the job or pipeline to complete from its start time. It sets a clear performance expectation for execution. If the job runs longer than this duration, it is considered an SLA breach. This helps in tracking efficiency and identifying performance issues.</td></tr></tbody></table>

5. Next, specify the SLA Tolerance.

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top">Note: SLA Tolerance defines an additional buffer time allowed beyond the SLA duration before raising alerts or marking a failure. It accounts for minor or acceptable delays due to system or network fluctuations. This prevents unnecessary alerts for small deviations. It helps differentiate between critical delays and manageable ones .</td></tr></tbody></table>

6. If you want to send a warning email in case the schedule is completed later than the average time, then select the ![](<../../.gitbook/assets/unknown (6).png>) checkbox, and then specify the From and To settings.
7. If you want to Kill running job when SLA + tolerance limit is breached, then select the ![](<../../.gitbook/assets/unknown (7).png>) checkbox.

<figure><img src="../../.gitbook/assets/unknown (8).png" alt=""><figcaption><p align="center">ETL Job Node - Property Sheet</p></figcaption></figure>

<mark style="color:blue;">**Job Parameters**</mark>

The parameters run\_by, run\_on, run\_time, resource\_key, and scheduler\_run\_id are system-generated runtime parameters that provide context about a job execution. They are automatically populated when the scheduler triggers the pipeline and are primarily used for tracking, monitoring, and auditing purposes.

<figure><img src="../../.gitbook/assets/unknown (9).png" alt=""><figcaption><p>  ETL Job Parameters</p></figcaption></figure>

**ETL Job Parameters Description**

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Parameter</strong></td><td valign="top"><strong>Meaning</strong></td><td valign="top"><strong>Purpose</strong></td></tr><tr><td valign="top">run_by</td><td valign="top">Identifies the user or system account that triggered the job execution.</td><td valign="top">Useful for audit tracking and debugging—you can know who initiated the process (manual user, scheduler, or service account)</td></tr><tr><td valign="top">run_on</td><td valign="top">The date on which the job was executed.</td><td valign="top">Helps in logging, reporting, and partitioning data based on execution date.</td></tr><tr><td valign="top">run_time</td><td valign="top">The exact time the job started (or was triggered).</td><td valign="top">Useful for monitoring job duration, sequencing jobs, and troubleshooting delays.</td></tr><tr><td valign="top">resource_key</td><td valign="top"><p>Typically represents a specific resource identifier, such as:</p><p>●      Dataset / file / table reference</p><p>●      Environment-specific key</p><p> </p></td><td valign="top">Used for dynamic resource allocation or parameterizing data sources/targets.</td></tr><tr><td valign="top">scheduler_run_id</td><td valign="top">A unique execution ID generated by the scheduler</td><td valign="top"><p>Tracks a specific run instance</p><p>Helps correlate logs across systems</p></td></tr></tbody></table>

<mark style="color:blue;">**Setup Failure and Success Conditions**</mark>

1. **Setting Up Failure Condition**
   1. On the ETL JOB Property Sheet, click the On Condition tab.
   2. The Failure tab is displayed by default.
   3. From the Action drop-down box,  select the required option choosing from Move to Next Week, Abort and Raise Incident, Send Mail-Move to Next Week, or Send Mail-Abort and Raise Incident. For example, Move to Next Week.
   4. In the Message box, enter the appropriate message.

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If Send Mail-Move to Next Week or Send Mail-Abort and Raise Incident chose,  then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/unknown (10).png" alt=""><figcaption><p align="center">Property Sheet - Failure Settings</p></figcaption></figure>

2. **Setting Up Success Condition**
   1. In the ETL JOB Property Sheet, click the On Condition tab.
   2. Next, click the Success tab.
   3. From the Action drop-down box, select the required option choosing from Move to Next Week, Abort and Raise Incident, Send Mail-Move to Next Week, or Send Mail-Abort and Raise Incident. For example, Move to Next Week.
   4. In the Message box, enter the appropriate message.

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If Send Mail-Move to Next Week or Send Mail-Abort and Raise Incident chose,l then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

<p align="center"></p>

**3.3.3.2.3.5.** \
**3.3.2.3.6.**

The Connection Refresh node ensures that all required data source and target connections are active and valid before execution. It refreshes authentication tokens, credentials, or sessions to maintain uninterrupted connectivity. This step helps in identifying and resolving connection issues early in the pipeline.

The procedure to configure the Connection Refresh Node involves steps including:

●      Adding Connection Refresh node to the pipeline canvas

●      Selecting connection

●      Setting up Failure and Success conditions

The following sections provide detailed guidance on setting up the ETL Job node.

**3.3.2.4.1. Add Connection Refresh Node on the Main Workspace**

1. On the Scheduler page, from the left navigation bar, drag the Connection Refresh Node on to the Main Workspace.

The Properties Sheet section is displayed on the right side.

2.

**3.3.4.1. Overview**

This is the final step in the scheduler creation process. As part of this, you can specify the Scheduler Name, Description, Server, Catalogue, Business Owner, and Technical Owner. &#x20;

**3.3.4.2. Procedure**

1. In the Finish section, enter all the mandatory details including Scheduler Name, Description, Server, Catalogue, Business Owner, and Technical Owner.
2. Click the Finish button.

<figure><img src="../../.gitbook/assets/unknown (28).png" alt=""><figcaption><p align="center">Scheduler Details</p></figcaption></figure>

The scheduler is created on the Scheduler List page. See the image below.

<figure><img src="../../.gitbook/assets/unknown (29).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>2.<strong>Configure ETL Job Node</strong></summary>

**Overview**

Select Job is the first step in creating a scheduler. As part of this step, you need to create a pipeline to orchestrate dependent tasks—ETL execution, metadata synchronization, and connection validation—into a single controlled workflow. This ensures the correct execution order, manages dependencies, enables centralized scheduling, and improves reliability.

The ETL Job node performs the core data extraction, transformation, and loading process, the Metadata Refresh node synchronizes schema changes to prevent inconsistencies, and the Connection Refresh node ensures valid and active system connectivity. Together, these nodes enable accurate, reliable, and efficient pipeline execution.

**Configure ETL Job Node**

The ETL Job node is responsible for executing the core data processing workflow, including extraction, transformation, and loading of data. It applies business rules and data transformations to convert raw data into a usable format. This node ensures that data is accurately moved from source systems to target systems.

The procedure to configure the ETL job node involves steps including:

* Adding ETL Job Node to the pipeline canvas
* Choosing an ETL Job
* Scheduling SLA
* Setting up Failure and Success conditions

**Procedure**

The following sections provide detailed guidance on setting up the ETL Job node.

1. On the **Scheduler page**, click the **Create** button in **Create Scheduler.**

<figure><img src="../../.gitbook/assets/unknown (3).png" alt=""><figcaption><p align="center">Scheduler Page</p></figcaption></figure>

3. The **Scheduler page** is displayed.&#x20;
4. On the **Scheduler page**, from the **left navigation bar**, drag the **ETL Job Node** on to the **Main Workplace.**

<figure><img src="../../.gitbook/assets/unknown (4).png" alt=""><figcaption><p align="center">ETL Job Node</p></figcaption></figure>

5. The Property Sheet section is displayed on the right side.

<mark style="color:blue;">**Choose an ETL Job**</mark>

1. On the **Properties Sheet,** click the **Action** tab if it is not already displayed by default.
2. On the **Action** tab, select an **ETL Job** either from the **Choose from a list of ETL Jobs** drop-down box or select from the **Recent Jobs.**

<figure><img src="../../.gitbook/assets/unknown (5).png" alt=""><figcaption><p align="center">Selecting ETL Job</p></figcaption></figure>

<mark style="color:blue;">**Schedule SLA**</mark>

**Purpose**

Scheduling an SLA (Service Level Agreement) defines the expected completion time or deadline for your pipeline or job. It helps ensure that critical processes (like ETL jobs) finish within a committed time window. This is important for business operations that depend on timely data availability. It also enables monitoring and alerts if the job is delayed or misses its target.

**Procedure**

1. On the **Property Sheet** section, expand the **Schedule SLA panel**.
2. The **Schedule SL**A panel is expanded.
3. On the **Schedule SLA** panel, select the **Active** checkbox.
4. In the **SLA Definition** section, specify the **SLA duration.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note</strong></mark><strong>: SLA Duration</strong> specifies the maximum time allowed for the job or pipeline to complete from its start time. It sets a clear performance expectation for execution. If the job runs longer than this duration, it is considered an SLA breach. This helps in tracking efficiency and identifying performance issues.</td></tr></tbody></table>

5. Next, specify the **SLA Tolerance.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note</strong></mark><strong>: SLA Tolerance</strong> defines an additional buffer time allowed beyond the SLA duration before raising alerts or marking a failure. It accounts for minor or acceptable delays due to system or network fluctuations. This prevents unnecessary alerts for small deviations. It helps differentiate between critical delays and manageable ones .</td></tr></tbody></table>

5\.     If you want to send a **warning email** in case the schedule is completed later than the average time, then select the ![](<../../.gitbook/assets/unknown (32).png>) checkbox, and then specify the **From** and **To** settings.

6\.     If you want to **Kill running job** when SLA + tolerance limit is breached, then select the ![](<../../.gitbook/assets/unknown (33).png>) checkbox.

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption><p>ETL Job Node - Property Sheet</p></figcaption></figure>

**Job Parameters**

The parameters run\_by, run\_on, run\_time, resource\_key, and scheduler\_run\_id are **system-generated** runtime parameters that provide context about a job execution. They are automatically populated when the scheduler triggers the pipeline and are primarily used for tracking, monitoring, and auditing purposes.

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption><p>ETL Job Parameters</p></figcaption></figure>

**Metadata Refresh Node Job Parameters Description**

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Parameter</strong></td><td valign="top"><strong>Meaning</strong></td><td valign="top"><strong>Purpose</strong></td></tr><tr><td valign="top"><strong>run_by</strong></td><td valign="top">Identifies the <strong>user or system</strong> account that triggered the job execution.</td><td valign="top">Useful for <strong>audit tracking and debugging</strong>—you can know who initiated the process (manual user, scheduler, or service account)</td></tr><tr><td valign="top"><strong>run_on</strong></td><td valign="top">The date on which the job was executed.</td><td valign="top">Helps in <strong>logging, reporting, and partitioning data</strong> based on execution date.</td></tr><tr><td valign="top"><strong>run_time</strong></td><td valign="top">The exact time the job started (or was triggered).</td><td valign="top">Useful for <strong>monitoring job duration, sequencing jobs,</strong> and troubleshooting delays.</td></tr><tr><td valign="top"><strong>resource_key</strong></td><td valign="top"><p>Typically represents a <strong>specific resource identifier</strong>, such as:</p><ol><li>Dataset / file / table reference</li><li>Environment-specific key</li></ol><p> </p></td><td valign="top">Used for d<strong>ynamic resource allocation</strong> or <strong>parameterizing data sources/targets.</strong></td></tr><tr><td valign="top"><strong>scheduler_run_id</strong></td><td valign="top">A unique <strong>execution ID generated by the scheduler</strong></td><td valign="top"><p>Tracks a <strong>specific run instance</strong></p><p>Helps correlate logs across systems</p></td></tr></tbody></table>

<mark style="color:blue;">**Set up Failure or Success Condition**</mark>                    &#x20;

1. **Setting Up Failure Condition**
   1. On the **Metadata Node Property Sheet,** click the **On Condition** tab.
   2. The Failure tab is displayed by default.
   3. From the **Action** drop-down box, select the required **option** choosing from **Move to Next Week**, **Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, Move to Next Week.

3\.     In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note</strong>:</mark> If <strong>Send Mail-Move to Next Week</strong> or <strong>Send Mail-Abort and Raise Incident</strong> chose,l then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

**Setting Up Success Condition**

1. In the **Metadata Refresh Node Property Sheet**, click the **On Condition tab**.
2. Next, click the **Success** tab.
3. From the **Action** drop-down box, select the required option choosing from **Move to Next Week, Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, **Move to Next Week.**
4. In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If <strong>Send Mail-Move to Next Week or Send Mail-Abort and Raise Incident</strong> chose then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

</details>

<details>

<summary><strong>3.Configure Metadata Node</strong></summary>

<mark style="color:blue;">**Overview**</mark>

The Metadata Refresh node ensures that the system has the most up-to-date information about data structures such as tables, columns, and data types. It synchronizes any schema changes from source or target systems to avoid inconsistencies during processing. This helps prevent failures caused by mismatched or outdated metadata definitions. It plays a critical role in maintaining data accuracy and compatibility.

The procedure to configure the Metadata Refresh node involves steps including:

●      Adding Metadata Refresh Node to the pipeline canvas

●      Selecting Datasource and Tables

●      Setting up Discovery Settings

●      Setting up Failure and Success conditions

The following sections provide detailed guidance on setting up the ETL Job node.

<mark style="color:blue;">**Add Metadata Refresh Node on the Main Workspace**</mark>

1. On the **Scheduler page**, from the **left navigation bar**, drag the **Metadata Refresh Node** on to the **Main Workplace**, and connect the **Metadata Refresh Node** to the **ETL Job Node.**
2. Once the **Metadata Refresh Node** is added on the Main Workplace, the Properties Sheet section is displayed on the right side.

<figure><img src="../../.gitbook/assets/unknown (11).png" alt=""><figcaption><p align="center">Metadata Refresh Node</p></figcaption></figure>

<mark style="color:blue;">**Select Data source and Tables**</mark>

1. On the **Properties Sheet,** click the **Action** tab if it is not already displayed by default.
2. On the **Action** tab, From the **Select Data source** drop-down box, select the **required data source.**
3. From the **Table** field, select the **required tables.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> You can select multiple tables depending on the requirement.</td></tr></tbody></table>

<mark style="color:blue;">**Set up Discovery Settings**</mark>

1. On the **Action tab**, select the required **Discovery Settings** choosing from **Identify PII**, **Data Profiling, Data Summary, and Table Classification**.  Refer to the below table for the description of the discovery settings.

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Discovery Setting</strong></td><td valign="top"><strong>Purpose</strong></td></tr><tr><td valign="top">Identify PII</td><td valign="top">This setting detects and flags sensitive fields containing personally identifiable information (PII) to support data privacy and compliance requirements.</td></tr><tr><td valign="top">Data Profiling</td><td valign="top">This setting analyzes data to understand its structure, quality, patterns, and anomalies for better validation and governance.</td></tr><tr><td valign="top">Data Summary</td><td valign="top">This setting generates high-level statistics (such as counts, distributions, and null values) to provide an overview of the dataset.</td></tr><tr><td valign="top">Table Classification</td><td valign="top">This setting categorizes tables based on their content and usage (e.g., transactional, master, sensitive) to aid in data organization and governance.</td></tr></tbody></table>

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If you want to keep the AI/search system up to date with the latest data information, then select the <img src="../../.gitbook/assets/unknown (12).png" alt=""> checkbox, and then select the <strong>Target Vector DB.</strong></td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/unknown (13).png" alt=""><figcaption><p align="center">Metadata Action Settings</p></figcaption></figure>

<mark style="color:blue;">**Schedule SLA**</mark>

**Purpose**

Scheduling an SLA (Service Level Agreement) defines the expected completion time or deadline for your pipeline or job. It helps ensure that critical processes (like ETL jobs) finish within a committed time window. This is important for business operations that depend on timely data availability. It also enables monitoring and alerts if the job is delayed or misses its target.

**Procedure**

1. Go to the **Property Sheet** section on the right side of the application and expand the Schedule **SLA panel.**
2. The **Schedule SLA** panel is expanded.
3. On the **Schedule SLA** panel, select the **Active** checkbox.
4. In the **SLA Definition** section, specify the **SLA duration.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> <strong>SLA Duration</strong> specifies the maximum time allowed for the job or pipeline to complete from its start time. It sets a clear performance expectation for execution. If the job runs longer than this duration, it is considered an SLA breach. This helps in tracking efficiency and identifying performance issues.</td></tr></tbody></table>

5. Next, specify the **SLA Tolerance.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark><strong> SLA Tolerance</strong> defines an additional buffer time allowed beyond the SLA duration before raising alerts or marking a failure. It accounts for minor or acceptable delays due to system or network fluctuations. This prevents unnecessary alerts for small deviations. It helps differentiate between critical delays and manageable ones .</td></tr></tbody></table>

6. If you want to send a **warning email** in case the schedule is completed later than the average time, then select the ![](<../../.gitbook/assets/unknown (14).png>) checkbox, and then specify the **From** and **To** settings.
7. If you want to **Kill running job** when SLA + tolerance limit is breached, then select the ![](<../../.gitbook/assets/unknown (15).png>) checkbox.

<figure><img src="../../.gitbook/assets/unknown (16).png" alt=""><figcaption><p align="center">SLA Settings</p></figcaption></figure>

<mark style="color:blue;">**Job Parameters**</mark>

The parameters run\_by, run\_on, run\_time, resource\_key, and scheduler\_run\_id are **system-generated** runtime parameters that provide context about a job execution. **They are automatically populated** when the scheduler triggers the pipeline and are primarily used for tracking, monitoring, and auditing purposes.

**Metadata Refresh Node Job Parameters Description**

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Parameter</strong></td><td valign="top"><strong>Meaning</strong></td><td valign="top"><strong>Purpose</strong></td></tr><tr><td valign="top"><strong>run_by</strong></td><td valign="top">Identifies the <strong>user or system</strong> account that triggered the job execution.</td><td valign="top">Useful for <strong>audit tracking and debugging</strong>—you can know who initiated the process (manual user, scheduler, or service account)</td></tr><tr><td valign="top"><strong>run_on</strong></td><td valign="top">The date on which the job was executed.</td><td valign="top">Helps in <strong>logging, reporting, and partitioning data</strong> based on execution date.</td></tr><tr><td valign="top"><strong>run_time</strong></td><td valign="top">The exact time the job started (or was triggered).</td><td valign="top">Useful for <strong>monitoring job duration, sequencing jobs,</strong> and troubleshooting delays.</td></tr><tr><td valign="top"><strong>resource_key</strong></td><td valign="top"><p>Typically represents a <strong>specific resource identifier</strong>, such as:</p><ol><li>Dataset / file / table reference</li><li>Environment-specific key</li></ol><p> </p></td><td valign="top">Used for d<strong>ynamic resource allocation</strong> or <strong>parameterizing data sources/targets.</strong></td></tr><tr><td valign="top"><strong>scheduler_run_id</strong></td><td valign="top">A unique <strong>execution ID generated by the scheduler</strong></td><td valign="top"><p>Tracks a <strong>specific run instance</strong></p><p>Helps correlate logs across systems</p></td></tr></tbody></table>

<mark style="color:blue;">**Set up Failure or Success Condition**</mark>

1. **Setting Up Failure Condition**
   1. On the **Metadata Node Property Sheet,** click the **On Condition** tab.
   2. The Failure tab is displayed by default.
   3. From the **Action** drop-down box, select the required **option** choosing from **Move to Next Week**, **Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, Move to Next Week.

3\.     In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note</strong>:</mark> If <strong>Send Mail-Move to Next Week</strong> or <strong>Send Mail-Abort and Raise Incident</strong> chose,l then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/unknown (17).png" alt=""><figcaption><p align="center">Property Sheet - Failure Settings</p></figcaption></figure>

**Setting Up Success Condition**

1. In the **Metadata Refresh Node Property Sheet**, click the **On Condition tab**.
2. Next, click the **Success** tab.
3. From the **Action** drop-down box, select the required option choosing from **Move to Next Week, Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, **Move to Next Week.**
4. In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If <strong>Send Mail-Move to Next Week or Send Mail-Abort and Raise Incident</strong> chose then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

</details>

<details>

<summary>4.<strong>Configure Connection Refresh Node</strong></summary>

The **Connection Refresh node** ensures that all required data source and target connections are active and valid before execution. It refreshes authentication tokens, credentials, or sessions to maintain uninterrupted connectivity. This step helps in identifying and resolving connection issues early in the pipeline.

The procedure to configure the **Connection Refresh Node** involves steps including:

1. Adding Connection Refresh node to the pipeline canvas
2. Selecting connection
3. Setting up Failure and Success conditions

The following sections provide detailed guidance on setting up the ETL Job node.

<mark style="color:blue;">**Add Connection Refresh Node on the Main Workspace**</mark>

1. On the **Scheduler page,** from the **left navigation bar**, drag the **Connection Refresh Node** on to the **Main Workspace.**
2. The Properties Sheet section is displayed on the right side.
3. Next, connect the **Connection Refresh Node** to the **Metadata Refresh Node.**

<mark style="color:blue;">**Select Connection**</mark>

1. Go to the **Connection Refresh** section on the **Properties Sheet.**
2. Click the **Action** tab if it is not already displayed by default.
3. On the **Action** tab, from the **Select Connection** drop-down box, select the connection.

<figure><img src="../../.gitbook/assets/unknown (18).png" alt=""><figcaption><p align="center">Selecting Connection</p></figcaption></figure>

<mark style="color:blue;">**Schedule SLA**</mark>

**Purpose**

Scheduling an SLA (Service Level Agreement) defines the expected completion time or deadline for your pipeline or job. It helps ensure that critical processes (like ETL jobs) finish within a committed time window. This is important for business operations that depend on timely data availability. It also enables monitoring and alerts if the job is delayed or misses its target.



**Procedure**

1. Go to the **Property Sheet** section on the right side of the application and expand the Schedule **SLA panel.**
2. The **Schedule SLA** panel is expanded.
3. On the **Schedule SLA** panel, select the **Active** checkbox.
4. In the **SLA Definition** section, specify the **SLA duration.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> <strong>SLA Duration</strong> specifies the maximum time allowed for the job or pipeline to complete from its start time. It sets a clear performance expectation for execution. If the job runs longer than this duration, it is considered an SLA breach. This helps in tracking efficiency and identifying performance issues.</td></tr></tbody></table>

4\.     Next, specify the **SLA Tolerance.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top">Note: SLA Tolerance defines an additional buffer time allowed beyond the SLA duration before raising alerts or marking a failure. It accounts for minor or acceptable delays due to system or network fluctuations. This prevents unnecessary alerts for small deviations. It helps differentiate between critical delays and manageable ones .</td></tr><tr><td valign="top"></td></tr></tbody></table>

* If you want to send a **warning email** in case the schedule is completed later than the average time, then select the ![](<../../.gitbook/assets/unknown (14).png>) checkbox, and then specify the **From** and **To** settings.
* If you want to **Kill running job** when SLA + tolerance limit is breached, then select the ![](<../../.gitbook/assets/unknown (15).png>) checkbox.

<figure><img src="../../.gitbook/assets/unknown (21).png" alt=""><figcaption></figcaption></figure>

**3.3.2.4.4. Job Parameters**

The parameters run\_by, run\_on, run\_time, resource\_key, and scheduler\_run\_id are system-generated runtime parameters that provide context about a job execution. They are automatically populated when the scheduler triggers the pipeline and are primarily used for tracking, monitoring, and auditing purposes.

**Connection Refresh Node Job Parameters Description**

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Parameter</strong></td><td valign="top"><strong>Meaning</strong></td><td valign="top"><strong>Purpose</strong></td></tr><tr><td valign="top"><strong>run_by</strong></td><td valign="top">Identifies the <strong>user or system</strong> account that triggered the job execution.</td><td valign="top">Useful for <strong>audit tracking and debugging</strong>—you can know who initiated the process (manual user, scheduler, or service account)</td></tr><tr><td valign="top"><strong>run_on</strong></td><td valign="top">The date on which the job was executed.</td><td valign="top">Helps in <strong>logging, reporting, and partitioning data</strong> based on execution date.</td></tr><tr><td valign="top"><strong>run_time</strong></td><td valign="top">The exact time the job started (or was triggered).</td><td valign="top">Useful for <strong>monitoring job duration, sequencing jobs,</strong> and troubleshooting delays.</td></tr><tr><td valign="top"><strong>resource_key</strong></td><td valign="top"><p>Typically represents a <strong>specific resource identifier</strong>, such as:</p><ol><li>Dataset / file / table reference</li><li>Environment-specific key</li></ol><p> </p></td><td valign="top">Used for d<strong>ynamic resource allocation</strong> or <strong>parameterizing data sources/targets.</strong></td></tr><tr><td valign="top"><strong>scheduler_run_id</strong></td><td valign="top">A unique <strong>execution ID generated by the scheduler</strong></td><td valign="top"><p>Tracks a <strong>specific run instance</strong></p><p>Helps correlate logs across systems</p></td></tr></tbody></table>

<mark style="color:blue;">**Set up Failure or Success Condition**</mark>

1. **Setting Up Failure Condition**
   1. On the **Metadata Node Property Sheet,** click the **On Condition** tab.
   2. The Failure tab is displayed by default.
   3. From the **Action** drop-down box, select the required **option** choosing from **Move to Next Week**, **Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, Move to Next Week.

3\.     In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note</strong>:</mark> If <strong>Send Mail-Move to Next Week</strong> or <strong>Send Mail-Abort and Raise Incident</strong> chose,l then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/unknown (22).png" alt=""><figcaption><p align="center">Property Sheet - Failure Settings</p></figcaption></figure>

**Setting Up Success Condition**

1. In the **Metadata Refresh Node Property Sheet**, click the **On Condition tab**.
2. Next, click the **Success** tab.
3. From the **Action** drop-down box, select the required option choosing from **Move to Next Week, Abort and Raise Incident, Send Mail-Move to Next Week**, or **Send Mail-Abort and Raise Incident.** For example, **Move to Next Week.**
4. In the **Message** box, enter the **appropriate message.**

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><mark style="color:red;"><strong>Note:</strong></mark> If <strong>Send Mail-Move to Next Week or Send Mail-Abort and Raise Incident</strong> chose,l then you need to specify SMTP Server and Recipients also.</td></tr></tbody></table>

5. Finally, click the Next button.
6. The Frequency section is highlighted.

#### 3.3.3. Define Frequency <a href="#wjly60tmvijv" id="wjly60tmvijv"></a>

**3.3.3.1. Overview**

Defining Frequency is the next step after creating the pipeline in the scheduler creation process. It specifies how often and when the pipeline should run automatically (e.g., hourly, daily, weekly). It ensures that data processing happens at regular, predefined intervals without manual intervention.

This helps keep data fresh, consistent, and available on time for downstream systems and reporting. It also aligns job execution with business needs and data update cycles.

**3.3.3.2. Procedure**

The below step-by-step instructions help you understand the defining frequency procedure.

1. In the Frequency section, select the scheduler frequency choosing from Run Once, Daily, Weekly, and Monthly.
2. Select Start Date, End Date, Start Time, and End Time.
3. If you want the scheduler to run on a recurring basis, then select the ![](<../../.gitbook/assets/unknown (23).png>)checkbox.
4. Select the Recurring Frequency choosing from Seconds, Minutes, and Hours, and then enter the required value. For example, 15 Minutes.
5. Click the Next button.

<figure><img src="../../.gitbook/assets/unknown (24).png" alt=""><figcaption><p align="center">Defining Frequency</p></figcaption></figure>

The [External Dependency section is displayed.](https://qa4.scikiq.com/scheduler/edit/SCHDCLNT0007000049?server=default#wizard-h-2)

3.3.4. Specify External dependency

**3.3.4.1. Overview**

Specifying External Dependency while creating a scheduler determines whether the pipeline should run independently or wait for another schedule/job to complete before starting. &#x20;

**3.3.4.2. Procedure**

1. If you want the schedule to run independently:

●      Select the ![](<../../.gitbook/assets/unknown (25).png>)checkbox.

2. If the schedule is dependent on another schedule:

●      Select the ![](<../../.gitbook/assets/unknown (26).png>)checkbox.

●      Next from the drop-down box, select the required option choosing from Closest Preceding (c), Same Schedule Date (s), Relative Interval (r), and Absolute Interval (a). Refer to the below table for the description of these options.

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top">Dependency Option</td><td valign="top">Description</td></tr><tr><td valign="top">Closest Preceding (c)</td><td valign="top">This means your schedule will wait for the most recent completed run of the parent schedule before it starts.</td></tr><tr><td valign="top">Same Schedule Date (s)</td><td valign="top">This ensures your schedule runs only after the parent schedule runs for the same calendar date is completed.</td></tr><tr><td valign="top">Relative Interval (r)</td><td valign="top">This option allows dependency based on a relative time gap between schedules.</td></tr><tr><td valign="top">Absolute Interval (a)</td><td valign="top">This defines dependency using a fixed, exact time offset from the parent schedule.</td></tr></tbody></table>

3. After selecting the Dependency option, drag a schedule from the Select Scheduler box and place it in the Dependent Scheduler box.
4. Click the Next button.

<figure><img src="../../.gitbook/assets/unknown (27).png" alt=""><figcaption><p align="center">Defining External Dependency</p></figcaption></figure>

The Finish section is displayed.

&#x20;3.3.5. Completion



</details>

<details>

<summary>5.<strong>Define Frequency</strong></summary>

**Overview**

Defining Frequency is the next step after creating the pipeline in the scheduler creation process. It specifies **how often and when the pipeline should run automatically** (e.g., hourly, daily, weekly). It ensures that data processing happens at **regular, predefined intervals** without manual intervention.

This helps keep data **fresh, consistent, and available on time** for downstream systems and reporting. It also aligns job execution with **business needs and data update cycles.**

**Procedure**

The below step-by-step instructions help you understand the defining frequency procedure.

1. In the Frequency section, select the **scheduler frequency** choosing from **Run Once, Daily, Weekly, and Monthly.**
2. Select **Start Date, End Date, Start Time,** and **End Time**.
3. If you want the **scheduler to run on a recurring basis**, then select the ![](<../../.gitbook/assets/unknown (30).png>)checkbox.
4. Select the **Recurring Frequency** choosing from **Seconds, Minutes, and Hours**, and then enter the required **value**. For example, 15 Minutes.
5. Click the **Next** button.

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

6. The External Dependency section is displayed.

</details>

<details>

<summary><strong>6.Specify External dependency</strong></summary>

**Overview**

Specifying **External Dependency** while creating a scheduler determines **whether the pipeline should run independently or wait for another schedule/job to complete** before starting. &#x20;

**3.3.4.2. Procedure**

1. If you want the schedule to run independently:
   1. Select the ![](<../../.gitbook/assets/unknown (34).png>)checkbox.
2. If the schedule is dependent on another schedule:
   1. Select the ![](<../../.gitbook/assets/unknown (35).png>)checkbox.
   2. Next from the drop-down box, select the required option choosing from Closest Preceding (c), Same Schedule Date (s), Relative Interval (r), and Absolute Interval (a). Refer to the below table for the description of these options.

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Dependency Option</strong></td><td valign="top"><strong>Description</strong></td></tr><tr><td valign="top">Closest Preceding (c)</td><td valign="top">This means your schedule will wait for the most recent completed run of the parent schedule before it starts.</td></tr><tr><td valign="top">Same Schedule Date (s)</td><td valign="top">This ensures your schedule runs only after the parent schedule runs for the same calendar date is completed.</td></tr><tr><td valign="top">Relative Interval (r)</td><td valign="top">This option allows dependency based on a <strong>relative time gap</strong> between schedules.</td></tr><tr><td valign="top">Absolute Interval (a)</td><td valign="top">This defines dependency using a f<strong>ixed, exact time offset</strong> from the parent schedule.</td></tr></tbody></table>

3. After selecting the **Dependency** option, drag a **schedule** from the **Select Scheduler box** and place it in the **Dependent Scheduler** box.
4. Click the **Next** button.

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

5. The Finish section is displayed.

</details>

<details>

<summary><strong>7.Completion</strong></summary>

**Overview**

This is the final step in the scheduler creation process. As part of this, you can specify the S**cheduler Name, Description, Server, Catalogue, Business Owner**, and **Technical Owner.** &#x20;

**Procedure**

1. In the **Finish** section, enter all the mandatory details including S**cheduler Name, Description, Server, Catalogue, Business Owner,** and **Technical Owner.**
2. Click the **Finish** button.

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption><p>Scheduler Details</p></figcaption></figure>

The scheduler is created on the Scheduler List page. See the image below.

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption><p>Scheduler List</p></figcaption></figure>

</details>

<details>

<summary><strong>8.Viewing Running Scheduler List</strong></summary>

1. On the **SCIKIQ left** navigation bar, click **Scikiq Orchestrator** under **SCIKIQ CURATE.**

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption><p>SCIKIQ Orchestrator Menu Item</p></figcaption></figure>

2. The Scheduler page is displayed.
3. On the **Scheduler page**, click the **View** button in the **Running Scheduler List** section. See the image below.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Running Scheduler List - View Button</p></figcaption></figure>

4. The Scheduler List is displayed.

</details>

<details>

<summary><strong>9.Viewing All Scheduler List</strong></summary>

1. On the **SCIKIQ left** navigation bar, click **Scikiq Orchestrator** under **SCIKIQ CURATE.**

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption><p>SCIKIQ Orchestrator Menu Item</p></figcaption></figure>

2. The Scheduler page is displayed.
3. On the **Scheduler page**, click the View button in the **All-Scheduler List** section. See the image below.

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption><p>All Scheduler List - View Button</p></figcaption></figure>

4. The Scheduler List is displayed.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption><p>All Scheduler List</p></figcaption></figure>

</details>

### Related Topics

* [**SCIKIQ Scheduler List**](scikiq-schedules.md)

