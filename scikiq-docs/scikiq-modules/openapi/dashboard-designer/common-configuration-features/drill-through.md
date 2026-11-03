---
hidden: true
icon: page
---

# Drill Through

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

**Drill Through** is a dashboard navigation feature that allows users to move from one sheet to another while retaining the context of the selected data point.&#x20;

When a user right-clicks a data point within a dashboard component, the application displays a list of available target sheets. Upon selecting a target sheet, the application navigates to that sheet and automatically applies the selected data point value as a filter.

As a result, the target sheet displays only the data relevant to the selected value.<br>

***

### **Using Drill Through Feature**

**Prerequisite/Precondition**

* The **field (column)** used in the **source component** must also exist as a **Page Filter** on the **target sheet.**&#x20;
* The **filter field names/column** mapping must match between the **source** and **destination sheets**.

**Important condition:**

The **target sheet** must have **country\_name** configured as a **Page Filter**. Otherwise, the **Drill-Through** filter context cannot be applied, and the selected **value** will not be passed to the **target sheet**.

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

***

## Related Topics

* [**Adding Visualization Charts**](../adding-visualization-charts.md)
* [**Fields**](fields.md)
* [**Styling**](styling.md)
* [**Filters**](filters.md)
