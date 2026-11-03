---
hidden: true
icon: page
---

# Defining DQ Rules

***

**Contents**

* [**Instructions for Using this Page**](defining-dq-rules.md#instructions-for-using-this-page)
* [**Overview**](defining-dq-rules.md#overview)
* [**Procedure**](defining-dq-rules.md#procedure)
* [**Related Topics**](defining-dq-rules.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## **Overview**

**Purpose**

The purpose of **defining Data Quality (DQ) rules** is to establish the criteria and business rules that data must satisfy to be considered accurate, complete, consistent, and valid. These rules serve as a standard for evaluating and maintaining data quality across datasets.

***

## Procedure

In the SCIKIQ application, you can define a DQ rule by specifying attributes such as the **target column, operator, comparison value, rule name,** and the applicable **data quality dimension**.&#x20;

After defining a rule, you can test it to verify its effectiveness, review the validation results, and apply the rule to the dataset during exploratory data analysis (EDA). Once validated, the rule can be saved for future use.

> <mark style="color:red;">**Note:**</mark> You can define/apply multiple rules to a column.

The below **step-by-step instructions** help you understand how to define data quality rules:

_**To define DQ rules**_

1. On the **Data Profiling** page, click the **Define DQ Rules** button on the **Top Menu.**

The **Data Quality Rules** page is displayed in a new window.

2. On the **DQ Rules** page, define the quality by specifying the required **column, operator, value, rule name,** and **DQ dimensions**, and then click the **Test** button.

<figure><img src="../../../.gitbook/assets/image (2412).png" alt=""><figcaption></figcaption></figure>

The Rule List page is displayed with the applied data quality rule test result.&#x20;

<figure><img src="../../../.gitbook/assets/image (2413).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * To **remove** a rule, click the **Delete** ![](<../../../.gitbook/assets/image (2414).png>) button corresponding to that rule.
> * To **view** the rule information of a rule, click the **Rule Information** ![](<../../../.gitbook/assets/image (2415).png>) button.
> * To **test** a rule, click the **Test Rule** ![](<../../../.gitbook/assets/image (2416).png>) button corresponding to it.

3. Next, on the  **Rule List** page, click the **Apply** button.

<figure><img src="../../../.gitbook/assets/image (2420).png" alt=""><figcaption></figcaption></figure>

The specified DQ rule are applied and the **Success** message is displayed.

4. Now, click the **Save** button to save the applied DQ rules.

<figure><img src="../../../.gitbook/assets/image (2422).png" alt=""><figcaption></figcaption></figure>

The **Save DQ** dialogue box is displayed.

5. On the **Save DQ** dialogue box, specify a **name** for the DQ rule, and then click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (2423).png" alt=""><figcaption></figcaption></figure>

The defined DQ rules are saved and the **Success** message is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (2424).png" alt=""><figcaption></figcaption></figure>

***

## Related Topics

* [**Creating a New EDA Version**](creating-a-new-eda-version.md)
* [**Downloading Sample Data**](downloading-sample-data.md)
* [**Exporting EDA**](exporting-eda.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
