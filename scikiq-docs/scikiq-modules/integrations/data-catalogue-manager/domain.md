# Domain

### **Domain**

In data management, a domain is a broad category or field of information. It's a way to classify data based on the subject or topic it pertains to. For example, in a database, domains could include customer data, product data, employee data, and so on. Each of these represents a distinct domain within the database.

#### **Examples**&#x20;

* **Customer Data**: Covers all information related to customers, such as names and addresses.
* **Product Data**: Includes details about products, such as descriptions and pricing.
* **Employee Data**: Encompasses records related to employees, like job titles and salaries.

Each example denotes a separate domain, facilitating effective data management within a database.

### **Subdomain**

A subdomain is a more specific category or subset within a broader domain. It's a way to further organize and classify data. For instance, within the "customer data" domain, there could be subdomains for personal information, purchase history, contact details, and more. Subdomains help in structuring data within a domain, making it easier to navigate and manage.

#### **Examples of Subdomains**

* **Personal Information**: Includes data such as names, birth dates, and social security numbers.
* **Purchase History**: Encompasses transaction records, purchase timestamps, and items bought.
* **Contact Details**: Covers email addresses, phone numbers, and mailing addresses.

These examples illustrate how subdomains provide further granularity, enabling more efficient data management.

#### **Purpose of Using Domains and Subdomains**

The use of domains and subdomains serves several important purposes:

* **Organization**: They help in categorizing and structuring data systematically, making it easier to locate and manage.
* **Scalability**: By dividing data into domains and subdomains, it's easier to scale information systems as they grow.
* **Access Control**: Assigning different roles and permissions to various domains or subdomains enhances security and data privacy.
* **Efficiency**: Improves data retrieval and processing efficiency by allowing precise targeting of specific data subsets.

### How to create Data Domains in ScikIQ

*   A Domain is a logical grouping of Assets (according to their function or knowledge area), which is owned by a business area.

    * For example, _a domain named ‘Transaction Capture’ groups all assets related to customer transactions, servicing, disputes, chargebacks, and payments in a Credit Card Company._&#x74;

    Comment

CommentData Domains are high-level categories of Institutional Data for the purpose of assigning accountability and responsibility.

_**In the screenshot example below, the Settlements Data Domain is created under the Parent domain “Enterprise Data Domain” for a Client name.**_

a) Each Data Domain is expected to be created under the Parent domain.

b) By Default, Domain owners are automatically populated with client names but can be changed to anyone with the data owner privileges

<figure><img src="../../../.gitbook/assets/image (1025).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1026).png" alt=""><figcaption></figcaption></figure>

Just like catalogue, domains once created can be modified by owner.

## How to create Sub Domains in ScikIQ

* Sub-domains provide a second level of data organization. You can create deep hierarchies based on your business case requirements.
  * In the Screenshot example below, Bonds is created as a Sub-domain under a data domain called Settlement which belongs to the _Trading Catalogue for a Client name ABN Amro Clearing._

<figure><img src="../../../.gitbook/assets/image (1027).png" alt=""><figcaption></figcaption></figure>

* Sub Domain owners are automatically populated with Domain owners but can be changed to anyone with the data owner privileges
* &#x20;Sub Domains are expected to be attached to a domain
* ScikIQ data governance enables businesses to assign a Business owner and Technical owner per domain (or sub-domain) and ask them to keep it up to date.  A Subdomain allows users to further collate similar sets of data within a Business construct.

<figure><img src="../../../.gitbook/assets/image (1028).png" alt=""><figcaption></figcaption></figure>

<br>
