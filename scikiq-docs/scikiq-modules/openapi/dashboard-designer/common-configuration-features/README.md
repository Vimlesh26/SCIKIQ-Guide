---
icon: laptop-binary
---

# Common Configuration Features

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **Dashboard Designer** provides several common features that help you build interactive and visually appealing dashboards. These include **Fields** for selecting and organizing data, **Styling** for customizing the appearance of dashboard components, **Filters** for displaying relevant data, **Drilldown** for exploring data at different levels of detail, **Drill Through** for navigating to detailed reports or related dashboards, and **Sheets** for organizing multiple dashboard views within a single dashboard.&#x20;

Together, these features enable you to create informative, interactive, and user-friendly dashboards.

***

### Common Configuration Features

{% tabs %}
{% tab title="Fields" %}
> <mark style="color:red;">**Note:**</mark> The procedure for adding fields is described on each individual visualization chart page. This section explains how to modify and sort fields and metrics.

**Modifying Fields**

The Fields feature allows you to add **Dimensions, Metrics, Legend, Category, Geo Dimension, X Category,** or **Y Category** based on the chart type.  Based on the requirement, fields can be renamed, updated, changed, and removed. When multiple fields are available, they can also be sorted accordingly.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The below mentioned field modification procedure is applicable to all the field types, including **Dimension, Legend, Category, Geo Dimension, X Category,** and **Y Category**.

<details>

<summary><strong>Rename a Field</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to rename a field. The same procedure can be followed to rename fields in any chart type.

**Overview**

The **Rename** Column feature in a pie chart allows you to modify the display name of a field without changing the underlying data. This helps present more meaningful and user-friendly labels for better clarity and understanding. It is especially useful for simplifying technical field names into business-friendly terms for end users.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to use the Rename feature:

1. Under the **Fields** section, hover the **cursor** on the left side of the required **field**.&#x20;

The Edit icon is displayed.

2. Click the **Edit icon**, and then from the drop-down menu, select **Rename**.

<img src="../../../../.gitbook/assets/unknown (212).png" alt="" height="309" width="542">

The Dimension dialogue box is displayed.

3. On the **Dimension** dialogue box, **rename** the field, and then click the **Update** button.

<img src="../../../../.gitbook/assets/unknown (213).png" alt="" height="315" width="513">

The field is renamed.

</details>

<details>

<summary><strong>Update a Field</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand update a field. The same procedure can be followed to update fields in any chart type.

**Overview**

The **Format** feature allows you to modify the display format of a field label without changing the underlying data. It typically provides options such as **uppercase, lowercase,** or **capitalization,** helping improve readability and maintain consistent formatting across the dashboard.

**Procedure**

The below step-by-step instructions help you understand how to use the Format feature:

1. Under the **Fields** section, hover the **cursor** on the left side of the required **field**.&#x20;

The Edit icon is displayed.

2. Click the **Edit icon**, and then from the drop-down menu, select **Format**.

<img src="../../../../.gitbook/assets/unknown (216).png" alt="" height="313" width="520">

The Text Transform dialog box is displayed.

2. On the **Text Transform** dialog box, select the required option, and then click the **Ok** button.

<img src="../../../../.gitbook/assets/unknown (217).png" alt="" height="289" width="569">

The field table is changed as per the change made.

</details>

<details>

<summary><strong>Convert a Field</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to use conversion feature. The same procedure can be followed in any chart type.

**Overview**

The Conversion feature allows you to define how a column’s data should be interpreted and structured before displaying it in the chart. It provides options like **Normal, Nested Key,** and **Nested Column** to handle simple or complex (nested) data formats, ensuring the data is correctly processed for accurate visualization. &#x20;

**Procedure**

The below step-by-step instructions help you understand how to use the Conversion feature:

1. Under the **Fields** section, hover the **cursor** on the left side of the required **field**.&#x20;

The Edit icon is displayed.

2. Click the **Edit icon**, and then from the drop-down menu, select **Conversion**.

<img src="../../../../.gitbook/assets/unknown (221).png" alt="" width="532">

The Conversion dialogue box is displayed.

2. On the **Conversion** dialogue box, from the **Select Conversion** drop-down box, select the required option choosing from **Normal, Nested Key,** and **Nested Column**.

> <mark style="color:red;">**Note:**</mark> Here is the description for conversion options:
>
> * **Normal:** Uses data as-is without any special structure
> * N**ested Key:** Extracts values from a nested data structure using a key
> * **Nested Column:** Handles data stored in nested or hierarchical columns

2. From the **Column Order** drop-down box, select the required option choosing from **ASC** and **DESC**.
3. Click the **Save** button.

<img src="../../../../.gitbook/assets/unknown (222).png" alt="" height="230" width="577">

</details>

<details>

<summary><strong>Change Field</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to change a field. The same procedure can be followed to change fields in any chart type.

1. Under the **Fields** section, hover the **cursor** on the right side of the required **field**.&#x20;

The Edit icon is displayed.

2. From the drop-down menu, click the **Edit** icon.&#x20;

<figure><img src="../../../../.gitbook/assets/image (1801).png" alt="" width="563"><figcaption></figcaption></figure>

The Select Field dialogue box is displayed.

3. From the **Select Field** dialogue box, select the required **field**, and then click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (1802).png" alt="" width="563"><figcaption></figcaption></figure>

The field is updated.

</details>

**Modifying Metrics**

After adding a metric, you can **update** and **format** it based on the requirement. You can also **change** a metric and **remove** it, if required.

Expand the panels below to understand how to configure these options.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The below mentioned metric field modification procedure is also applicable to **Tooltips**.

<details>

<summary><strong>Update a Metric</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to update a metric. The same procedure can be followed in any chart type.

**Overview**

The **Edit** feature allows you to update an existing metric by changing its aggregation type. For example, you can change **Sum** to **Count**, **Distinct Count**, **Average**, **Min**, **Max**, **First**, or **Last.**

**Procedure**

The below step-by-step instructions help you understand how to update a metric:

1. Under the **Metrics** section, hover the **cursor** on the left side of the required **metric**.&#x20;

The Edit icon is displayed.

2. Click the **Edit icon**, and then from the drop-down menu, select **Edit**.

<figure><img src="../../../../.gitbook/assets/image (1804).png" alt="" width="526"><figcaption></figcaption></figure>

The Metrics Edit dialogue box is displayed.

3. On the **Metrics Edit** dialogue box, select the required **metric**. For example, Count.

<figure><img src="../../../../.gitbook/assets/image (1791).png" alt="" width="500"><figcaption></figcaption></figure>

The metric is updated.

</details>

<details>

<summary><strong>Format a Metric</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to format a metric. The same procedure can be followed in any chart type.

**Overview**&#x20;

The **Format** feature allows you to configure column formatting options to control how data values are displayed in charts and dashboards. This includes settings such as **Decimal Places**, **Display Units**, **Prefix**, **Suffix**, **Negative Value Format**, and **Number Separators**. These options help improve data readability, presentation, and consistency by displaying values in a more meaningful and user-friendly format.

**Procedure**

The below step-by-step instructions help you understand how to update column formatting:

1. Under the **Metrics** section, hover the **cursor** on the left side of the required **metric**.&#x20;

The Edit icon is displayed.

2. Click the **Edit icon**, and then from the drop-down menu, select **Format**.

<figure><img src="../../../../.gitbook/assets/image (1792).png" alt="" width="515"><figcaption></figcaption></figure>

The Column Formatting dialogue box is displayed.

3. On the Column **Formatting** dialogue box, specify **Decimal Places**, **Display Units**, **Prefix**, **Suffix**, **Negative Value Format**, and **Number Separators,** and then click the **Save** button.

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of **Formatting** fields.

<figure><img src="../../../../.gitbook/assets/image (1793).png" alt="" width="543"><figcaption></figcaption></figure>

**Formatting Fields Description**

<table><thead><tr><th width="197">Field</th><th>Description</th></tr></thead><tbody><tr><td>Decimal Places</td><td>Specify the number of digits to display after the decimal point for numeric values.</td></tr><tr><td>Display Units</td><td>Define the unit in which values should be displayed, such as Auto, Thousands, Millions, or Billions.</td></tr><tr><td>Prefix</td><td>Add a custom text or symbol before the displayed value.</td></tr><tr><td>Suffix</td><td>Add a custom text or symbol after the displayed value.</td></tr><tr><td>Currency Symbol</td><td>Specify the currency symbol to be displayed with the value.</td></tr><tr><td>Show Negatives As</td><td>Define how negative values should be represented, such as using brackets or a negative sign.</td></tr><tr><td>Display Null As</td><td>Define the value or text to display when the actual data value is null or empty.</td></tr><tr><td>Include Thousands Separators</td><td>Selecting this options displays numbers using standard thousand separators for improved readability (for example, 1,000,000).</td></tr><tr><td>Include Indian Separators</td><td>Selecting this options displays numbers using the Indian numbering format (for example, 10,00,000).</td></tr><tr><td>No Separators</td><td>Selecting this options displays numbers without any separators.</td></tr></tbody></table>



</details>

<details>

<summary><strong>Change a Metric</strong></summary>

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to change a metric. The same procedure can be followed to change metrics in any chart type.

1. Under the **Fields** section, hover the **cursor** on the right side of the required **metric**, and then click the **Edit** icon.

<figure><img src="../../../../.gitbook/assets/image (1805).png" alt="" width="563"><figcaption></figcaption></figure>

The Select Field dialogue box is displayed.

3. From the **Select Field** dialogue box, select the required **metric**, and then click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (1802).png" alt="" width="563"><figcaption></figcaption></figure>

The metric is updated.

</details>

**Sorting Fields**

The Sorting feature allows you to arrange fields in a specific order using either Ascending (ASC) or Descending (DESC) options. Ascending order organizes fields from lowest to highest (e.g., A–Z or 1–100), while descending order arranges them from highest to lowest (e.g., Z–A or 100–1), making it easier to analyze and interpret the information.&#x20;

**Procedure**

> <mark style="color:red;">**Note:**</mark> The Pie Chart example below helps you understand how to sort fields. The same procedure can be followed to sort fields in any chart type.

The below step-by-step instructions help you understand how to use the Sort feature:

1. Under **Fields**, scroll down to **Sort**, and then click the **Edit** icon on the left side of the required field.

The Sort menu is displayed.

2. From the **Sort** menu, select either **ASC** or **Desc**.

<figure><img src="../../../../.gitbook/assets/image (2502).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Styling" %}
**Overview**

The **Styling** feature allows you to configure various visual properties such as Title, Subtitle, Series Color, Chart Formatting, Legend, Margin, Card Border, Background Color, Label Length, X-Axis, Y-Axis, Series Type, and Data Labels. However, all charts do not support the same styling options. The available styling configurations vary depending on the chart type. &#x20;

***

**Styling Options**

<details>

<summary><strong>Background Color</strong></summary>

**Overview**

As part of background customization, you can modify both the paper background color and the plot background color. The paper background refers to the overall chart area, while the plot background applies specifically to the region where the data is displayed, allowing better control over the chart’s visual appearance.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to change the background color:

1. Under the Margin section, expand the Background Color section.
2. In the Background Color section, change either the paper color or plot color or both .

The vertical bar chart is displayed as shown in the below example image.

<img src="../../../../.gitbook/assets/unknown (105).png" alt="" height="386" width="534">

<br>

</details>

<details>

<summary><strong>Card Border</strong></summary>

**Overview**

Card border refers to the visible outline or boundary around the chart container (card), used to visually separate it from other elements on the dashboard and enhance its appearance.&#x20;

**Procedure**

> <mark style="color:red;">**Note:**</mark> Although the below example pertains to a Vertical Bar Chart, the same procedure can be followed to configure the Card Border for all chart types.

The below step-by-step instructions help you understand how to change the card border:

1. Under the **Styling Chart**, expand the **Card Border** panel.
2. In the Card Border section, from the Style drop-down box, select the required option. For example, Dotted.
3. Specify the Size, Color, Radius, and Margins.
4. Click the Fetch Data button.

Once the above changes are made, the vertical bar chart is displayed as shown below.

<img src="../../../../.gitbook/assets/unknown (104).png" alt="" height="398" width="539">

<br>

</details>

<details>

<summary><strong>Conditional Formatting</strong></summary>

**Overview**

Conditional Formatting is a feature used to automatically apply formatting, such as colors, icons, or styles based on specific conditions or rules.

**Procedure**

> <mark style="color:red;">**Note:**</mark> Although this example pertains to a Table, the same procedure can be followed to configure the conditional formatting for all chart types.

The below step-by-step instructions help you understand how to configure conditional formatting.

1. Under the **Styling Chart**, expand **Conditional Formatting**, and then click the **Conditional Formatting** button.

<img src="../../../../.gitbook/assets/unknown (264).png" alt="" height="347" width="558">

The Conditional Statement section is displayed.

2. On the **Conditional Statement** section, click the **Add Row** button.

The Conditional Statement fields are displayed.

3. From the **Conditional Statement** fields, select the **Format Column, Base Column, Operator 1, Value 1, Operator  2,** and **Value 2.**&#x20;

Here is the description for the above mentioned **conditional statement** fields.

<table><thead><tr><th width="167.5555419921875">Field</th><th>Description</th></tr></thead><tbody><tr><td>Format Column</td><td>The <strong>Format Column</strong> specifies the column to which the formatting should be applied.</td></tr><tr><td>Base Column</td><td>The <strong>Base Column</strong> specifies the column whose values are evaluated to check the condition.</td></tr><tr><td>Operator 1</td><td><strong>Operator 1</strong> defines the comparison condition.</td></tr><tr><td>Value 1</td><td><strong>Value 1</strong> specifies the value used for comparison with Operator 1.</td></tr><tr><td>Operator 2</td><td><strong>Operator 2</strong> is an optional second condition used to create range-based conditions.</td></tr><tr><td>Value 2</td><td><strong>Value 2</strong> specifies the comparison value for Operator 2.</td></tr></tbody></table>

4. Click the **Icon** button and the **Shape** button to upload an **icon** and a **shape.**
5. Click the **BG Color** button to **change the background color.**
6. Click the **Text Color** button to change the text color.

> <mark style="color:red;">**Note:**</mark> If you want to remove the conditional statement row, click the Delete <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAVCAYAAABG1c6oAAABIUlEQVR4AeyTv2vCUBDHv3VoS0MLHV3azaFT55KhOIngXyO46Ogg2dxdXR1UBBcRBHchKCgOghAj4qCI4lP0DDEQ3xkzOCgY7sjlfnzIu8c3IITYXdMDuPJzj8BxB9Na3fYchn9RDByPw3RqdczG8r7kI3dLmKc02wvYumY6WDk1DYuuq2h9yEA1gY8I1SJJfDcrrB/rQZX6TkwGuhr6mGSymPQo2SvDyJQxp9DLLgBHEMUqhEkIs411sY0NhV52Aeg1ytcewNO9/EBJJ6CEKB+K4T0dwyuFXnZ+h8ZBMS3rVjc6KUe3rhpLUsraOI9kgW/hfzzpBVstmvRe6Z94Dv+yVBb4Qmr5avAqsdTTyCOoKv6BbKfPJPuHPmfZttsH7gEAAP//1Qq+pgAAAAZJREFUAwC1icjrRtGTfwAAAABJRU5ErkJggg==" alt="" data-size="original">
>
> button.

7. Finally, click the **Apply** button.

<img src="../../../../.gitbook/assets/unknown (265).png" alt="" height="240" width="624">



</details>

<details>

<summary><strong>Chart Formatting (Pie Chart)</strong></summary>

**Overview**

As part of chart formatting, you can increase the pie chart **hole size** and also the **explosion**. You can also change the display label as well.

> <mark style="color:red;">**Note:**</mark> Here is the description for Hole and Explosion.
>
> * **Hole:** Refers to the empty center space of the chart,  Adjusting the hole size converts a pie chart into a donut chart and controls how large the center opening is.
> * **Explosion:** Refers to the separation of slices from the center. Adjusting explosion moves slices outward to highlight or emphasize them.

**Procedure**

The below step-by-step instructions help you understand how to do these:

1. Under the **Styling Chart**, expand the **Chart Formatting** section.&#x20;

The Chart Formatting section is expanded.

2. To increase or decrease the **hole size**, then drag the **Hole Size Slider.**
3. To increase or decrease the **explosion size**, then drag the **Explosion Slider.**
4. If you want to change the **label,** then from the **Display Label** drop-down box, select the required option.

After making the above changes, the pie-chart is displayed as shown in the below example image.

<img src="../../../../.gitbook/assets/unknown (266).png" alt="" height="350" width="565">



</details>

<details>

<summary><strong>Chart Formatting (Gauze Chart)</strong></summary>

**Overview**

As part of chart formatting, you will specify the **Shape, Shape Type, Delta Position,  Delta Color, Tick Formatting, Label, Width, Color, Border Width, Border Color, Bar Thickness, Bar BG Color,** and **Auto Refresh.**

> <mark style="color:red;">**Note:**</mark> Here is the description for the above.
>
> * **Shape** – Defines the overall visual style of the gauge chart, such as **Angular** or other available display types.
> * **Shape Type** – Specifies the display format or layout of the selected gauge style, such as **gauge + number + delta**.
> * **Delta Position** – Determines the position where the delta value is displayed within the gauge chart.
> * **Delta Color** – Specifies the color used to represent the delta value or indicator.
> * **Tick Formatting** – Enables or disables the display of tick marks and related formatting options on the gauge chart.
> * **Label** – Specifies whether labels should be displayed for the gauge ticks or scale values.
> * **Width** – Defines the width or thickness of the tick marks displayed on the gauge.
> * **Color** – Specifies the color applied to the tick labels or tick elements.
> * **Border Width** – Defines the thickness of the border displayed around the tick elements.
> * **Border Color** – Specifies the color of the border applied to the tick elements.
> * **Bar Thickness** – Defines the thickness of the gauge bar displayed in the chart.
> * **Bar BG Color** – Specifies the background color of the gauge bar area.
> * **Auto Refresh** – Enables automatic refreshing of the chart to display updated data at regular intervals.

**Procedure**

The below step-by-step instructions help you understand how to do these:

1. Under the **Styling Chart**, expand the **Chart Formatting** section.&#x20;

The Chart Formatting section is expanded.

2. In the Chart Formatting section, specify the **Shape, Shape Type, Delta Position,  Delta Color, Tick Formatting, Label, Width, Color, Border Width, Border Color, Bar Thickness, Bar BG Color,** and **Auto Refresh.**

</details>

<details>

<summary><strong>Title</strong></summary>

**Applicable Components**

The **Title** property is applicable to multiple components of the dashboard.

**Purpose**

The purpose of configuring a **Title** is to clearly identify and describe the information represented in a dashboard component such as Pie Chart, Vertical Bar, Horizontal Bar, and Text Box, etc. A title helps users quickly understand the purpose and context of the visualization without needing additional explanation.

**Procedure**

The example below helps you understand how to configure the Title.&#x20;

> <mark style="color:red;">**Note:**</mark> Although this example pertains to a Pie Chart, the same procedure can be followed to configure the Title for all dashboard components.

Step-by-Step Instructions:

1. Under the **Styling** section, click the **Styling** icon.

<img src="../../../../.gitbook/assets/unknown (119).png" alt="" height="254" width="522">

The Styling fields section is displayed.

2. In the **Title** field, enter a **title**.
3. If required, change the **Font Type** and **Font Size.**
4. Use the Horizontal Align and Vertical Align range sliders to align the title either horizontally or vertically depending on the requirement. For example,  horizontally.

<img src="../../../../.gitbook/assets/unknown (120).png" alt="" height="390" width="580">

</details>

<details>

<summary><strong>Image Property</strong></summary>

**Applicable Charts**

* Local Image
* Web Image

**Overview**

The **Fit Card** option in **Image Property** is used to automatically adjust and resize the image so that it fits within the dimensions of the widget card or container. When enabled, the image is automatically scaled to match the card dimensions while fitting within the available display area. This helps ensure that the image is presented properly within the widget.

**Procedure**

> <mark style="color:red;">**Note:**</mark> Although the example below pertains to a **Local Image**, the same procedure can be followed to configure the **Image Property** for all applicable dashboard components.

The below step-by-step instructions help you understand how to configure the image property:

1. Under the **Styling Chart**, expand the **Image Property** panel.
2. In the **Image Property** panel, turn on the **Fit Card** option.

<figure><img src="../../../../.gitbook/assets/image (1867).png" alt="" width="500"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Subtitle</strong> </summary>

**Purpose**

The purpose of configuring a **Sub Title** in dashboard charts is to provide additional information or context related to the chart title. It helps users better understand the data being presented without overcrowding the main title.

In simple terms, the sub title acts as a secondary heading that provides extra details about the chart.

**Applicable Charts**

While creating a chart, sub title can be configured for the below:

* Info Widget
* Vertical Bar Chart
* Vertical Stack Bar
* Dot Plot Chart
* Bubble Chart
* Waterfall Chart

**Procedure**

The Sub title configuration is the same as the title configuration; therefore, follow the steps outlined in the above [Title](./#title) section.&#x20;

</details>

<details>

<summary><strong>Series Color</strong></summary>

**Purpose**

The purpose of **Series  Color** in charts is for better visualization and easy identification of data categories. For example, in a Pie Chart, different slice colors help users easily distinguish between categories, while in Bar or Line Charts, different series colors help identify multiple data series.

**Applicable Charts**

The **Series Color** is applicable to the below mentioned charts :

* Pie Chart
* Vertical Bar Chart
* Horizontal Bar Chart
* Vertical Stack Bar Chart
* Horizontal Stack Bar Chart
* Dot Plot Chart
* Bubble Chart

**Procedure**

The example below helps you understand how to change the series color:

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * Whenever the above-mentioned charts are created, the Series Colors are applied automatically by default. You are not required to configure the colors explicitly; however, the default colors can be modified if needed.&#x20;
> * Although this example pertains to a Pie Chart, the same procedure can be followed to other applicable charts.

**Step-by-Step Instructions**&#x20;

1. If you want to change Series (Slice) Color, then under the **Styling** section, expand **Series Color.**&#x20;

The set of series colors are displayed with their colors.

2. On the set of series colors, click the **required color**. For example, 00341.

<img src="../../../../.gitbook/assets/unknown (124).png" alt="" height="364" width="525">

The color picker is displayed.

3. From the **color picker**, select the required **color,** and then click the **Choose** button.

<img src="../../../../.gitbook/assets/unknown (125).png" alt="" height="270" width="555">

The series color is changed. See the image below.

<img src="../../../../.gitbook/assets/unknown (126).png" alt="" height="264" width="558">

</details>

<details>

<summary><strong>Legend</strong></summary>

**Purpose**

The purpose of configuring a **Legend** in a chart is to help users identify and understand the meaning of different data series, categories, or colors used in the visualization. For example, in a Pie Chart, the legend indicates which color represents each category, while in a Line or Bar Chart, it identifies different data series.

**Applicable Charts**

The Legend is applicable to all the charts **except** Info Widget, Gauge Chart, Radial Chart, Multiple Radial Chart, Tree Map, and Table type charts.

**Procedure**

The example below helps you understand how to change the series color:

> <mark style="color:red;">**Note:**</mark> Although this example pertains to a Pie Chart, the same procedure can be followed to other applicable charts.

**Step-by-Step Instructions**&#x20;

1. Under the **Styling Chart** section, expand the **Legend** section.
2. In the **Legend** section, enable the **Show Legend** option.
3. In the **Limit** field, specify the maximum number of legend items to be displayed in the chart.
4. Specify the **limit, orientation, X Position** and **Y Position, font type, family**, and **color**, and **box opacity.**

{% hint style="info" %}
**Tip:** Here is the description for the above:

* **Limit:** Specifies the maximum number of legend items to be displayed in the chart. This helps avoid overcrowding when the chart contains many categories or series.
* **Orientation:** Determines the direction in which legend items are displayed. The common orientations include - Horizontal and Vertical.
* **X Position** controls the horizontal placement.
* **Y Position** controls the vertical placement.
* **Box Opacity:** Controls the transparency level of the legend background box. Higher opacity makes the background more solid and Lower opacity makes the background more transparent.
{% endhint %}

After making the above changes, the pie-chart is displayed as shown in the below example image.

<figure><img src="../../../../.gitbook/assets/image (1790).png" alt="" width="563"><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Margin</strong></summary>

**Applicable Charts**

* Pie Chart
* Bar Charts
* Line Chart
* Dot, Bubble, and waterfall Charts
* Gauge Chart, Radial, and Multiple Radial Charts
* Heat Map

**Overview**

Margin refers to the empty space around the chart’s outer edges, used to ensure proper spacing from the container or other elements and to improve readability.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to configure the margins.

1. Under the Styling section, expand the Margin section.
2. In the Margin section, specify the Left, Right, Top, and Bottom margins as required. For example, change the Top margin from 100 to 78.

After making the changes, the vertical bar chart is displayed as shown in the below example image.

<img src="../../../../.gitbook/assets/unknown (103).png" alt="" height="365" width="529">

<br>

</details>

<details>

<summary><strong>Value</strong></summary>

**Overview**

The purpose of the **Value** field is to configure and customize how the primary data value is displayed within the widget. It allows you to control the appearance, formatting, and positioning of the displayed value to improve readability and visual presentation.

**Procedure**

The below step-by-step instructions help you understand how to configure the value.

1. Under the Styling section, expand the **Value** section.
2. If required, change the default **Font Type, Color,** and **Size**.
3. Specify the **Prefix** and **Suffix** values.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * In the **Prefix** field, you can add **text** or **symbols** to display **before** the value in the widget. _Example:_ Adding **$** before **58** displays **$58.**
> * In the **Suffix** field, you can add **text** or **symbols** to display **after** the value in the widget. _Example:_ Adding **%** before **58** displays **58%.**

4. Align the **Value** by selecting one of the **Left**, **Center**, or **Right** alignment icons.

Once the value is configured, it is displayed as shown in the example image below.

<figure><img src="../../../../.gitbook/assets/image (1871).png" alt="" width="547"><figcaption></figcaption></figure>





</details>

<details>

<summary><strong>Label Length</strong></summary>

**Applicable Charts**

* Pie Chart

**Overview**

In a pie chart, label length refers to the maximum number of characters shown for each slice’s label, controlling how much of the label text is displayed (often truncating longer labels for better readability).  &#x20;

**Procedure**

The below step-by-step instructions help you understand how to change the label length:

1. Under the **Styling Chart** section, expand the Label Length section.
2. In the **Label Length** section, specify the **label length.**
3. Click the **Fetch Data** button.

<figure><img src="../../../../.gitbook/assets/image (1872).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>X Axis</strong></summary>

**Applicable Charts**

* All Bar Charts
* Line Chart
* Dot Plot Chart&#x20;
* Bubble Chart
* Waterfall Chart

**Procedure**

The example below helps you understand how to configure X Axis:

1. In the Styling section, under Sub Title, expand X Axis pane.

The X Axis pane is expanded.

2. On the X Axis pane:
3. Enter the title, font type, size, and color.
4. From the Position drop-down box, select either Top or Bottom.
5. Select the other required options.

The X axis is displayed as per the configuration.

<img src="../../../../.gitbook/assets/unknown (106).png" alt="" height="345" width="498">

<br>

</details>

<details>

<summary><strong>Y Axis</strong></summary>

**Applicable Charts**

* All Bar Charts
* Line Chart
* Dot Plot Chart&#x20;
* Bubble Chart
* Waterfall Chart

**Procedure**

The example below helps you understand how to configure Y Axis:

1. In the Styling section, under Sub Title, expand the Y Axis pane.

The Y Axis pane is expanded.

2. On the Y Axis pane:
3. Enter the title, font type, size, and color.
4. From the Position drop-down box, select either Left or Right.
5. Select the other required options.

The Y axis is displayed as per the configuration.

<img src="../../../../.gitbook/assets/unknown (108).png" alt="" height="358" width="480">

<br>

</details>

<details>

<summary><strong>Series Type</strong></summary>

**Applicable Charts**

* Vertical Bar Chart
* Horizontal Bar Chart
* Vertical Stack Bar Chart
* Dot Plot Chart

**Overview**

This feature allows you to define how each data series should be displayed in the chart, either as a bar or as a line. This provides flexibility in visualizing different types of data within the same chart.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to configure the series type:

1. Under the Styling Chart, expand the Series Type pane.

The Series Type pane is expanded.

2. On the Series Type pane, from the drop-down box, select Bar or Line. For example, Line.

<img src="../../../../.gitbook/assets/unknown (109).png" alt="" height="298" width="580">

</details>

<details>

<summary><strong>Data Labels</strong></summary>

**Applicable Charts and Widgets**

* All Bar Charts
* Line Chart
* Dot Plot Chart
* Bubble Chart
* Waterfall Chart
* Heat Map
* Map Widget
* World Map Widget

**Overview**

Enabling the **Data Labels** feature allows users to view values or text directly on chart elements such as bars, lines, slices, points, or segments.

**Procedure**

> <mark style="color:red;">**Note:**</mark> The process of configuring **Data Labels** is the same for all applicable visualization charts. The **Vertical Bar Chart** image is provided for illustration purposes only.

The below step-by-step instructions help you understand how to configure the Data Labels:

1. Under the **Styling Chart**, expand the **Data Labels** panel.

The **Data Labels** panel is expanded.

2. On the **Data Labels** panel, enable the **Show** option.
3. Configure the other required properties including **Position, Display Units, Separators, Decimal, Currency, Prefix** and **Suffix** as required. See the below example image.

<figure><img src="../../../../.gitbook/assets/image (1844).png" alt="" width="492"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Graph Properties</strong> </summary>

**Applicable Charts**

* Line Chart

**Overview**

As part of configuring the **Graph Properties**, you can enable the **Fill Area and Fill Stack Area**, and specify **Fill Type, Shape, Dash,** and Series Color.&#x20;

**Procedure**

1. Under the Styling Chart, expand the **Graph Properties** panel.

The **Graph Properties** panel is expanded.

2. On the **Graph Properties** panel, turn on the **Fill Area** and **Fill Stack Area** options.

> <mark style="color:red;">**Note:**</mark> Here is the description for **Fill Area** and **Fill Stack Area** options.
>
> * **Fill Area** – Enables the area beneath the line to be filled with color, making it easier to visualize the magnitude and trend of data.
> * **Fill Stack Area** – Fills the area between multiple stacked lines, helping users understand the cumulative contribution of different data series.

3. Specify the **Fill**, **Shape**, **Dash**, and **Series Color** for each field.

> <mark style="color:red;">**Note:**</mark> Here is the description for the above.
>
> * **Fill** – Specifies the color or fill style applied to the area beneath the line when the Fill Area option is enabled.&#x20;
> * **Shape** – Defines the style of markers used at data points on the line chart, such as circles, squares, or other shapes, making individual data points easier to identify.
> * **Dash** – Controls the line pattern displayed in the chart, such as solid, dotted, or dashed lines, helping differentiate between multiple data series.
> * **Series Color** – Specifies the color assigned to a particular data series, improving visual distinction and readability when multiple series are displayed.

<figure><img src="../../../../.gitbook/assets/image (1845).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Bubble Size</strong></summary>

**Applicable Charts**

* Bubble Chart

**Overview**

The purpose of **Bubble Size** in a **Bubble Chart** is to represent an additional data variable by controlling the size of each bubble. It allows users to visualize three dimensions of data within a single chart.

**Procedure**

The below instructions help you understand how increase or decrease the bubble size:

1. Under the **Styling Chart**, expand the **Bubble Chart** panel.

The **Bubble Chart** panel is expanded.

2. On the **Bubble Chart** panel, use the **Bubble Size slider** to **increase** or **decrease** the bubble size.

<figure><img src="../../../../.gitbook/assets/image (1846).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Waterfall Setting</strong></summary>

**Applicable Charts**

* Waterfall Chart

**Overview**

The **Waterfall Setting** option is used to configure the appearance and behavior of elements within a **Waterfall Chart**. It allows customizing how **positive, negative,** and **total values** are displayed, making the chart easier to understand and visually interpret.

**Procedure**

The below instructions help you understand how to configure Waterfall settings:

1. Under the **Styling Chart**, expand the **Waterfall Setting** panel.

The **Waterfall Setting** panel is expanded.

2. On the **Waterfall Setting** panel, specify **colors** for **Positive Value Color, Negative Value Color,** and **Total Value Color.**
3. Enable the **Net Total Label** option.

The Net Total Label field is displayed.

4. In the **Net Total Label** field, specify the **Net Total Label,** and then click the **Apply** button. See the example image below.

> <mark style="color:red;">**Note:**</mark> The **Net Total Label** is used to define a custom text label for the **final cumulative total bar** displayed in a **Waterfall Chart.**

<figure><img src="../../../../.gitbook/assets/image (1847).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Collapsible</strong></summary>

**Applicable Components**

* Group Button

**Overview**

The **Collapsible** property allows users to expand or collapse the content of a widget using a **Toggle** button. This feature helps optimize dashboard space by hiding content that is not immediately required and displaying it only when needed. It improves dashboard organization, reduces visual clutter, and enhances the overall user experience by providing a cleaner and more manageable layout.

**Procedure**

The below instructions help you understand how to configure **Collapsible** property settings:

1. Under the **Styling Chart**, expand the **Collapsible** panel.

The panel is expanded.

2. On the expanded **Collapsible** panel, enable the **Collapse** option.

The Toggle button is displayed on the Groupm Button.

3. In the **Toggle Button Text** field, enter a **name** for the Toggle butto&#x6E;**.**
4. From the **Button Style** drop-down box, select an appropriate style.
5. Specify the **Width** and **Height** of the Toggle button.
6. Specify the **Font Family, Font Size,** and **Font Style** of the Toggle button text.
7. Specify the **Background Color** of the Toggle button.
8. Specify the **Color** of Toggle button text.

<figure><img src="../../../../.gitbook/assets/image (1886).png" alt="" width="437"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Button Config</strong></summary>

**Applicable Components**

* Group Button

**Overview**

The **Button Config** property allows you to define various settings such as the required number of **Rows**, **Button Alignment**, **Button Display Name**, **Font Family**, **Font Size**, **Font Style**, **Font Color**, **Button Background Color**, **Width**, **Height**, **Margins**, **Border Radius**, and **Navigation Action Type**.&#x20;

These configuration options help customize the appearance, layout, and behavior of buttons within the **Group Button Widget**. Proper configuration improves visual presentation, enhances usability, and ensures a more organized and interactive user experience.

**Procedure**

The below instructions help you understand how to configure **Button Config** property settings:

> <mark style="color:red;">**Note:**</mark> The below mentioned procedure can be applied to all the buttons on the Group Button Widget.

1. Under the **Styling Chart**, expand the **Button Config** panel.

The panel is expanded.

2. On the expanded **Button Config** panel, specify the number of **Rows**, **Button Alignment**, **Button Display Name**, **Font Family**, **Font Size**, **Font Style**, **Font Color**, **Button Class**, **Button Background Color**, **Width**, **Height**, **Margins**, and **Border Radius.**
3. From the **Action Type** drop-down box, select the required **navigation type**.

Based on the selected navigation type, the corresponding fields are displayed in the Resource drop-down box.&#x20;

3. In the **Resource** drop-down box, select the appropriate **resource**.
4. If you want to get the page opened in a new tab, enable the ![](<../../../../.gitbook/assets/image (1889).png>) button.
5. Apply the same procedure to other buttons as well.

<figure><img src="../../../../.gitbook/assets/image (1887).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Group Spacing</strong></summary>

**Applicable Components**

* Group Button

**Overview**

The **Button Config** property allows you to define various settings such as the required number of **Rows**, **Button Alignment**, **Button Display Name**, **Font Family**, **Font Size**, **Font Style**, **Font Color**, **Button Background Color**, **Width**, **Height**, **Margins**, **Border Radius**, and **Navigation Action Type**.&#x20;

These configuration options help customize the appearance, layout, and behavior of buttons within the **Group Button Widget**. Proper configuration improves visual presentation, enhances usability, and ensures a more organized and interactive user experience.

**Procedure**

The below instructions help you understand how to configure **Group Spacing** property settings:

1. Under the **Styling Chart**, expand the **Group Spacing** panel.
2. On the expanded **Group Spacing** panel, specify the **Group Margin** and **Group Padding** values.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * **Group Margin** – Group Margin defines the space outside the Group Button container, creating separation between the widget and surrounding dashboard elements.
> * **Group Padding** – Group Padding defines the space inside the Group Button container, creating spacing between the widget border and its internal content.

3. From the **Spacing Presets**, select the required **preset** choosing from Default, Comfortable, Spacious, and Compact.&#x20;

> <mark style="color:red;">**Note:**</mark>**&#x20;Spacing Presets** are predefined layout settings used to control the spacing and arrangement of elements within a widget for improved appearance and consistency. Here is the description for **Default, Comfortable, Spacious,** and **Compact** spacing presets.&#x20;
>
> * **Default** – Applies the system-defined standard spacing configuration for the widget.
> * **Comfortable** – Applies moderate spacing between elements to provide a balanced and easy-to-read layout.
> * **Spacious** – Applies larger spacing between elements to create a more open and less cluttered appearance.
> * **Compact** – Applies reduced spacing between elements to display content in a denser layout and save space.

<figure><img src="../../../../.gitbook/assets/image (1890).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Graph Header</strong></summary>

**Applicable Charts**

* Tree Map

**Overview**

The process of configuring the **Graph Header** in a **Tree Map** involves defining various text properties such as **Font**, **Font Size**, and **Color** to customize the appearance of the header. These settings help improve readability and ensure that the header aligns with the overall dashboard design and styling requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the Graph Header:

1. Under the **Styling Chart**, expand **Graph Header** pane&#x6C;**.**
2. From the expanded **Graph Header** panel, specify the required **Font**, **Font Size**, and **Color.**

Once specified, the header is displayed with the specified settings. See the example image below:

<figure><img src="../../../../.gitbook/assets/image (1860).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Graph Color</strong></summary>

**Applicable Charts**

* Tree Map
* Heat Map

**Overview**

The process of configuring the **Graph Color** involves defining Color Mode and Base Color. The **Color Mode** determines the method used to apply colors to the blocks or sections whereas the **Base Color** specifies the primary color used as the foundation for the Tree Map or Heat Map color scheme.

**Procedure**

The below step-by-step instructions help you understand how to configure the Graph Header:

1. Under the **Styling Chart**, expand the **Graph Color** pane&#x6C;**.**
2. On the expanded **Graph Color** panel, specify the **Color Mode** choosing from either **Category** or **Gradient**.
3. Specify **Base Color**.

<figure><img src="../../../../.gitbook/assets/image (1861).png" alt="" width="515"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Graph Text</strong></summary>

**Applicable Charts**

* Tree Map

**Overview**

The process of configuring the **Graph Text** involves defining various text properties such as **Font**, **Font Size**, and **Color** to customize the appearance of the displayed text. These settings help improve readability and ensure that the text aligns with the overall dashboard design and styling requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the Graph Text:

1. Under the **Styling Chart**, expand **Graph Text** pane&#x6C;**.**
2. From the expanded **Graph Text** panel, specify the required **Font**, **Font Size**, and **Color.**

<figure><img src="../../../../.gitbook/assets/image (1862).png" alt="" width="510"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Map Style</strong></summary>

**Applicable Charts**

* Map Widget
* World Map Widget

**Overview**

The process of configuring the **Map Style** involves defining various properties such as **Map Layout, Map Style, Bubble Color, Size, Opacity Level,** and **Clustered Markers** to customize the visual appearance and behavior of the map. These settings help control how geographical data is displayed, improve readability, and enhance the overall presentation of location-based information.&#x20;

**Procedure**

The below step-by-step instructions help you understand how to configure the Map Style:

1. Under the **Styling Chart**, expand **Map Style** pane&#x6C;**.**
2. From the expanded **Map Style** panel, specify the required **Map Layout, Map Style, Bubble Color, Size, Opacity Level,** and **Clustered Markers.**

> <mark style="color:red;">**Note:**</mark> Here is the description for the above fields.
>
> **Map Layout** – Defines the overall theme or display layout of the map, such as **Light** or other available map themes.
>
> **Map Style** – Specifies the visualization style, which includes **Bubble, Icon, Circle,** and **Image** used to display geographical data on the map.
>
> **Bubble Color** – Defines the color used for the bubbles displayed on the map to represent data points or values.
>
> **Size** – Controls the size of the bubbles displayed on the map.
>
> **Opacity Level** – Specifies the transparency level of the bubbles, where lower values make them more transparent and higher values make them more visible.
>
> **Use Clustered Markers** – Groups nearby map markers into a single cluster to reduce visual clutter and improve map readability when a large number of data points are displayed.

<figure><img src="../../../../.gitbook/assets/image (1927).png" alt="" width="440"><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Map Control</strong></summary>

**Applicable Charts**

* Map Widget

**Overview**

The **Map Control** section allows you to configure navigation and zoom-related settings for the **Map Widget**. As part of the configuration, you will enable **Zoom Control**, define the **Zoom Level**, and set **Minimum** and **Maximum Zoom** limits. These settings help control how users interact with the map, improve navigation, and ensure an optimal viewing experience for geographical data.

**Procedure**

The below step-by-step instructions help you understand how to configure the Map Control:

1. Under the **Styling Chart**, expand **Map Control** pane&#x6C;**.**
2. On the expanded **Map Control** panel, enable **Zoom Control.**
3. Specify the required **Zoom Level**, and set **Minimum** and **Maximum Zoom** limit&#x73;**.**

<figure><img src="../../../../.gitbook/assets/image (1928).png" alt="" width="485"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Header</strong></summary>

**Applicable Components**

* Table
* Pivot Table
* Custom Table

**Overview**

The process of configuring the **Header** involves specifying properties such as **Font Family, Font Size, Font Color, Background Color, Alignment,** and **Fixed** **Header** options to customize its appearance and behavior. These settings help improve readability, enhance the visual presentation, and ensure consistency with the overall dashboard design. Additionally, the **Alignment** option controls the positioning of the header content, while the **Fixed** **Header** option keeps the header in a constant position during navigation or scrolling.

**Procedure**

The below step-by-step instructions help you understand how to configure the header :

1. Under the **Styling Chart**, expand the **Header** pane&#x6C;**.**
2. Select the **Font Family, Size, Color,** and **Background Color**.
3. Select the header **text alignment** choosing from **Align Left**, **Align Center** or **Align Right**.
4. Enable the **Fixed Header** option if you want the column headers to remain visible at the top even while scrolling through the table data.
5. If you want to change the header width, click the **Reset Width** button.

<img src="../../../../.gitbook/assets/unknown (257).png" alt="" height="405" width="560">

</details>

<details>

<summary><strong>Body</strong></summary>

**Applicable Charts**

* Table
* Pivot Table
* Custom Table

**Overview**

The process of configuring the **Body** involves specifying properties such as **Font Family, Font Size, Font Color, Background Color,** and **Alignment** to customize its appearance. These settings help improve readability, enhance the visual presentation, and maintain consistency with the overall dashboard design and styling requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the body :

1. Under the **Styling Chart**, expand the **Body** pane&#x6C;**.**
2. Select the **Font Family, Size, Color,** and **Background Color**.
3. Select the **Body** **Text Alignment** choosing from **Align Left**, **Align Center** or **Align Right**.

<figure><img src="../../../../.gitbook/assets/image (1863).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Row</strong></summary>

**Applicable Charts**

* Table
* Pivot Table
* Custom Table

**Overview**

The process of configuring the **Row** in a **Table** involves specifying separate colors for **odd** and **even** rows to improve readability and enhance the visual appearance of the table. This alternating row-color pattern helps users easily distinguish between rows and improves data visibility.

**Procedure**

The below step-by-step instructions help you understand how to configure the row :

1. Under the **Styling Chart**, expand the **Row** pane&#x6C;**.**
2. Specify the **Odd Row Color** and **Even Row Color**.

<figure><img src="../../../../.gitbook/assets/image (1865).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Column</strong></summary>

**Applicable Charts**

* Table
* Pivot Table
* Custom Table

**Overview**

The process of configuring the **Column** in a table involves specifying separate colors for **odd** and **even** columns to improve readability and enhance the table's visual appearance. This alternating column-color pattern helps users easily distinguish between columns and improves data visibility.

**Procedure**

The below step-by-step instructions help you understand how to configure the column:

1. Under the **Styling Chart**, expand the **Column** pane&#x6C;**.**
2. Specify the **Odd Column Color** and **Even Column Color**.
3. If you want to **apply the column colors to headers**, then enable the **Apply to Header** option.

<img src="../../../../.gitbook/assets/unknown (261).png" alt="" height="333" width="575">

</details>

<details>

<summary><strong>Table Property</strong></summary>

**Applicable Components**

* Table
* Pivot Table
* Custom Table

**Overview**

As part of configuring **Table Properties**, you can customize settings such as **Table Border, Border Style, Border Size, Border Color, Cell Padding,** and **Top and Bottom Margins**. These properties help control the overall structure and appearance of the table, improve readability, enhance spacing between content, and ensure consistency with the overall dashboard design and formatting requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the table properties:

1. Under the **Styling Chart**, expand the **Table Properties** pane&#x6C;**.**
2. Under the **Table Properties** section, select the required **Table Border** option choosing from **Border All, Outer Border, Column Border, Row Border,** and **No Border.**&#x20;
3. Select the **Border Style, Size,** and **Color.**
4. Specify the **Cell Padding.**
5. Specify the **Top** and **Bottom** **margins.**

See the below example image.

<img src="../../../../.gitbook/assets/unknown (263).png" alt="" height="416" width="584">

</details>

<details>

<summary><strong>Download</strong></summary>

**Applicable Components**

* Table
* Pivot Table
* Custom Table

**Overview**

Configuring the **Download** feature enables users to export and download table data in multiple formats, such as **XLS, CSV,** and **PDF**. Supporting multiple file formats provides flexibility and helps meet different reporting and business requirements.

**Procedure**

The below step-by-step instructions help you understand how to configure the Download feature:

1. Under the **Styling Chart**, expand the **Download** pane&#x6C;**.**
2. On the **Download** panel, turn on **PDF, XLS,** and **CSV** option&#x73;**.**&#x20;

Once configured, the **PDF, XLS,** and **CSV** buttons are displayed on the table.

<figure><img src="../../../../.gitbook/assets/image (1868).png" alt="" width="527"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Table Settings</strong></summary>

**Applicable Components**

* Table
* Pivot Table
* Custom Table

**Overview**

The process of configuring **Table Properties** also includes setting up **Search** and **Pagination** functionalities. These features help users efficiently navigate and manage large volumes of data within the table. The **Search** functionality enables users to quickly locate specific records based on keywords or values, while **Pagination** organizes data into multiple pages, improving readability and reducing clutter by displaying a manageable number of records at a time.

**Procedure**

The below step-by-step instructions help you understand how to configure the table settings:

1. Under the **Styling Chart**, expand the **Table Settings** pane&#x6C;**.**
2. Under the **Table Settings** panel, enable the **Search** and **Pagination** option&#x73;**.**&#x20;
3. In the **Records Per Page** field, specify the **Number** of records per page.

The Search and Pagination options are displayed on the table as shown in the example image below:

<figure><img src="../../../../.gitbook/assets/image (1866).png" alt="" width="559"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Value Tag</strong></summary>

**Applicable Components**

* Active Textbox

**Overview**&#x20;

The **Value Tag** configuration enables you to select the required **Metrics** added in the **Field** tab and display them dynamically within the **Active Text Box**. This feature allows metric values to be integrated with text content, enabling the displayed information to update automatically based on the underlying data. It helps present key information in a more meaningful and interactive manner, improving readability and providing real-time insights within the dashboard.

**Procedure**

1. Under the S**tyling Chart**, expand **Value Tag.**
2. From the **Select Tag** drop-down box, select the required **value**.

<figure><img src="../../../../.gitbook/assets/image (1929).png" alt="" width="479"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Card Indicator</strong> </summary>

**Overview**

The **Card Indicator Property** is used to improve the visual presentation of a Dashboard and highlight important metrics or KPIs.

**Procedure**

1. On the **Designer** page, under the **Styling Chart**, expand the **Card Indicator** panel .

The panel is expanded.

2. Specify the **Indicator Line, Size, Color, Margin**, and **Padding**.

> <mark style="color:red;">**Note:**</mark> The **Indicator Line** specifies the position of the indicator line within the chart/widget, such as **Left**, **Right**, **Top**, or **Bottom**. This determines where the visual indicator appears.

3. If required, apply [**Conditional Formatting**](./#conditional-formatting) by clicking the ![](<../../../../.gitbook/assets/image (1884).png>) button, and then configuring it.

<figure><img src="../../../../.gitbook/assets/image (1885).png" alt="" width="529"><figcaption></figcaption></figure>



</details>

<details>

<summary><strong>Icon</strong> </summary>

**Overview**

The purpose of displaying an **Icon** in a chart is to provide a visual representation that enhances understanding and improves the overall appearance of the chart or widget. Icons help users quickly identify the meaning or context of the displayed information.

**Procedure**

If you want to show the icon on a chart or widget, then follow the below steps.

1. On the **Designer** page, under the **Styling Chart**, enable the **Show Icon** option.
2. From the **Group of Icons**, select the **relevant icon**.
3. From the **Icon Size Menu**, choose the required **size**.&#x20;
4. Select the **Icon color** and **Background color.**
5. Use the **Horizontal** and **Vertical Alignment** **sliders** to align the icon as required.
6. From the **Icon Opacity** drop-down box, specify the **opacity**.
7. From the **Icon Radius** drop-down box, specify the **radius.**

The icon is displayed as configured.

</details>
{% endtab %}

{% tab title="Drilldown" %}
**Overview**

The **Drill Down** feature in a Dashboard enables interaction between the components placed on it. Once components such as **Pie Charts, Vertical Bar Charts, Tables**, and others are added to the dashboard, their fields are automatically mapped with the corresponding fields of other dashboard components.&#x20;

This mapping enables seamless interaction among the components. For example, when a user clicks on a row in a **Table**, the related data in all other components is automatically filtered and updated accordingly, providing a more focused and interactive data analysis experience.

In simple terms, drilldown helps users move from overview data to granular data through interactive chart navigation.

***

**Configuring Drill Down**

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * The minimum **prerequisite** for using the **Drill Down** feature is to have at least **two components** added to the Dashboard, as interaction requires one component to communicate with and filter data in another component.
> * <mark style="color:red;">**Note:**</mark> The **Drilldown** feature is generally configured by default. However, if it is not already configured, you can enable it manually as required.

The below step-by-step instructions help you understand how to configure the drill down option:

1. Under the **Styling Chart**, click the **Drill Down** icon.

The Drill Down section is displayed.

2. In the **Drill Down** section, click **Show** next to the **Enable Drill Down** option.

<figure><img src="../../../../.gitbook/assets/image (1874).png" alt=""><figcaption><p>Dashboard - Enable Drill Down Option</p></figcaption></figure>

The Drill Down feature is configured.

> <mark style="color:red;">**Note:**</mark> There is no need to modify the **Source** or **Destination** fields in the respective drop-down lists, as the fields are automatically mapped by default.
{% endtab %}

{% tab title="Filters" %}
**Overview**

The **Filters** feature enables users to refine and control the data displayed in the dashboard by applying filters at **Dashboard**, **Page**, and **Graph** levels. Dashboard-level filters affect the entire dashboard, Page-level filters apply only to a specific page, and Graph-level filters impact only the selected chart or widget. This provides flexibility for targeted analysis and a more interactive dashboard experience.

***

**Configuring Filters**

The below step-by-step instructions help you understand how to configure the Filters feature:

> <mark style="color:red;">**Note:**</mark> Whenever a **filter value is modified**, ensure that you click the **Apply** button to save and apply the changes for the selected filter column.

1. On the **Dashboard Designer**, expand the **Filters** panel.

<figure><img src="../../../../.gitbook/assets/image (1875).png" alt="" width="563"><figcaption></figcaption></figure>

The **Filters** panel is expanded.

2. From the expanded dataset on the left navigation pane, **drag the required fields** and place them under **Filter on Dashboard**, **Filter on Page**, and **Filter on Graph.**
3. **Define Filter Type**

* On the **Filter** panel, expand the field panel to which you want to configure the filter.

The field panel is expanded.

* From the **Filter Type** drop-down box, select either **Basic Filter** or **Advanced Filter.**

4. **Define Selection Type**

* From the **Selection Type** drop-down box, select either **Single** or **Multiple,** and then click the **Apply** button.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * To remove a field, click the **Remove** ![](<../../../../.gitbook/assets/image (1857).png>)button next to the field.
> * To **hide** a filter, click the **Hide Filter**![](<../../../../.gitbook/assets/image (1855).png>) icon on it. The **Hide Filter** option is visible in only in View mode.
> * To **lock** a filter, click the **Lock Filter** ![](<../../../../.gitbook/assets/image (1856).png>)icon on it. Once locked, no action can be performed. The **Lock Filter** option is visible in only in View mode.

5. Click the **Update** button on the top right side of the application.

<figure><img src="../../../../.gitbook/assets/image (1859).png" alt="" width="563"><figcaption></figcaption></figure>

The **Save Dashboard** dialogue box is displayed.

6. &#x20;On the **Save Dashboard** dialogue box, click the **Update** button.

<figure><img src="../../../../.gitbook/assets/image (1850).png" alt="" width="563"><figcaption></figcaption></figure>

The Dashboard is updated.

7. Next, on the T**op Menu,** click the **View** button to preview the filters.

<figure><img src="../../../../.gitbook/assets/image (1851).png" alt="" width="563"><figcaption></figcaption></figure>

The Dashboard is displayed.

8. On the **Dashboard**, click **Filters** on the top right side of the application.

<figure><img src="../../../../.gitbook/assets/image (1852).png" alt="" width="563"><figcaption></figcaption></figure>

The Filters are displayed.

<figure><img src="../../../../.gitbook/assets/image (1853).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Drill Through" %}
**Overview**

**Drill Through** is a dashboard navigation feature that allows users to move from one sheet to another while retaining the context of the selected data point.&#x20;

When a user right-clicks a data point within a dashboard component, the application displays a list of available target sheets. Upon selecting a target sheet, the application navigates to that sheet and automatically applies the selected data point value as a filter.

As a result, the target sheet displays only the data relevant to the selected value.

***

**Using Drill Through Feature**

> <mark style="color:red;">**Note**</mark>
>
> **Prerequisite/Precondition**
>
> * The **field (column)** used in the **source component** must also exist as a **Page Filter** on the **target sheet.**&#x20;
> * The **filter field names/column** mapping must match between the **source** and **destination sheets**.
>
> **Important condition:**
>
> The **target sheet** must have **country\_name** configured as a **Page Filter**. Otherwise, the **Drill-Through** filter context cannot be applied, and the selected **value** will not be passed to the **target sheet**.

**Procedure**

The below step-by-step instructions help you understand how to use the **Drill Through** feature:

> <mark style="color:red;">**Note:**</mark> If any changes are made to the sheet, then **right click** on that **Sheet Tab** at the bottom of the screen, and select the **Save Sheet** option from the displayed menu.&#x20;
>
> See the below image.

<figure><img src="../../../../.gitbook/assets/image (1963).png" alt=""><figcaption></figcaption></figure>

**Step-by-Step Instructions**

1. On the **Dashboard Designer**, select a **Data Point** from a component. (For example, a Chart, Table, or a Widget).
2. Now, **right click** on the selected **Data Point.**

The list of available sheets is displayed.&#x20;

3. On the **list of available sheets**, click the **Target Sheet.**

<figure><img src="../../../../.gitbook/assets/image (1964).png" alt=""><figcaption></figcaption></figure>

The dashboard navigates to the selected sheet and the selected data point value is passed as a filter context to the target sheet. Also, the target sheet data is filtered automatically based on that value.

{% hint style="info" %}
**Example**

Suppose a component contains the field **country\_name**, and the user selects the data point **INDIA**. When the user right-clicks on **INDIA** and performs a **Drill Through** to another sheet, the dashboard navigates to the selected sheet and automatically applies the filter **country\_name = INDIA**.&#x20;

As a result, only the data related to **INDIA** is displayed on the target sheet.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> To navigate between the sheets, you can also use the **Back** button on the top left corner of the sheets.
{% endtab %}

{% tab title="Sheets" %}
**Overview**

In the **Dashboard Designer**, the **Sheets** functionality enables you to create and manage multiple sheets within a dashboard for different reporting and analysis purposes. These sheets can be used to organize related visualizations, present data from different perspectives, and support seamless navigation and interaction across the dashboard.

As part of sheet management, you can perform actions such as **Rename Sheet, Duplicate Sheet, Set as Default, Save Sheet, Hide Sheet,** and **Delete Sheet**. These features help you organize, maintain, and customize dashboard sheets according to your business requirements. Refer to the procedures below to learn how to perform each of these tasks.

***

**Procedure**

Expand the panels below to view detailed instructions and step-by-step information:

<details>

<summary><strong>Create Sheet</strong></summary>

**Overview**

The **Create Sheet** action allows you to add a new sheet to the dashboard for displaying additional visualizations, widgets, or data views. It helps organize information across multiple sheets within the same dashboard.

**Procedure**

The below step-by-step instructions help you understand how to create a sheet on Dashboard Designer.

1. On the **Dashboard Designer**, right-click the **New Dashboard Sheet** button at the bottom.

<figure><img src="../../../../.gitbook/assets/image (1967).png" alt=""><figcaption></figcaption></figure>

The Create Sheet dialogue box is displayed.

2. On the **Create Sheet** dialogue box:

* In the **Sheet Name** field, enter a **name** for the new sheet.
* Click the **Create** button.

<figure><img src="../../../../.gitbook/assets/image (1969).png" alt=""><figcaption></figcaption></figure>

The sheet is created. See the below image.

<figure><img src="../../../../.gitbook/assets/image (1970).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Rename Sheet</strong></summary>

**Overview**

The **Rename Sheet** action allows you to change the name of an existing sheet to better reflect its purpose or content. This helps improve dashboard organization and usability.

**Procedure**

The below step-by-step instructions help you understand how to rename a sheet on Dashboard Designer.

1. On the **Dashboard Designer**, right-click the dashboard sheet, which you want to rename.

The pop-up menu is displayed.

2. On the pop-up menu, click **Rename Sheet.**

<figure><img src="../../../../.gitbook/assets/image (1971).png" alt=""><figcaption></figcaption></figure>

The **Rename Sheet** dialogue box is displayed.

3. On the **Rename Sheet** dialogue box:

* In the **Sheet Name** field, enter a **new name** for the sheet. For example, changing Account Management to Finance Management.
* Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (1972).png" alt=""><figcaption></figcaption></figure>

The sheet is renamed, See the image below.

<figure><img src="../../../../.gitbook/assets/image (1973).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Duplicate Sheet</strong></summary>

**Overview**

The **Duplicate Sheet** action creates an exact copy of an existing sheet, including its components and configurations. This helps save time when creating similar dashboard views.

**Procedure**

The below step-by-step instructions help you understand how to duplicate a sheet on Dashboard Designer.

1. On the **Dashboard Designer**, right-click the dashboard sheet, which you want to duplicate.

The pop-up menu is displayed.

2. On the pop-up menu, click **Duplicate Sheet.**

<figure><img src="../../../../.gitbook/assets/image (1974).png" alt=""><figcaption></figcaption></figure>

The Duplicate Sheet dialogue box is displayed.

3. On the **Duplicate Sheet** dialogue box:

* In the **New Sheet Name field**, enter a **name** for the sheet.
* Click the **Duplicate** button.

<figure><img src="../../../../.gitbook/assets/image (1975).png" alt=""><figcaption></figcaption></figure>

The sheet is duplicated. See the image below.

<figure><img src="../../../../.gitbook/assets/image (1976).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Set as Default</strong></summary>

**Overview**

The **Set as Default** action designates a sheet as the default landing page when the dashboard is opened. This ensures users are presented with the most important or frequently used sheet first.

**Procedure**

The below step-by-step instructions help you understand how to set a dashboard sheet as a default sheet.&#x20;

1. On the **Dashboard Designer**, right-click on the dashboard sheet, which you want to **set as default** .

The pop-up menu is displayed.

2. On the pop-up menu, click **Set as Default.**

<figure><img src="../../../../.gitbook/assets/image (1978).png" alt=""><figcaption></figcaption></figure>

The **Set as Default** dialogue box is displayed.

3. On the **Set as Default** dialogue box, click the **Set as Default** button.

<figure><img src="../../../../.gitbook/assets/image (1979).png" alt=""><figcaption></figcaption></figure>

The **Sheet set as default successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (1980).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Save Sheet</strong></summary>

**Overview**

The **Save Sheet** action stores all changes made to the sheet, including component configurations and layout updates. This helps preserve the latest version of the dashboard sheet.

**Procedure**

The below step-by-step instructions help you understand how to save a sheet.&#x20;

1. On the **Dashboard Designer**, right-click on the dashboard sheet, which you want to save.

The pop-up menu is displayed.

2. On the pop-up menu, click **Save Sheet**.

<figure><img src="../../../../.gitbook/assets/image (1981).png" alt=""><figcaption></figcaption></figure>

The **Dashboard updated successfully** message is displayed.

<figure><img src="../../../../.gitbook/assets/image (1982).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Hide Sheet</strong></summary>

**Overview**

The **Hide Sheet** action removes a sheet from the dashboard navigation without deleting it. This is useful for restricting access to certain sheets or temporarily removing them from view.

**Procedure**

The below step-by-step instructions help you understand how to hide a sheet.&#x20;

1. On the **Dashboard Designer**, right-click on the dashboard sheet, which you want to hide.

The pop-up menu is displayed.

2. On the pop-up menu, click **Hide Sheet**.

<figure><img src="../../../../.gitbook/assets/image (1983).png" alt=""><figcaption></figcaption></figure>

The Disable dialogue box is displayed.

3. On the **Disable Sheet** dialogue box, click the **Disable** button.

<figure><img src="../../../../.gitbook/assets/image (1984).png" alt=""><figcaption></figcaption></figure>

The sheet is disabled. See the success message below.

<figure><img src="../../../../.gitbook/assets/image (1988).png" alt=""><figcaption></figcaption></figure>

4. If you want to enable the disabled sheet, right-click on the disabled sheet.

The pop-up menu is displayed.

5. On the pop-up menu, click **Show Sheet.**

<figure><img src="../../../../.gitbook/assets/image (1987).png" alt=""><figcaption></figcaption></figure>

The sheet is visible.

</details>

<details>

<summary><strong>Delete Sheet</strong></summary>

**Overview**

The **Delete Sheet** action permanently removes a sheet and its associated configurations from the dashboard. This helps maintain a clean and organized dashboard by removing sheets that are no longer required.

**Procedure**

The below step-by-step instructions help you understand how to hide a sheet.&#x20;

1. On the **Dashboard Designer**, right-click on the dashboard sheet, which you want to delete.

The pop-up menu is displayed.

2. On the pop-up menu, click **Delete Sheet**.

<figure><img src="../../../../.gitbook/assets/image (1989).png" alt=""><figcaption></figcaption></figure>

The **Delete Sheet** message box is displayed.&#x20;

3. On the **Delete Sheet** message box, click the **Yes** button.

<figure><img src="../../../../.gitbook/assets/image (1990).png" alt=""><figcaption></figcaption></figure>

The sheet is deleted.

</details>
{% endtab %}
{% endtabs %}

