# Migration Requests

A Migration Request is a documented and trackable entry initiated by a user to migrate specific request from one environment to another.

#### Components

* **Request ID**: Unique ID for each request.
* **Title/Description**: What the request covers.
* **Migration Type**: Data, Process, Configuration.
* **Requested By**: Who initiated it.
* **Approval Path**: List of approvers (if required).
* **Assets List**: Items to be migrated.
* **Target Environment**: Destination environment.
* **Status**: Draft, Submitted, In Review, Approved, Executed, Completed.

### Navigating to Migration Request Dashboard

<figure><img src="../../../.gitbook/assets/image (1212).png" alt=""><figcaption></figcaption></figure>

Once the job is created, users are redirected to the Data Migration Request dashboard which provides a comprehensive view of all submitted migration jobs.

* Job Listing Panel: Lists multiple migration jobs including historical records. Each job is represented by a card showing:
  * Source and target systems (e.g., Oracle → SCIKIQ DNA Hub).
  * Status of the job (CREATED, FINISHED, ERROR, etc.).
  * Action buttons (RUN, RE-RUN, CREATE PHYSICAL MODEL) for control and rerun.
* Quick Filters: Users can filter by job status, data source, or page size for effective tracking.
* Action Highlight: The topmost job (DTAMCLINT0043000064) is in CREATED state and ready to be executed using the RUN button.

This dashboard offers real-time visibility into all data migration workflows, supporting governance, operational tracking, and error resolution at scale.



<figure><img src="../../../.gitbook/assets/image (613).png" alt=""><figcaption></figcaption></figure>

### Viewing Migration Request Summary

Clicking on a job card expands the Request Detail View that presents a job-specific breakdown:

* Meta Information: Includes:
  * Task name and description.
  * Request ID.
  * Submission time and initiator’s identity.
  * Current Status: Still listed as CREATED, indicating readiness for execution.
* Pod Assignment Panels:
  * Tables like TRADES\_28thApril and TRADE\_OPTIONS are organized into Pods (POD1, POD2).
  * Status indicators for tasks like Pod Assignment, Source Stats Capture, Data Copy, and Discovery.
* Filter Used: Custom filters (e.g., test1) are shown against each table when applied during preprocessing.
* Execution Timeline: Start times are recorded and displayed; end time updates upon completion.

This screen serves as the command center for migration execution monitoring, revealing the lifecycle stage of each table and transformation involved in the job.

<figure><img src="../../../.gitbook/assets/image (614).png" alt=""><figcaption></figcaption></figure>

Confirmation of Migration Job Execution Start

Upon clicking the RUN button, a toast notification appears at the bottom right of the screen:

* Message: “Data Migration Started”
* Visual Cue: Green success indicator confirms that the system has transitioned from configuration state to execution.

This final interface feedback validates the system’s responsiveness and helps the user transition focus from job setup to performance tracking and post-migration analysis.

<figure><img src="../../../.gitbook/assets/image (615).png" alt=""><figcaption></figcaption></figure>

### Monitor Real-Time Job Execution – Status: In Progress

Once the user triggers the migration process, the job status transitions from CREATED to IN PROGRESS, indicating the pipeline is actively processing the data from the source (Oracle) to the target (SCIKIQ DnA Hub).

Key observations:

* Progress Bars show the sequential execution of subtasks:
  * POD Assignment
  * Source Stats Capture
  * Data Copy
  * Discovery
* Highlight: A green progress bar shows the completed step Source Stats Capture, while Data Copy and Discovery are still running.
* Filter Application: The custom filter test1 remains associated with the TRADES table migration.
* Time Tracking: Each step logs start and end timestamps, aiding in performance audits and operational benchmarking.

This stage provides transparency in execution and is critical for identifying runtime bottlenecks or latency issues.



<figure><img src="../../../.gitbook/assets/image (616).png" alt=""><figcaption></figcaption></figure>

### Job Status – Data Copied

Once the data extraction, transformation (if applied), and load (ETL) are complete, the job status is updated to DATA COPIED.

Highlights:

* Orange Label (DATA COPIED) is shown both at the job level and table level.
* Pod Details: Information for POD2 has also appeared, indicating parallel execution for different tables.
* Execution Trail: Each subtask's execution % and status (e.g., 100% Done, 0% Done, In Progress) are visible.
* Control Panel: Discovery and Data Quality checks remain optional at this point.

This serves as a checkpoint before entering validation stages such as reconciliation, metadata verification, and downstream audit readiness.

<figure><img src="../../../.gitbook/assets/image (617).png" alt=""><figcaption></figcaption></figure>

### Row-Level Reconciliation – Green Signal

The job details pane now shows the reconciliation indicator as green, signifying that row-level reconciliation has passed successfully.

#### Breakdown:

* Source Table: TRADES
* Destination Table: TRADES\_28thApril
* Source/Target Row Count: Both equal to 18
* Start/End Time: Clearly recorded with millisecond precision
* Status: DATA COPIED
* Reconciliation Status: Green tick confirms that row count matches and no data integrity violation has occurred.

This screen is pivotal for regulatory compliance in industries like finance and healthcare where reconciliation logs are mandatory for audits.

<figure><img src="../../../.gitbook/assets/image (618).png" alt=""><figcaption></figcaption></figure>

### Column-Level Profile Validation

Clicking on the reconciliation tile brings up a column-level table profile, offering detailed insights into each column’s transformation and integrity post-migration.

Attributes Tracked:

* Source vs Destination Column Name and Type
* Source/Target Count (Total, Null, Unique)
* Data Type Mapping (e.g., NUMBER → numeric(37,15), DATE → timestamp)

Additionally:

* A CSV Export button allows users to download the reconciliation results for offline reporting or audit archival.

This in-depth validation ensures semantic consistency and confirms that no corruption or loss occurred during migration essential for mission-critical datasets.



<figure><img src="../../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure>

### Reconciliation Summary Panel

The bottom section of the job view provides a dashboard-style summary across multiple quality dimensions:

* &#x20;Reconciliation: Green means success
* Discovery: Indicates if metadata discovery has been completed
* &#x20;Data Quality: Assessment of nulls, data types, uniqueness, etc.
* &#x20;Delta Job: If enabled, delta handling or change data capture is shown

These toggles empower the user to:

* Trigger advanced metadata analysis
* Flag schema anomalies or drift
* Validate business rules through pre-defined quality checks

This final visual check establishes trustworthiness and completeness before handing the data over to BI tools, analytics layers, or business teams.

&#x20;

<figure><img src="../../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure>

Final Migration Status, Physical Model Creation, and Job Tracking

### Final Migration Summary Panel

This image provides a comprehensive summary of a data migration task post-execution. It showcases the metadata associated with the migration job, including:

* Request Number: DTAMCLNT0043000064
* Submitted By: Vimlesh Singh
* Submission Date: 28-04-2025 04:17:52 PM
* Current Status: Data Copied (green label)
* Total Cost: Not Available (indicative of either cost not yet calculated or cost tracking disabled)

Below the metadata block, the panel captures the pod assignment and task lifecycle events:

* POD1 Assignment and Timeline: 100% completed; all components like Source Stats Capture, Data Copy, and Discovery are tracked with visual progress indicators.
* Execution Logs: Confirmed start and end times of the task steps (Source Capture, Copy, and Discovery)
* Row Statistics: Source Table TRADES was migrated into TRADES\_28thApril with 18 source rows, 18 target rows, and status marked as Data Copied.

This panel is critical for auditability and governance teams to review the data pipeline completion status and monitor for data integrity.

<figure><img src="../../../.gitbook/assets/image (621).png" alt=""><figcaption><p>Migration Completion and Transition to Physical Model Creation</p></figcaption></figure>

Upon successful data migration and reconciliation, the job status is marked as FINISHED, as indicated in the top header.

A key feature becomes available here: "Create Physical Model". This option is highlighted in green and serves as the logical next step post-migration. It allows users to:

* Visualize the structure of newly ingested tables
* Build relational mappings between tables (primary/foreign key relationships)
* Prepare the data for downstream consumption in analytics and reporting workflows

This interface links data migration with semantic and data modeling tasks, ensuring continuity in the data lifecycle.

<figure><img src="../../../.gitbook/assets/image (622).png" alt=""><figcaption></figcaption></figure>

### Physical Model Canvas Interface

This image showcases the Physical Model Designer Studio, where the user has successfully pulled the migrated tables (TRADES\_28thApril and TRADE\_OPTIONS) into the design canvas.

Key highlights:

* Tables Available on Left Panel: A full list of entities accessible within the current data source (VS\_SciKiQ)
* Canvas Area: Allows drag-and-drop functionality for selected tables
* System Columns Auto-Appended: Columns such as ska\_created\_at, ska\_updated\_at, etc., are automatically injected for operational metadata tracking
* No active joins defined yet: This is an opportunity for users to establish relationships between entities for lineage and business semantics

This step is fundamental for constructing enterprise-ready datasets suitable for semantic querying, BI visualization, or publishing to other systems



<figure><img src="../../../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure>

### Advanced Search and Filtering of Migration Jobs

The final image illustrates the Data Migration Dashboard’s Advanced Search Panel, a feature built to help users track and manage large volumes of migration tasks.

#### Functional elements:

* Filter by Migration Status: Dropdown options include All, Created, In Progress, Submitted, Data Copied, Partial, Finished, and Error
* Pagination Controls: Page size selectors (e.g., 20 results per page)
* Search Filters: Source Type, Target Type, Connection Names, and Table Identifiers can all be used to narrow down results

This tool is essential for administrators and project managers who oversee numerous migrations across different systems. It ensures traceability, performance auditing, and quick access to problematic or completed jobs.

<figure><img src="../../../.gitbook/assets/image (624).png" alt=""><figcaption></figcaption></figure>

{% file src="../../../.gitbook/assets/Data Migration in Scikiq (1).docx" %}
