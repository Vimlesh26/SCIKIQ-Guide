---
hidden: true
icon: page
---

# Copy of Drill Through

**Contents**

* [**Instructions for Using this Page**](copy-of-drill-through.md#instructions-for-using-this-page)
* [**Overview**](copy-of-drill-through.md#overview)
* [**Procedure to Use Drill Through Feature**](copy-of-drill-through.md#procedure-to-use-drill-through-feature)
* [**Related Topics**](copy-of-drill-through.md#related-topics)

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**What is Drill Through?**

**Drill Through** is a dashboard navigation feature that allows users to move from one sheet to another while retaining the context of the selected data point.&#x20;

When a user right-clicks a data point within a dashboard component, the application displays a list of available target sheets. Upon selecting a target sheet, the application navigates to that sheet and automatically applies the selected data point value as a filter.

As a result, the target sheet displays only the data relevant to the selected value.<br>

***

## **Procedure to Use Drill Through Feature**

The below step-by-step instructions help you understand how to use the Drill Through option:

**Prerequisite/Precondition**

* The field (column) used in the source component must also exist as a Page Filter on the target sheet.&#x20;
* The filter field names/column mapping must match between the source and destination sheets.

**Example**

Suppose a component contains the field: country\_name and the user selects the data point: INDIA. When the user right-clicks on "INDIA" and drills through to another sheet: The dashboard navigates to the selected sheet. The target sheet is automatically filtered as: country\_name = INDIA.

As a result, only data related to INDIA is displayed.

<br>

<br>

**Step-by-Step Instructions**

1. On the **Dashboard Designer**, select a **Data Point** from a component. (For example, a chart, table, or widget).
2. Now, **right click** on the selected **Data Point.**

The list of available sheets is displayed.&#x20;

3. On the **list of available sheets**, click the **Target Sheet.**

The dashboard navigates to the selected sheet and the selected data point value is passed as a filter context to the target sheet. Also, the target sheet data is filtered automatically based on that value.

<br>

3. &#x20;first ensure that the **source column** and **destination column** are the same in the sheets where you want to apply the filters.
4. If any changes are made in a sheet, then **Right Click** on that Sheet Tab at the bottom of the screen, and select the **Save Sheet** option from the displayed menu.&#x20;

<figure><img src="../../../../.gitbook/assets/image (1960).png" alt=""><figcaption></figcaption></figure>

The sheet is saved.

3. Now, right click on the required row, and then select the sheet to which you wish to navigate to.

> <mark style="color:red;">**Note:**</mark> To navigate between the sheets, you can also use the **Back** button on the top left corner of the sheets.

<figure><img src="../../../../.gitbook/assets/image (1943).png" alt=""><figcaption></figcaption></figure>

The navigated sheet opens with the filtered values applied.

***

## Related Topics

* [**Adding Visualization Charts**](../adding-visualization-charts.md)
* [**Fields**](fields.md)
* [**Styling**](styling.md)
* [**Filters**](filters.md)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
