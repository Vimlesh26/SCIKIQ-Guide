---
hidden: true
icon: clipboard-user
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# SCIKIQ ARCHIVAL

**Contents**

* [**Instructions for Using this Page**](./#instructions-for-using-this-page)
* [**About Data Archival**](./#id-1.about-data-archival)
* [**About SCIKIQ Data Archival**](./#id-2.about-data-archival)
* [**Related Topics**](./#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

<details>

<summary><strong>1.About Data Archival</strong></summary>

Data Archival is the process of moving old or rarely used data to a separate storage location for long-term preservation. The archived data is not used in daily operations but is kept for future reference, legal compliance, or historical analysis. &#x20;

Archiving also frees up space in active systems and improves system performance by keeping only frequently used data in the main system.

</details>

<details>

<summary><strong>2.About SCIKIQ Data Archival</strong></summary>

SCIKIQ Archival is a data lifecycle management system that moves inactive or historical data from production databases to cost-effective cloud storage such as Amazon S3.&#x20;

As enterprise databases grow with continuous data generation, they can cause slow queries, higher infrastructure costs, longer backups, and maintenance difficulties. SCIKIQ Archival solves this by identifying inactive data through predefined policies and archiving it securely.&#x20;

The archived data remains accessible for auditing, compliance, and historical analysis without affecting the performance of the production system.&#x20;

</details>

<details>

<summary><strong>3.Architecture Overview</strong></summary>

SCIKIQ acts as a middleware archival engine between the production database and cloud storage, enabling the efficient movement and management of historical data.&#x20;

The architecture includes the following components:&#x20;

* Application System: The business application that generates operational data. The examples include Banking systems, Telecom billing platforms, Healthcare management systems, etc.&#x20;
* AWS Storage Buckets: Archived data is stored in Amazon S3 buckets, which are organized into different storage tiers based on how frequently the data is accessed.&#x20;

Lifecycle Management: AWS lifecycle policies automatically move archived data between storage tiers to optimize storage costs over time.

</details>

## Related Topics

* [**Configuring SCIKIQ Archival**](configuring-scikiq-archival/)



[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
