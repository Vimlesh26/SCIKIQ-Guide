---
icon: laptop-binary
---

# Adding Visualization Charts

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The SCiKIQ Designer module enables you to build interactive dashboards by adding various components such as Info Widget, Pie Chart, Bar Chart, Stacked Chart, Line Chart, Dot Plot Chart, Bubble Chart, Waterfall Chart, Radial Visualization Charts, Map Charts, and Tables, etc.  These components help visualize data in different formats, allowing you to analyze trends, compare values, and present key insights effectively based on your requirements. &#x20;

***

### Choosing a Right Chart

The table below explains which chart can be used for different requirements.

<table><thead><tr><th width="372">If you want to ...</th><th>Then use...</th></tr></thead><tbody><tr><td>Show proportions</td><td>Pie chart</td></tr><tr><td>Compare categories</td><td>Bar chart</td></tr><tr><td>Show trends</td><td>Line chart</td></tr><tr><td>Compare sub-groups</td><td>Stacked bar</td></tr></tbody></table>

***

### **Visualization Chart Types**

{% tabs %}
{% tab title="Info Widget" %}
**Overview**

An **Info Widget** is a dashboard component used to display important summary information in a simple and easy-to-read format. It is generally used to highlight key values, metrics, or status information at a glance.

***

**Procedure**

The process of creating an **Info Widget** involves several steps, including **Placing Info Widget on the Right Pane, Adding the required** **Metric** and **Configuring** **Styling properties,** and **Filters**. These configurations help customize the widget’s appearance, enable interactive data exploration, and refine the displayed information based on specific requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Info Widget on the Right Pane</strong> </summary>

1. From the **Styling** section, drag the I**nfo Widget** onto the **Right Pane**.

<figure><img src="../../../.gitbook/assets/image (1777).png" alt=""><figcaption><p>Info Widget</p></figcaption></figure>

</details>

<details>

<summary><strong>Add Metrics</strong></summary>

1. From the expanded dataset, drag a field to the **Metric** under the **Styling Chart**.

The field is added to the metric.

> <mark style="color:red;">**Note:**</mark> After adding a field as a metric, you can perform the following actions on it, as required:
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

2. Next, click on the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1773).png" alt=""><figcaption><p>Add Metric</p></figcaption></figure>

The Info Widget displayed the data. See the image below.

<figure><img src="../../../.gitbook/assets/image (1778).png" alt=""><figcaption><p>Info Widget</p></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1819).png" alt="" width="539"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. REfer to </td></tr><tr><td><a href="common-configuration-features/styling.md#subtitle">Sub Title</a></td><td>Provides additional information or context related to the chart title.</td></tr><tr><td><a href="common-configuration-features/styling.md#value">Value</a></td><td>Displays the key metric or data value represented within the chart or widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#icon">Show Icon</a></td><td>Adds a visual symbol to enhance the appearance and improve the understanding of the chart or widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#conditional-formatting">Conditional Formatting</a></td><td>Applies predefined formatting rules to dynamically change the appearance of data based on specified conditions.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-indicator-property">Card Indicator</a></td><td>Displays visual indicators such as arrows, symbols, or status markers to represent trends or data conditions.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>
{% endtab %}

{% tab title="Pie Chart" %}
**Overview**

A **Pie Chart** is a circular chart that represents data as proportional slices, with each slice showing a category’s share of the whole, making it ideal for visualizing percentage-based data.

**When to use**

A Pie Chart is best used when you want to show how different parts make up a whole, especially when there are only a few categories.

**Example**

An example for this is - if a company’s total sales come from North (40%), South (30%), East (20%), and West (10%), a pie chart clearly shows each region’s contribution at a glance.

***

**Creation Procedure**

The process of creating a **Pie Chart** involves several steps, including **Placing Pie Chart on the Right Pane, Adding the required Dimension** and **Metric** and **Configuring** **Styling properties, Drilldown, and Filters**. These configurations help customize the widget’s appearance, enable interactive data exploration, and refine the displayed information based on specific requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Pie Chart on the Right Pane</strong> </summary>

* From the **Styling** section, drag the **Pie Chart**  on to the **Right Pane**.

![](<../../../.gitbook/assets/unknown (229).png>)

</details>

<details>

<summary><strong>Add Legend and Metric</strong></summary>

1. **Add Legend**

* From the expanded dataset, drag a field to the **Legend** under the **Styling Chart**. For example, Company Code.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag a field to the **Metric** under the **Styling** Chart.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on metric:
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* If required, sort fields by clicking the **Edit** icon on the field in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The pie chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1810).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1820).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and interpreted.</td></tr><tr><td><a href="common-configuration-features/styling.md#chart-formatting-pie-chart">Chart Formatting</a></td><td>As part of chart formatting, you can increase or decrease the pie chart hole size and explosion. </td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr><tr><td><a href="common-configuration-features/styling.md#label-length">Label Length</a></td><td>The purpose of specifying <strong>Label Length</strong> in a Pie Chart is to limit the number of characters displayed for labels, helping prevent clutter and improve chart readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Vertical Bar Chart" %}
**Overview**

A **Vertical Bar Chart** is a chart used to compare values across different categories using vertical bars. In this chart, the bars grow upward from the horizontal axis. The height of each bar represents the value of a category. Higher bars indicate larger values.

**When to use**

A Vertical Bar Chart is commonly used when:

* Comparing values across categories
* Showing sales, counts, or performance data
* Displaying trends for a small number of categories

***

**Creation Procedure**

The process of creating a **Vertical Bar Chart** involves multiple steps, including placing the **Vertical Bar Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Vertical Bar on the Right Pane</strong> </summary>

* From the **Styling** section, drag the **Vertical Bar Chart** on to the **Right Pane**.

<figure><img src="../../../.gitbook/assets/image (1794).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension and Legend**

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric and ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.** For example, Company Key and Company Name.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* In the **Sort** section, click the **Edit** icon on the left side of the required field.&#x20;

The Sort menu is displayed.

* From the Sort menu, select either **ASC** or **Desc**.

4. Next, click the **Fetch Data** button.

The Vertical Bar Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1811).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1821).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#subtitle">Sub Title</a></td><td>Provides additional information or context related to the chart title.</td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-type">Series Type</a></td><td>Defines the visual representation style used for the data series in the chart. It controls how the series appears and is displayed in the visualization.<br><em>Example:</em> Bar, Line, Area, or other supported series styles.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>



</details>

<details>

<summary><strong>Drill Down</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Vertical Stack Bar Chart" %}
**Overview**

A **Vertical Stacked Bar Chart** displays multiple data series stacked within each vertical bar, allowing you to compare total values across categories while also showing the contribution of each sub-category.

**When to use**

You can use a Vertical Stacked Bar Chart when you want to compare total values across categories and also see how each part contributes to the total.

**Example**

An example for this is - showing total sales for each region while breaking it down into product categories like electronics, clothing, and furniture within the same bar.

***

**Creation Procedure**

The process of creating a **Vertical Stack Bar Chart** involves multiple steps, including placing the **Vertical Bar Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Vertical Stack Bar on the Right Pane</strong> </summary>

* From the **Styling** section, drag the **Vertical Stack Bar Chart** on to the **Right Pane**.

![](<../../../.gitbook/assets/unknown (231).png>)

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension and Legend**

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric and ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.** For example, Company Key and Company Name.

> <mark style="color:red;">**Note:**</mark> When **multiple** metrics are added, the chart is displayed as a **Stacked Bar Chart**. However, when only a **single** metric is added, the chart is displayed as a normal **Bar Chart**.
>
> Refer to the images below for an example.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* In the **Sort** section, click the **Edit** icon on the left side of the required field.&#x20;

The Sort menu is displayed.

* From the Sort menu, select either **ASC** or **Desc**.

4. Next, click the **Fetch Data** button.

The Vertical Bar Chart is displayed as per the configuration. See the below images.



&#x20;                   **Vertical Stack Bar Chart with Multiple Metrics**

<figure><img src="../../../.gitbook/assets/image (1941).png" alt="" width="503"><figcaption></figcaption></figure>

&#x20;                   **Vertical Stack Bar Chart with Single Metric**

<figure><img src="../../../.gitbook/assets/image (1942).png" alt="" width="500"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1818).png" alt="" width="543"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#subtitle">Sub Title</a></td><td>Provides additional information or context related to the chart title.</td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-type">Series Type</a></td><td>Defines the visual representation style used for the data series in the chart. It controls how the series appears and is displayed in the visualization.<br><em>Example:</em> Bar, Line, Area, or other supported series styles.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>



</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Horizontal Bar Chart" %}
**Overview**

A **Horizontal Bar Chart** uses horizontal bars, with categories on the vertical (Y) axis and values on the horizontal (X) axis, making it especially useful when category names are long or when you want clearer readability.

**When to use**

You can use a Horizontal Bar Chart when you want to compare values across different categories, especially if the category names are long or easier to read horizontally.

**Example**

An example for this is - comparing sales across regions like North America, Asia Pacific, and the Middle East is clearer in a horizontal layout.

***

**Creation Procedure**

The process of creating a **Horizontal Bar Chart** involves multiple steps, including placing the **Horizontal Bar Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Horizontal Bar on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Horizontal Bar** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (226).png" alt="" height="292" width="624">

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric** and **ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.** For example, Company Key and Company Name.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* If required, sort fields by clicking the **Edit** icon in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The Horizontal Bar Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1812).png" alt="" width="500"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1822).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-type">Series Type</a></td><td>Defines the visual representation style used for the data series in the chart. It controls how the series appears and is displayed in the visualization.<br><em>Example:</em> Bar, Line, Area, or other supported series styles.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down  Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Horizontal Stack Bar Chart" %}
**Overview**

A **Horizontal Stacked Bar Chart** shows multiple data series stacked within horizontal bars, helping visualize part-to-whole relationships while making long category names easier to read.

**When to use**

You can use Use a Horizontal Stacked Bar Chart when you want to compare totals across categories and also see how each part contributes—especially when category names are long.

**Example**

An example for this is - showing total sales by region with each bar split into product categories like electronics, clothing, and furniture.

***

**Creation Procedure**&#x20;

The process of creating a **Horizontal Stack Bar Chart** involves multiple steps, including placing the **Horizontal Bar Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Horizontal Stack Bar on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Horizontal Stack Bar** on to the **Right Pane**.

![](<../../../.gitbook/assets/unknown (228).png>)

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric** and **ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.** For example, Company Key and Company Name.

> <mark style="color:red;">**Note:**</mark> When **multiple** metrics are added, the chart is displayed as a **Stacked Bar Chart**. However, when only a **single** metric is added, the chart is displayed as a normal **Bar Chart**.
>
> Refer to the images below for an example.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* If required, sort fields by clicking the **Edit** icon in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The Horizontal Bar Chart is displayed as per the configuration. See the below images.

**Horizontal Stack Bar Chart with Multiple Metrics**

<figure><img src="../../../.gitbook/assets/image (1947).png" alt=""><figcaption></figcaption></figure>

**Horizontal Stack Bar Chart with Multiple Metrics**

<figure><img src="../../../.gitbook/assets/image (1948).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1823).png" alt="" width="544"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Line Chart" %}
**Overview**

A **Line Chart** displays data points connected by lines to show how one or more values change over time or across a continuous range, making it ideal for identifying trends and patterns.

In a Line Chart:

* Data points are plotted on the chart.
* A line connects the points to show the trend.
* The horizontal axis (X-axis) usually represents time or categories.
* The vertical axis (Y-axis) represents numerical values

**When to use**

Use a Line Chart when you want to show how a value changes over time or across a continuous range.

**Example**

An example for this is - tracking monthly sales throughout the year to see whether they are increasing or decreasing.

***

**Creation Procedure**

The process of creating a **Line Chart** involves multiple steps, including placing the **Line Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Line Chart on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Line Chart** on to the **Right Pane**.

<figure><img src="../../../.gitbook/assets/image (1824).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric** and **ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.**

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

* If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The Line Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1949).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1827).png" alt="" width="512"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#graph-properties">Graph Properties</a></td><td>In a <strong>Line Chart</strong>, <strong>Graph Properties</strong> are configuration settings that control the appearance and display behavior of the graph, improving readability and data interpretation.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Dot Plot Chart" %}
**Overview**

A Dot Plot Chart is a visualization that represents data values as dots along a common axis, making it easy to compare multiple data points across categories in a simple and uncluttered manner.&#x20;

Key Features of a Dot Plot Chart:

* Represents data using dots
* Easy to compare values across categories
* Reduces visual clutter compared to bar charts
* Useful for displaying distributions and comparison

**When to use**

You can use a Dot Plot Chart when you want to compare many values across categories in a clean and uncluttered way, especially when labels are long or data points are numerous.

**Example**

An example for this is - comparing employee performance scores across multiple departments where each department has several individuals.

***

**Creation Procedure**

The process of creating a **Dot Plot** **Chart** involves multiple steps, including placing the **Dot Plot Chart** on the **Right Pane**, adding the required **Dimension, Legend, Metric,** and **Tooltip** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Dot Plot Chart on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Dot Plot** **Chart** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (232).png" alt="" height="299" width="579">

</details>

<details>

<summary><strong>Add Dimension, Legend, Metric, and ToolTip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric** and **ToolTip**

* From the expanded dataset, drag **two** more fields and place them under **Metric** and **ToolTip** under the **Styling** **Chart.** For example, Company Key and Company Name.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric and ToolTip.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1828).png" alt=""><figcaption></figcaption></figure>

The Dot Plot Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1829).png" alt="" width="524"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1830).png" alt="" width="458"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#subtitle">Sub Title</a></td><td>Provides additional information or context related to the chart title.</td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Bubble Chart" %}
**Overview**

A Bubble Chart is a visualization that displays data using bubbles plotted on the X-axis and Y-axis, where the size of each bubble represents an additional quantitative value, helping compare relationships and magnitude simultaneously.&#x20;

In a Bubble Chart:

* The position of the bubble represents two values (X and Y axes).
* The size of the bubble represents another value.
* Larger bubbles indicate higher values

**When to use**

You can use a Bubble Chart when you want to compare and analyze the relationship between **three variables** simultaneously. It is useful for identifying patterns, trends, clusters, or outliers in data.

**Example**

Suppose a company wants to analyze product performance:

* **X-Axis:** Product Price
* **Y-Axis:** Sales Revenue
* **Bubble Size:** Number of Units Sold

In this case:

* Products with higher prices and higher revenue appear toward the upper-right area of the chart.
* Larger bubbles indicate products with more units sold.
* Smaller bubbles indicate products with lower sales volume

***

**Creation Procedure**&#x20;

The process of creating a **Bubble** **Chart** involves multiple steps, including placing the **Bubble Chart** on the **Right Pane**, adding the required **Category, Legend, Metric X, Metric Y** and **Bubble Size** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Bubble Chart on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Bubble** **Chart** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (233).png" alt="" height="284" width="568">

</details>

<details>

<summary><strong>Add Category, Legend, Metric X, Metric Y, and Bubble Size</strong></summary>

1. **Add Category** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Category** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Category and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metrics** and **Bubble Size**

* From the expanded dataset, drag **two** more fields and place them under **Metric X** and **Metric Y.**
* Drag **one** more field and place it under **Bubble Size.** &#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metrics and Bubble Size.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1831).png" alt="" width="486"><figcaption></figcaption></figure>

The Bubble Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1832).png" alt="" width="560"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1833).png" alt="" width="500"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#bubble-size">Bubble Size</a></td><td>Represents the relationship between three different variables, where the <strong>X-axis</strong> represents one variable, the <strong>Y-axis</strong> represents another variable, and the <strong>bubble size</strong> represents the third variable, enabling users to analyze patterns, trends, and comparisons in the data.</td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#series-color">Series Color</a></td><td>Configuring <strong>Series Color</strong> is to assign or customize colors for individual slices so that different categories can be easily distinguished and in</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Waterfall Chart" %}
**Overview**

A Waterfall Chart is a visualization that shows how an initial value increases or decreases through a series of positive and negative changes, helping illustrate the cumulative effect of sequential data changes.

In this chart:

* Each bar represents an increase or decrease in value.
* Positive values usually extend upward.
* Negative values usually extend downward.
* The final bar shows the ending total.

**When to use**

You can use a **Waterfall Chart** when you want to visualize how an initial value changes through a series of positive and negative contributions, eventually arriving at a final value. It helps users understand the cumulative effect of sequential increases and decreases in data.

***

**Creation Procedure**&#x20;

The process of creating a **Waterfall** **Chart** involves multiple steps, including placing the **Waterfall Chart** on the **Right Pane**, adding the required **Dimension** and **Metric** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Waterfall Chart on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Waterfall** **Chart** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (234).png" alt="" height="281" width="583">

</details>

<details>

<summary><strong>Add Dimension and Metric</strong> </summary>

1. **Add Dimension**

* On the left pane, from the expanded dataset, drag a field and place it under **Dimension** in the **Fields** section. For example, Company Code.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Dimension:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag **one** more field and place it under **Metric.**

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1834).png" alt="" width="497"><figcaption></figcaption></figure>

The Waterfall Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1835).png" alt="" width="542"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1836).png" alt="" width="466"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#subtitle">Sub Title</a></td><td>Provides additional information or context related to the chart title.</td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#waterfall-setting">Waterfall Setting</a></td><td>Represents configuration options that control how the chart displays and interprets cumulative increases and decreases in data values. These settings help define the appearance and behavior of the chart to improve clarity and data representation.</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Heat Map" %}
**Overview**

A Heatmap is added to a dashboard to visually represent data values using colors. It helps users quickly identify patterns, trends, high values, low values, and problem areas within large datasets.

In a Heatmap:

* Different colors represent different value ranges.
* Higher values may appear in darker or stronger colors.
* Lower values may appear in lighter colors.
* The color intensity helps users analyze data quickly&#x20;

Real-Time Use Cases

* Sales performance analysis
* Website traffic analysis
* Employee attendance tracking
* SLA monitoring

***

**Creation Procedure**&#x20;

The process of creating a **Heat Map** involves multiple steps, including placing the **Heat Map Widget** on the **Right Pane**, adding the required **X Category, Y Category** and **Metric** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Heat Map on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag **Heat Map** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (278).png" alt="" height="303" width="624">

</details>

<details>

<summary><strong>Add X Category, Y Category</strong> and <strong>Metric</strong> </summary>

1. **Add X Category and Y Category**

* On the left pane, from the expanded dataset, drag **two** fields and place them under **X Category** and **Y Category** in the **Fields** section. &#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the X Category and Y Category:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag **one** more field and place it under **Metric.**

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1881).png" alt=""><figcaption></figcaption></figure>

The Heat Map is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1882).png" alt="" width="545"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1883).png" alt="" width="442"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#x-axis">X Axis</a></td><td>Represents the categories or dimensions displayed along the horizontal axis of the chart.<br><em>Example:</em> Months (January, February, March) or Product Categories</td></tr><tr><td><a href="common-configuration-features/styling.md#y-axis">Y Axis</a></td><td>Represents the numerical values or metrics displayed along the vertical axis of the chart.<br><em>Example:</em> Sales Amount, Revenue, Quantity, or Profit.</td></tr><tr><td><a href="common-configuration-features/styling.md#graph-color">Graph Color</a></td><td>Represents the color category used to indicate the Heat Map graph color.</td></tr><tr><td><a href="common-configuration-features/styling.md#data-labels">Data Labels</a></td><td>Displays the actual values or information directly on the bars in the chart, allowing users to view exact data values without referring to the axis scale.<br><em>Example:</em> Displaying <strong>5000</strong> above a bar representing sales.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>The purpose of configuring a <strong>Legend</strong> in a chart is to help users identify and interpret the different data series, categories, or colors represented in the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Tree Map" %}
**Overview**

A Treemap is used in a dashboard to visually represent hierarchical or category-based data using rectangles, helping users quickly compare values and understand how different categories contribute to the total. &#x20;

Real-Time Use Cases

* Sales analysis by category
* Budget allocation analysis
* File storage usage
* Market share analysis
* Resource utilization analysis

***

**Creation Procedure**&#x20;

The process of creating a **Tree Map** involves multiple steps, including placing the **Tree Map Widget** on the **Right Pane**, adding the required **Dimension** and **Metric** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the chart’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Tree Map on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag **Tree Map** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (236).png" alt="" height="282" width="550">

</details>

<details>

<summary><strong>Add Dimension</strong> and <strong>Metric</strong> </summary>

1. **Add Dimension**

* On the left pane, from the expanded dataset, drag the required field and place it under **Dimension** in the **Fields** section. &#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Dimension:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag **one** more field and place it under **Metric.**

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

Once done, the Tree Map is displayed as shown in the example image below.

<img src="../../../.gitbook/assets/unknown (237).png" alt="" height="381" width="624">

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a chart is to customize the appearance and presentation of the chart so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options listed in the below table:

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#graph-header">Graph Header</a></td><td>Represents the title or heading displayed for the visualization. It provides a descriptive label that helps users understand what the Tree Map represents and gives context to the displayed data.</td></tr><tr><td><a href="common-configuration-features/styling.md#graph-color">Graph Color</a></td><td>Represents the color category used to indicate the Tree Map graph color.</td></tr><tr><td><a href="common-configuration-features/styling.md#graph-text">Graph Text</a></td><td>Represents the text labels displayed within the individual sections or blocks of the Tree Map.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Specifies the background color of the chart or widget to improve visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Table" %}
**Overview**

The purpose of adding a Table in a dashboard is to display detailed and structured data in rows and columns. Tables help users view exact values, compare records, and analyze information in a clear and organized manner. Unlike charts, which provide visual summaries and trends, tables display precise data details.

***

**Creation Procedure**

The process of creating a **Table** involves multiple steps, including placing the **Table** on the **Right Pane**, adding the required **Dimension** and **Metric** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the table’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Table on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Table** on to the **Right Pane**.

<figure><img src="../../../.gitbook/assets/image (1837).png" alt="" width="538"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Dimension and Metric</strong> </summary>

1. **Add Dimension**

* On the left pane, from the expanded dataset, drag a field and place it under **Dimension** in the **Fields** section. For example, Company Code.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Dimension:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag **one** more field and place it under **Metric.**

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the fields, hover the cursor on the left side of a field in the **Sort** section.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1838).png" alt="" width="478"><figcaption></figcaption></figure>

The Table Chart is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1839).png" alt="" width="536"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a table is to customize the appearance and presentation of the table so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1876).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#header">Header</a></td><td>Represents the top section of a table that displays the names or labels of columns.</td></tr><tr><td><a href="common-configuration-features/styling.md#body">Body</a></td><td>Represents the main section of a table that contains the actual data records.</td></tr><tr><td><a href="common-configuration-features/styling.md#row">Row</a></td><td>Represents a horizontal arrangement of related data values within a table.</td></tr><tr><td><a href="common-configuration-features/styling.md#column">Column</a></td><td>Represents a vertical arrangement of data values belonging to a specific field or category.</td></tr><tr><td><a href="common-configuration-features/styling.md#table-property">Table Property</a></td><td>Represents configuration settings used to customize the appearance and behavior of the table.</td></tr><tr><td><a href="common-configuration-features/styling.md#conditional-formatting">Conditional Formatting</a></td><td>Represents a feature that automatically applies predefined formatting such as colors, icons, or styles to table data based on specified conditions or rules, helping highlight important information and improve data analysis.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#download">Download</a></td><td>Enables configuring downloading the table in PDF, XLS, and CSV.</td></tr><tr><td><a href="common-configuration-features/styling.md#table-settings">Table Settings</a></td><td>Enables configuring Search and Pagination in the table.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Pivot Table" %}
**Overview**

The purpose of creating a **Pivot Table** in a dashboard is to summarize, organize, and analyze large amounts of data in a flexible and interactive manner. It helps users quickly view data from different perspectives without modifying the original dataset.&#x20;

In simple terms, a Pivot Table should be used in a dashboard whenever there is a need to summarize, group, compare, filter, and analyze large amounts of data efficiently and interactively.

**Real-Time Use Cases**

* Sales performance analysis
* Financial reporting
* Employee performance tracking
* Inventory management
* Customer analysis
* Project status reporting

***

**Creation Procedure**

The process of creating a **Pivot** **Table** involves multiple steps, including placing the **Table** on the **Right Pane**, adding the required **Row Dimension and Column Dimension** and **Metric** fields, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the table’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Pivot Table on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Pivot** **Table** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (270).png" alt="" height="260" width="556">

</details>

<details>

<summary><strong>Add Dimension and Metric</strong> </summary>

1. **Add Row Dimension and Column Dimension**

* On the left pane, from the expanded dataset, drag **two** fields and place them under **Row Dimension** and **Column Dimension** in the **Fields** section. &#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the Row Dimension and Column Dimension:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)
> * [**Remove** ](common-configuration-features/fields.md#remove-field)

2. **Add Metric**

* From the expanded dataset, drag **one** more field and place it under **Metric.**
* Drag two more fields and place them under **Row Sort** and **Column Sort**.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric, Row Sort, and Column Sort.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. **Sort Fields**&#x20;

*   If you want to sort the **Rows** and **Columns**, hover the cursor on the left side of those fields.

    The Sort menu is displayed.
* From the **Sort** menu, select either **ASC** or **Desc.**

5. Next, click the **Fetch Data** button.

<figure><img src="../../../.gitbook/assets/image (1878).png" alt=""><figcaption></figcaption></figure>

The Pivot Table is displayed. See the image below.

<figure><img src="../../../.gitbook/assets/image (1879).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a table is to customize the appearance and presentation of the table so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1880).png" alt="" width="490"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#header">Header</a></td><td>Represents the top section of a table that displays the names or labels of columns.</td></tr><tr><td><a href="common-configuration-features/styling.md#body">Body</a></td><td>Represents the main section of a table that contains the actual data records.</td></tr><tr><td><a href="common-configuration-features/styling.md#row">Row</a></td><td>Represents a horizontal arrangement of related data values within a table.</td></tr><tr><td><a href="common-configuration-features/styling.md#column">Column</a></td><td>Represents a vertical arrangement of data values belonging to a specific field or category.</td></tr><tr><td><a href="common-configuration-features/styling.md#table-property">Table Property</a></td><td>Represents configuration settings used to customize the appearance and behavior of the table.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#download">Download</a></td><td>Enables configuring downloading the table in PDF, XLS, and CSV.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Custom Table" %}
**Overview**

The purpose of creating a Custom Table in a dashboard is to display data in a user-defined format based on specific business or reporting requirements. It provides greater flexibility compared to a standard table by allowing to customize the structure, layout, calculations, formatting, and displayed data.

A Custom Table helps present information exactly in the way users want to view and analyze it.

**Real-Time Use Cases**

* Financial dashboards
* SLA monitoring reports
* Sales performance reports
* Employee evaluation reports
* Audit and compliance reports

***

**Creation Procedure**

The process of creating a **Custom** **Table** involves multiple steps, including placing the **Custom Table Widget** on the **Right Pane**, specifying the required **Number of Rows** and **Columns**, and configuring additional options such as **Styling properties**, **Drilldown**, and **Filters**. These configurations help customize the table’s appearance, support interactive data analysis, and refine the displayed information according to specific business requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Custom Table on the Right Pane</strong> </summary>

* From the **Styling** **Chart**, drag the **Custom** **Table** on to the **Right Pane**.

<figure><img src="../../../.gitbook/assets/image (1840).png" alt="" width="522"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Specify Number of Rows and Columns</strong></summary>

1. Under the **Fields** section, in the **Records** field, specify the **number of records**.
2. Specify the **number of** **Rows** and **Columns**.
3. Click the **Fetch Data** button.

The custom table is created. See the below image.

<img src="../../../.gitbook/assets/unknown (235).png" alt="" height="389" width="532">

</details>

<details>

<summary><strong>Add Fields</strong></summary>

1. **Name the Column Header**

* On the **Custom Table**, click on the **Table Headers**, and enter relevant names. For example, Company Name, Budget Amount . and Actual Amount. See the below image.

<figure><img src="../../../.gitbook/assets/image (1950).png" alt=""><figcaption></figcaption></figure>

2. **Add Fields**

* From the expanded dataset on the left pane, drag the appropriate fields, and place them in the cells under column headers.&#x20;

<figure><img src="../../../.gitbook/assets/image (1953).png" alt=""><figcaption></figcaption></figure>

3. **If you want to replicate a field**

* Select the **Apply to all columns** checkbox next the required field.

The same field is replicated in the other cells of that row. See the below image.

<figure><img src="../../../.gitbook/assets/image (1954).png" alt=""><figcaption></figcaption></figure>

4. **If you want to add column level filters**

* On the **Column Header**, click the **Filter** icon.

The Filter pop up is displayed.

* From the expanded dataset on the left menu or from the Filters section, drag the required field and place them on the pop up.&#x20;
* Next, click the **Edit** icon next the field.

<figure><img src="../../../.gitbook/assets/image (1955).png" alt=""><figcaption></figcaption></figure>

The Filter Config Setting screen is displayed.

* On the **Filter Config Setting** screen, from the **Filter Type** drop-down box, select **Basic Filter** or **Advanced Filter**.
* From the **Selection Type** area, select **Single** or **Multiple**.
* Select the required fields, and then clik the **Apply Filter** button.

<figure><img src="../../../.gitbook/assets/image (1956).png" alt=""><figcaption></figcaption></figure>

The filter is applied.

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while creating a table is to customize the appearance and presentation of the table so that the data is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1841).png" alt="" width="512"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Specifies the main heading of the chart to indicate the purpose or content of the visualization. </td></tr><tr><td><a href="common-configuration-features/styling.md#header">Header</a></td><td>Represents the top section of a table that displays the names or labels of columns.</td></tr><tr><td><a href="common-configuration-features/styling.md#body">Body</a></td><td>Represents the main section of a table that contains the actual data records.</td></tr><tr><td><a href="common-configuration-features/styling.md#row">Row</a></td><td>Represents a horizontal arrangement of related data values within a table.</td></tr><tr><td><a href="common-configuration-features/styling.md#table-property">Table Property</a></td><td>Represents configuration settings used to customize the appearance and behavior of the table.</td></tr><tr><td><a href="common-configuration-features/styling.md#conditional-formatting">Conditional Formatting</a></td><td>Represents a feature that automatically applies predefined formatting such as colors, icons, or styles to table data based on specified conditions or rules, helping highlight important information and improve data analysis.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#download">Download</a></td><td>Enables configuring downloading the table in PDF, XLS, and CSV.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Local Image" %}
**Overview**

The purpose of configuring a Local Image Widget in a dashboard is to display images stored locally or uploaded within the application to enhance the dashboard’s visual appearance, usability, and information presentation.

**Real-Time Use Cases**

* Showing company logo, product images, and status icons, etc.

***

**Configuration Procedure**

The process of configuring the Local Image Widget involves multiple steps, including placing the **Local Image Widget** on the **Designer Right Pane**, **uploading image**, and configuring **Styling properties**. The Styling properties  configurations help customize the appearance of the image.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Local Image Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Local Image Widget** on to the **Right Pane**.

<img src="../../../.gitbook/assets/unknown (238).png" alt="" width="563">

The local image widget is placed on the right pane.

</details>

<details>

<summary><strong>Upload Image</strong>  </summary>

* On the **Local Image Widget** , click the **Browse** button, and then upload the required image .

The image is uploaded. See the below example image.

<img src="../../../.gitbook/assets/unknown (239).png" alt="" height="350" width="594">

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while adding an image is to customize the appearance so it is displayed in a clear, meaningful, and visually appealing manner. In simple terms, styling properties help transform a basic chart into a more informative, attractive, and user-friendly visualization.

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options shown in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1842).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Provides a descriptive heading for the image and help users understand its context or purpose within the dashboard</td></tr><tr><td><a href="common-configuration-features/styling.md#image-property">Image Property</a></td><td>Used to automatically resize and adjust the image so that it fits within the boundaries of the widget card or container.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#download">Download</a></td><td>Enables configuring downloading the table in PDF, XLS, and CSV.</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Web Image" %}
**Overview**

The purpose of adding a **Web Image** in a dashboard is to display images dynamically using an image link (URL) from an external web source instead of uploading the image directly into the application. In simple terms, the widget allows the dashboard to load and display images directly from the internet or a hosted server using a URL.

***

**Configuration Procedure**&#x20;

The process of configuring the Web Image Widget involves steps, including placing the **Web Image Widget** on the **Designer Right Pane**, entering **Image URL in the Widget** **URL Field**, and configuring  **Styling properties.** These configurations help customize the appearance of the image.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Web Image Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Web Image Widget** on to the **Right Pane**.

The web image widget is placed on the right pane.

![](<../../../.gitbook/assets/unknown (240).png>)

</details>

<details>

<summary><strong>Enter Image URL</strong> </summary>

* On the **Local Image Widget**, enter the **Image URL,** and then click the **Load** button.

<figure><img src="../../../.gitbook/assets/image (1843).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling Properties** while adding an image is to customize the appearance so it is displayed in a clear, meaningful, and visually appealing manner.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options listed in the below table:

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Provides a descriptive heading for the image and help users understand its context or purpose within the dashboard</td></tr><tr><td><a href="common-configuration-features/styling.md#image-property">Image Property</a></td><td>Used to automatically resize and adjust the image so that it fits within the boundaries of the widget card or container.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Defines the border style and appearance around the chart or widget card for better visual separation.</td></tr><tr><td><a href="common-configuration-features/styling.md#download">Download</a></td><td>Enables configuring downloading the table in PDF, XLS, and CSV.</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Link" %}
## Overview

The purpose of configuring a **Link** in a dashboard is to enable users to navigate to external websites, internal pages, reports, dashboards, or other resources directly from the dashboard. It helps improve accessibility and provides quick access to related information or actions without leaving the dashboard environment.

***

## **Configuration Procedure**&#x20;

The process of configuring the **Link** involves steps, including placing the **Link** component on the **Designer Right Pane** and configuring **Styling properties** including **Title** and **URL**.&#x20;

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Link Component on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Link** component on to the **Right Pane**.

The **Link** component is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1920).png" alt="" width="554"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong> </summary>

**Overview**

As part of configuring the styling properties, you will add a title, URL (either an external or internal), and specify card border.

**Procedure**

1. **Add a Title**

* Under the **Styling Chart**, enter a **title** for the link in the **Title** field.&#x20;
* Specify the **Font Family, Size**, and **Style.**

2. **Add a URL**

* In the **Hyperlink** field, enter either an **external** URL or **internal URL.** For example, External.

<figure><img src="../../../.gitbook/assets/image (1925).png" alt="" width="502"><figcaption></figcaption></figure>

3. **Specify Card Border**

* Under the **Styling Chart**, expand the **Card Border** panel.
* On the expanded panel, specify card border **Style, Size, Color, Card Shadow, Radius** and **Margins**.

</details>

<details>

<summary><strong>Preview Link</strong></summary>

1. Save the dashboard.
2. Next, click the **View** button on the **Top Menu** to preview.

The link is displayed as shown below.

<figure><img src="../../../.gitbook/assets/image (1926).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Group Button" %}
## Overview

The **Group Button** widget is used to organize and display multiple buttons within a single container, allowing users to perform actions or navigate efficiently within the dashboard. It helps improve usability by grouping related options together in a structured and easily accessible manner.

***

## **Configuration Procedure**

The process of configuring the **Group Button** involves steps, including placing the Group Button on the **Designer Right Pane**, and then configuring  **Styling properties**. These configurations help customize the appearance of the Group Button.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Group Button Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Group Button Widget** on to the **Right Pane**.

The Group Button Widget  is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1918).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Group Button Widget** is to customize its appearance and improve the overall visual presentation and usability of the dashboard. Styling options help make the Group Button more intuitive, visually consistent, and aligned with dashboard design requirements.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1919).png" alt="" width="497"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#collapsible">Collapsible</a></td><td>Configuring the <strong>Collapsible</strong> property displays a <strong>Toggle</strong> button on the <strong>Group Button Widget</strong>, allowing users to expand or collapse the widget content as required. This helps optimize dashboard space and improves the overall user experience.</td></tr><tr><td><a href="common-configuration-features/styling.md#button-config">Button Config</a></td><td>Configuring the <strong>Button Config</strong> property allows you to define the required number of rows and set the alignment of buttons within the <strong>Group Button Widget</strong>. These settings help organize the button layout, improve visual presentation, and ensure a better user experience.</td></tr><tr><td><a href="common-configuration-features/styling.md#group-spacing">Group Spacing</a></td><td>Configuring the <strong>Group Spacing</strong> property allows you to define <strong>Group Margin</strong> and <strong>Group Padding</strong> settings to control the spacing within and around the <strong>Group Button Widget</strong>. These settings help improve layout organization, maintain proper spacing between elements, and enhance the overall visual appearance of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Configuring the <strong>Background Color</strong> property allows you to define the background color of the <strong>Group Button Widget</strong>, helping improve its visual appearance and maintain consistency with the overall dashboard design.</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Group Widget" %}
**Overview**

The purpose of creating a **Group Widget** in a dashboard is to organize and combine multiple dashboard components into a single container for better structure and management. It helps users group related charts, widgets, images, buttons, or other elements together, making the dashboard more organized and easier to navigate.

The main purposes of a Group Widget are:

* To logically group related dashboard components.
* To improve dashboard organization and layout management.
* To reduce visual clutter and enhance readability.
* To enable collective management of grouped elements.
* To improve the overall user experience and dashboard presentation.

For example, a Group Widget can be used to place **sales charts, KPI widgets, and related filters** together within a single section of the dashboard.

***

**Configuration Procedure**

The process of configuring the **Group Widget** involves multiple steps, including placing the **Group Widget** on the **Designer Right Pane**, adding the required components within the group, and configuring **Styling properties.**&#x20;

These configurations help customize the appearance and behavior of the Group Widget, improve layout organization, and ensure consistency with the overall dashboard design.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Group Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Group Widget** on to the **Right Pane**.

The Group Widget  is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1910).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Components in the Group Widget</strong></summary>

1. In the **Group Widget**, add the required **components**, which you want to group. For example, Info Widgets or Textboxes, etc.

<figure><img src="../../../.gitbook/assets/image (1912).png" alt="" width="536"><figcaption></figcaption></figure>

2. Click the **View** button on the **Top Menu** to preview.

> <mark style="color:red;">**Note**</mark>: Make sure to save the dashboard before clicking the View button.

<figure><img src="../../../.gitbook/assets/image (1914).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Group Widget** is to customize its appearance and improve the overall visual presentation and usability of the dashboard. Styling options help make the Group Widget more intuitive, visually consistent, and aligned with dashboard design requirements.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1911).png" alt="" width="539"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="https://sites.gitbook.com/preview/site_FLgWP/~/revisions/LRzRub70MLbg7Fj00AsG/scikiq-modules/openapi/dashboard-designer/common-configuration-features/styling#title">Title</a></td><td>Specifies the main heading of the Group to indicate the purpose or content of the visualization.</td></tr><tr><td><a href="common-configuration-features/styling.md#icon">Icon</a></td><td>Turning the Icon gets displayeds  it on the group.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Configuring the <strong>Background Color</strong> property allows you to define the background color of the <strong>Group Button Widget</strong>, helping improve its visual appearance and maintain consistency with the overall dashboard design.</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Text Box" %}
**Overview**

The purpose of a **Text Box** in a dashboard is to display static text or descriptive information that provides additional context and guidance to users. It helps improve dashboard readability by presenting titles, instructions, notes, explanations, or important messages alongside visual components.

***

**Configuration Procedure**

The process of configuring the **Text Box** involves steps, including placing the **Text Box** component on the **Designer Right Pane** and configuring its **Styling properties**.&#x20;

The styling options allow you to customize the appearance of the text by defining settings such as **Font Family, Font Size, Font Color, Background Color, Alignment,** and other formatting properties.&#x20;

Proper configuration helps improve readability, enhance visual presentation, and ensure consistency with the overall dashboard design. The Text Box can also be used to display titles, instructions, descriptions, or other informational content within the dashboard.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Text Box on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Text Box** component on to the **Right Pane**.

The **Text Box** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1893).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

These styling options allow you to customize the appearance of the text by defining settings such as **Font Family, Font Size, Font Color, Background Color, Alignment,** and **card border**.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1894).png" alt="" width="514"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Active Text Box" %}
**Overview**

The purpose of adding an **Active Textbox** in a dashboard is to display dynamic and interactive text information that changes automatically based on user actions, filters, selections, or underlying data.

Unlike a normal textbox, which displays static text, an Active Textbox updates its content dynamically according to the dashboard context.

**Real-Time Use Cases**

* Display selected filter values
* Show dynamic sales totals
* Display current dashboard parameters
* Show live system status

***

**Configuration Procedure**

The process of configuring the **Active Text Box** involves steps, including placing the **Active Text Box** component on the **Designer Right Pane**, adding the required **Metrics**, and configuring **Styling properties** and **Filters**.&#x20;

The styling options allow you to customize the appearance of the displayed content by defining settings such as **Font Family, Font Size, Font Color, Background Color,** and **Alignment**.&#x20;

The Active Text Box dynamically displays data values, making it useful for presenting key information and metrics within the dashboard.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Active Text Box on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Active** **Text Box** component on to the **Right Pane**.

The **Active Text Box** is placed on the right pane.

![](<../../../.gitbook/assets/unknown (281).png>)

</details>

<details>

<summary><strong>Add Metrics</strong></summary>

**Overview**

The **Active Text Box** allows you to enter static text directly into the text box and also drag and drop a **KPI field (Aggregated Value)** into it. This value is resolved when the underlying data is fetched.

**Procedure**

1. In the **Active Text Box**, type the required text.
2. From the expanded dataset, drag the required field and place it under **Metric** under the **Styling** **Chart.**

The field is displayed in the Active Text box. See the image below.

<figure><img src="../../../.gitbook/assets/image (1957).png" alt="" width="492"><figcaption></figcaption></figure>

3. Now, click the **Fetch** button.

The underlying value is displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (1958).png" alt="" width="488"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Metric.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for an **Active Text Box** is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1892).png" alt="" width="497"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#value-tag">Value Tag</a></td><td>Configuring the <strong>Value Tag</strong> in an <strong>Active Text Box</strong> dynamically displays field values or metric data within the text content.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#conditional-formatting">Conditional Formatting</a></td><td>Configuring the <strong>Conditional Formatting</strong> automatically applies predefined formatting such as colors, icons, or styles to table data based on specified conditions or rules, helping highlight important information and improve data analysis.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-indicator">Card Indicator</a></td><td>Configuring the  <strong>Card Indicator</strong> property in an <strong>Active Text Box</strong> is used to display a visual indicator that highlights the status, trend, or significance of the displayed value or information. It helps users quickly identify changes or key insights through visual elements such as icons, colors, or indicators</td></tr></tbody></table>



</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>
{% endtab %}

{% tab title="Map Widget" %}
**Overview**

The purpose of configuring a **Map Widget** is to display and visualize data based on geographical locations, allowing users to analyze location-specific information in an interactive and visually meaningful manner. It helps represent data on maps using regions, coordinates, markers, or location-based metrics.

The main purposes of configuring a Map Widget are:

* To visualize data across geographical locations or regions.
* To identify location-based trends, patterns, and distributions.
* To improve data analysis through interactive map representations.
* To display region-specific metrics and insights.
* To enhance decision-making by providing geographical context to the data.

***

**Creation Procedure**&#x20;

The process of configuring the **Map Widget** involves multiple steps, including placing the **Map Widget** component on the **Designer Right Pane**, adding the required **Geo Dimension, Metric, Legend, Label,** and **Size**, and configuring its **Styling properties**. These styling options allow you to customize various elements such as **Title, Map Style, Map Control, Card Border, Data Labels,** and **Legend**.&#x20;

Proper configuration helps improve the visual representation of geographical data, enhances readability, and ensures consistency with the overall dashboard design and presentation requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Map Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Map Widget** component on to the **Right Pane**.

The **Map Widget** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1930).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Geo Dimension, Metric, Legend, Label,</strong> <strong>Size,</strong> and <strong>Tool Tip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Geo** **Dimension** and **Legend** under the **Styling Chart**. For example, Company Code and Company Name.&#x20;

> <mark style="color:red;">**Note:**</mark> Make sure to add the field under **Geo Dimension**. Otherwise, the map will not be displayed.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)

2. **Add Metric, Label, Size, and** **Tool Tip**

* From the expanded dataset, drag **four** more fields and place them under **Metric, Label, Size, and** **Tool Tip** under the **Styling** **Chart.**&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on **Metric , Label, Size, and** **Tool Tip**.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. From the **Geo Level** drop-down box, select the level choosing from **Country, State,** or **City.**

> <mark style="color:red;">**Note:**</mark> Make sure to select the **Geo Level**. Otherwise, the map will not be displayed.

4. **Sort Fields**&#x20;

* If required, sort fields by clicking the **Edit** icon in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The Map is displayed.

<figure><img src="../../../.gitbook/assets/image (1945).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Map Widget** is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1898).png" alt="" width="489"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#map-style">Map Style</a></td><td>Configuring the  <strong>Map Style</strong> property allows you to define the visual appearance of the map, such as the map theme, colors, and display format, to improve presentation and readability.</td></tr><tr><td><a href="common-configuration-features/styling.md#map-control">Map Control</a></td><td>Configuring the <strong>Map Control</strong> property allows you to configure interactive map features such as zoom, navigation, and map movement controls to enhance user interaction. </td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#bubble-size">Data Labels</a></td><td>Configuring the <strong>Data Labels</strong> property enables the display of values or text directly on map elements, helping users identify location-specific information more easily.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>Configuring the <strong>Legend</strong> property displays information that explains the meaning of colors, symbols, or categories used on the map, helping users interpret the displayed data accurately.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="World Map Widget" %}
**Overview**

The purpose of configuring a **World Map Widget** is to display and visualize data across geographical locations worldwide, allowing users to analyze location-specific information in an interactive and visually meaningful manner. It helps represent data using countries, regions, coordinates, markers, or location-based metrics to provide geographical insights.

The main purposes of configuring a **World Map Widget** are:

* To visualize data across different geographical locations and regions worldwide.
* To identify location-based trends, patterns, and distributions.
* To improve data analysis through interactive map visualizations.
* To display region-specific metrics and insights.
* To support better decision-making by providing.

***

**Configuration Procedure**

The process of configuring the **World Map Widget** involves multiple steps, including placing the **World Map Widget** component on the **Designer Right Pane**, adding the required **Geo Dimension, Metric, Legend, Label,** and **Size**, and configuring its **Styling properties**. These styling options allow you to customize various elements such as **Title, Map Style, Map Control, Card Border, Data Labels,** and **Legend**.&#x20;

Proper configuration helps improve the visual representation of geographical data, enhances readability, and ensures consistency with the overall dashboard design and presentation requirements.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place World Map Widget on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **World** **Map Widget** component on to the **Right Pane**.

The **World Map Widget** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1899).png" alt="" width="554"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Geo Dimension, Metric, Legend, Label,</strong> <strong>Size,</strong> and <strong>Tool Tip</strong></summary>

1. **Add Dimension** and **Legend**&#x20;

* From the expanded dataset, drag **two** fields and place them under **Geo** **Dimension** and **Legend** under the **Styling Chart**. &#x20;

> <mark style="color:red;">**Note:**</mark> Make sure to add the field under **Geo Dimension**. Otherwise, the map will not be displayed.

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on Dimension and Legend:
>
> * [**Rename**](common-configuration-features/fields.md#rename-a-field)
> * [**Update**](common-configuration-features/fields.md#update-a-field)
> * [**Convert**](common-configuration-features/fields.md#convert-a-field)
> * [**Change**](common-configuration-features/fields.md#change-field)

2. **Add Metric, Label, Size, and** **Tool Tip**

* From the expanded dataset, drag **four** more fields and place them under **Metric, Label, Size, and** **Tool Tip** under the **Styling** **Chart.**&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on **Metric , Label, Size, and** **Tool Tip**.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

3. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

4. From the **Geo Level** drop-down box, select the level choosing from **Country, State,** or **City.**

> <mark style="color:red;">**Note:**</mark> Make sure to select the **Geo Level**. Otherwise, the map will not be displayed.

4. **Sort Fields**&#x20;

* If required, sort fields by clicking the **Edit** icon in the **Sort** section.

The Sort menu is displayed.

* From the **Sort** menu, select either **ASC** or **Desc**.

5. Next, click the **Fetch Data** button.

The World Map is displayed.

<figure><img src="../../../.gitbook/assets/image (1961).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a World Map is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1901).png" alt="" width="503"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#map-style">Map Style</a></td><td>Configuring the  <strong>Map Style</strong> property allows you to define the visual appearance of the map, such as the map theme, colors, and display format, to improve presentation and readability.</td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#bubble-size">Data Labels</a></td><td>Configuring the <strong>Data Labels</strong> property enables the display of values or text directly on map elements, helping users identify location-specific information more easily.</td></tr><tr><td><a href="common-configuration-features/styling.md#legend">Legend</a></td><td>Configuring the <strong>Legend</strong> property displays information that explains the meaning of colors, symbols, or categories used on the map, helping users interpret the displayed data accurately.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>

<details>

<summary><strong>Drill Through Feature</strong></summary>

The **Drill Through** feature enables users to navigate between sheets while preserving the context of a selected data point. By right-clicking a component data point, users can select a target sheet, and the selected value is automatically applied as a filter on that sheet to display related data. For Drill Through to work, the corresponding field must be configured as a **Page Filter** on the target sheet.

For more information, refer to [**Drill Through**](common-configuration-features/drill-through.md) page.

</details>
{% endtab %}

{% tab title="Gauge Chart" %}
**Overview**

The purpose of creating a **Gauge Chart** in a dashboard is to visually represent the performance or progress of a metric against a predefined target or threshold. It provides a quick and intuitive way for users to understand whether a value is within the expected range, below target, or exceeding expectations.

The main purposes of a **Gauge Chart** are:

* To display the current status or performance of a metric.
* To compare actual values against target values.
* To highlight progress toward goals or KPIs.
* To provide quick visual insights using a meter-like representation.
* To support faster decision-making through easy-to-understand visual indicators.

For example, a Gauge Chart can be used to display **Sales Achievement**, **Revenue Progress**, **Customer Satisfaction Score**, or **Resource Utilization Percentage**.

***

**Creation Procedure**

The process of creating the **Gauge Chart** involves multiple steps, including placing the **Gauge Chart** component on the **Designer Right Pane**, adding the required **Metric Value**, **Metric Delta Value**, and **Metric Target Value**, and configuring its **Styling properties**. These styling options allow you to customize various elements such as **Title, Chart Formatting, Value, Card Border, Margin,** and **Background Color**.&#x20;

Proper configuration helps improve the visual presentation of the chart, enhance readability, and effectively highlight key metrics and performance indicators.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Gauge Chart on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Gauge Chart** component on to the **Right Pane**.

The **Gauge Chart** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1915).png" alt="" width="530"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Metric Value, Metric Delta Value, and Metric Target Value</strong></summary>

1. From the expanded dataset, drag **three** fields and place them under **Metric Value, Metric Delta Value, and Metric Target Value** under the **Styling Chart**.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on **Metric Value, Metric Delta Value, and Metric Target Value**.
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

2. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

3. Next, click the **Fetch Data** button.

The Gauge Chart is displayed.



</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Gauge Chart** is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1917).png" alt="" width="498"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#chart-formatting-gauze-chart">Chart Formatting</a></td><td>Configuring the Chart Formatting customizes the visual appearance and display behavior of the chart. It allows users to control how the gauge is presented so that important metrics can be displayed more clearly and effectively.</td></tr><tr><td><a href="common-configuration-features/styling.md#value">Value</a></td><td>Configuring the Value enables specify Prefix and Suffix.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Configuring  the background color of the chart improves visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down Feature</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>
{% endtab %}

{% tab title="Radial Chart" %}
**Overview**

The purpose of creating a **Radial Chart** in a dashboard is to visually represent the progress, percentage, or status of a metric using a circular format. It provides an intuitive way to display performance values and helps users quickly understand the current status of key metrics.

The main purposes of a Radial Chart are:

* To display the progress or completion percentage of a metric.
* To compare actual values against targets or predefined limits.
* To highlight key performance indicators (KPIs) in a visually appealing format.
* To provide quick and easy interpretation of data through circular visualization.
* To improve dashboard presentation and support faster decision-making.

For example, a Radial Chart can be used to display **Sales Achievement Percentage**, **Task Completion Rate**, **System Utilization**, or **Customer Satisfaction Score**.

***

**Creation Procedure**&#x20;

The process of configuring the **Radial Chart** involves multiple steps, including placing the **Radial Chart** component on the **Designer Right Pane**, adding the required **Metric Value**, and configuring its **Styling properties**. These styling options allow you to customize various elements such as **Title, Chart Formatting, Value, Card Border, Margin,** and **Background Color**.&#x20;

Proper configuration helps enhance the chart's visual presentation, improve readability, and effectively highlight key metrics and performance indicators for better analysis and decision-making.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Radial Chart on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Radial Chart** component on to the **Right Pane**.

The **Radial Chart** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1902).png" alt="" width="500"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Metric</strong></summary>

1. From the expanded dataset, drag a field and place it under **Metric**.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the **Metric.**
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

2. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

3. Next, click the **Fetch Data** button.

The Radial Chart is displayed.

<figure><img src="../../../.gitbook/assets/image (1905).png" alt="" width="521"><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Radial Chart** is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1906).png" alt="" width="489"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#chart-formatting-gauze-chart">Chart Formatting</a></td><td>The purpose of configuring <strong>Chart Formatting</strong> in a <strong>Radial Chart</strong> is to customize the visual appearance and display behavior of the chart to improve clarity and presentation. It allows users to control how the radial chart is displayed so that key metrics and progress indicators can be represented more effectively.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Configuring  the background color of the chart improves visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>
{% endtab %}

{% tab title="Multiple Radial Bar Chart" %}
**Overview**

The purpose of creating a **Multiple Radial Bar Chart** in a dashboard is to display and compare multiple metrics or progress indicators within a single circular visualization. It provides an effective way to represent the status, percentage, or performance of multiple data values simultaneously, making comparison easier and more intuitive.

The main purposes of a Multiple Radial Bar Chart are:

* To display multiple metrics within a single chart.
* To compare the performance or progress of different values simultaneously.
* To highlight key performance indicators (KPIs) in a visually appealing format.
* To improve data interpretation through a compact and interactive visualization.
* To support faster analysis and decision-making by presenting multiple insights in one view.

For example, a Multiple Radial Bar Chart can be used to display **Sales Achievement, Customer Satisfaction, Resource Utilization,** and **Task Completion Percentage** together in a single chart.

***

**Creation Procedure**&#x20;

The process of creating the **Multiple** **Radial  Bar Chart** involves multiple steps, including placing the **Multiple Radial Chart** component on the **Designer Right Pane**, adding the required **Metric Value**, and configuring its **Styling properties**. These styling options allow you to customize various elements such as **Title, Chart Formatting, Value, Card Border, Margin,** and **Background Color**.&#x20;

Proper configuration helps enhance the chart's visual presentation, improve readability, and effectively highlight key metrics and performance indicators for better analysis and decision-making.

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Place Radial Chart on the Right Pane</strong> </summary>

1. From the **Styling** **Chart**, drag the **Multiple Radial Bar Chart** component on to the **Right Pane**.

The **Multiple** **Radial Chart** is placed on the right pane.

<figure><img src="../../../.gitbook/assets/image (1907).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Add Metric</strong></summary>

1. From the expanded dataset, drag a field and place it under **Metric**.&#x20;

> <mark style="color:red;">**Note:**</mark> If required, you can perform the following actions on the **Metric.**
>
> * [**Update**](common-configuration-features/fields.md#update-a-metric)
> * [**Format**](common-configuration-features/fields.md#format-a-metric)
> * [**Change**](common-configuration-features/fields.md#change-a-metric)
> * [**Remove** ](common-configuration-features/fields.md#remove-a-metric)

2. **Specify Number of Records**

* In the **Records** field, enter the **number of records**, which you wish to view.

3. Next, click the **Fetch Data** button.

The Multiple Radial Bar Chart is displayed.

<figure><img src="../../../.gitbook/assets/image (1908).png" alt="" width="471"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Configure Styling Properties</strong></summary>

**Overview**

The purpose of configuring **Styling properties** for a **Radial Chart** is to customize the appearance and presentation of the displayed content. Styling options help improve readability, highlight important information, and ensure consistency with the overall dashboard design.&#x20;

**Procedure**

As part of configuring the **Styling Properties**, you need to configure the options highlighted  in the below image and listed in the below table:

<figure><img src="../../../.gitbook/assets/image (1909).png" alt="" width="475"><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> In the table below, click on a property to view detailed instructions for configuring it. For example, clicking **Title** displays the corresponding configuration details and instructions.

<table><thead><tr><th width="208.66668701171875">Property</th><th>Description</th></tr></thead><tbody><tr><td><a href="common-configuration-features/styling.md#title">Title</a></td><td>Configuring the <strong>Title</strong> allows you to specify a name or heading for the <strong>Text Box</strong>.</td></tr><tr><td><a href="common-configuration-features/styling.md#chart-formatting-gauze-chart">Chart Formatting</a></td><td>The purpose of configuring <strong>Chart Formatting</strong> in a <strong>Multiple Radial Bar Chart</strong> is to customize the visual appearance and display behavior of the chart to improve clarity and presentation. It allows users to control how the chart is displayed so that multiple metrics and progress indicators can be represented more effectively and interpreted easily.</td></tr><tr><td><a href="common-configuration-features/styling.md#margin">Margin</a></td><td>Refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability. </td></tr><tr><td><a href="common-configuration-features/styling.md#card-border">Card Border</a></td><td>Configuring the <strong>Card Border</strong> property allows you to define the border style and appearance of the <strong>Group Button</strong> card, helping improve visual separation and enhance the overall presentation of the widget.</td></tr><tr><td><a href="common-configuration-features/styling.md#background-color">Background Color</a></td><td>Configuring  the background color of the chart improves visual presentation and readability.</td></tr></tbody></table>

</details>

<details>

<summary><strong>Drill Down</strong></summary>

The **Drill Down** feature in dashboard charts enables users to explore data in greater detail by moving from a higher-level summary view to more granular information through chart interaction. It provides a hierarchical view of data, allowing users to analyze trends and gain deeper insights without switching to a different report or dashboard.

For more information, refer to [Drill Down ](common-configuration-features/drill-down.md)page.

</details>

<details>

<summary><strong>Configure Filters</strong></summary>

The purpose of configuring **Filters** while creating visualization charts in a dashboard is to control and refine the data displayed in the chart based on specific conditions or user requirements. Filters help focus only on relevant data, making analysis more meaningful and easier to interpret.

To know how to configure the filters, refer to [Filters](common-configuration-features/filters.md) page.

</details>
{% endtab %}
{% endtabs %}

***

### **Related Topics**

* [**Creating Dashboard**](creating-dashboard.md)
