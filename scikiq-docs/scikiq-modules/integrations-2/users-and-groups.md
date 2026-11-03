---
icon: user-group
---

# Users & Groups

### **Users & Groups**

* ScikIQ allows both Client Admin and Entity Admin to manage users, granting them the authority to create, edit, and delete user accounts.&#x20;
* This management is crucial for maintaining an organized user structure within the system. When a new user account is being created, the Admin must carefully select the appropriate role to ensure the user has the correct permissions and access levels necessary to perform their duties. Additionally, assigning the user to a specific entity is necessary to align them with the relevant organizational structure or project.&#x20;
* This enables streamlined operations and efficient management of resources within ScikIQ, guaranteeing that every user is properly categorized and functional according to their designated role and entity.

### How to create a new user

Client Admin and Entity Admin can create, edit, and delete users in ScikIQ. While creating user, role, and entity need to be selected.

Client admin can see a list of users from the “Users & Groups” menu and can create new user by clicking the “Create User” button on the same screen.

<figure><img src="../../.gitbook/assets/image (1037).png" alt=""><figcaption><p>ScikIQ user list</p></figcaption></figure>

A username, email ID, initial password, role, and entity need to be provided while creating a new user

**Entity and Role Selection**

**Entity Selection:** When creating a new user, administrators can choose from different entity options to properly align the user with the organizational structure:

* **Parent Default Entity:** Users can be assigned to the main enterprise entity, providing them with access to core organizational resources and standard operational frameworks.
* **Custom Entities:** Administrators also have the flexibility to select from custom-created entities that represent specific departments, projects, or organizational divisions. This ensures users are properly categorized according to their specific work scope and responsibilities.

**Role Assignment:** The role selection process offers comprehensive options to match user responsibilities with appropriate system permissions:

* **Predefined Roles:** The system provides standard roles such as Data Owner, Data Steward, Orchestrator, Entity Admin, Business CDO, and other built-in roles that come with predetermined permission sets and access levels.
* **Custom Roles:** Organizations can create and assign custom roles tailored to their specific operational needs and hierarchy structures, allowing for precise permission management.

**Access Control Framework:** Through this entity and role assignment process, the system enforces strict access control mechanisms:

* **Entity-Based Resource Access:** Users are only eligible to view and interact with resources that belong to their assigned entity, ensuring data segregation and organizational security.
* **Role-Based Permissions:** All menu permissions, system policies, and functional capabilities are determined by the role assigned to the user, creating a comprehensive permission framework that governs what actions users can perform within the ScikIQ platform.

<figure><img src="../../.gitbook/assets/image (1038).png" alt=""><figcaption><p>Create new user.</p></figcaption></figure>

A newly created user needs to log into ScikIQ using a password provided by the Admin. New users will see menus and resources based on the role assigned to them.

<figure><img src="../../.gitbook/assets/image (1039).png" alt=""><figcaption></figcaption></figure>

### **Creating Bulk Users in ScikIQ**

To streamline the process of adding multiple users to the system at once, ScikIQ provides a **Bulk User Creation** feature. Follow these steps to create bulk users efficiently.

**Step 1: Navigate to the Users & Groups Screen**

1. **Go to the Users & Groups screen**: Click on the “Users & Groups” section in the dashboard.

<figure><img src="../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

**Click on "Create Bulk Users"**: This will redirect you to the bulk user creation screen, where you can add multiple users simultaneously.

<figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>

**Bulk Users Creation Screen Overview**

There are three main tabs within the Bulk User Creation screen:

1. **User Details**
2. **Bulk Upload**
3. **Download Users**

<figure><img src="../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

#### **1. User Details Tab**

The **User Details** tab allows you to manually enter details for each user.

**Fields in the User Details Tab:**

* **First Name**: Enter the user's first name.
* **Last Name**: Enter the user's last name.
* **Email**: Provide the user’s email address.
* **Company**: Specify the user's company name.
* **Password**: Set the password for the user.
* **Confirm Password**: Re-enter the password for confirmation.

<figure><img src="../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>

**Assign Role, Entity, and Group:**

* **Assign Entity**: Select the user's entity from the dropdown.
  * Options: India, Enterprise Entity, etc.
* **Assign Role**: Choose the user’s role from the dropdown.
  * Options: Viewer, Report Designer, Data Analyst, Data Engineer, Orchestrator, Data Steward, Data Owner, Entity Admin/Business CDO, etc.

<figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>

* **Assign Group**: You can optionally add the user to a specific group or leave it blank.

**Make Client Admin:**

Check the box if you want to make the user a Client Admin.

<figure><img src="../../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure>

**Adding Users:**

1. After entering all the required details, **click on the “Add” button**.
2. You will see a flash message: **“Record added for final submit. Please check preview before final submit.”**

<figure><img src="../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

**Preview Changes:**

* Click on **"Preview Changes"** to review the users you’ve added.
* The preview will display the following:
  * **First Name**, **Last Name**, **Email**, **Company**
  * **Event Action**: Options to Edit or Delete.

<figure><img src="../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>

**Submitting Users:**

* After reviewing the added users, click on the **Submit button**.

<figure><img src="../../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

* All the users you’ve entered will be added at once, and the system will display a confirmation message that the users were added successfully.
* On the left side, you can see a list of all added users.

<figure><img src="../../.gitbook/assets/image (288).png" alt=""><figcaption></figcaption></figure>

#### **2. Bulk Upload Tab**

The **Bulk Upload** tab allows you to upload an Excel file containing user details, which will add multiple users at once.

<figure><img src="../../.gitbook/assets/image (290).png" alt=""><figcaption></figcaption></figure>

**Steps for Bulk Upload:**

1. **Download the Template File**:
   * Click on **Download Template File** to get the Excel template.

<figure><img src="../../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>

* Open the template in Excel.

1.  **Fill in the Details**:

    * In the template, fill out the following columns for each user:
      * **First Name**
      * **Last Name**
      * **Email**
      * **Company**
      * **Password**
    * Select the **Entity** from the dropdown.
    * Choose the **Role** from the dropdown.

    <figure><img src="../../.gitbook/assets/image (292).png" alt=""><figcaption></figcaption></figure>

    * Optionally, you can leave the **Group Name** blank or add the user to a specific group.
2. **Save the Excel File**:
   * After filling in the user details, save the file.
3.  **Upload the Excel File**:

    * Go back to the Bulk Upload tab in ScikIQ.
    * Click on **Browse** to select the saved Excel file.

    <figure><img src="../../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure>

    * Upload the file by clicking on **Upload XLS file**.

<figure><img src="../../.gitbook/assets/image (294).png" alt=""><figcaption></figcaption></figure>

1. **Submit the File**:
   * After uploading, the system will display a success message: **“User(s) added successfully”**.

<figure><img src="../../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>

#### **3. Download Users Tab**

The **Download Users** tab allows you to download a list of all the users in the system, including their email addresses, roles, and entities.

<figure><img src="../../.gitbook/assets/image (296).png" alt=""><figcaption></figcaption></figure>

**Steps to Download Users:**

1. Click on the **Download Users** button.
2. The system will generate and download a file with the following details for all users:
   * **Email**
   * **Role**
   * **Entity**

<figure><img src="../../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>

This file can be used for reference or record-keeping.

### **Conclusion**

Using the **Create Bulk Users** functionality in ScikIQ helps save time by allowing you to:

* Add users one by one via the **User Details** tab
* Add many users at once via the **Bulk Upload** tab
* Export user data through the **Download Users** tab

### Groups in ScikIQ

In ScikIQ, there are two types of groups that manage user access and collaboration:

1. **System Groups**\
   These are predefined by the system to manage default roles and permissions. They cannot be modified by users and are essential for maintaining basic access control structures.
2. **User-Defined Groups**\
   These groups can be created, modified, and managed by users to tailor access and permissions according to specific organizational needs or projects. User-defined groups allow for flexible collaboration setups and custom access rights.

### Managing User-Defined Groups in ScikIQ

User-defined groups in ScikIQ offer flexibility in managing user access and collaboration. These groups are created and managed by users according to their specific needs within an organization or project. Here are some key points about user-defined groups:

* **Creation and Management**: Users have the capability to create new groups, modify existing ones, and manage membership and permissions. This allows for dynamic and custom collaboration setups.
* **Custom Access Rights**: User-defined groups enable customizing access permissions so that users can interact with specific resources as required by their role or project participation.
* **Project-Specific Groups**: Organizations can set up groups for specific projects, allowing only relevant members to access and work on project-specific data and resources.
* **Enhanced Collaboration**: By defining user groups according to specific tasks or projects, teams can foster better collaboration and streamline workflows.

These groups facilitate a tailored approach to resource management and support an efficient work environment, helping organizations to meet their changing needs and challenges.

### How to Create Only One Group

There is a button on the group list screen to create a new group.

<figure><img src="../../.gitbook/assets/image (1040).png" alt=""><figcaption></figcaption></figure>

First, input the group name and add members to the group, following the steps illustrated below. Then, click on the 'Create Group' button.

<figure><img src="../../.gitbook/assets/image (1041).png" alt=""><figcaption></figcaption></figure>

As seen in the attached screen below, the group has been added to the list.

<figure><img src="../../.gitbook/assets/image (1042).png" alt=""><figcaption></figcaption></figure>

### Permission on Single Resource

Permission on a resource is a security and access management concept that defines the level of access an individual or group has to a specific resource. This includes actions such as viewing, editing, deleting, or sharing the resource. Managing these permissions is essential to protect the resource and ensure that users can interact with it according to their roles and responsibilities. Proper configuration of resource permissions helps prevent unauthorized access and potential misuse of sensitive information.

### Adding Users to a Group

To add users to a group, access the group membership management screen. Here, you will find an **Add Users** button. Click this button to select and add users to the group from the available list.

<figure><img src="../../.gitbook/assets/image (1044).png" alt=""><figcaption></figcaption></figure>

* Permission on a resource can be granted as a contributor or viewer.&#x20;
* Permission of a resource can be edited by the contributor or the owner of the resources.&#x20;
* If the resource is published as an asset, then it can be edited only by the Asset owner. If a resource is published as an asset and someone wants access to the asset, then they need to raise an asset access request.

### **Bulk Group Creation**

**Creating Bulk Groups and Assigning Resource Permissions**

In ScikIQ, groups are used to manage users collectively and streamline permission assignments across various data resources. This document outlines the steps to create user groups, add members, assign resource permissions, and apply conditional filters when needed. This allows organizations to manage user access control more efficiently and securely.

### **1. Accessing the Group Management Section**

To begin creating groups, follow the steps below:

1. Log into the ScikIQ platform using your administrative credentials.
2.  Navigate to the **Users & Groups** section from the main dashboard or side navigation panel.

    <figure><img src="../../.gitbook/assets/image (1550).png" alt=""><figcaption></figcaption></figure>
3.  Click on the Create Bulk **Groups** button.

    <figure><img src="../../.gitbook/assets/image (1551).png" alt=""><figcaption></figcaption></figure>
4.  To check if a similar group already exists, use the **Search Group** functionality.

    <figure><img src="../../.gitbook/assets/image (1552).png" alt=""><figcaption></figcaption></figure>
5. Click the **Create Group** button to start creating a new user group.

### **2. Enter Group Details**

On the group creation screen, you will need to provide basic details for the new group:

#### Fields to Fill:

* **Group Name**\
  Provide a unique and descriptive name for the group.\
  _&#x45;xample:_ Dubai Group
* **Description**\
  A short description explaining the purpose or the users covered by the group.\
  Maximum 500 characters.\
  _&#x45;xample: Group of_ Dubai Group _onboarded on 1st August 2025._

<figure><img src="../../.gitbook/assets/image (1553).png" alt=""><figcaption></figcaption></figure>

### **3. Adding Group Members**

After entering the group details, you can proceed to add users as group members.

#### Steps to Add Members:

1. Click the **Add Members** button.
2. A list of available users will appear.
3. Select users from the list by clicking on their names or using checkboxes.
4. Selected users can have varied roles such as:
   * Entity Admin
   * Data Engineer
   * Data Analyst
   * Data Owner
   * Data Steward
   * Orchestrator
   * Viewer
   * Report Designer

<figure><img src="../../.gitbook/assets/image (1554).png" alt=""><figcaption></figcaption></figure>

You can add as many users as needed to the group. Members added here will inherit all the permissions applied to the group.

### **4. Assigning Bulk Resource Permissions to the Group**

ScikIQ allows you to assign permissions to multiple resources at once (bulk resource assignment) for the selected group.

#### Supported Resource Types:

* Data Source
* Dataset and Logical Data Model (LDM)
* Dashboard
* Scheduler
* ETL

<figure><img src="../../.gitbook/assets/image (1555).png" alt=""><figcaption></figcaption></figure>

### **4.1 Assigning Permissions to Data Sources**

To assign permissions for **Data Source** type resources:

1. Select **Data Source** from the **Resource Type** dropdown.
2. Use the **Search Resource** field to find a specific data source.
3.  Select the data source from the list.

    <figure><img src="../../.gitbook/assets/image (1556).png" alt=""><figcaption></figcaption></figure>
4.  Choose the **Permission Role** to be assigned:

    * Viewer
    * Contributor

    <figure><img src="../../.gitbook/assets/image (1557).png" alt=""><figcaption></figcaption></figure>

You can repeat this process for multiple data sources. For each selected resource, assign the appropriate permission role separately.

<figure><img src="../../.gitbook/assets/image (1558).png" alt=""><figcaption></figcaption></figure>

### **4.2 Assigning Permissions to Dataset and LDM Resources**

If the selected resource type is **Dataset and LDM**, an additional configuration step is available: applying **filters** to restrict data visibility.

#### Steps:

1. Select **Dataset and LDM** as the resource type.
2. Use the **Search Resource** field to locate the desired LDM.
3.  Choose the **Permission Role** for the resource.

    <figure><img src="../../.gitbook/assets/image (1562).png" alt=""><figcaption></figcaption></figure>
4. After selection, the system displays the **Existing Filters** section.

<figure><img src="../../.gitbook/assets/image (1563).png" alt=""><figcaption></figcaption></figure>

#### Applying Filters:

You can apply a filter to limit the dataset a group can access.

_Example:_

* If the selected LDM is fm\_pro\_ldm, and the applied filter is `City = Dubai`,
*   then all group members will only see the data related to **Dubai** within that LDM.

    <figure><img src="../../.gitbook/assets/image (1564).png" alt=""><figcaption></figcaption></figure>

Note: If no filter is applied, users will have access to all data in the dataset based on their assigned role.

This feature is particularly useful for implementing **row-level security** in data access.

### **4.3 Assigning Permissions to Dashboards, Schedulers, and ETL**

For each of the other resource types:

1. Select the appropriate resource type (Dashboard, Scheduler, or ETL).
2. Search and select the resource.
3. Assign a **Permission Role**.

<figure><img src="../../.gitbook/assets/image (1565).png" alt=""><figcaption></figcaption></figure>

Repeat for each resource individually. Each resource and role combination must be defined manually.

### **5. Saving the Group**

After entering group details, adding members, and assigning all resource permissions:

1. Review the list of members and assigned permissions.
2. Click on the **add** or **Create Group** button at the bottom of the screen.
3. A confirmation message will display indicating that the group has been successfully created.

<figure><img src="../../.gitbook/assets/image (1566).png" alt=""><figcaption></figcaption></figure>

Click on the Submit button.&#x20;

<figure><img src="../../.gitbook/assets/image (1567).png" alt=""><figcaption></figcaption></figure>

The newly created group will now appear in the list under the **Groups** tab.

<figure><img src="../../.gitbook/assets/image (1568).png" alt=""><figcaption></figcaption></figure>

#### **Validation Example**

Log in using the **credentials of a user added to this group**.

They should now see **only the data filtered by `City = Dubai`** in the dashboards associated with that LDM.

<figure><img src="../../.gitbook/assets/image (1569).png" alt=""><figcaption></figcaption></figure>



