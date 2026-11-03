---
hidden: true
icon: sliders
---

# Deployment Configs

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format._<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The purpose of setting up a deployment platform such as Amazon ECS Cluster or Kubernetes Pod while creating an archival job is to provide the runtime environment where the archival processes are executed. It enables scalable and efficient handling of large volumes of data by distributing workloads across containers. This setup ensures high availability, fault tolerance, and better resource utilization during data archiving.

Overall, it improves performance, reliability, and operational control of the archival process.

***

### Deployment Tasks

{% tabs %}
{% tab title="Setup Deployment Platform " %}
As part of setting up the deployment platform, you can setup either Amazon ECS Cluster or Kubernetes Pod.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup Deployment on Amazon ECS Cluster</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival,** and then expand **Archival Jobs.**
2. On the expanded menu, click **Deployment Config.**

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

3. The Deployment Configuration page displayed. Click on **"+New Configuration"** Button

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

4. On the **Deployment Configuration** page, specify the **Configuration Name, Description,** and **select Amazon ECS Cluster.**

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

The Amazon ECS Cluster fields are displayed.

5. In the **Amazon ECS Cluster** fields, fill the required details, and then click the **Save Configuration** button.

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

The config is Created.

</details>

<details>

<summary><strong>2.Setup Deployment on Kubernetes POD</strong></summary>

1. On the **Deployment Configuratio**n page, specify the **Configuration Name, Description,** and **select Kubernetes POD.**&#x20;

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

The Kubernetes POD Configuration fields are displayed.

2. &#x20;In the **Kubernetes POD Configuration** fields, specify **CPU Units, Memory,** and then click the **Save Configuration** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

The config is created.

</details>
{% endtab %}

{% tab title="Manage Deployment Configurations" %}

{% endtab %}
{% endtabs %}

### Procedure

As part of setting up the deployment platform, you can setup either Amazon ECS Cluster or Kubernetes Pod.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup Deployment on Amazon ECS Cluster</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival,** and then expand **Archival Jobs.**
2. On the expanded menu, click **Deployment Config.**

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

3. The Deployment Configuration page displayed. Click on **"+New Configuration"** Button

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

4. On the **Deployment Configuration** page, specify the **Configuration Name, Description,** and **select Amazon ECS Cluster.**

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

The Amazon ECS Cluster fields are displayed.

5. In the **Amazon ECS Cluster** fields, fill the required details, and then click the **Save Configuration** button.

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

The config is Created.

</details>

<details>

<summary><strong>2.Setup Deployment on Kubernetes POD</strong></summary>

1. On the **Deployment Configuratio**n page, specify the **Configuration Name, Description,** and **select Kubernetes POD.**&#x20;

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

The Kubernetes POD Configuration fields are displayed.

2. &#x20;In the **Kubernetes POD Configuration** fields, specify **CPU Units, Memory,** and then click the **Save Configuration** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

The config is created.

</details>

***

### Manage Deployment Configurations

***

#### Overview

The Deployment Configuration Management functionality provides a centralized way to manage and control deployment configurations for archival processes. It allows you to view, update, and delete archival configurations as required, ensuring flexibility and accuracy in setup.

***

#### Procedure

As part of deployment configuration management, you can update the required archival configuration. If required, you can also delete an archival configuration.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Update Deployment Configuration</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Deployment Config**.

<figure><img src="../../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

The **Job Deployment Configurations** page is displayed.

3. On the **Job Deployment Configurations** page, click the **Edit** button corresponding to the required archival configuration.

<figure><img src="../../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

The **Deployment Config Management page** is displayed.

4. On the **Deployment Config Management page**, make the required changes, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (1684).png" alt=""><figcaption></figcaption></figure>

5. The Deployment Configuration is updated as per the changes made.

<figure><img src="../../../.gitbook/assets/image (1685).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>2.Delete Deployment Configuration</strong></summary>

1. On the **Job Deployment Configurations** page, click the **Delete** button corresponding to the required archival configuration.

<figure><img src="../../../.gitbook/assets/1 (12).png" alt=""><figcaption><p>Deployment Config Management - Delete Button </p></figcaption></figure>

The Delete message box is displayed.

2. On the **Delete** message box, click the **OK** button.

<figure><img src="../../../.gitbook/assets/image (1596).png" alt=""><figcaption></figcaption></figure>

3. The archival configuration is deleted.

</details>

***

### Related Topics

* [**Connect SCIKIQ to Source Database**](/broken/pages/NQamWuz7vUgQ2NLWzOdj)
* [**Configure Table Classification**](../../integrations/vs-meta-data-manager/table-classification.md)
* [**Create Compliance Framework**](../compliance/regulatory-compliance.md)
* [**Create Compliance Policy**](../compliance/compliance-policies.md)
* [**Configure AWS Setup**](../storages/configure-storage.md)
* [**Create Archival Job**](creating-a-table-archival-job.md)
* [**Deploy Archival Job**](/broken/pages/Lhd7keqyZR2EfkoA5qpT#id-2.deploy-archival-job)
* [**Validate Archived Data**](retrieve-data.md#validate-archived-data)
* [**View Archived Data**](retrieve-data.md)
* [**Delete Archived Data**](deletion-jobs.md)
