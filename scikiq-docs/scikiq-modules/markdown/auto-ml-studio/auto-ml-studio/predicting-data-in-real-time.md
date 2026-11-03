---
icon: page
---

# Predicting Data in Real Time

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Once an ML model is deployed, it is ready to be **used with new data to generate predictions**. The model uses the patterns and relationships it learned during the training process to analyse the new input data and produce the expected prediction or result. This allows the trained model to be applied to new records without having to train the model again.

***

### Procedure

The process of **predicting data in real time** is similar to predicting data using an existing ML Model. However, instead of selecting an existing model, you need to select **New Model** and choose the required **ML Module**, such as **Time Series**.

To perform the prediction, create a pipeline with an **Input Node, Transform Node, and ML Node**, and configure the required settings. For a Time Series model, these settings include **Target Column, Date Column, What You Are Forecasting?, Time Grain, Missing Periods,** and **Forecast Horizon**. You can also specify the **Seasonal Period**, if required.

Once the pipeline is configured and executed, the ML model processes the real-time data and **generates the predicted data**.

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Configuring Input Node" %}
1. On the **SCIKIQ Left Menu**, expand **SCIKIQ Delta Hub** under **SCIKIQ CONNECT**, and then click **Create Delta Pipeline**.

<figure><img src="../../../../.gitbook/assets/image (2786).png" alt=""><figcaption></figcaption></figure>

The **Draft Pipeline** screen is displayed.

2. On the **Draft Pipeline** screen, click **Create New One** button.

<figure><img src="../../../../.gitbook/assets/image (2787).png" alt=""><figcaption></figcaption></figure>

The **Create Delta Pipeline** page is displayed.

2. On the **Create Delta Pipeline** page, drag the required **Input node** from the **Node Palette** onto the right pane. For example, Database Input.

The Input fields are displayed on the left pane.

3. Now, on the **left pane**, specify the **Data Type, Datasource, Table,** and select the **required columns**.
4. Click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2807).png" alt=""><figcaption></figcaption></figure>

5. Next, click [**Configuring Transform Node**](predicting-data-in-real-time.md#configuring-transform-node).
{% endtab %}

{% tab title="Configuring Transform Node" %}
1. On the **Create Delta Pipeline** page, click the **Transform** button.

The **Transform Node Palette** is displayed.

2. From the **Transform Node Palette,** drag the required **transform node** (For example, Filter By Node.) on to the right pane, and connect the **Transform Node to the Input Node**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2790).png" alt=""><figcaption></figcaption></figure>

The Transform Node fields are displayed on the left pane.

3. Next, on the **left pane**, click the **Add/Edit Filter** button.

The **Add/Edit Filter** screen is displayed.

4. On the **Add/Edit Filter** screen:

A. Select the **parameter** for which want the prediction to be performed.

B. Select the **applicable operator**, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2810).png" alt=""><figcaption></figcaption></figure>

4. Next, click [**Configuring ML Model**](predicting-data-in-real-time.md#configuring-ml-node).
{% endtab %}

{% tab title="Configuring ML Node" %}
1. From the **Top Menu**, drag the **ML Node** onto the Canvas, and then connect the previous node to it.

<figure><img src="../../../../.gitbook/assets/image (2794).png" alt=""><figcaption></figcaption></figure>

The **ML Model settings** are displayed on the left menu.

2. On the left menu, under **ML Model**:

A. From the **Mode** drop-down box, select **New Model.**

B. From the **Model Type** drop-down box, select **Model type**. For example, Time series.

C. In the **Target Column** drop-downbox, select the required target column.

> <mark style="color:red;">**Note:**</mark> Selecting the Target Column tells the deployed ML model what value or outcome to predict from the provided real-time input data.

D. From the  drop-downbox, select the required date column.

> <mark style="color:red;">**Note:**</mark> The Date Column tells the Time Series ML model when the real-time data occurs or for which time period the prediction needs to be generated.

E. From the **What you are forecasting?** drop-downbox, select the required value. For example, Quantity.

G. From the **Time Grain** drop-downbox, select the required value. For example, Hourly.

> <mark style="color:red;">**Note:**</mark>
>
> * The **Time Grain** parameter specifies the **time interval at which the Time Series ML model should generate predictions**, such as **Hourly, Daily, or Weekly.**
> * If you don't want to choose a specific time interval, then select **Auto-detect from data** option. The **Auto-detect from Data** allows the Time Series ML model to **automatically determine the appropriate time grain or frequency from the date/time values in the data**, instead of selecting it manually.

H. From the **Missing Periods** drop -downbox, select the applicable option.

> <mark style="color:red;">**Note:**</mark>
>
> * The **Missing Periods** parameter specifies **how the Time Series ML model should handle gaps in the expected sequence of time periods when predicting real-time data**.
> * If you don't want to choose a specific option, then choose Auto (Zero for Quantities, Carry Forward for Prices). This option automatically handles missing periods by assigning **zero to missing quantity values** and **carrying forward the most recent available price values**.

I. In the **Forecast Horizon**, specify the period for which you want to forecast.

J. In the **Seasonal Period** field (Optional), specify the applicable value.

> <mark style="color:red;">**Note:**</mark>The **Seasonal Period** parameter specifies the **length of a recurring pattern or cycle in the time-series data**. It helps the Time Series ML mode identify and use repeated patterns when generating predictions.
>
> However, this parameter is optional.

H. Click the **Run** button.

<figure><img src="../../../../.gitbook/assets/image (2823).png" alt=""><figcaption></figcaption></figure>

The predicted data is generated.
{% endtab %}
{% endtabs %}



***

### Related Topics

* [**Predicting Data Using an Existing ML Model**](predicting-data-using-an-existing-ml-model.md)

