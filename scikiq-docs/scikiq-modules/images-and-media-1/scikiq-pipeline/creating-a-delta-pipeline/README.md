---
icon: code-branch
---

# Creating a Delta Pipeline

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Creating a new Delta Pipeline involves a series of configuration steps. As part of the process, you must configure the **Input Node**, **Transform Nodes**, **Output Node**, **Execution Settings**, and **Parameters**.

Click the tabs below to view the description of each configuration step

{% tabs %}
{% tab title=" Input Node" %}
The **Input Node** defines **where the data originates** for the delta pipeline. It is used to establish the connection to the source system and specify what data should be ingested (such as tables, files, or queries). Proper configuration ensures that only the intended data enters the pipeline. It also supports incremental logic by identifying which records should be considered new or updated.&#x20;

To learn how to configure input nodes, click [**Configuring Input Nodes**](configuring-input-nodes.md).
{% endtab %}

{% tab title="Transform Node" %}
The **Transform Node** defines **how the data is modified, enriched, or processed** within the pipeline. It is used to apply business logic such as calculations, data mappings, formatting, cleansing, and rule-based transformations. This ensures that raw data is converted into meaningful and usable information. Proper transformation design is essential for accurate analytical and operational outcomes.

To learn how to configure transform nodes, click [**Applying Transform Nodes**](applying-transform-nodes.md)**.**
{% endtab %}

{% tab title="Output Nodes" %}
The **Output Node** defines **where the processed data is written** after transformations are applied. It ensures that data is delivered to the correct target system, table, or asset with the expected structure. Proper configuration helps maintain data integrity and consistency in the destination. It also supports controlled data publishing for downstream consumption.

To learn how to use the output nodes, click [**Using Output Nodes**](using-output-nodes.md).
{% endtab %}

{% tab title="Execution Settings" %}
Execution Settings control **how and when the pipeline runs**. This includes parameters such as execution mode, scheduling behavior, performance settings, and error-handling behavior. Proper configuration ensures reliable execution, optimal resource usage, and predictable pipeline behavior. It also supports operational stability in production environments.

To learn how to configure execution settings, click [**Configuring Execution Settings**](configuring-execution-settings.md).
{% endtab %}

{% tab title="Parameters" %}
**Parameters** allow the pipeline to be **dynamic and reusable** by accepting values at runtime instead of hardcoding them. They are commonly used for filters, dates, file paths, environment values, or thresholds. This improves flexibility and allows the same pipeline to be used across different scenarios. Proper parameterization also supports automation and operational scalability.

To learn how to configure parameters, click **Configuring Parameters**.
{% endtab %}
{% endtabs %}

***

### Related Topics

* [**Managing a Delta Pipeline**](/broken/pages/vLPVrjbzT8iMRGC7KtVt)
