---
icon: page
---

# Creating an ML Model

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Creating an ML Model involves a series of **sequential steps** that help ensure the model is built, tested, and made ready for use. These steps include **Preparing Data**, **Creating an ML Use Case**, **Selecting an ML Model**, **Performing a Test Run**, and **Deploying the ML Model**.&#x20;

Each step has a specific purpose, starting with preparing suitable data, defining the prediction objective, selecting an appropriate model, evaluating its performance, and finally making the selected model available for generating predictions.

Click on the below tabs to view detailed information about these steps.

{% tabs %}
{% tab title="Preparing Data" %}
**Overview**

**Preparing data** is an important step before selecting and training an ML model because the quality and structure of the data directly affect the model's performance. It ensures that the data is **clean, complete, relevant, and in a suitable format** for machine-learning algorithms.

**Procedure**

The below step-by-step instructions help you understand how to prepare data:

_**To prepare data**_

{% stepper %}
{% step %}
**Navigate to Auto ML Studio Page**

* On the **SCIKIQ Left Menu Bar**, expand **Auto ML Studio** under **ML/GENAI Studio**, and then click **Auto ML Studio.**

<figure><img src="../../../../.gitbook/assets/image (2766).png" alt=""><figcaption></figcaption></figure>

The **Auto ML Studio** page is displayed.
{% endstep %}

{% step %}
**Select Data Source**

1. On the **Auto ML Studio** page, select the required datasource choosing from **Dataset, Table/Topic,** or **Storage** based on your requirement. For example, Table/Topic.

The **Table Connection** and **Table** drop-down boxes are displayed.

2. From the **Table Connection** drop-down box, select the required table.

Once selected, the data is displayed on the right pane by undergoing EDA process. Also, the EDA tab is activated.

<figure><img src="../../../../.gitbook/assets/image (2797).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Next, click [**Creating an ML Use Case**](creating-an-ml-model.md#creating-an-ml-use-case)**.**
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Creating an ML Use Case" %}
**Overview**

Creating an **ML Use Case** helps define **what you want the machine-learning model to achieve** and what problem you want it to solve. It provides a clear objective for the ML process and helps the system determine how the selected data should be used to build a suitable model.

**Procedure**

The below step-by-step instructions help you understand how to create an ML use case:

_**To create an**_ _**ML use cas**_**e**

1. On the **Auto ML Studio** page, click the **ML Models** tab on the top.

<figure><img src="../../../../.gitbook/assets/image (2770).png" alt=""><figcaption></figcaption></figure>

The **Create ML Use Case** dialogue box is displayed.

2. On the **Create ML Use Case** dialogue box, click the **Create ML Use Case** button.

The **Name** and **Description** fields are displayed.

3. Specify a **Name** and **Description** for the ML use case, and then click the **Save** button.

<figure><img src="../../../../.gitbook/assets/image (2798).png" alt=""><figcaption></figcaption></figure>

4. Next, click [**Selecting an ML Module**](creating-an-ml-model.md#selecting-an-ml-module).
{% endtab %}

{% tab title="Selecting an ML Module" %}
**Overview**

Selecting an **ML Module** helps determine the **type of machine-learning problem you want to solve**. AutoML Studio provides different modules—**Anomaly, Classification, Clustering, Regression,** and **Time Series**—and selecting the appropriate one helps AutoML identify the type of model and approach suitable for the selected data and prediction objective.

See the below below table to understand the purpose of each of these ML Modules.

<table><thead><tr><th width="131.44439697265625" valign="top">ML Module</th><th valign="top">Purpose</th><th valign="top">Example</th></tr></thead><tbody><tr><td valign="top">Anomaly</td><td valign="top">Identifies unusual or abnormal patterns in data</td><td valign="top">Detecting unusual credit-card transactions</td></tr><tr><td valign="top">Classification</td><td valign="top">Categorizes data into predefined groups or classes</td><td valign="top">Predicting whether a customer will Churn or Not Churn</td></tr><tr><td valign="top">Clustering</td><td valign="top">Groups similar data items together without predefined categories</td><td valign="top">Grouping customers based on their purchasing behavior</td></tr><tr><td valign="top">Regression</td><td valign="top">Predicts a numerical or continuous value</td><td valign="top">Predicting the price of a house</td></tr><tr><td valign="top">Time Series</td><td valign="top">Analyzes data over time and predicts future values based on historical patterns</td><td valign="top">Forecasting next month's sales</td></tr></tbody></table>

**Procedure**

The below step-by-step instructions help you understand how to select an ML model:

_**To select an**_ _**ML model**_

1. On the **Auto ML Studio** page, from the **ML Model** drop-down box, select the **required module** choosing from **Anomaly, Classification, Clustering, Regression,** or **Time Series.** For example, **Time Series.**
2. From the **Select Parameters** section, select all the required **parameters**.

> <mark style="color:red;">**Note**</mark>:&#x20;
>
> * Each of the ML Modules has some common fields and some module-specific fields that need to be completed.&#x20;
> * Refer to the below [**Module Parameters**](creating-an-ml-model.md#module-parameters) table for description of the parameters.

3. Click the **Compare** button.

<figure><img src="../../../../.gitbook/assets/image (2799).png" alt=""><figcaption></figcaption></figure>

The **Module Comparison** table is displayed by showcasing the suggested model on the right pane. See the below image.

<figure><img src="../../../../.gitbook/assets/image (2800).png" alt=""><figcaption></figcaption></figure>

4. Next, click [**Performing Test Run**](creating-an-ml-model.md#performing-test-run).

***

#### **Module Parameters**

<table><thead><tr><th valign="top">Field/Parameter</th><th valign="top">Description</th><th valign="top">Applicable Modules</th></tr></thead><tbody><tr><td valign="top">Prediction Label</td><td valign="top">In this field, specify the target column that the ML model should predict.</td><td valign="top"><p>Anomaly</p><p>Clustering</p></td></tr><tr><td valign="top">Ignored Features</td><td valign="top">In this field, specify the features that are not required for prediction.</td><td valign="top">All modules</td></tr><tr><td valign="top">Numeric Imputation</td><td valign="top"><p>From this drop-down box, select the required option choosing from <strong>Drop, Mean, Median, Mode, K-Nearest Neighbors, and User Defined Value.</strong>   </p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>Numerical Imputation</strong> replaces missing values in numerical columns with appropriate numerical values, such as the mean or median, so that the data can be effectively used for analysis and machine learning.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Categorical Imputation</td><td valign="top"><p>From this drop-down box, select the required option choosing from <strong>Mode</strong> or <strong>User Defined Value.</strong>  </p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>Categorical Imputation</strong> <strong>replaces missing values in categorical columns with an appropriate category or value</strong>, so the data can be effectively used for analysis and machine learning.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Remove Outliers</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False</strong> to specify whether the outliers have to be removed or not.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> An an outlier is a value that is significantly different from the other values in the data.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Normalize</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False</strong> to specify whether normalization has to be  applied or not.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> A <strong>normalization parameter</strong> is a setting used to <strong>scale numerical data to a common range or scale</strong>, so that variables with different value ranges can be treated more consistently by a machine-learning model.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Transformation</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False</strong> to specify whether transformation has to be  applied or not.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> A <strong>Transform</strong> parameter is a setting used to <strong>change or convert data into a different format or scale</strong> so that it is more suitable for analysis or machine-learning models.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Remove Multicollinearity</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False</strong> to specify whether to remove Multicollinearity or not.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> The <strong>Remove Multicollinearity</strong> parameter is a setting that helps <strong>identify and remove highly correlated input features</strong> that provide similar or redundant information to the ML model. In simple terms, it helps reduce duplication among input variables, which can improve the reliability and performance of the ML model<strong>.</strong></p></td><td valign="top"></td></tr><tr><td valign="top">Feature Selection</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False.</strong></p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> The <strong>Feature Selection</strong> parameter is a setting that helps <strong>identify and select the most relevant input features</strong> for building the ML model while excluding features that are less useful.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Fix Imbalance</td><td valign="top"><p>From this drop-down box, select <strong>True</strong> or <strong>False</strong> to address imbalance.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> The <strong>Fix Imbalance</strong> parameter is a setting that helps address situations where one category in the target data has significantly more records than another category. It helps balance the data so that the ML model does not become overly biased toward the category with more records.</p></td><td valign="top">All modules except Time Series</td></tr><tr><td valign="top">Training Data Percent</td><td valign="top"><p>In this field, specify the <strong>Training Data Percent</strong>.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark><strong> Training Data Percent</strong> specifies <strong>the percentage of the available data</strong> that the ML model uses to learn patterns before making predictions.</p></td><td valign="top"><p>Classification</p><p>Regression</p></td></tr><tr><td valign="top">Date column</td><td valign="top"><p>From this drop-down box, select an <strong>Index Column</strong>.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the  <strong>Index Column</strong> tells the model which column identifies the individual time series or groups of observations being forecast.</p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Target </td><td valign="top"><p>From this drop-down box, select the <strong>Target Column</strong>.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>Target Column</strong> tells the Time Series model about the value that is to be predicted in the future.</p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Forecast Horizon</td><td valign="top">The <strong>Forecast Horizon</strong> parameter specifies how far into the future the model should make predictions.</td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Target Imputation</td><td valign="top"><p>From this drop-down box, select the <strong>Target Imputation</strong> choosing from <a data-footnote-ref href="#user-content-fn-1"><mark style="color:$primary;"><strong>Forward Fill</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-2"><mark style="color:$primary;"><strong>Backward Fill</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-3"><mark style="color:$primary;"><strong>Mean</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-4"><mark style="color:$primary;"><strong>Median</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-5"><mark style="color:$primary;"><strong>Linear Interpolation</strong></mark></a> <a data-footnote-ref href="#user-content-fn-6"><mark style="color:$primary;"><strong>Drift</strong></mark> </a>or <a data-footnote-ref href="#user-content-fn-7"><mark style="color:$primary;"><strong>Random</strong></mark></a><strong>.</strong></p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>Target Imputation</strong> tells the Time Series model how to fill missing values in the Target Column so that the complete time-series data can be used for training and forecasting.</p><p></p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Exogenous Imputation</td><td valign="top"><p>From this drop-down box, select the <strong>Target Imputation</strong> choosing from <a data-footnote-ref href="#user-content-fn-1"><mark style="color:$primary;"><strong>Forward Fill</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-2"><mark style="color:$primary;"><strong>Backward Fill</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-3"><mark style="color:$primary;"><strong>Mean</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-4"><mark style="color:$primary;"><strong>Median</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-5"><mark style="color:$primary;"><strong>Linear Interpolation</strong></mark></a> <a data-footnote-ref href="#user-content-fn-6"><mark style="color:$primary;"><strong>Drift</strong></mark> </a>or <a data-footnote-ref href="#user-content-fn-7"><mark style="color:$primary;"><strong>Random</strong></mark></a><strong>.</strong></p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>Exogenous Imputation</strong> tells the Time Series model how to fill missing values in the Target Column so that the complete time-series data can be used for training and forecasting.<br></p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Target Transformation</td><td valign="top"><p>From this drop-down box, select the <strong>target transformation</strong> choosing from <a data-footnote-ref href="#user-content-fn-8"><mark style="color:$primary;"><strong>Box-Cox</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-9"><mark style="color:$primary;"><strong>Logarithmic</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-10"><mark style="color:$primary;"><strong>Square Root</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-11"><mark style="color:$primary;"><strong>Exponential</strong></mark></a> or <a data-footnote-ref href="#user-content-fn-12"><mark style="color:$primary;"><strong>Cosine</strong></mark>.</a> </p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the target transformation tells the Time Series model how to transform the Target Column values so that trends, patterns, and variations in the data can be modelled more effectively.</p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Exogenous Transformation</td><td valign="top"><p>From this drop-down box, select the <strong>exogenous transformation</strong> choosing from <a data-footnote-ref href="#user-content-fn-13"><mark style="color:$primary;"><strong>Box-Cox</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-14"><mark style="color:$primary;"><strong>Logarithmic</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-10"><mark style="color:$primary;"><strong>Square Root</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-15"><mark style="color:$primary;"><strong>Exponential</strong></mark></a> or <a data-footnote-ref href="#user-content-fn-16"><mark style="color:$primary;"><strong>Cosine</strong></mark></a><mark style="color:$primary;"><strong>.</strong></mark></p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>exogenous</strong> <strong>transformation</strong> tells the Time Series model how to transform external input variables so that their patterns and relationship with the Target Column can be modelled more effectively.</p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Target Scaling</td><td valign="top"><p>From this drop-down box, select target scaling choosing from <a data-footnote-ref href="#user-content-fn-17"><mark style="color:$primary;"><strong>Z-Score</strong></mark></a><strong>,</strong> <a data-footnote-ref href="#user-content-fn-18"><mark style="color:$primary;"><strong>Min-Max</strong></mark></a>, <a data-footnote-ref href="#user-content-fn-19"><mark style="color:$primary;"><strong>Max-Abs</strong></mark></a>, or <a data-footnote-ref href="#user-content-fn-20"><mark style="color:$primary;"><strong>Robust</strong></mark></a>.</p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> Selecting the <strong>target scaling</strong> tells the Time Series model how to rescale the Target Column values so that they are represented on a more consistent scale for modelling and forecasting</p></td><td valign="top">Only Time Series</td></tr><tr><td valign="top">Fold Strategy</td><td valign="top"><p>From this drop-down box, select the fold strategy choosing from <a data-footnote-ref href="#user-content-fn-21"><mark style="color:$primary;"><strong>Expanding</strong></mark></a><mark style="color:$primary;"><strong>,</strong></mark> <a data-footnote-ref href="#user-content-fn-22"><mark style="color:$primary;"><strong>Rolling</strong></mark></a><strong>,</strong> or <a data-footnote-ref href="#user-content-fn-23"><mark style="color:$primary;"><strong>Sliding</strong></mark></a><strong>.</strong></p><p></p><p><mark style="color:red;"><strong>Note:</strong></mark> The <strong>Fold Strategy</strong> tells the Time Series model how to create successive training and validation periods while preserving the chronological order of the data<strong>.</strong></p></td><td valign="top"></td></tr></tbody></table>


{% endtab %}

{% tab title="Performing Test Run" %}
**Overview**

The **Test Run** allows you to **run the suggested ML model on the selected data to evaluate its performance before deploying it**.

Once AutoML displays a suggested model, you can use the Test Run to verify how well the model performs with the selected data and configured parameters. The Test Run provides performance results or evaluation metrics that help you determine whether the model is suitable for deployment.

**Procedure**

The below step-by-step instructions help you understand how to performing test run:

{% stepper %}
{% step %}
**Performing Test Run**

1. On the **ML Models tab,** click the **Test Run** button.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2801).png" alt=""><figcaption></figcaption></figure>

The **Model Results** and **Model Information** sections are displayed.
{% endstep %}

{% step %}
**Downloading Documentation**

* **If you want to download the documentation,** click the **Documentation** button.

<figure><img src="../../../../.gitbook/assets/image (2819).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Tip:** Downloading Documentation allows you to save and review the ML model's details, configuration, and other relevant information for future reference, sharing, and record-keeping.&#x20;
{% endhint %}
{% endstep %}

{% step %}
Next, click [**Deploying the ML Model**](creating-an-ml-model.md#deploying-the-ml-model)**.**
{% endstep %}
{% endstepper %}
{% endtab %}

{% tab title="Deploying the ML Model" %}
**Overview**

**Deploying the selected ML model** makes the trained and evaluated model **available for actual use to generate predictions on new data**.

Once the model has been tested and its performance is considered satisfactory, deployment makes the model accessible for prediction tasks. The deployed model can then receive new or previously unseen data and use the patterns it learned during training to produce predictions or results.

**Procedure**

The below step-by-step instructions help you understand how to deploy the selected model:

1. On the **ML Models tab,** click the **Deploy Model** button.

<figure><img src="../../../../.gitbook/assets/image (2804).png" alt=""><figcaption></figcaption></figure>

The **Deploy Experiment** dialogue box is displayed.

2. On the **Deploy Experiment** dialogue box, specify a **name** and **description** for the ML model, and then click on the **Deploy** button.

<figure><img src="../../../../.gitbook/assets/image (2805).png" alt=""><figcaption></figcaption></figure>

The **Experiment saved and request submitted in queue for training and development** success message is displayed.&#x20;

Also the **Deployment In Progress** appears on the screen.

See the below image.

<figure><img src="../../../../.gitbook/assets/image (2806).png" alt=""><figcaption></figcaption></figure>


{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Predicting Data Using an Existing ML Model**](predicting-data-using-an-existing-ml-model.md)
* [**Predicting Data in Real Time**](predicting-data-in-real-time.md)



[^1]: Replaces a missing value with the most recent available value before it

[^2]: Replaces a missing value with the next available value after it

[^3]: Replaces missing values with the average of the available target values

[^4]: Replaces missing values with the middle value of the available target values, which can be useful when the data contains extreme values

[^5]: Estimates a missing value by calculating a value between the known values before and after the missing value

[^6]: Estimates missing values based on the overall change or trend observed in the time-series data

[^7]: Replaces missing values with randomly selected values based on the available target data or its distribution

[^8]: Transforms the target data to make its distribution more suitable for modelling, particularly when the data is highly skewed

[^9]: Reduces the effect of very large values and can make rapidly increasing data easier for the model to analyse

[^10]: Reduces the effect of large values and can help make highly variable data more suitable for modelling

[^11]: Applies an exponential transformation to the target values to represent or model certain growth patterns

[^12]: Applies a cosine transformation to the target values and can be useful for data with periodic or cyclical patterns, depending on the modelling approach

[^13]: Transforms the exogenous data to make its distribution more suitable for modelling, particularly when the data is highly skewed

[^14]: Reduces the effect of very large values and can make rapidly increasing data easier for the model to process

[^15]: Applies an exponential transformation to the exogenous values to represent or model certain growth patterns

[^16]: Applies a cosine transformation to the exogenous values and can help represent certain cyclical or periodic patterns, depending on the data and modelling approach

[^17]: Scales the target values based on their mean and standard deviation, so the values are expressed in terms of how far they are from the average

[^18]: Scales the target values to a specified range, commonly between 0 and 1, based on the minimum and maximum values

[^19]: Scales the target values based on the largest absolute value, generally keeping the values within the range of -1 to 1

[^20]: Scales the target values using statistics such as the median and interquartile range, making it less affected by extreme values or outliers

[^21]: The training data starts with an initial period and progressively increases by adding newer observations in each fold, while the validation period moves forward.

[^22]: The training and validation periods move forward through the data while maintaining a fixed or defined window for training, depending on the configuration.

[^23]: Both the training and validation windows move forward through the data, keeping the training window focused on a recent period rather than continuously adding older observations.
