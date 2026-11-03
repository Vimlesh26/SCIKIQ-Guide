---
hidden: true
icon: container-storage
---

# Logical Data Model

### What Is a Logical Data Model? <a href="#what-is-a-logical-data-model" id="what-is-a-logical-data-model"></a>

* A "LDM" stands for "Logical Data Model." A Logical Data Model is a high-level representation of an organization's data, often used in database design and data management. It defines the structure and relationships of data elements without specifying how they are physically implemented in a database.
* Logical data models bring together the two most vital basics of application development — business requirements and quality data structure — into a visual representation.&#x20;
* Business analysts and data architects are responsible for creating these models. They map relevant business processes and reveal the business requirements in order to create a model that meets company goals. Moreover, they prepare a technical map of rules and structures depending on the scope of the project.

### Components of a Logical Data Model

* A logical data model has three main components:
  * **Entities** are the objects we want to represent in our data model and are usually represented by a table. Examples of entities include customers, orders, products, or categories.
  * **Attributes** appear as columns in specific tables. Examples include product identifier and product name (for the _Product_) category identifier and category name (for the _Category_).
  * **Relationships** define the associations between entities. This may be 1:1, 1:N, or M: N. For example, one product could be related to another by a specific product category.

### Needs of the Logical Data Model:

1. **Data Clarity**: LDM provides clear data definitions, ensuring that data elements are well-understood.
2. **Data Consistency**: It maintains consistency in data representation, which is crucial for dashboard accuracy.
3. **Data Quality**: LDM promotes data quality and integrity by setting standards and validation rules.
4. **Data Integration**: It simplifies data integration from multiple sources.
5. **Data Governance**: LDM is essential for data governance, including security, access, and compliance.
6. **Scalability**: It allows for scalability to adapt to changing data needs.
7. **Collaboration**: Fosters collaboration and shared understanding among teams.
8. **Documentation**: Provides documentation of the data model for easy reference.
9. **Reducing Redundancy**: Identifies and eliminates redundant data elements, reducing costs.
10. **Better Decision-Making**: Supports data-driven decision-making by ensuring data accuracy and consistency.

### Create Logical Data Models in ScikIQ

Navigate to Logical Data Models

* Begin by logging into ScikiQ, and then navigate to the "Logical Data Model" sub-menu.

<figure><img src="../../.gitbook/assets/image (917).png" alt=""><figcaption></figcaption></figure>

After clicking on the "LDM" tab, the screen will appear as shown below

<figure><img src="../../.gitbook/assets/image (918).png" alt=""><figcaption></figcaption></figure>

### Features on the Right Side of the LDM Page

Here are some of the key features available on the right side of the Logical Data Model page:

#### Define Relationship

The "Define Relationship" section illustrates the interconnections between tables, displaying how many entries in one table correspond to those in another, and the direction in which data flows. These relationships are crucial for understanding data integration, guiding database design, and facilitating effective data analysis.

<figure><img src="../../.gitbook/assets/image (919).png" alt=""><figcaption></figcaption></figure>

#### **Fullscreen** <a href="#fullscreen" id="fullscreen"></a>

* This option helps the user to view the LDM page on full screen.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FmGYZqkh65EyUMW2lFsQe%2Fuploads%2FJT6KqgBHA9rmLBIvm3RB%2Fimage.png?alt=media&#x26;token=fa7db02d-a2a9-4ae2-8f17-4cf425b82bb0" alt=""><figcaption></figcaption></figure>

#### **Clear** <a href="#clear" id="clear"></a>

* It will clear the entire selected tables or functionalities on the LDM page.

<figure><img src="../../.gitbook/assets/image (920).png" alt=""><figcaption></figcaption></figure>

### **Save** 

* This helps the user to save the LDM job created.

<figure><img src="../../.gitbook/assets/image (921).png" alt=""><figcaption></figcaption></figure>

### Steps for LDM creation

In SCIKIQ, it's essential to establish a source connection for analysis. This source can take the form of a database, spreadsheet, or an accessible data source via an API.

#### Step 1: Begin by logging into SCIKIQ, and then navigate to the "Logical Data Model" sub-menu.

<figure><img src="../../.gitbook/assets/image (922).png" alt=""><figcaption></figcaption></figure>

After clicking on the "LDM" tab, the screen will appear as shown below:

<figure><img src="../../.gitbook/assets/image (923).png" alt=""><figcaption></figcaption></figure>

#### Step 2:

* Choose the source type, and it will display the connected connections in the drop-down menu. Select the appropriate connection from the list

<figure><img src="../../.gitbook/assets/image (924).png" alt=""><figcaption></figcaption></figure>

### Create Star Schema-----In prog.....

#### Step 3:

* Use drag and drop to select the table, as shown in the screen below.

<figure><img src="../../.gitbook/assets/image (925).png" alt=""><figcaption></figcaption></figure>

#### Step 4:

* Here, you can select columns based on your needs or edit the alias names for columns as required.

<figure><img src="../../.gitbook/assets/image (926).png" alt=""><figcaption></figcaption></figure>

#### Step 5:

* Click on the **relationship icon,** and you can define relationships between the selected tables. here Choose the source table and target tables.

<figure><img src="../../.gitbook/assets/image (927).png" alt=""><figcaption></figcaption></figure>

**Relationship Type**:&#x20;

* **One-to-One (1:1)**: Each record in the source table is related to one and only one record in the target table, and vice versa.
* **One-to-Many (1:N)**: Each record in the source table can be related to multiple records in the target table, but each record in the target table is related to only one record in the source table.
* **Many-to-One (N:1)**: The reverse of one-to-many, where multiple records in the source table can be related to one record in the target table.
* **Many-to-Many (N: N)**: Multiple records in the source table can be related to multiple records in the target table, and vice versa.

#### Step 6:

* On this page, you can view established relationships. Here, you have the option to create additional relationships between tables, modify existing ones, or remove defined relationships.

<figure><img src="../../.gitbook/assets/image (928).png" alt=""><figcaption></figcaption></figure>

#### Step 7:

* Click on the "**Save**" button.&#x20;
* It will prompt you to provide metadata and governance details.&#x20;
* After entering the necessary information and specifying the LDM name.
* click the "Finish" button. This action will add the LDM to the list.

<figure><img src="../../.gitbook/assets/image (929).png" alt=""><figcaption></figcaption></figure>

#### Step 8:

* &#x20;When you have created the logical data model (LDM) you'll find it listed on the business data model page. This is where you can see all your LDMs and datasets.

<figure><img src="../../.gitbook/assets/image (930).png" alt=""><figcaption></figcaption></figure>
