# SOP\_Data\_Migration

Standard Operating Procedure (SOP)\
OP-10006 Feature to schedule data migration



### 1. Purpose <a href="#toc207273184" id="toc207273184"></a>

This SOP outlines the step-by-step process to schedule and execute a Table Data Migration in the platform. It ensures consistent data transfer, proper scheduling, and automation while maintaining full control and traceability.

### 2. Prerequisites <a href="#toc207273185" id="toc207273185"></a>

• User must have valid access rights to the platform.\
• Source and Target Data sources should already be configured.\
• Tables to be migrated must be available and accessible.\
• Verify that the Migration feature is enabled in the platform.

### 3. Detailed Procedure to Schedule Table Data Migration <a href="#toc207273186" id="toc207273186"></a>

### 3.1 Login to ScikIQ Platform <a href="#toc207273187" id="toc207273187"></a>

1. Open the ScikIQ Platform login page in your browser.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/0 (1).png>)

1. Enter your username and password.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/1 (4).png>)

1. Click Login to access the Home page.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/2 (1).png>)

### 3.2 Navigate to Data Migration Feature <a href="#toc207273188" id="toc207273188"></a>

1. From the left navigation menu, select Data Migration.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/3 (1).png>)

### 3.3 Select Source and Target Data sources <a href="#toc207273189" id="toc207273189"></a>

1. In the configuration screen, choose the Source Data source.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/4 (1).png>)

1. Select the Target data source where the data will be migrated.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/5 (1).png>)

### 3.4 Select Tables for Migration <a href="#toc207273190" id="toc207273190"></a>

1. Browse or search for the tables you wish to migrate.
2. Select one or multiple tables as required.
3. Click Next.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/6 (1).png>)

### 3.5 Analyze & Sync <a href="#toc207273191" id="toc207273191"></a>

1. Review the table metadata, add new columns if required.
2. Choose migration type: New Table or Existing Table.
3. If New Table is selected, provide a new table name.
4. Apply optional EDA (Exploratory Data Analysis), DQ (Data Quality), or edit metadata.
5. Click Next.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/7 (1).png>)

### 3.6 POD Management <a href="#toc207273192" id="toc207273192"></a>

1. All selected tables will be displayed on the default POD.
2. Additional PODs can be created, and tables can be dragged & dropped into them.
3. Click Next.

![](<../../.gitbook/assets/8 (1).png>)

### 3.7 Review & Submit <a href="#toc207273193" id="toc207273193"></a>

1. Provide the Task Name and Description.
2. Review the task summary.
3. Click Finish to submit.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/9 (1).png>)<br>

1. After clicking Finish, a confirmation message will appear: 'Data migration job is created successfully!' with a request number.
2. Click OK to proceed.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/10 (1).png>)

### 3.8 Data Migration Request <a href="#toc207273194" id="toc207273194"></a>

1. The platform will redirect to the Migration Request screen where the new migration will be listed.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/11 (1).png>)

### 3.9 Migration Schedule <a href="#toc207273195" id="toc207273195"></a>

1. Click RUN on the migration job.\
   ![A screenshot of a computer

   AI-generated content may be incorrect.](<../../.gitbook/assets/12 (1).png>)
2. In the scheduler window, choose one of the following options:
   1. Run Now – job starts immediately.
   2. Run Later – specify Start Date and Start Time.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/13 (1).png>)

1. Select the **“Run Later”** option, then specify the start date and time.
   1. _Example: The job is scheduled for 28_<sup>_th_</sup>_&#x20;August at **9:25AM.**_

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/14 (1).png>)

1. Click Save. A successful message will appear: 'Migration Scheduled', and job status will change from Created to Submitted.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/15 (1).png>)

### 3.10 Before Execution <a href="#toc207273196" id="toc207273196"></a>

1. Start Time and End Time fields will remain blank.
2. Job status will show as **Created**.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/16 (1).png>)

### 3.11 During Execution <a href="#toc207273197" id="toc207273197"></a>

1. **At Scheduled Time**- The migration job status changes to **In Progress**.
2. For each selected table, the status will show as **Data Copied** once the data transfer is complete.
3. Start and End times are updated for every migrated table.
4. Source row count and Target row count are displayed for comparison.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/17 (1).png>)

### 3.12 After Migration Completion <a href="#toc207273198" id="toc207273198"></a>

1. Once validation/discovery is complete, the overall migration job status changes from **Data Copied** to **Finished**.

![A screenshot of a computer

AI-generated content may be incorrect.](<../../.gitbook/assets/18 (1).png>)

1. The target database will contain the migrated tables, and users can verify the successful transfer.

![](<../../.gitbook/assets/19 (1).png>)
