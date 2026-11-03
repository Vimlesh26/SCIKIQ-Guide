# Notify Node

**Contents**

* [**Instructions for Using this Page**](notify-node.md#instructions-for-using-this-page)
* [**Overview**](notify-node.md#overview)
* [**Procedure**](notify-node.md#procedure)
* [**Related Topics**](notify-node.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]

***

## Overview

This page explains how to use the **Notify** nod&#x65;**.** It is used to send automated alerts or messages when specific conditions in the data pipeline are met. This helps users monitor the pipeline, detect errors, and receive updates about important events during pipeline execution.

The **Notify Node** sends notifications based on conditions. The following are the different types of notifications:

* Email
* Webhook
* API Write

***

## Procedure

The procedure to use the **Notify** node involves the steps including [Add and Connect Notify Node](notify-node.md#add-and-connect-notify-node), [Configure Notify Node Settings,](notify-node.md#configure-notify-node-settings) [Save Pipeline](notify-node.md#save-pipeline), and [Preview Result](notify-node.md#preview-result). The expandable panels below provide guided assistance for each step in the procedure.&#x20;

Expand the panels to view detailed, step-by-step instructions.

<details>

<summary><strong>Add Notify Node</strong></summary>

1. On the **Left Navigation Bar**, under **SCIKIQ CONNECT**, expand **SCIKIQ Delta Hub,** and then click either **Create API Pipeline** or **Create Delta Pipeline**. For example, Create Delta Pipeline.

<figure><img src="../../../../.gitbook/assets/S.png" alt=""><figcaption><p>Create Delta Pipeline Menu Item</p></figcaption></figure>

The Create Delta Pipeline page is displayed.

2. From the **Top Toolbar**, drag the **Notify node** on to the **Main Workspace.**
3. Connect the **Notify node** to the node whose output triggers the notificatio&#x6E;**.**

<figure><img src="../../../../.gitbook/assets/S (306).png" alt=""><figcaption><p>Connecting Notify Node</p></figcaption></figure>

Once connected, the Notify section is displayed on the left pane.

</details>

<details>

<summary><strong>Configure Notify Node Settings</strong></summary>

**Procedure:**

The below step-by-step instructions describe how to select database type:

**Step-by-Step Instructions**

1. On the **Left Pane,** click the **Add** ![](<../../../../.gitbook/assets/image (2491).png>) .

The Notify expandable panel is displayed.

2. Expand the **Notify** **expandable panel**, and then from the **Notify drop-down box**, select the **notification channel** choosing from **Webhook, API Write,** or **Email.** For example, Email.

{% hint style="info" %}
**Tip:** The **notification channels** specify how the notification will be sent when the **Notify node** is triggered in the pipeline.

Here is the description of these channels:

* **Webhook:** This channel sends a notification to another application through an **HTTP request**.
* **API Write:** This channel  sends notification data to another system using an **API call**.
* **Email:** This channel sends a **notification email** to specified recipients.
{% endhint %}

&#x20;3\. From the **Email Config** drop-down box, select the **email config**. For example, Gmail SMTP.

4. From the **Email Template** drop-down box, select the **required template.**

{% hint style="info" %}
**Tip:** If required, you can create a new template by clicking the **Add Template** ![](<../../../../.gitbook/assets/image (2492).png>) link.
{% endhint %}

4. Click the **Email Config** tab, and then specify the To Email.
5. In the Subject field, change the subject if required.
6. Enable **Data Repeat, Attached Table,** and **From Column** based on the requirement. Refer to the below tip for the description of these.

{% hint style="info" %}
**Tip:**&#x20;

* **Data Repeat:** Enable this option repeats the email content for each record in the dataset.
* **Attached Table:** Enable this option adds the dataset as a table in the email.
* **From Column:** Enable this option uses email addresses from a data column as recipients.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/S (307).png" alt=""><figcaption><p>Configuring Notify Node Settings</p></figcaption></figure>













</details>

<details>

<summary><strong>Save Pipeline</strong></summary>

**Procedure**

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1. On the extreme right of the **Top Toolbar**, click the **Save** button.

<figure><img src="../../../../.gitbook/assets/S (13).png" alt=""><figcaption></figcaption></figure>

The Save Data Pipeline dialogue box is displayed.

2. In the **Name** field, enter a **name** for the pipeline.&#x20;
3. In the **Description,** enter the **summary** of the delta pipeline.
4. Next, configure the **meta data** by specifying **Catalogue, Data Domain, Sub Data Domain, Business Owner,** and **Technical Owner.**
5. Finally, click the **Save and Submit** button.

<figure><img src="../../../../.gitbook/assets/S (308).png" alt="" width="563"><figcaption><p>Saving Pipeline</p></figcaption></figure>

The Pipeline is saved.

</details>

<details>

<summary><strong>Preview Result</strong></summary>

**Procedure**&#x20;

The information below outlines the step-by-step instructions for completing this task:

**Step-by-Step Instructions**

1\. On the **Data Pipelines** page, click the **Edit** icon corresponding to the **Notify** node.

The connected nodes are displayed.

2. On the **Right Pane**, click the **Preview** icon on the top of **Notify** nod&#x65;**.**
3. Click the **Preview** icon on the top of **Notify** node.&#x20;

Once triggered, the notification is sent to the configured email address. See the example image below.

<figure><img src="../../../../.gitbook/assets/S (309).png" alt=""><figcaption><p>Notification Email</p></figcaption></figure>



</details>

## Related Topics

* [Configuring Input Nodes](/broken/pages/Qe52MzyFrHp43dWO41kf)
* [Configuring Output Nodes](/broken/pages/BOHoiMbsoFJCedoWAASx)
* [Configuring Transform Nodes](/broken/pages/hbzg9uHn194g3ivtwx4q)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
