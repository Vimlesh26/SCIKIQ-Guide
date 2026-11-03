# SOP\_Restore\_Deleted\_Resources

Standard Operating Procedure (SOP)

**Task: Restore Functionality of Resources**

**Reference:** OP-8189

### 1. Purpose <a href="#toc207206048" id="toc207206048"></a>

This Standard Operating Procedure (SOP) provides a **step-by-step process** to restore deleted resources such as **ETLs, Schedulers, Data sources, Datasets, and Dashboards** in the ScikIQ platform.

It ensures that only authorized roles can perform recovery, maintain auditability, and highlight special considerations (e.g., data source permissions).

### 2. Scope <a href="#toc207206049" id="toc207206049"></a>

* **Resources Covered:**
  * Datasources
  * ETLs
  * Schedulers
  * Datasets
  * Dashboards
* **Applicable Roles:**
  * Catalogue Owner- Data Owner
  * Entity Admin
  * Client Admin

### 3. Requirement & Setup <a href="#toc207206050" id="toc207206050"></a>

*
  1. **Role Privileges Update**: Execute the **role privileges script** in both **API DB** and **Auth DB** as per **HotFix V3.3.0 script file**.
  2. **Service Restart**: Restart the **Auth Go Service** after running the script to apply the changes.

### 4. Pre-requisites <a href="#toc207206051" id="toc207206051"></a>

• The resource must have been previously created in the account and later deleted.\
• You must have one of the following roles: Data Owner, Entity Admin, or Client Admin.\
• You must have login access to the ScikIQ Platform.

### 5.General Procedure <a href="#hlk207035392" id="hlk207035392"></a>

### 5.1 Login to ScikIQ Platform <a href="#toc207206053" id="toc207206053"></a>

Step 1: Open the ScikIQ Platform login page in your browser.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/0.png)

Step 2: Enter your username and password.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/1 (3).png>)

Step 3: Click Login to access the Home page.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/2.png)

### 5.2 Navigate to Resource Section <a href="#toc207206054" id="toc207206054"></a>

1\. From the left-side navigation panel, locate the resource category.

2\. Select the relevant resource type: Datasources, ETLs, Schedulers, Datasets, LDMs, or Dashboards.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/3.png)

### 6. Restore Deleted Datasource <a href="#toc207206055" id="toc207206055"></a>

Detailed step-by-step process to restore deleted Datasources in the ScikIQ Platform.

### 6.1 Delete a Datasource <a href="#toc207206056" id="toc207206056"></a>

**Step 1**: Navigate to the resource listing page and select the desired resource type (e.g., _Data source_).

**Step 2:** Click on the list sub-menu. The page will display all connected/available resources.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/4.png)

**Step 3:** Locate the Data source you want to delete and click on the Delete button in the Action column.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/5.png)

**Step 4:** A confirmation prompt will appear with the notification: _“Are you sure you want to delete?”_

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/6.png)

**Step 5:** Click Yes to confirm.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/7.png)

* The resource will be removed from the list.
* A flash message will appear: “**SCIK-0173: Connection deleted successfully.”**
* The total count of resources will decrease as the resource is deleted.

.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/8.png)

### 6.2 Display Deleted Datasources <a href="#toc207206057" id="toc207206057"></a>

**Step 1**: On the resource listing page, go to the top-right corner and locate the toggle Show Deleted Resource.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/9.png)

**Step 2:** Enable the toggle.

* The page will refresh automatically.
* Deleted resources will now be visible in the list.
* These deleted resources are highlighted in a different style (e.g., grayed-out entries or red-highlighted rows) to distinguish them from active resources.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/10.png)

2\. Deleted resources will be visible in a distinct style (e.g., highlighted in red).

### 6.3 Restore Deleted Datasource <a href="#toc207206058" id="toc207206058"></a>

**Step** 1. Locate the deleted Datasource in the list.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/11.png)

**Step 2.** Click the Restore/Reactivate button.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/12.png)

**Step 3**: Confirm restoration. A success notification will appear.

The restored Datasource will now be available in the active resource list.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/13.png)

### 6.4 Special Considerations for Datasource Restoration <a href="#toc207206059" id="toc207206059"></a>

• Validate **connection details and credentials** after restoration..\
• **Sharing/permissions are removed** upon deletion; they must be **re-applied manually**..

### 7. Restore Deleted ETL Pipeline <a href="#toc207206060" id="toc207206060"></a>

Detailed step-by-step process to restore deleted ETL Pipelines in the ScikIQ Platform.

### 7.1 Delete a ETL Pipeline <a href="#toc207206061" id="toc207206061"></a>

**Step 1**. Navigate to the ETL Pipeline listing page.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/14.png)

**Step 2.** Select the ETL Pipeline you want to delete and click Delete button in the Action column.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/15.png)

**Step 3:** A confirmation prompt will appear with the notification: “Are you sure you want to delete?”

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/16.png)

**Step 4:** Click **Yes** to confirm.

* The ETL pipeline will be removed from the active list.
* A flash message will appear: “ETL pipeline deleted successfully.”
* The total count of ETL resources will decrease.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/17.png)

### 7.2 Display Deleted ETL Pipelines <a href="#toc207206062" id="toc207206062"></a>

**Step 1:** On the resource listing page, enable the 'Show Deleted Resource' toggle.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/18.png)

**Step 2.** Deleted resources will be visible in a distinct style (e.g., highlighted in red).

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/19.png)

### 7.3 Restore Deleted ETL Pipeline <a href="#toc207206063" id="toc207206063"></a>

**Step 1:** Scroll through or use the search option to find the deleted ETL pipeline you want to restore.

![A screenshot of a computer

AI-generated content may be incorrect.](../../.gitbook/assets/20.png)

**Step 2:** In the Action column, a new button appears for deleted ETL resources -the **Restore** (or **Reactivate**) button with a reactivation icon.

**Step 3:** Click on the **Restore** button. Review the details and click **Yes** (or confirm) to proceed.

**Step 5:** A success notification will be displayed:

* Flash message: “ETL pipeline activated successfully.”
* A notification pop-up will also appear on the screen.

**Step 6:** The restored ETL pipeline will now reappear in the active resource list. You can now use, edit, and configure it as required.

### 7.4 Special Considerations for ETL Pipeline Restoration <a href="#toc207206064" id="toc207206064"></a>

* If the restored ETL pipeline has dependencies on other resources (such as datasets, data sources, or schedulers), verify that those linked resources are also active and available.
* Review ETL steps, mappings, and configuration after restoration..
* Edit or revalidate the ETL before using it.
* All restoration actions are logged for audit purposes. Only authorized roles may perform restoration.
* If the ETL pipeline was previously scheduled or linked to triggers, confirm its schedule and re-link as needed.
* **Note:** Permissions are not restored automatically. You must grant them again manually.

### 8. Restore Deleted Scheduler <a href="#toc207206065" id="toc207206065"></a>

Detailed step-by-step process to restore deleted Schedulers in the ScikIQ Platform.

### 8.1 Delete a Scheduler <a href="#toc207206066" id="toc207206066"></a>

**Step 1.** Navigate to the Scheduler listing page.

**Step 2**. Select the Scheduler you want to delete and click Delete.

**Step 3:** A confirmation prompt will appear: “Are you sure you want to delete?”

**Step 4:** Click **Yes** to confirm.

* The Scheduler will be removed from the active list.
* A flash message will appear: “SCIK-0038: schedule removed.”
* The total count of Schedulers will decrease.

### 8.2 Display Deleted Schedulers <a href="#toc207206067" id="toc207206067"></a>

**Step 1**: On the resource listing page, enable the 'Show Deleted Resource' toggle. Deleted resources will be visible in a distinct style (e.g., **highlighted in red**).

### 8.3 Restore Deleted Scheduler <a href="#toc207206068" id="toc207206068"></a>

**Step 1.** Locate the deleted Scheduler in the list.

**Step 2.** Click the Restore/Reactivate button.

**Step 3:** Click **yes** to confirm delete.

A success notification will be displayed:

* Flash message: “Scheduler activated successfully.”
* A notification pop-up will also appear on the screen.

**Step 7:** The restored Scheduler will now reappear in the active resource list. You can now use, edit, and configure it as required.

### 8.4 Important Note- Post Restoration status <a href="#toc207206069" id="toc207206069"></a>

After restoration, the **Scheduler status will be set to Paused** by default, and the **Next Run Start Date** will be blank.

**To start the Scheduler:** Click the **Edit** button on the restored Scheduler.

Make necessary updates (if any) and click **Next**.

Set the **Start Date and Time**.

Click **Finish** to start the Scheduler.

The Scheduler will now run at the configured start time and date.

### 8.5 Special Considerations for Scheduler Restoration <a href="#toc207206070" id="toc207206070"></a>

* After restoring a Scheduler, edit and save the configuration before it can run.
* Verify that dependent resources (ETLs, datasets, data sources) are active.
* All restoration actions are logged and only authorized roles can perform them.
* The Scheduler may need configuration updates based on dependencies.
* **Note:** Permissions are not restored automatically; they must be granted again manually.

### 9. Restore Deleted Logical Data Model (LDM) <a href="#toc207206071" id="toc207206071"></a>

Detailed step-by-step process to restore deleted Logical Data Model (LDM)s in the ScikIQ Platform.

### 9.1 Delete a Logical Data Model (LDM) <a href="#toc207206072" id="toc207206072"></a>

**Step 1:** Navigate to the Logical Data Model (LDM) listing page.

**Step 2.** Select the Logical Data Model (LDM) you want to delete and click Delete.

**Step 3:** A confirmation prompt will appear with the notification: “Are you sure you want to delete?”

**Step 5:** Click **Yes** to confirm.

* The LDM will be removed from the active list.
* A flash message will appear: “SCIK-0173: LDM deleted successfully.”
* The total count of LDM resources will decrease.

### 9.2 Display Deleted Logical Data Model (LDM)s <a href="#toc207206073" id="toc207206073"></a>

**Step 1**. On the resource listing page, enable the 'Show Deleted Resource' toggle

**Step 2:** Deleted LDMs will now be visible in the list. These deleted resources are highlighted in a different style (e.g., **highlighted in red**) to distinguish them from active resources.

### 9.3 Restore Deleted Logical Data Model (LDM) <a href="#toc207206074" id="toc207206074"></a>

**Step 1.** Locate the deleted Logical Data Model (LDM) in the list.

**Step 2:** Click on the **Restore** button.

**Step 3:** Click **Yes** to confirm.

**Step 4:** A success notification will be displayed:

* Flash message: “LDM activated successfully.”
* A notification pop-up will also appear on the screen.

**Step 5:** The restored LDM will now reappear in the active resource list. You can now use, edit, and configure it as required.

### 9.4 Special Considerations for Logical Data Model (LDM) Restoration <a href="#toc207206075" id="toc207206075"></a>

* If the restored LDM has dependencies on other resources (such as datasets, data sources, or ETLs), verify that those linked resources are also active and available.
* Review the LDM configuration to confirm mappings and relationships are correct.
* You may need to edit or revalidate the restored LDM for its intended business use.
* All restoration actions are logged for audit purposes. Only authorized roles may perform restoration.
* If the LDM was previously integrated into any dashboards or reports, confirm its status and re-link as needed.

### 10. Restore Deleted Dashboard <a href="#toc207206076" id="toc207206076"></a>

Detailed step-by-step process to restore deleted Dashboards in the ScikIQ Platform.

### 10.1 Delete a Dashboard <a href="#toc207206077" id="toc207206077"></a>

**Step 1**. Navigate to the Dashboard listing page.

**Step 2:** Select the Dashboard you want to delete and click Delete.

**Step 3 :**&#x41; confirmation prompt will appear: “Are you sure you want to delete?”

**Step 5:** Click **Yes** to confirm.

* The Dashboard will be removed from the active list.
* A flash message will appear: “SCIK-0173: Dashboard deleted successfully.”
* The total count of Dashboards will decrease.

### 10.2 Display Deleted Dashboards <a href="#toc207206078" id="toc207206078"></a>

**Step 1.** On the resource listing page, enable the 'Show Deleted Resource' toggle

**Step 2:** Deleted resources will be visible in a distinct style (e.g highlighted in red).

### 10.3 Restore Deleted Dashboard <a href="#toc207206079" id="toc207206079"></a>

**Step 1:** Locate the deleted Dashboard in the list.

**Step 2:** Click the Restore/Reactivate button.

**Step 3**: Review the details and click **Yes** (or confirm) to proceed.

**Step 4:** A success notification will be displayed:

* Flash message: “Dashboard activated successfully.”
* A notification pop-up will also appear on the screen.

\
The restored Dashboard will now reappear in the active resource list. You can now use, edit, and configure it as required.

### 10.4 Special Considerations for Dashboard Restoration <a href="#toc207206080" id="toc207206080"></a>

* If the restored Dashboard has dependencies on other resources (such as datasets or LDMs), verify that those linked resources are also active and available.
* Review the Dashboard configuration to confirm visualizations and filters are correct.
* You may need to edit or revalidate the restored Dashboard for its intended business use.
* All restoration actions are logged for audit purposes. Only authorized roles may perform restoration.
* If the Dashboard was previously shared, then all permission granted will also be deleted for that you need to again defines as needed

### 11. Audit & Compliance <a href="#toc207206081" id="toc207206081"></a>

• All actions (delete, restore) are logged.\
• Audit trails are available to authorized roles for compliance.\
• Only authorized roles may perform restoration.
