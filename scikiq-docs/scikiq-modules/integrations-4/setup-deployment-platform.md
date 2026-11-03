# Setup Deployment Platform

***

**Contents**

* [**Instructions for Using this Page**](setup-deployment-platform.md#instructions-for-using-this-page)
* [**Overview**](setup-deployment-platform.md#overview)
* [**Procedure**](setup-deployment-platform.md#procedure)
* [**Related Topics**](setup-deployment-platform.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

The purpose of setting up a deployment platform such as Amazon ECS Cluster or Kubernetes Pod while creating an archival job is to provide the runtime environment where the archival processes are executed. It enables scalable and efficient handling of large volumes of data by distributing workloads across containers. This setup ensures high availability, fault tolerance, and better resource utilization during data archiving.

Overall, it improves performance, reliability, and operational control of the archival process.

***

## Procedure

As part of setting up the deployment platform, you can setup either Amazon ECS Cluster or Kubernetes Pod.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup Deployment on Amazon ECS Cluster</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival,** and then expand **Archival Jobs.**
2. On the expanded menu, click **Deployment Config.**

<figure><img src="../../.gitbook/assets/image (233).png" alt=""><figcaption><p>Deployment Config Menu Item</p></figcaption></figure>

The Deployment Configuration page displayed.

3. On the **Deployment Configuration** page, specify the **Configuration Name, Description,** and **select Amazon ECS Cluster.**

<figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption><p>Deployment Configuration Page</p></figcaption></figure>

The Amazon ECS Cluster fields are displayed.

4. In the **Amazon ECS Cluster** fields, fill the required details, and then click the **Save Configuration** button.

<figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption><p>Amazon ECS Cluster Fields</p></figcaption></figure>

The config is deployed.

</details>

<details>

<summary><strong>2.Setup Deployment on Kubernetes POD</strong></summary>

1.On the **Deployment Configuratio**n page, specify the **Configuration Name, Description,** and **select Kubernetes POD.**&#x20;

<figure><img src="../../.gitbook/assets/image (236).png" alt=""><figcaption><p>Deployment Configuration Page</p></figcaption></figure>

The Kubernetes POD Configuration fields are displayed.

2\. In the **Kubernetes POD Configuration** fields, specify **CPU Units, Memory,** and then click the **Save Configuration** button.&#x20;

<figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption><p>Kubernetes POD Configuration Fields</p></figcaption></figure>

The config is deployed.

</details>

***

## Related Topics

* [Connect SCIKIQ to Source Database](/broken/pages/1miPFvCEFxfy7uZat3C4)
* [Configure Table Classification](/broken/pages/fy1vjHIN7Nys8uAuddaO)
* [Create Compliance Framework](/broken/pages/J0o8JvIQ5NXn822xZNDA)
* [Create Compliance Policy](/broken/pages/5gBXOCk95Uv7C11YfBLO)
* [Configure AWS Setup](/broken/pages/26PZ6KCui7ZjC3abzdND)
* [Create Archival Job](/broken/pages/54s7haLhTK625sePPPzh)
* [Setup Deployment Platform](/broken/pages/qpdRebf35FBbmvMZlRTo)
* [Deploy Archival Job](/broken/pages/hEN0BpaQWg865JKIDrtG)
* [Manage Deployment Configurations](/broken/pages/ctJKSQVRrDMRLHYUvlWy)
* [Validate Archived Data](/broken/pages/RWHaxNCgJded7Q8xd9FP)
* [View Archived Data](/broken/pages/6xWaChqxS1moikwvFJk7)
* [Delete Archived Data](/broken/pages/oXzQfmDzcrDAFOL2TO5w)



[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
