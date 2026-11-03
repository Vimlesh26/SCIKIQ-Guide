---
icon: page
---

# Deploying a Data Product

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The process of deploying a data product involves a series of configuration and review steps to ensure that it is deployed correctly. These steps include _General Configuration, Access Configuration, Metadata Configuration, Deployment Configuration, and Review & Deploy_.

The below Procedure section provides a detailed description of each of these:

***

### Procedure

Click on the below tabs to view step-by-step instructions.

{% tabs %}
{% tab title="General Configuration" %}
1. On the **Data Product Marketplace Registration** message box, click the **Ok** button. See the below image.

<figure><img src="../../../.gitbook/assets/image (2652).png" alt=""><figcaption></figcaption></figure>

The Product page is displayed.

2. On the **Product** page, click the **Deploy** tab.

<figure><img src="../../../.gitbook/assets/image (2655).png" alt=""><figcaption></figcaption></figure>

The General Configuration section is displayed.

3. On the **General Configuration** section, specify the **Data Product Type** choosing from **Dashboard as a Service, LDM as a Product, AI as a Product,** and **Data as a Product.**
4. Select **Cloud Provider** and then click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2656).png" alt=""><figcaption></figcaption></figure>

The Access Configuration section is displayed.

5. Next, click [**Access Configuration**](deploying-a-data-product.md#access-configuration).
{% endtab %}

{% tab title="Access Configuration" %}
**Overview**

As part of **Access Configuration**, you need to configure the client credentials and infrastructure settings required to securely deploy and access the data product. This includes entering the **Client Name**, **Client Email**, and **Client Password**, and confirming the password.&#x20;

You also need to configure the required access and cloud infrastructure details, including the **Access Key**, **Secret Key**, **Region**, **Bucket**, **VPC**, **Subnets**, and **Security Group**.&#x20;

Together, these settings help establish the required authentication, secure access, and network environment for the successful deployment and use of the data product.

**Procedure**

1. On the **Access Configuration** section:

A. Specify **Client Name, Client Email, Client Password**, and **confirm Client Password.**

B. Also, specify **Access Key, Secret Key, Region, Bucket, VPC, Subnets,** and **Security Group.**

C. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2657).png" alt=""><figcaption></figcaption></figure>

The Metadata DB Configuration section is displayed.

2. Next, click [**Metadata DB Configuration**](deploying-a-data-product.md#metadata-db-configuration)**.**&#x20;
{% endtab %}

{% tab title="Metadata DB Configuration" %}
**Overview**

Configuring the **Metadata Configuration** helps set up the database environment required to store and manage the deployed data product's metadata.

Settings such as **Metadata DB, Engine Version, DB Cluster Identifier, DB Name, credentials, DB Instance Class,** and **DB Deployment Options** ensure that the database is configured with the appropriate capacity, access, and deployment settings for reliable operation.

**Procedure**

1. On the **Metadata DB Configuration** section, specify **Metadata DB, Engine Version, DB Cluster Identifier, DB Name, Master User Name, Master User Password, DB Interface Class,** and **DB Deployment Options**.
2. Click the **Reuse Instance** button.

<figure><img src="../../../.gitbook/assets/image (2658).png" alt=""><figcaption></figcaption></figure>

The deployment process starts. See the image below.

<figure><img src="../../../.gitbook/assets/image (2659).png" alt=""><figcaption></figcaption></figure>

3. Once the deployment is completed, click the **Next** button.

The Deployment Configuration section is displayed.

4. Next, click [**Deployment Configuration**](deploying-a-data-product.md#deployment-configuration).
{% endtab %}

{% tab title="Deployment Configuration" %}
**Overview**

Configuring the **Deployment Configuration** defines how and where the data product is deployed and runs. Settings such as **Deployment Type, ECS Cluster Name, Load Balancer Type, ECS Task Role,** and **ECS Task Execution Role** help specify the deployment environment, manage traffic to the deployed product, and provide the required permissions for ECS tasks to run and access necessary resources securely.

**Procedure**

1. On the **Deployment Configuration** section, specify **Deployment Type,  ECS Cluster Name, Load Balancer Type, ECS Task Role,** and **ECS Task execution Role.**&#x20;
2. Click the **Next** button.

<figure><img src="../../../.gitbook/assets/image (2661).png" alt=""><figcaption></figcaption></figure>

The Review & Deploy section is displayed.

3. Next. click **Review & Deploy**.
{% endtab %}

{% tab title="Review & Deploy" %}
**Overview**

**Reviewing the deployment details** before deploying helps verify that all configurations, settings, and required information are correct and complete. This helps identify and correct any errors before deployment, reducing the risk of deployment failures and ensuring that the data product is deployed with the intended configuration.

**Procedure**

* On the **Review & Deploy** section, review the details, and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (2663).png" alt=""><figcaption></figcaption></figure>

The Deployment Progress screen is displayed showcasing the deployment progress. Once completed, the data product is displayed on the Product List page.
{% endtab %}
{% endtabs %}

### Related Topics

* [**Managing Product Deployments**](managing-product-deployments.md)&#x20;

