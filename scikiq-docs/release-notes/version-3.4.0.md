# Version 3.4.0

### 1. Introduction

This Release Notes document outlines the updates introduced in version 3.4.0 of the SCIKIQ application. The release includes new features and bug fixes tracked through the Open Project system.

### 2. Release Overview

This release introduces two major developments: Audit History and Dashboard features.

The Audit History functionality enables users to view and track changes made across Admin Settings, POD Config, Data Pipelines, Scheduler, and Dashboard modules.

In addition to this, the Dashboard has been upgraded with the following key features:

●      The inclusion of a Download XLS feature within the pivot table, which enables downloading pivot table data in XLS format.

●      Enhanced pivot tables with a new Total column and Sort option.

●      A two-dimensional heatmap in Dashboard to represent correlation values through color intensity.

This document also provides details of the resolved and known issues addressed in this release.

### 3. New Features

### 3.1. Audit History

#### 3.1.1. Audit History in Admin Settings

In Admin Settings, the Audit History functionality enables viewing detailed records of all changes, including the action performed, field modified, old value, new value, user who made the modification, and timestamp of the change.

To view Audit History:

1. Go to the Left Navigation Menu.
2. Under the Access Management, click Admin Settings.
3. On the Admin Settings, click the History button.

Here is an example of how the audit history is displayed in Admin Settings.

<figure><img src="../.gitbook/assets/unknown (37).png" alt=""><figcaption></figcaption></figure>

### 3.1.2. Audit History in POD Config

In POD Config, the Audit History functionality enables viewing detailed records of all changes, including the date, field, old value, new value, and user who made the change.

To view Audit History:

1. Go to the Left Navigation Menu.
2. Under the Access Management, click POD Config.
3. On the Configuration page, click the History button.

Here is an example of how the audit history is displayed in POD Config.

<figure><img src="../.gitbook/assets/unknown (38).png" alt=""><figcaption></figcaption></figure>

### 3.1.3. Audit History in Delta Pipelines

In Delta Pipelines, the Audit History functionality enables viewing detailed records of all changes, including the action (Update, Store, or Delete), field, old value, new value, and user who made the change.

To view Audit History:

1. Go to the Left Navigation Menu.
2. Under SKIKIQ CONNECT, click Scikiq Delta Hub.
3. Under  Scikiq Delta Hub, click Delta Pipelines.
4. On the Delta Pipelines page, select the required pipeline, and then enter it in the Search field
5. From the displayed Search Results, click on the required result.
6. On the next page, click the Audit History tab.

Here is an example of how the audit history is displayed in Delta Pipelines:

<figure><img src="../.gitbook/assets/unknown (39).png" alt=""><figcaption></figcaption></figure>

### 3.1.4. Audit History in Scheduler

In Scheduler, the Audit History functionality enables viewing detailed records of all changes, including the action, field, old value, new value, and user who made the change.

To view Audit History:

1. Go to the Left Navigation Menu.
2. Scroll down to SCIKIQ CURATE, and then click Scikiq Schedules.
3. On the Scheduler List page, select the required Scheduler, and then enter it in the Search field at the top.
4. From the displayed Search Results, click on the required result.
5. On the next page, click the Audit History tab.

Here is an example of how the audit history is displayed in Scheduler:

<figure><img src="../.gitbook/assets/unknown (40).png" alt=""><figcaption></figcaption></figure>

### 3.1.5. Audit History in Dashboard

In Dashboard, the Audit History functionality enables viewing detailed records of all changes, including the action, field, old value, new value, and user who made the change.

To view Audit History:

1. Go to Left Navigation Menu
2. Scroll down to SCIKIQ Consume, and then click Dashboard List.
3.  On the Dashboard List page, scroll towards right, and then click the Change History icon corresponding to the required Dashboard List.

    <figure><img src="../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>
4. On the Dashboard Change Log screen, click the Down Arrow corresponding to the required log.

Here is an example of how the audit history is displayed in Dashboard:

<figure><img src="../.gitbook/assets/unknown (41).png" alt=""><figcaption></figcaption></figure>

### 3.2. Dashboard Upgrades

#### 3.2.1. Download XLS in XLS Pivot Table

In this release, the pivot tables have been provided with the Download XLS feature. This provides the ability to download pivot table data in XLS format.  &#x20;

<figure><img src="../.gitbook/assets/image (265).png" alt=""><figcaption></figcaption></figure>

#### 3.2.2. Total Column in Pivot Table Data

In a Pivot Table, a Total Column can now be created by turning on the Sub Total toggle button.  This provides the ability to sort the pivot table data row wise.

<figure><img src="../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

#### 3.2.3. Heat Map in Dashboard

Another important feature is a two-dimensional heatmap in the Dashboard. This allows for changing the correlational values with the required color intensity.

<figure><img src="../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

### 5. Resolved Issues

#### 5.1. Issues related to CBI client

1. Duplicate tables issue (OP-1168): Earlier, when creating the oracle connection, if the schema name was not given, then duplicate tables were being displayed. It has been resolved now.

#### 5.2. Issues related to EFS client

1. Scheduler issue (OP-11785): Previously, the scheduler update time was changing automatically even when no changes were made.  It has been resolved now.
2. Pipeline issue (OP-11810): Previously, in the pipeline, the IF condition was not working.  It has been resolved now.
3. Pipeline issue (OP-11806): The user should not be able to update an existing pipeline if two nodes have the same name, and an alert message should be displayed.  It has been resolved now.
4. Delta Pipeline issue (OP-11820): Previously, the Delta Pipeline - Api node preview was missing.  It has been resolved now.
5. Components' auto-update issue (OP-1184): Previously, in the Dashboard screen, filter values persist across sheets, but components do not auto-update based on the selected filters until the Apply Filter button is clicked again.  It has been resolved now.
6. Resource Migration issue (OP-11919): The ML server URL should not be mandatory on Config. Page. It has been resolved now.&#x20;
7. Variables issue (OP-11845): Previously, variable values could not be used in Table filters. It has been resolved now.&#x20;
8. Delta Pipeline screen issue (OP-11860): Previously, unable to remove the backslash (\\) from the value on the created delta pipeline screen.
9. Dashboard-level filters issue (OP-11885): Previously, when saving a dashboard as a copy, dashboard-level filters applied in the original were not visible in the new dashboard. It has been resolved now.
10. Dashboard Designer issue (OP-11873): After drilling down, data is displayed correctly but not in table format, with some cells extending beyond their borders.  It has been resolved now.
11. Scheduler issue (OP-11948): Daily-> during running state, somehow it stops but then it does not start for the next run time.  It has been resolved now.

#### 5.3. Issues related to Jaleel

1. Sum Operation issue (OP-11819: Previously, there was a Sum Operation issue with PostgreSQL Numeric Column. It has been resolved now.
2. OP-11821:   Previously, there was a LDM Load/Refresh Error.  It has been resolved now.

#### 5.4. Other Issues

1. Error log issue (OP-11889): Previously, Daily Scheduler for LDM was not running, and no error log was being generated. It has been resolved now.
2. TotalYTD Function issue (OP-11921): Previously, the TotalYTD Function in Dashboard was not working. It has been resolved now.
3. Dashboard Screen issue (OP-11924): Previously, the selected filter values on the first dashboard were not automatically applied to the second linked dashboard after navigation.  It has been resolved now.

### 6. Known issues

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top">OP ID</td><td valign="top">Location</td><td valign="top">Issue Description</td></tr><tr><td valign="top">OP-11970</td><td valign="top">Audit History</td><td valign="top">In the Audit History, detailed version comparison between pipeline revisions with deep comparison.</td></tr><tr><td valign="top">OP-8998</td><td valign="top">Create Delta Pipeline screen</td><td valign="top">In the Create Delta Pipeline screen, if the selected format is Avro, the load node is not connected to the previous node when writing the message to a new topic.</td></tr><tr><td valign="top">OP-11960</td><td valign="top">Audit History</td><td valign="top">In Audit History, owner names change on their own after adding components, showing wrong updates in audit history.</td></tr><tr><td valign="top">OP-1195</td><td valign="top">Dashboard</td><td valign="top">On the Dashboard screen, Audit history shows dimension added instead of removed and updates filter index without any changes.</td></tr><tr><td valign="top">OP-1192</td><td valign="top">Dashboard Details</td><td valign="top">On the Dashboard Details screen, the Dashboard Metadata screen displays blank.</td></tr><tr><td valign="top">OP-11886</td><td valign="top">Dashboard</td><td valign="top">On the Dashboard screen, the calculated Field Modal was not opening.</td></tr><tr><td valign="top">OP-11839</td><td valign="top">Dashboard</td><td valign="top">On the Dashboard screen, deleted Drill Relationships reappear after saving and fetching data.</td></tr><tr><td valign="top">OP-11822</td><td valign="top">Home page</td><td valign="top">On the Home page, on opening any dashboard in View mode, the screen appears blank with no visible components.</td></tr><tr><td valign="top">OP-11967</td><td valign="top">Dashboard</td><td valign="top">On the Dashboard screen, restoring a deleted resource does not generate an audit history entry for the Dashboard resource.</td></tr></tbody></table>

&#x20;

<br>

## &#x20; <a href="#s3ngp0nasag8" id="s3ngp0nasag8"></a>
