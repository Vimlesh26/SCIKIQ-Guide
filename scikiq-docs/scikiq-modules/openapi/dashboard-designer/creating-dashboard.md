---
icon: laptop-binary
---

# Creating Dashboard

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The process of creating a dashboard involves a series of sequential steps. To begin, navigate to the Dashboard Designer page, where you can provide a title for the dashboard and optionally add a logo.

On the Dashboard Designer page, you can select either a custom template or a prebuilt template based on your requirements. Once a template is selected, the Page Styling section becomes available under the Styling panel, allowing you to configure the dashboard layout, height, width, background color, and theme.

After defining the template and page styling, you can add visualizations such as Pie Charts, Info Widgets, Horizontal Bar Charts, Vertical Bar Charts, Horizontal Stacked Bar Charts, Vertical Stacked Bar Charts, Line Charts, Bubble Charts, and Waterfall Charts. Once all the required components are added and the dashboard is saved, it will be displayed on the Dashboard List page.. &#x20;

***

### Procedure

{% tabs %}
{% tab title="Prerequisites" %}
Availability of **Logical Data Model** is the main prerequisite for creating a dashboard.
{% endtab %}

{% tab title="Add Logo" %}


1. On the **SCIKIQ left navigation bar**, click **Dashboard Designe**r under **SCIKIQ Consume**.

<img src="../../../.gitbook/assets/unknown (90).png" alt="Dashboard Designer Menu Item" height="232" width="464">

The Dashboard Designer page is displayed.

2. On the **Dashboard Designer** page, click the **Logo** button.

<img src="../../../.gitbook/assets/unknown (91).png" alt="Logo Button" height="235" width="488">

3. Browse to the location where the logo is available, and then click the **Open** button.

<img src="../../../.gitbook/assets/unknown (92).png" alt="Uploading Logo Selection" height="317" width="452">

The logo is added. See the example image below.

4.  If you want to remove or change the logo, click the **Remove**&#x20;

    button next to the logo.
{% endtab %}

{% tab title="Add Template" %}
**Overview**

The SCiKIQ Designer allows you to create a dashboard by choosing either a predefined template or a custom template, depending on your requirements. Predefined templates provide ready-made layouts and configurations for quick setup, while custom templates offer the flexibility to design components, layout, and data settings from scratch to meet specific business needs.

**Procedure**

* On the **Dashboard Designer** page, select either the **Custom Template** or a **Predefined Template**. For example, the Custom Template.

<figure><img src="../../../.gitbook/assets/image (1770).png" alt=""><figcaption><p>Dashboard Templates</p></figcaption></figure>

The Source Dataset drop-down box is activated on the left pane.
{% endtab %}

{% tab title="Define Page Styling" %}
**Overview**

Page Styling in a dashboard refers to the visual customization of the entire dashboard page, including settings like background color, fonts, spacing, themes, and overall layout to ensure a consistent and visually appealing design.&#x20;

**Procedure**

The step-by-step instructions describe how to define page styling:

1. On the **left pane**, in the **Page Styling** section, select the **Page Layout** choosing from either **Page Fit Layout** or **Box Layout**.

> <mark style="color:red;">**Note:**</mark> Here is the description for Page Fit Layout and Box Layout.
>
> * **Page Fit Layout:** A layout where the entire dashboard page and its components automatically adjust to fit the available screen space, ensuring optimal use of the display without empty areas.
> * **Box Layout:** A layout that arranges dashboard components in a structured row or column (horizontal or vertical), allowing better control over alignment, spacing, and organization of multiple elements.
>
>

2. Select the **Height, Width, Side Margin**, and **BG Color**.
3. Select the required **dashboard theme**.

<img src="../../../.gitbook/assets/unknown (95).png" alt="Page Styling" height="469" width="555">
{% endtab %}

{% tab title="Select Dataset" %}
**Overview**

As part of data selection, you can choose either **Dataset** or **Direct Table**. A Dataset is a predefined and structured set of data with applied calculations or filters, making it ideal for consistent and easy widget creation, whereas a Direct Table provides raw data directly from the database, allowing flexibility for real-time data usage and custom filtering or calculations.

**Procedure**

The step-by-step instructions describe how to select a dataset:

1. On the Dashboard Designer page, from the Source Dataset drop-down box, select either Dataset or Direct Table. For example, Dataset.
2. From the Dataset drop-down box, select the dataset.

<figure><img src="../../../.gitbook/assets/image (1771).png" alt=""><figcaption><p>Source Data</p></figcaption></figure>

The Styling section is activated.
{% endtab %}

{% tab title="Add Visualization Charts" %}
Refer to [Adding Visualization Charts](adding-visualization-charts.md)
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Dashboard Designer**](./)
