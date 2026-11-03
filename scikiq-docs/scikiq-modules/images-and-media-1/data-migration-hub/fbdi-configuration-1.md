---
icon: file-fragment
---

# FBDI Configuration

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

<details>

<summary><strong>What is FBDI?</strong></summary>

**FBDI (File-Based Data Import)** is a method used in Oracle Fusion Applications to import large volumes of data into the system using structured files. It allows data from external sources—such as Oracle E-Business Suite (EBS) or legacy systems—to be loaded into Oracle Fusion in a controlled and standardized way.

In FBDI, data is first prepared in predefined templates that follow Oracle’s data structure and validation rules. These files are then uploaded to the system, where they are processed through interface tables and validation programs before being imported into the target application tables.

</details>

<details>

<summary><strong>Configuring SCIKIQ FBDI</strong></summary>

Configuring SCIKIQ FBDI enables you to extract data from Oracle EBS, stage and store it in Amazon S3, and subsequently load it into Oracle Fusion using the File-Based Data Import (FBDI) process. This approach ensures a structured, scalable, and reliable data migration workflow across systems.

</details>

***

### Configuration Procedure

The process of configuring SCIKIQ FBDI involves the below mentioned two key steps.

{% tabs %}
{% tab title="1. Create Template for Oracle Fusion" %}
**Overview**

Creating a template establishes a standardized table structure to import data from Oracle EBS. It defines a predefined format that ensures data is structured, validated, and aligned with system requirements, thereby enabling accurate and error-free data import.

The template creation process consists of two main steps: **configuring template details** and **adding columns.**&#x20;

The sections below provide step-by-step instructions to guide you through each of these steps.

**Procedure**

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Configure Template Details</strong></summary>

**Overview**

In the **Configure Template Details** step, you are required to provide key information such as the template name, display name, schema name, object owner, object type, table name, and description.

**Procedure**

&#x20;1\.  On the **SCIKIQ Left Navigation Bar**, expand **Scikiq Migration Hub** under **SCIKIQ CONNECT**, and then click **Create FBDI Template**.&#x20;

<figure><img src="../../../.gitbook/assets/S (146).png" alt=""><figcaption><p>Create FBDI Template Menu Item</p></figcaption></figure>

The FBDI Template page is displayed.

2. On the **Right Pane** of **FBDI Template page,** enter the **Template name, Display name,** **Schema name, Object Owner,** and **Description**.

> <mark style="color:red;">**Note:**</mark> Refer to the below **Template Field Description** table for the description of these fields.

<figure><img src="../../../.gitbook/assets/1 (8).png" alt=""><figcaption><p>FBDI Template Page</p></figcaption></figure>

**Template Field Description**

<table><thead><tr><th width="212" valign="top">Field</th><th valign="top">Purpose</th></tr></thead><tbody><tr><td valign="top">Template name</td><td valign="top">Specifying the <strong>Template name</strong> provides a <strong>unique identifier</strong> for the template so it can be easily referenced, reused, and managed</td></tr><tr><td valign="top">Display name</td><td valign="top">The purpose of specifying a <strong>Template Display Name</strong> is to provide a user-friendly and easily recognizable label for the template in the application interface.</td></tr><tr><td valign="top">Schema name</td><td valign="top">In this field, specify <strong>Fusion</strong>. Specify the Fusion option makes the FBDI-based data imports are executed within the predefined Fusion application schema.</td></tr><tr><td valign="top">Object Owner</td><td valign="top"><p>In this field, select the required <strong>Oracle Fusion application schema module</strong>. For example GL.</p><p></p><p>Here is the complete list of Object Owner values with their meanings, presented in a single consolidated list:</p><p></p><ul><li>Fusion – Core Fusion schema containing shared/common objects</li><li>GL – General Ledger (financial accounting)</li><li>AP – Accounts Payable (supplier invoices, payments)</li><li>AR – Accounts Receivable (customer invoices, receipts)</li><li>XLA – Subledger Accounting (accounting engine for subledgers)</li><li>FA – Fixed Assets (asset management)</li><li>CE – Cash Management (banking and cash transactions)</li><li>ZX – Tax (tax configuration and processing)</li><li>IBY – Payments (payment processing engine)</li><li>IEX – Collections (collections and dunning processes)</li><li>EXM – Expenses (employee expense management)</li><li>FUN – Financial Utilities (cross-functional financial processes)</li><li>JE – Journal-related or localization schema</li><li>JG – Localization or regional financial schema</li><li>JL – Localization or ledger-related schema</li><li>JV – Journal or localization-related schema</li><li>JA – Localization or regional accounting schema</li><li>FV – Financials vertical/public sector-related schema</li><li>XLV – Ledger/valuation-related supporting schema</li><li>VRM – Revenue management–related schema</li><li>ARB – Advanced receivables/billing–related schema</li><li>CXX – Custom or extension schema (customer-specific)</li></ul></td></tr></tbody></table>

</details>

<details>

<summary><strong>2.Add Columns</strong></summary>

**Overview**

In the **Add Columns** step, you need to define the structure of the template by specifying details such as column name, display name, data type, column order, and description.

**Procedure**

1. After entering all the required template details, click the  **Add Column** button on the **FBDI Template** page.

> <mark style="color:red;">**Note:**</mark> To create a template, you need to add at least a column.

<figure><img src="../../../.gitbook/assets/1 (9).png" alt=""><figcaption><p>FBDI Template Page - Add Column Button</p></figcaption></figure>

The Add/Edit Column Details dialogue box is displayed.

2. On the **Add/Edit Column Details** dialogue box, enter the **Column Name, Display Name, Data Type, Column Order,** and **Description**.

{% hint style="info" %}
**Tip:** When adding columns to a template, make sure you use the exact column names as defined in the Oracle documentation. Along with the column name, also specify the required properties such as data type, precision, and scale.

For example, if you are creating a template for General Ledger, you must refer to the Oracle documentation and add columns using the exact names provided there. If the documentation specifies a column name like ACCESS\_SET\_ID, you should use that exact name in your template without any changes.

Here is the link for Oracle documentation:

[https://docs.oracle.com/en/cloud/saas/financials/26a/oedmf/glaccesssets-25895.html#Details](https://docs.oracle.com/en/cloud/saas/financials/26a/oedmf/glaccesssets-25895.html#Details)
{% endhint %}

3. From the **Is Nullable** drop-down box, select **Yes** or **No**.

{% hint style="info" %}
**Tip:** The Is Nullable options (Yes/No) indicates whether a field (column) in a table or template can accept empty (NULL) values or must always have a value.
{% endhint %}

4. Click the **Save Column** button.

<figure><img src="../../../.gitbook/assets/1 (10).png" alt=""><figcaption><p>Add/Edit Column Details Dialogue Box</p></figcaption></figure>

The column is created and displayed on the FBDI Template page.

<figure><img src="../../../.gitbook/assets/1 (11).png" alt=""><figcaption><p>FBDI Template Column</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* To view the column details, click the View ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAcCAYAAAB2+A+pAAACbElEQVR4AeyWX0hTURzHv2fqhjVNF7g9uFGwcE/ZQz1E+BQUmI29SIJaSNAfilBJmlj2Z4+WPfRv07UWxCRIIs0ijCJtsdCkhuuv2EMz21YazmaJ7nbP2YPDeec23PBh997vuef8zrm/zznfcx6u6Nn7IS4VGv71mQuXCPxVIJcimeIREQ8DR0RTEEiDU2ByCLG6reY4DuPjP/Gwyw5zezduWXrwst+JaX8gNP0EymVX7PP9xrmzN3Gy/ho6Op5icPAj+vucuHH9Pg4faoHN1ovZ2bm40VHBo6Pfcea0GSNfxlCoLMDF1uMwmhpgtuhRV78PYnEWerpf4XLrXQQC/+KCC4Knpv7AZHwAP//OzMpATU0p3G4v9lcb0Kg3YsNGBcr27mAw57sRdN57DrolLBBDIQh2OFxwf/OyFHK5DDJZLh4/cmB+LsjidvswijRKgBDQq+/FW4y5fbQakwTBKqUcdKU0SyDwFxx/S6VraJNpXe5azMzw9vIHjwYUivXIy5PSakwSBBdpVNBqS1iSyQk/Bl5/wJGjOpyoLUdT8wFs3aZB75MB1k/3uqp6N6Q5CxNjHVEKQTAhBDpdCcq0oX2kJ5qe5OB8EN4fkzBcsMLl+orsbAlq68p521VRMJFdgmA6NCNThIqKnThvOIjNxWoMvfmEq1c60d7WBY9nAqV7tqPl0jEUb9lEh8elqGCaiRACtboQp/SVuGNrhqmtARZrI6y3m1BZtQv5+Tl0WNxaFhyekRDC9lEiEYeHE6rHBU6IIPBRGixgzMqH01avvKcCGZnVXs80kqml2KJk/siH514MZyteHExF+z8AAAD//0QWUH4AAAAGSURBVAMAnIFdVMIQ8jEAAAAASUVORK5CYII=) icon.
* To update the column, click the Edit ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACEAAAAhCAYAAABX5MJvAAABbElEQVR4AeyXvUoDQRSFDwFTCRYB7QWtTJFYiYUWVlpbpIs+gPY2gkZRxDK1BgwKis8g+gSCpLCR+ANml40/SEAwWTnChSVZZGd3NglhFg53f+be++2Z20zizrl3e60E+uDqTwir9oVuyLsBvk6Mjg0jTnkBeO8LwQ/dlIEQtwfPCav2hkrlAa7ryk8GitqceHm2UdguYXfnBDfXt0ogWiAI8NNsYm4+A7fVwsX5Fer1z0AucFFkiGr1Fft7ZRS2jpFOjyOXW8DK6hJSqRHWD6RIEAQ4PDiD43yg0fhGsXiJmdkpZLITgZrLotAQXgAWSyaHkM8vKjnAPCoUhB/A2vqysgMEoJQhdAMoQzw9WpAZYDK3IIoDrEEpOWHb739DyERdAKylBMEESicA6ylBZKcnUT7dxFFpI/QQsmm7lCDak3U9Gwhx0jhhnBAHJPrORNyHH2kusQMizkOPt7YAMHZA8GUs+qeogRBzfgEAAP//G/59rQAAAAZJREFUAwDHaXYsUUP/7QAAAABJRU5ErkJggg==) icon.
* To delete the column, click the Delete ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACEAAAAiCAYAAADRcLDBAAABP0lEQVR4AeyXu2oCQRSG/90kVkJCCG5AYpv0eQMfIV0ISUiTFJYpEkJAZHVtxULBSgSxsNFXsLNXC5sVLbyAnY3ijRUO7LgWO+J4gVn4OTvDnDnf/mebo9aGzcWhpeIIHglBTWCcGPRH2IeoOEUGwtr0aV6IlFVjXQ6I9QP7WEsIcvl0nZhN56jXTVSrjZU67QF91FaRywnT7OLj3cDbqw4jmkMyUVzp9yeNl+cIdD2L8XjCDcIFEbjTEIt/IWp8blQo9ASP50IsxNm5inKpgv+/zEa1zB4URRELwX27ywSudri8k/uYhCDLpBNbO3H/EKBcJl5eeaHdXjN7bhfc7QgGH5EvhB1Kpb/h99+4rcuc44Zgsne0kBBkpHRCOkEOUHT8E6KHHypsjwyEyKHHZxuq7ADWOwNhbRxCEoJcXwIAAP//vsswrgAAAAZJREFUAwC3+lIu2s/ZUgAAAABJRU5ErkJggg==) icon.
{% endhint %}

5. After creating the column, click the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHMAAAAmCAYAAAD3AKSiAAAFDUlEQVR4AexZPUwcRxT+du8uihuIoOEKChqUk6PEcgdKxVElUhpTpLoi5CKhVPhElcKicIUwVYQUQgqqFNBEStyAy9BFJIqFRePCis6VZbshCne7+d7M/rF7cLd3C1rOg25vd2bem/fe9817M9zarvkbGgRsmL+hQcCQOTRUAobMYSaz5QALP7Tw3rdnsJfMlTcMhBfhR3iKr8NEZn75Ywu//e2ik3Bc2bSvHwHhRfgRnuLWE2T+8qeLf8/iYqadJwSEH+Ep7lOCTGE+LmTa+UOgE08JMvPn9jvpUV9BGzL7gi2fSobMfPLSl1eGzL5gy6eSITOfvPTllSEzNWwFPN0sYiu13tUrZE9mrQhnsxRcT2tXFYSN/UehnajNV8vZh5U+CpL+qIhGesW+NbKNulrEqxlgO/gZkL8NzpRwNYQ6mL/v/dy46+L1qYsVz+7YBu32DcnNVcyWTMHhFHgmd3W1cZsA396RRiyTHhTYydXLLN6v8tH7NJZL0Jl1Xl73eUI93GSeIFuDDBF7RezThj+2X43aCcvn1gMuwmUuTvqnZJW/HQzHKpGKRRb1po3KLQtr1Fd9fKcRrSRp4+lgOdGVLZkHLey90QEIAOcyskZTv3qZtNTGk1GCWCXZhy7ufswx5VoBX0272GNmbRG88pEvf4a9ERLRa8kmwGsjTvii4AhY43zKBCzcRVuNrZwAcwtcVJ5f2y8t3IuU6Mok8JCLUX5s34bdocIwhnFXzSUyNmOZ+5TzEYexoFqcYf4AGCge7XjXbx/FroK9CtRXfQIcgCXW8Q8LOy7KC/4eV8DcLW9G9jenbX2gqFmovHRRJ3BTo0BF6WudxQmgPN6bu41xC5iwg33bmWF71PL2L71YxPr6X7o8PybY0n72Vr7D6/iohXWvWX/uojJFory2vjl4TF8dZp+6xI4eiH3bGCSe2GQXNntD50L1ywaYdVzVstpnmVENrvjyic4IWzKT5Vhrt/E7M0JktqYsHD9vs9tCmWQ/2fUXhr73uhd+OAK8DmxpXft+SAwNZPTRlSQ4IzAzO088WDyd50z2Zkqm3qfCfQcoYJYZ1fwHEIBD8zo4v61XfRGzoy5+2pFeIRiR8itlinsYF4WMdrtkvg8mbTR8wVoRTlBm/c7u97ASsJze8RdaRK/KOCJNVREi7fBxsHjCeS5/ypTM9Q1mwSGw6JcdHgJwqPeM+qqD5nTBK30WmrJffe4d3VlqjycIzAsnLGurbfwx6cuXcO8tM10RfXlAanSnhZUX4d7t3AFWOJ8aS/MV2Oe28MaBPsi5aJ5aWJRDFffGhyd89uL9Di6OWd7VWeGAcpEDUJ32+46nR58zJVPZJJDqMMASK3cNgIyQDK/PXmphXogPSp8eO19GI/96UO/8mMwXuQjqWDCX7lcLi3riQ1hixU6Le7KWQUxPdKJ2mpEDmE0ytJbnl2dPdJQN2hrbaEVO72KLi5v9cgACPD22RT5qR887+Hf2ZA7uk5mhTwQMmRcAV+epPKwqFwjlrNuQmTNCBnHHkJkGvZzLGjJzTlAa9wyZadDKuawhM+cEpXHPkJkGrZzLGjJzTlAa9xJkFhM9aaYzsteFQCeeEtR98YmF90vX5ZKx0w8Cwo/wFNdNkPnz10V89pGFTszHlU37+hEQXoQf4SluPUGmCO9+U8R/3+uXwuqlq/dWYJieb2oswovwIzx1JTMuYNo3B4FEZt4c142ncQT+BwAA///RSaLgAAAABklEQVQDAI+9Bcwhe9qeAAAAAElFTkSuQmCC) button in the **Template Details** column.&#x20;

&#x20;      The Template Saved message box is displayed.

6. On the **Template Saved** message box, click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (1572).png" alt=""><figcaption><p>Template Saved Message Box</p></figcaption></figure>

The template is created and displayed on the FBDI Template List page.&#x20;

<figure><img src="../../../.gitbook/assets/image (1573).png" alt=""><figcaption><p>FBDI Templates List Page</p></figcaption></figure>

{% hint style="info" %}
**Tip:**&#x20;

* To view the template details, click the View ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAeCAYAAADQBxWhAAACN0lEQVR4AeyWXUgUURTHfzOZrpZaQWUkBUlUZBT0sBIEthgSWxJFtZRJvRhoH1JsgZFsVpgUu/RBZNRGJdkXhERkQT35UJAJWrKFBT70uWjbpu4auNvOhY0xcWdcHH3QYc6Zc8+99/zu/V8Yruz3+8OjbTJj8IxT6OdvPowy9SkOknduxjRG2tRAJR4EVZJG2wTUUIWHJW9vIMjd+ucU7TvB2m1lrN9pp6ziHC+b3hEKhXUvVDe0+e0HCvdWcqW2HpMpkYN7bNg25vGp4wtHT9dw5OQlunx+XWBdUE97B46z1/jl78aat4ozx0pJSU5i2ZIsLlfbyZwzizet76k6f4ue3qAmWBMaCPaJ3XX3BEhKnMw6Sw437zdQ6bzOIceFyM/ES/4aswAp4EfPGkUcy2lCg31/+On7LWpIkkR/f4ivPzpFOxwO893bhRzJi0TEeTt9KPlIOOSrCZ2enspumxVZllEW0Or5SMmuTaxYupDN1lxyVmbzqrlNABSZtxZYkCRJtIdymlBl4mrzcooLC5QQd91jXjS+5nDpDvJzzThr7tDS1k562lTKDxQxe+YMMS6W0wWVJIktGyy4XeVkL17AjXtP2F7ioNheTVOLR+y49mIFi7LmxWL969MFjY6en5mB6/h+nta5eHD1FA/dVTTcdgq5U5JN0WGa32FBo9USEiahnHVa6hTN84vOUX/jgqoLxBNPQONRTfeccSyvEbfB/3UfIO9I3wLV9dTgAVB1h5HxmED/AgAA//+52la7AAAABklEQVQDAHGxhm3/pxqYAAAAAElFTkSuQmCC) icon.
* To update the template, click the Edit ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAeCAYAAADQBxWhAAABR0lEQVR4AeyWTUsCURSGX+cHZNIm6Nf0sYxmE9UiWrbrB7QM+gHRJmgRfZJhREGURBHRQl2J4MqF4ELxA0VHl8p4z4B6/Rg46r260GHe4XDnnvPMeQ8D17Asy560DEzhmlFoOluGLslT7LN3ZXkRqiUDKe6D0qJuzaFsh+v1Bvyv3/gLRWHbNitvbHuj8QSu/O84PbvBfySmF0od3j0HkUxlcHx0AI8HyBVK+qAEfHj5wvXTBy7v35DNF/F4cYLtzVU90BbwNvDZAYgufd4F0a0IOquu0VAzHQQ83DexZ27AMHhA+hI21A24s7XG7pCAJBZUJZANrVRrCP6Gab8jsnSUDp1k8WB1Kva173GBVIgFXfJ5nV/iJ3COXXN96BkSSBYLKieoiOdQFS661phhe3WcBnt97rJX9SlQrieDu6DyC53xVKBNAAAA//+tzOX9AAAABklEQVQDADDcUG1LYh8qAAAAAElFTkSuQmCC) icon.
* To delete the column, click the Delete ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAgCAYAAADud3N8AAABSUlEQVR4AeyWP0gCURzHv7iUWYQREdGfIWhqa6ixqTEampyCHII2g+DGoFqiIYImW4tawiAIa4gWcXJwcxUVUU5FRQX/cYfDO3/I/U58KNw9+N49fve934f3fW94rs4YhgtjGDaFJtMqZEncRRLv2soCRi0RqM0JVCvKlgMlCbfbHRRKZaQyOVzdB3F0coljv4K30C/yahGVao38M6jAjrdUrkC5ecK5codYPKH3azZbeP0Iwx+4xfPLp17jPNhQ7/wcLs582NvZJjrY38Wp75DD0z1sqObO5lSEvv+Jwn9R1BsNzcKSJSirI8PkQBkhDW+Z/HiXFr2Y9bjJEjdWl+GZoXVi7BUsrXRrcx0/74+IfAUNergOwD091Wtp/rIENW/HczhQXk5Dumwcr4zbYP8uGOId9S1Q7CeCDVDxg8y5jaAyDo5Zzy4AAAD//wrpwoQAAAAGSURBVAMAI+SRl6w/rn4AAAAASUVORK5CYII=) icon.
{% endhint %}

</details>


{% endtab %}

{% tab title="2. Set up FBDI Job Configuration" %}
**Overview**

Setting up the FBDI Job Configuration functionality enables you to define and prepare jobs for processing data using the FBDI framework. It allows you to specify required parameters such as data sources, file formats, and mapping details to ensure accurate data handling. This setup ensures that data is properly structured and ready for seamless integration into the target system.

**Procedure**

In the SCIKIQ application, setting up the FBDI Job Configuration involves a series of steps, including **selecting the template and connection, adding tables, defining relationships between tables, mapping fields, validating the configuration,** and finally **executing the job**.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Select Template and Connection</strong></summary>

**Overview**

Selecting the Template and Connection during FBDI job configuration defines what data to process and from where to retrieve it. The template provides the predefined structure, fields, and format required for the data, ensuring it aligns with Oracle Fusion’s import requirements.

The Connection specifies the source system (such as Oracle EBS) from which the data will be extracted. Together, they ensure that the right data is selected, structured correctly, and ready for seamless processing and import.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, expand **Scikiq Migration Hub** under **SCIKIQ CONNECT**, and then click **FBDI Configuration**.

<figure><img src="../../../.gitbook/assets/image (1574).png" alt=""><figcaption><p>FBDI Configuration Menu Item</p></figcaption></figure>

&#x20;     The FBDI Job Configuration page is displayed.

2. On the **FBDI Job Configuration page** :

* From the **FBDI Template** drop-down box, select the required **template.**

{% hint style="info" %}
**Tip:** Based on the requirement, you can either select an existing template or create a new one.
{% endhint %}

* From the **Select Connection** drop-down box, select the **connection**.&#x20;

<figure><img src="../../../.gitbook/assets/image (1575).png" alt=""><figcaption><p>FBDI Job Configuration - Selecting Template and Connection</p></figcaption></figure>

</details>

<details>

<summary><strong>2.Add Tables</strong></summary>

**Overview**

Adding tables during FBDI job configuration defines which data needs to be processed and migrated. It ensures that all required entities (such as headers and related details) are included in the job. This helps in organizing the data flow and supports proper mapping and relationships between tables. Overall, it ensures complete and accurate data is prepared for successful import into the target system.

**Procedure**

1. **If you want to get table suggestions from AI**

* Click the **Get AI Table Suggestions** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEEAAAAxCAYAAACF1cSEAAADLklEQVR4AeyXS2gTQRjH/7tpfEEUevAiVEUEwYuopVbB0pMIgnjwcVBLPPhGDx6kFwURYg8WH3jxVq1UPBjEk8WDR4P4QA+WXpTS+LjESqxEzO4436abdDeziVuzYzKdMN9O9psvs/P/5dvZb80f0wU2382E/kBD4ElQBWEoY2DdJQOJc6YyRnpIF9crbB4IFNj/yED2uyEMblUn6SFdpE+kwQMh9QTI/xKFtb6PdJE+kRIPBCImClLFF6TPA0EVsWF1aAicmIagIXACvOlMkAVh2xoDGzsqtUfnSgNbVlfO+TrKLUxs+Uf/+EVKJixPGBhOxnD7YAyjZ9twY38MuZ/ilYeJFc8Q3isFQvqNjcxHhiNbTXTzDBh5YWP8KxOuNkyscII5OKVAoHW1L6EjEI8BHe3iW6EUAdSLdeMa1ZuNmqjWPCd7TCxdbCA5ZOHiYwudq4L3hDCxta4ZZkwKhKdjDL2DRdzN2BgYtbHrVhGTU6VlpvbE8Hkgjuv7eIpwV61YPhxJkwLBf//nC8DkN4YrHMCJ7SayUwx93SZuHohV7RVubCTqZyaVAmHmWp6OABznAB68tLE5VQT1h7pMDO4tZYQnOOKT/wKBAJzpNZH5wHB02HIkpl/byE0zbJpVTzgDEg7SIbgAFsWBnrWGUzvsXG/gGt8TKPXPPyxBkaC9fAmpEGYDoBUsaAMO81vgTrINhd/AsXsWnvPsoDGZJg2CH4ArkkB84hujC0DZsjkIAIF4l2WeDFCybA4DgKCkQ5TYFN8Ii/R2CAvAFaRM2TxXAMqUzSSEjB6D7r/r9v49wPW7vTJl86sJholc9atyPQAEIqjEprGoLJI9gZ71p+9beP+lAuJvAEQlst68kUCgiz4bZzg1YuFtloEyw60DaKzZLDIIJJRAbLhcdF6QKDvI14wWKYRmFCxak4bAqWgIGgInwJvOBA2BE+BNZ4KGwAnwpjPBD2HFskqtz8eUa0H6PJnQvwNILFROuyOIdJE+58R38EDo62JI7WYIIub7bcuckh7SRfpEi/ZAoAAKHLvAkL9qK2Okh3SRPpFVQRAFqe4TQlBdtF+fhgDgDwAAAP//Fj0lKQAAAAZJREFUAwDjGeJhN6Ld5wAAAABJRU5ErkJggg==)button to get the relevant table suggestions.

&#x20;     AI analyzes the template and displays the relevant tables.

2. **If you want to add tables manually**

* Select the **tables** from the S**elect Source Tables** drop-down box.

&#x20;      Once done, the selected tables are displayed as a list.

3. From the **list of tables**, select the **applicable tables** by clicking the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAhCAYAAACBQRgKAAADA0lEQVR4AeyXSWgTURjH/7PRCNVU0KLSenCtFy9F1AgVl4oXT4IguIF4KFS0oIWAKJ4KKlRB8CCK20noQQQR3FAwIlK04sGliqhViBQMClIyk+f83/AQMzMlS2ObSUK+vDff8vL93ve9ZEYXNfrSUaOvOnitFT6w4oOfBNb122jozkLvqj5h3syfHGEF9YHTOXHCxsO3AlknLGxq65k38ycHeYKy9YEfGnCqFjgfkBtAnnw9r33gqfeC+shIGI8PnLsUGWoXJIzHB+761sS7Dl5umXs36aAUss7OlToy/ZYUzsNiXh01ceeA6TMf32IgfdLCeLG+oDzFhFW8c5kOSt76gZcdizWM2ZDCeaBThZUTBl5MnqsXaBj6IpD+KcC5il2/VMPnPhO5c5YcY5ayAOd3GFJP24Y27a+hxFlZ4F0dOp4lTbw4YmJ5iyaFc+poC8qJ7dk6U8PHUYEnHwQ4p46+yc0GB2w8beNiSqClyQOkfVu7jguPc/JOsmka0OA/ATK20I+ywL9mgJcjQlZv9JcAhZWkjragJFRrP3onQGHLL2r2AOfGgcxv4P4bgWM3HQx/F3IJZVdrDjwX8phIY4kfZYHfGMph7xUHuy85GPkBKZxTR1tATrK1p8eAy3sMKbMagYTb+kG+ldSVBV5sYmxZtrZqWT4A3Xst0DYH4Pn+5nZQ3G1jzimc8zuG017l57kdwWuOk9rqTEJJ5xkbFHUdNO5a5e0zW1zZU+45n92oYfsKHX23vaeiuwdN3Oo2MSPmHYGrT3O4Puh21xpd/sDxvPOIqDVKGb1MSoksIYYbE+/JgiAqnGc5tj+LfdccebZbk7b8AaOOvoyhL+3sEAr1zYf/XYc+xch/BS8msUr71sErvcNTbf16xVVFLEPNojGG8fgqnljo/YVEA9u9OQrh8YGf2mogbJeqbTPIQZ6gvH3g7fM1pHpNrF2iVe0GEJj5k4M8BYHTic4PekyMnbXknRIfBatJmDfzJwd5gsRX8SCnKOrq4FGs6nhMUa94KPsfAAAA///iO/18AAAABklEQVQDABwCemlOlx+nAAAAAElFTkSuQmCC) button corresponding to each of them.
4. If you want to **add all the tables**, then click the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGMAAAAjCAYAAACAY7T5AAAFe0lEQVR4AeyYf0yVVRjHH4n4JZBC7vLDVqLYICJXA10iskbNtia6hkQrprVKlmusZW2Ya43FKvtHq2mZ1qy1WFvaXzXkD3+QmY7SEizR3EIEYkAhyOVG2Ps58bL7vlwuXe4P7uywPfc95znPec453+/zPOfljRgYdF7TEh4YRIj+CxsENBlhQ4WIJkOTEUYIhNFWJmTG0N8uqW7dJ9nHnpX5RzZoCSAGYAq2YOwpBixkYHT/91ulrqtR+keuerLXOj8QAFOwBWOwtruykFHz62fSMdwnw6N/2e10P0AIgC0Yg7XdpYWMA93faSLsCAWhDyFgbXdtIYM0shvofnAQ8IS1hYzgLOvFqx6yIKDJsMAxsx1Nhh/4Hy/YJgguqjNLpa14r/CkPx0JOBkvLXpY3sreoPbC8+XMdapt/ylLW6E2zwFo28dD1QfMA3nVXpfDpm/Vp7Ij52mvdv4OBpQMiKi89UFJjIyT7TlPybq0Apk1a5bHPZanr1D6qIhIWZ6Updqh/ilMvsPYa6zXZYn09JhkGRhxSv6cTK+2/g4GjAyTiK9+b5KhUZesTVkmu3+rl5pzdRP2CAiLZ6dJ05/n5eLVrgmHJFPIGKIRMSOSeS1F7wg6xD2iaaNDmIsPFkZ//r73BGGs64F9qpTga9edlZIakyQrk3PGyw1z3AUCrhj/ANd3/yCQYvp1twlUe1pkPJ9RIsXzlkh8ZIxQhh5y5Mnj84sEIlzXRrwSwcYLkrIlwcieE3+0CuJ+SEB6ZXGZImru14/Ktgv7lT8i9M2s9caXgSFBv/HHnXLPTYtU6YAsyC05+Zoag2R84Iv1EiJjZW9bgxqD/MfSV6KWjT/tlA5nrxzuOSPLGjcrnfsP8/F7bvCy1HefUkPBzGKfybgrcYGUpi2X17MqpDytUMrTC6UqY7U8efpt+S9EcCIz2hp7W+Sb3rOoDD//li13ohiobf1cbml4Qi4MdqrIhDz0dZePKv1zZ95XmUWEf5m3RWUNkQ7ZqdFJmEqPq19Yiw7z3cfQTSbue2G9dmePFN+cK5A02Rx/9D6Tcbr/oqw/tV2cxgfFZ25bZUTuF5ISPUd2526SEsfSSUuTuUkOQrSZ4O3KrVQZho4x087X5y8D7SryyRoEAgHQVz/u9gRNvJH9mxeuVSTfHp8uyVGJAknudoFq+0wGC3NwMmFgZEiWJGZIVfMecRr3xJ62gx7vCOaYwkESjBJF+QE05ONLh8YPSQRTowGCOZQn7oCFs1OEyDT11G70lCiifUGcQ7BlDjruCtoI66WOZQnz8d8x3MvQpEJgECCUMPaIUBpdoyMqEyed6MfAtMhgPQgpOrZFqpo/kAajnuYffWFKIjgg9RowAB0/CKWKQ6525MuRnmZ51bj0uQ+4cInK/Z3HhXL14tmP1NsPejKKu4EyhXzb97NgyxgvDz2uK5ZyssN4u2MM0j5pP8w6SvqNgKKs8frKXkzhXiQLThj3mqkj0wgI9kYwdBofVckWiKeMYsfbJGO0fZVpk+HrQtgDdPahTYLQRodwSMqKeYmafaIRAWzsmMNcdMiak7WoldBGh+CLzMWeQcgvbXpDlTFHfYUiFj3CmszhSd8U/NltGcMO/+wRG+bypI8eoY2trxJSMnzd3P/N/rong6glm8wsCWeCr3sywhl8+940GXZEZrCvyZhB8O1LW8jgA5/dQPeDg4AnrC1krJm3VKIjbgzO6trrOAJgDNbjirGGhYytGY9IavRcTcgYOMF4QAQYg7Xdv4WM2Bui5ODdNVLmKDD+042z2+q+nwhQmsAWjGMNrO3uLGQwCCG1mRXScu+7cqnwQy0BxABMwRaMwdouE8iwG+h+6BDQZIQO6ylX0mRMCVHoDP4BAAD//8fYcXsAAAAGSURBVAMA+vG2I/tH/AYAAAAASUVORK5CYII=) button.

{% hint style="info" %}
**Tip:** To view the **Data Quality Notes** of a table, click the **Expand** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABYAAAAbCAYAAAB4Kn/lAAABD0lEQVR4AeySy2rCUBRFN45K6ai0pQ/6KS2dltJRKf6d+BiI4gPEiSiIvyMiatSoEZR1ByGJuRoHTiSBDSfn7L1u7iGZ3YWejC70pGB/sekqrmkVznwp5N/JUuBBlrFCf8VoPFOx0VOu2tFwNLFlzCxf6xovmThjCOyu1vK8rZyFq3KrbwDREAdW2gNNnYXxkol6eA+B318f9ff9obvbm1h4EIoHLxlAUYXADDESIBj88nOgcA7ANKPwQr2rUrNnrs+BHIwHr02xYMwEAQBabzy5q41ZET1meI7JCiYEABBwRE2P2SkdBRMG9P/zqezvl6jpJdFJMJC35we9PN1TJlYicGJawJiC/WWkq/BXsQcAAP//khW0zQAAAAZJREFUAwDJys/fexHdsAAAAABJRU5ErkJggg==) button corresponding to it.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1576).png" alt=""><figcaption><p>FBDI Job Configuration - Adding Tables</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * To **add all the AI suggested tables,** click the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGMAAAAjCAYAAACAY7T5AAAFe0lEQVR4AeyYf0yVVRjHH4n4JZBC7vLDVqLYICJXA10iskbNtia6hkQrprVKlmusZW2Ya43FKvtHq2mZ1qy1WFvaXzXkD3+QmY7SEizR3EIEYkAhyOVG2Ps58bL7vlwuXe4P7uywPfc95znPec453+/zPOfljRgYdF7TEh4YRIj+CxsENBlhQ4WIJkOTEUYIhNFWJmTG0N8uqW7dJ9nHnpX5RzZoCSAGYAq2YOwpBixkYHT/91ulrqtR+keuerLXOj8QAFOwBWOwtruykFHz62fSMdwnw6N/2e10P0AIgC0Yg7XdpYWMA93faSLsCAWhDyFgbXdtIYM0shvofnAQ8IS1hYzgLOvFqx6yIKDJsMAxsx1Nhh/4Hy/YJgguqjNLpa14r/CkPx0JOBkvLXpY3sreoPbC8+XMdapt/ylLW6E2zwFo28dD1QfMA3nVXpfDpm/Vp7Ij52mvdv4OBpQMiKi89UFJjIyT7TlPybq0Apk1a5bHPZanr1D6qIhIWZ6Updqh/ilMvsPYa6zXZYn09JhkGRhxSv6cTK+2/g4GjAyTiK9+b5KhUZesTVkmu3+rl5pzdRP2CAiLZ6dJ05/n5eLVrgmHJFPIGKIRMSOSeS1F7wg6xD2iaaNDmIsPFkZ//r73BGGs64F9qpTga9edlZIakyQrk3PGyw1z3AUCrhj/ANd3/yCQYvp1twlUe1pkPJ9RIsXzlkh8ZIxQhh5y5Mnj84sEIlzXRrwSwcYLkrIlwcieE3+0CuJ+SEB6ZXGZImru14/Ktgv7lT8i9M2s9caXgSFBv/HHnXLPTYtU6YAsyC05+Zoag2R84Iv1EiJjZW9bgxqD/MfSV6KWjT/tlA5nrxzuOSPLGjcrnfsP8/F7bvCy1HefUkPBzGKfybgrcYGUpi2X17MqpDytUMrTC6UqY7U8efpt+S9EcCIz2hp7W+Sb3rOoDD//li13ohiobf1cbml4Qi4MdqrIhDz0dZePKv1zZ95XmUWEf5m3RWUNkQ7ZqdFJmEqPq19Yiw7z3cfQTSbue2G9dmePFN+cK5A02Rx/9D6Tcbr/oqw/tV2cxgfFZ25bZUTuF5ISPUd2526SEsfSSUuTuUkOQrSZ4O3KrVQZho4x087X5y8D7SryyRoEAgHQVz/u9gRNvJH9mxeuVSTfHp8uyVGJAknudoFq+0wGC3NwMmFgZEiWJGZIVfMecRr3xJ62gx7vCOaYwkESjBJF+QE05ONLh8YPSQRTowGCOZQn7oCFs1OEyDT11G70lCiifUGcQ7BlDjruCtoI66WOZQnz8d8x3MvQpEJgECCUMPaIUBpdoyMqEyed6MfAtMhgPQgpOrZFqpo/kAajnuYffWFKIjgg9RowAB0/CKWKQ6525MuRnmZ51bj0uQ+4cInK/Z3HhXL14tmP1NsPejKKu4EyhXzb97NgyxgvDz2uK5ZyssN4u2MM0j5pP8w6SvqNgKKs8frKXkzhXiQLThj3mqkj0wgI9kYwdBofVckWiKeMYsfbJGO0fZVpk+HrQtgDdPahTYLQRodwSMqKeYmafaIRAWzsmMNcdMiak7WoldBGh+CLzMWeQcgvbXpDlTFHfYUiFj3CmszhSd8U/NltGcMO/+wRG+bypI8eoY2trxJSMnzd3P/N/rong6glm8wsCWeCr3sywhl8+940GXZEZrCvyZhB8O1LW8jgA5/dQPeDg4AnrC1krJm3VKIjbgzO6trrOAJgDNbjirGGhYytGY9IavRcTcgYOMF4QAQYg7Xdv4WM2Bui5ODdNVLmKDD+042z2+q+nwhQmsAWjGMNrO3uLGQwCCG1mRXScu+7cqnwQy0BxABMwRaMwdouE8iwG+h+6BDQZIQO6ylX0mRMCVHoDP4BAAD//8fYcXsAAAAGSURBVAMA+vG2I/tH/AYAAAAASUVORK5CYII=) button.&#x20;
> * To **remove all the AI suggested tables** from the FBDI Job Configuration page, click the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFYAAAAiCAYAAADF5S4gAAAEZklEQVR4AeyaW2wUVRiAfzettlakRYsFscS0CGq4lCoYEmu9gEVNFYPRhKiJRhJNJNEHX3z2xQdIeIAEwguEBBJCgQdYIIFSknLthRIupS2Eck+5BgqFNpT5TnI2PWc7w+wOy/U0/XfOfzln5nzzzz9nZjd2o7un38mDZxAT95cRAg5sRrCKOLAPC2xvX59srWuShcs2yH8LVzvxYQAfOMFrsHNjZCxBK9Zsk34v8sfZn8i/87534sMAPnCCF9w8ZMa/Aba2/qCMGlkoMyrKpGDoS0agU0wC8IETvOBmeq0ae6TtlLw/cYwd4/QAAvCCmx1iZOz17lsuU21C99HJXLjZYQZY2+n09Ak4sOmzC+z5WIJtONgu/y9aIx0nzwUefFgn4zAe44btM1hcKrZIYK9euyEra2rl7IXLxj73NLVKTXyX3L3bb9i1Eq9tSFofY9P+p2EbCWy+tyQrGV0kazfVJ+Dubjwq+w60ydSysRKLPefLqPCVofL33FlqnfzD1xXScviEaLjl40vlnz9mS8noEb79U3EwDuMxbir9osRGAsuOP5g8Tt6bUKrgbt7RKPtb2uXbmdNk5GvDcIcSJj7hnTel80yX3Oq5o0rAgqXr1BZ9ycp4IsNpY2NgrhZ0YnlKROdyp43EvSuDuMtXrwsx+NCx40coEZSKIDu+VCUyWHY4ZdJYKSkukgNe1k3/cFJKUOmvpftmjwf2tlbV9nBbp2D//acvVHYXFRbI8c7zyscHvp+/+1TI+jPnLsrR9tMqrtw72awvgUqcFnTsVR+Xq7gvP5sih1o7xc+u+6W6fSBg9za3Soc32Yle1m3d2ZwoC6kezGDx+S/nSW9vnyxevlHV8+oZU+Xdt4oTocNfzZdh+UPU+js7O0vGlY5SPkqNalgfuTkvSN6LORLf3qCyeMTwAmHMXB+71T20Ggsd6RNITdWX/+cfTU6UBfuG5tPdMDNhJjjQSJmgPuqM5PLVl/TAuLDt3JznZe6cKlXf2Z8+YX72sOPacZHAsiroOHneqKnUXB7zGr0lk9+qwD4Iahw3r+LXC4UJDvTj217fIgD+85dq8cvEgX2C2tTnDVv2qBAAUzJQ/Oz40pFIYFkVzJlVmVRTWRF85dWuoFVB16VrMn9JjboprVpfJ9y8qirLk+ZA/dvXfEzFEU+WRbm7U585WYxF9lNvZ3r11s+edEAhDZHAhtxHUhgA7VeS2HQg2fnXb9+oLKX+UQp0PCdSx9FG0Kmz9NHQ2aJjR2hjoz7T1uPRxu9nZ+x05JGATedAn7Q+DmyGztgzDzZDXN2XiQ5spghkaFyjFAzJy5Ur3hurDO3rqRwWXnCzJ2eAfXvMG+rNlB3kdH8CvMmDmx1hgK2cNl5On+2SLXVNLnNtUpZOpsIJXnCz3ObNKzsrS/i+nLeofF/Ok4mTwX+0Ah84wQtugWBxEjS9okzm/VqtXqvpJxS3NX+8Ah84wQtuthilwHY6PX0CDmz67AJ7OrCBeNJ33gMAAP//N7JRtwAAAAZJREFUAwCV5NDB/0w1vQAAAABJRU5ErkJggg==)button.&#x20;
> * To **retry for the AI suggested tables**, click the ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEoAAAAkCAYAAAAuLqxbAAAEwUlEQVR4AeyaeUwUVxzHv67LsS5UPFAOhVbEYitpK6VtaINYW8SaHhixRtMrtjZtrEk1MTH+bUz8Q40STTziFU0UvC/wxItoDBqvuApoEPDCA5SFxUXxfV8y47rsuMOsGrPMZt/Mzu/93rz5fub73jwyWBqdrjaz+GdggfnRRcAEpQsTYIIyAsrd2op9R85g4YrtmL1wQ6co1ErN1P4yZqqjmLi28CDaRPYvY7/GrKk/d4pCrdRM7WQg5Pv8qqBKSs+jX1w0sjM/QY/uET6TgzFIrdRM7WSgpVEFdam8GukfJWvlBX2c2slAS6gK6pGzuVM5yRsInUUG3nHlWAWlBMy9bwImKN9c2kUDAnXBUYVFK3fIZcSc/AKsEU/NunsN7ToJhoBhUMUlp3H45AWMHpGOmVPGYfrfuRiQGIN1W0pQfu2GJpuikjIJ1nOdxjaaDTwqKqtuIn/VTtyvf+QRfTM/DYG6XFkLXnTe6C8xICEGFksXhIZY8VX6B8j4dDAOlZ6Ds8mlqSC6V3dMm5wr12n//Pod7tytR9n5Cs18paL+oRNud6ty2MF9YOkWI80dldWge/r0jmrXPDXlXVi7WnC9tq5dna+ALTwM9m7hUIZss+sxlq4rUl2nuI0giw6Voam5BcvXF8sbxZs1f9lWrNq4H3MXF6JYuJV7xtkXncd6upjHgRSLkcaNThfoCu+2TiHCUVENd+sTXK6sEaUWT5+2eae9cNzsapHuU863eU8pEuKjpdvoOjqTQtNSByJneBq62cLw54SRSEqMBT90WEyfHpjx71hkfpGKKLFYVob+terbTMFnHw+S+0A2hkBF2J87wLNzuxARYbfhYWOTdEhc355yWHrm8DfdM2/pFumaJWt2g84kCDpADsNzFbKOOcy990B7TgoRQz75vTieFrbwUAmZbqYzHRU1GJzcHz2jImV9IBtDoFKS+uNq1S05t3h3zoueND4bE8YMR2SEzbtaHtM9dMv4HzMRYu2KlIH9ZFzZ0Dmef2tOzM1Sqvzu6R668MRpBx40NILX47eRjgRDoN5PipfWL9h1HLxrHF68gweOncXqggNyeNBd/vrn8ImP7Y0y4SC2552nu5Rjti/cdUzOR/ytpyjnuHjlunzAxPXtpaeZ3xxDoHjWkVlDMezzIdh39Azm5G/EguXbUHPzLrKHDUV4WChTdJVRYt6hA9ZuOgjCGjMqQ7bjsOMSgvOhq8UtY1Hv2OVTT5nMZdDHhg5tEE9IznUcjj5SOhwyDIo9DUlJxH9/fC8n3plT8vBb3gjEiomVdVolJysNkyfmyPkE4kMH/P/XT2qMwlivDL3fx32DDwcliExIF3PSZqEbWdiWe5ngseGkz2HoEQroZ0CgAur5NTXmE5LLCA5h3oRX1U3QgcoRjqUbO/IA0AMz6EDpEW0kxwSlk5oJqqOgIu02uUDT2S7o0rg4JQMtYaqjuNQ/dbZcK++tiL/Oi6B2MtDqQwWVlZGKmht12Cve65GuVoNgi1MrNVM7GWjpU0GFWK3gO64uIpPvuLgq7gyFWqmZ2slAyPf5VUGxlonfivd6Uyf9IFfbXI8Ee6FWaqZ2MtAqL4DSSjLjMP9JQ68JTEfpJGWCMkHpJKAz7RkAAAD//0L83W0AAAAGSURBVAMAQpkwRaxN+0sAAAAASUVORK5CYII=) button.

</details>

<details>

<summary><strong>3.Define Relationships</strong></summary>

**Overview**

Defining relationships between tables during FBDI job configuration ensures that related data is correctly linked and processed together. It helps maintain the correct order of data loading, especially for parent-child records.&#x20;

This prevents errors and preserves data integrity during the import process. Overall, it ensures that the data is accurate, consistent, and properly structured in the target system.

**Procedure**&#x20;

1. After adding the tables, click the **Relationships** button on the top right side of the **FBDI Job Configuration** page.

<figure><img src="../../../.gitbook/assets/image (1577).png" alt=""><figcaption><p>FBDI Job Configuration Page - Relationships Button</p></figcaption></figure>

The Define Relationships screen is displayed.

2. On the **Define Relationships** screen, do any one of the below:

* To get relationship suggestions **automatically**, click the **Suggest Relationships** button.
* To define relationships **manually**, click the **Add Join Condition** button.

<figure><img src="../../../.gitbook/assets/image (1578).png" alt=""><figcaption><p>Define Table Relationships</p></figcaption></figure>

Once done, the table relationships are displayed. See the below example image.

<figure><img src="../../../.gitbook/assets/image (1579).png" alt=""><figcaption><p>Table Relationships</p></figcaption></figure>

3. Next, on the **Define Table Relationships** screen, do any one of the below:

* Click the **Accept All** button to accept all the tables.
* Click the **Add button** corresponding to each table to accept individually.

&#x20;      Once done, the relationships are added and success messages are displayed.

<figure><img src="../../../.gitbook/assets/image (1580).png" alt=""><figcaption><p>Define Table Relationships Screen</p></figcaption></figure>

4. Verify all the **Join Conditions** by scrolling through the **Define Table Relationships**, and manually specify if anything is missed out and if there are any mismatches.&#x20;
5. Finally, click the **Save Joins** button.

<figure><img src="../../../.gitbook/assets/image (1581).png" alt="" width="563"><figcaption><p>Define Table Relationships Screen -  Save Joins Button</p></figcaption></figure>

&#x20;       The Join Conditions are saved successfully.

{% hint style="info" %}
**Tip:** You can view the **SQL Query** at the bottom of the **Define Table Relationships** screen.
{% endhint %}

</details>

<details>

<summary><strong>4.Map Fields</strong></summary>

**Overview**

The purpose of mapping fields during FBDI job configuration is to ensure that data from the source system is correctly aligned with the corresponding fields in the target system. It defines how each source column is transformed and placed into the required FBDI template structure.

This step helps maintain data accuracy, consistency, and proper formatting during the import process. It also prevents errors by ensuring that all mandatory and relevant fields are correctly populated. Overall, field mapping ensures that the data is correctly interpreted and successfully loaded into the target system.

**Procedure**&#x20;

You can **map the fields either manually or by using Auto Map** functionality. The below step-by-step instructions describe the process:

1. **To map the fields manually**

* On the  **FBDI Job Configuration** page, from the **Source Fields** drop-down box, select the **source field** corresponding to each target field.

> <mark style="color:red;">**Note:**</mark> Make sure that the selected fields are **Not Nullable**.

2. **To map the fields using Auto Map functionality**

* On the  **FBDI Job Configuration** page, click the ![](<../../../.gitbook/assets/unknown (42).png>)button.

<figure><img src="../../../.gitbook/assets/image (1582).png" alt=""><figcaption><p>FBDI Job Configuration Page - Mapping Fields</p></figcaption></figure>

&#x20;     Once done, the **SCIKIQ Alert** message box is displayed.

* On the **SCIKIQ Alert** message box, **review** the message, and then click the **Yes** button.

<figure><img src="../../../.gitbook/assets/image (1583).png" alt=""><figcaption><p>SCIKIQ Alert Message Box</p></figcaption></figure>

&#x20;     Once done, the **Auto Mapping Results** message box is displayed.

* On the **Auto Mapping Results** screen, click the **Continue with Mapping** button.

<figure><img src="../../../.gitbook/assets/image (1584).png" alt=""><figcaption><p>Auto Mapping Results</p></figcaption></figure>

3. **To map the fields using Custom fields**

* On the **FBDI Job Configuration** page, click the **Custom** button.

<figure><img src="../../../.gitbook/assets/image (1585).png" alt=""><figcaption><p>FBDI Job Configuration Page - Custom Button</p></figcaption></figure>

&#x20;     The Custom Calculator dialogue box is displayed.

* On the **Custom Calculator** dialogue box, enter the **Column Name, Custom Expression**, and then click the **Add** button.

<figure><img src="../../../.gitbook/assets/image (1586).png" alt=""><figcaption><p>FBDI Job Configuration Page - Custom Calculator Dialogue Box</p></figcaption></figure>

&#x20;     The **Custom field added successfully** message box is displayed.

* Next, from the **Source Field** drop-down box, select the **custom** field, which you have created, and then click the **Configuration** button.

<figure><img src="../../../.gitbook/assets/image (1587).png" alt=""><figcaption><p>FBDI Job Configuration Page - Custom Field Selection</p></figcaption></figure>

The custom field is mapped.

</details>

<details>

<summary><strong>5.Validate Configuration</strong></summary>

**Overview**

The purpose of validating the configuration during FBDI job setup is to ensure that all settings are correct and complete before execution. It checks for errors such as missing mappings, incorrect relationships, or invalid data formats.

This step helps identify and fix issues early, preventing failures during the actual data load. Overall, it ensures a smooth, accurate, and error-free execution of the FBDI job.

**Procedure**

1. On the **FBDB Job Configuration** page, click the **Validate Configuration** button.

<figure><img src="../../../.gitbook/assets/image (1588).png" alt=""><figcaption><p>Validate Configuration</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Make sure to select the Target Storage option from the **Select Target Storage** drop-down box.

2. Next, **review and rectify** the validation errors, if any, and then click the ![](<../../../.gitbook/assets/unknown (43).png>)button.

&#x20;      The **Save FBDI Job Configuration** dialogue box is displayed.

3. On the **Save FBDI Job Configuration** dialogue box:

* Enter a **name** for the configuration and provide the **description**.
* Next, click the **Validate Configuration** button.
* Once the validation is successful, click the **Save Configuration** button.

<figure><img src="../../../.gitbook/assets/image (1589).png" alt=""><figcaption><p>Save FBDI Job Configuration Dialogue Box</p></figcaption></figure>

The FBDI Job configuration is saved and displayed on the Saved FBDI Configurations page.

</details>

<details>

<summary>6<strong>.Execute Configuration</strong></summary>

**Overview**

The purpose of executing the configuration during FBDI job setup is to run the job and process the data as per the defined settings. It initiates the extraction, transformation, and loading of data into the target system.

This step applies all configurations such as mappings, relationships, and validations to perform the actual data import. Overall, it completes the process by moving the prepared data into Oracle Fusion successfully.

**Procedure**

1. On the **Saved FBDI Configurations** page, click the **Expand** button, and **review** the entire configured information.
2. After reviewing, click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (1590).png" alt=""><figcaption><p>Saved FBDI Configurations Page - Run Button</p></figcaption></figure>

&#x20;     The Confirmation message box is displayed.

3. On the **Confirmation** message box, click the **Yes** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (1591).png" alt=""><figcaption><p>FBDI Job Configuration Confirmation Message Box</p></figcaption></figure>

The Deployment started successfully message box is displayed.

<figure><img src="../../../.gitbook/assets/image (1592).png" alt=""><figcaption><p>Saved FBDI Configurations Page - Deployment Success Message</p></figcaption></figure>

After successful deployment, the Success status and the File Location are displayed on the Saved FBDI Configurations page.

<figure><img src="../../../.gitbook/assets/image (1593).png" alt=""><figcaption><p>Saved FBDI Configurations Page - Deployment Status and File Location</p></figcaption></figure>

</details>
{% endtab %}
{% endtabs %}



***

### Related Topics

* [**Saved FBDI Configurations**](saved-fbdi-configurations.md)

{% content-ref url="../../images-and-media/scikiq-pipelines/" %}
[scikiq-pipelines](../../images-and-media/scikiq-pipelines/)
{% endcontent-ref %}
