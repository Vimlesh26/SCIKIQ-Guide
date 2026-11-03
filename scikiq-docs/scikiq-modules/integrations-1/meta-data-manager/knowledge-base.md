---
icon: page
---

# Knowledge Base

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to manage knowledge base. A **Knowledge Base** in metadata stores business questions or user entries along with their corresponding SQL queries. It helps map natural-language questions to SQL queries, enabling users to retrieve relevant data more easily and improving the consistency of data access and analysis.

***

### Managing **Knowledge Base**

{% tabs %}
{% tab title="Navigating to Knowledge Base Management Page" %}
**Overview**

This section describes how to navigate to the **Knowledge Base** page. Follow the below mentioned step-by-step instructions.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Control**, and then expand **Meta Data Manager**.

&#x20;     The Meta Data Manager menu is displayed.

2. From the **Meta Data Manager** menu, select **Knowledge Base.**

<figure><img src="../../../.gitbook/assets/image (3150).png" alt=""><figcaption></figcaption></figure>

The Knowledge Base Management page is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (3151).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Adding a Knowledge Base Entry" %}
**Overview**

This section describes how to add a knowledge base entry. **Adding a Knowledge Base entry** enables to map natural-language questions to corresponding SQL queries and specify the relevant domain, database connection, table, and columns. This helps the system retrieve relevant data and provide more accurate responses to user queries.

**Procedure**

The below step-by-step instructions help you understand how to add a knowledge base entry in Knowledge Base Management.

_**To add a knowledge base entry**_&#x20;

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**Specify Knowledge Entry Details**

1. On the **Knowledge Base Management** page, click the **Add New** button.

<figure><img src="../../../.gitbook/assets/image (3152).png" alt=""><figcaption></figcaption></figure>

The **Add Knowledge Base Entry** dialogue box is displayed.

3. On the **Add Knowledge Base Entry** dialogue box:

A. In the **User Query** box, enter your **natural-language question** that represents the information, which you want to retrieve.

B. In the **SQL Query** box, enter the **SQL statement** corresponding to the  query to retrieve the required data from the database.

C. From the **Domain** drop-down box, select the **business domain** to which the query belongs.

D.  From the **Connection** drop-down box, select the **database connection** from which the required data is retrieved.

E. From the **Table** drop-down box, select the **database table** containing the data required to answer the user query.

G. From the **Column** drop-down box, select the **table columns** required to retrieve the relevant information.

> <mark style="color:red;">**Note:**</mark>
>
> * To add more rows to Physical Schema Mapping, click the **Add Row** button.
> * To delete a row from the Physical Schema Mapping, click the **Delete** button corresponding to it.

H. Finally, click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3155).png" alt=""><figcaption></figcaption></figure>

The knowledge base entry is created and displayed on the Knowledge base Management page. See the below image.

<figure><img src="../../../.gitbook/assets/image (3154).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Viewing Knowledge Entry Details" %}
**Overview**

This section describes how to view the details of a knowledge base entry. **Viewing the details of a Knowledge Base entry** helps to review the user query, corresponding SQL query, and associated domain, connection, table, and column details to verify the configuration and ensure accurate data retrieval.

**Procedure**

The below step-by-step instructions help you understand how to view the details of a knowledge base entry.

_**To view the details of a knowledge base entry**_&#x20;

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**View Knowledge Base Entry Details**

1. On the **Knowledge Base Management** page, click the **View Details** icon corresponding to the required knowledge base entry.

<figure><img src="../../../.gitbook/assets/image (3156).png" alt=""><figcaption></figcaption></figure>

The **Knowledge Base Entry** screen appears by displaying the details.

<figure><img src="../../../.gitbook/assets/image (3158).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Sending for Approval" %}
**Overview**

This section describes how to send a knowledge base entry for approval. **Sending a Knowledge Base entry for approval** enables designated reviewers to validate the user query, corresponding SQL query, and associated metadata before approval, ensuring accuracy and compliance with data governance standards.

**Procedure**

The below step-by-step instructions help you understand how to send a knowledge base entry for approval.

_**To send a knowledge base entry for approval**_

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**Configure Approval Mapping**

1. On the **Knowledge Base Management** page, click the **Send for Approval** icon corresponding to the required knowledge base entry.

<figure><img src="../../../.gitbook/assets/image (3159).png" alt=""><figcaption></figcaption></figure>

The **Send Selected Knowledge Base Entry(s) for Approval** screen is displayed.

2. On the **Send Selected Knowledge Base Entry(s) for Approval** screen:

A. From the **User** drop-down box, select the **approver**.

B. Click the **Send for Approval** button.

<figure><img src="../../../.gitbook/assets/image (3160).png" alt=""><figcaption></figcaption></figure>

After submitting the Knowledge Base entry for approval, its **Sent Status is displayed as Submitted** and its **Approval Status as Pending** on the Knowledge Base Management page.

<figure><img src="../../../.gitbook/assets/image (3161).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Updating a Knowledge Base Entry" %}
**Overview**

This section describes how to update a knowledge base entry. **Updating a Knowledge Base entry** allows to modify the user query, SQL query, or associated metadata to reflect changes in business requirements or data structures.&#x20;

This may be necessary to correct errors, update query logic, or keep the entry accurate and relevant.

**Procedure**

The below step-by-step instructions help you understand how to update a knowledge base entry.

_**To update a knowledge base entry**_

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**Update the knowledge base entry**

1. On the **Knowledge Base Management** page, click the **Edit** icon corresponding to the required knowledge base entry.

<figure><img src="../../../.gitbook/assets/image (3162).png" alt=""><figcaption></figcaption></figure>

The **Edit Knowledge Base Entry** screen is displayed.

2. On the **Edit Knowledge Base Entry** screen, **make the required changes**, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (3163).png" alt=""><figcaption></figcaption></figure>

The **Knowledge Base Entry** is updated as per the changes made.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deleting a Knowledge Base Entry" %}
**Overview**

This section describes how to delete a knowledge base entry. **Deleting a Knowledge Base entry** allows to remove outdated, incorrect, or redundant entries that are no longer required.&#x20;

This helps maintain an accurate and relevant knowledge base and prevents obsolete queries from being used.

**Procedure**

The below step-by-step instructions help you understand how to delete a knowledge base entry.

_**To delete a knowledge base entry**_

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**Delete the knowledge base entry**

1. On the **Knowledge Base Management** page, click the **Delete** icon corresponding to the required knowledge base entry.

<figure><img src="../../../.gitbook/assets/image (3165).png" alt=""><figcaption></figcaption></figure>

The **Delete** message is displayed.

2. On the **Delete** message, click the **Delete** button.

<figure><img src="../../../.gitbook/assets/image (3166).png" alt=""><figcaption></figcaption></figure>

The **Knowledge Base Entry** is deleted.
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Bulk Uploading of Knowledge Base Entries" %}
**Overview**

This section describes how to upload knowledge base entries in bulk. **Bulk uploading Knowledge Base entries** allows to add multiple entries at once using a supported file format, reducing manual effort, saving time, and ensuring consistency when managing large volumes of knowledge base data.

**Procedure**

Uploading Knowledge Base entries in bulk involves the steps including **downloading the Knowledge Base entry template, entering the entries in the template,** and **uploading the completed template.**

Follow the step-by-step instructions below to upload Knowledge Base entries in bulk.

_**To upload knowledge base entries in bulk**_

{% stepper %}
{% step %}
**Navigate to Knowledge Base Management page**

SCIKIQ Left Navigation Bar>>SCIKIQ Control>>Meta Data Manager>> Knowledge Base Management.
{% endstep %}

{% step %}
**Download Knowledge Base Entry Template**

1. On the **Knowledge Base Management** page, click the **Import** button.

<figure><img src="../../../.gitbook/assets/image (3167).png" alt=""><figcaption></figcaption></figure>

The **Import Knowledge Base Data** screen is displayed.

2. On the **Import Knowledge Base Data** screen, click the **Download Template** button.

<figure><img src="../../../.gitbook/assets/image (3168).png" alt=""><figcaption></figcaption></figure>

The template is downloaded in XLSX format in the local system.
{% endstep %}

{% step %}
**Enter the KB entries in the template**&#x20;

1. Browse to the location where the template is downloaded, and then open it.
2. In the template, required number of KB entries, and then save it.&#x20;
{% endstep %}

{% step %}
**Upload the Completed Template**

1. Go back to the Knowledge Base Template, and again click the click the **Import** button.

The **Import Knowledge Base Data** screen is displayed.

2. On the **Import Knowledge Base Data** screen, click the **Choose File** button to browse to the location where the completed templated, and then select it.&#x20;

<figure><img src="../../../.gitbook/assets/image (3169).png" alt=""><figcaption></figcaption></figure>

The template entries are uploaded and displayed on the Knowledge Base Management page.
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}

### Related Topics

* [**Assets**](../../integrations/meta-data-manager/assets/)
* [**Data Dictionary**](../../integrations/meta-data-manager/data-dictionary/)
* [**Dataset Metadata**](../../integrations/meta-data-manager/dataset-metadata/)
* [**Glossary**](../../integrations/meta-data-manager/glossary/)
* [**Business Terms**](../../integrations/meta-data-manager/business-terms/)
