---
hidden: true
icon: cards-blank
---

# Create FBDI Template

**Contents**

* [**Instructions for Using this Page**](create-fbdi-template.md#instructions-for-using-this-page)
* [**Overview**](create-fbdi-template.md#overview)
* [**Procedure**](create-fbdi-template.md#procedure)
* [**Related Topics**](create-fbdi-template.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### **Purpose**

Creating a template establishes a standardized table structure to import data from Oracle EBS. It defines a predefined format that ensures data is structured, validated, and aligned with system requirements, thereby enabling accurate and error-free data import.

The template creation process consists of two main steps: **configuring template details** and **adding columns.**&#x20;

The sections below provide step-by-step instructions to guide you through each of these steps.

### **Procedure**

{% tabs %}
{% tab title="1. Configure Template Details" %}
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
{% endtab %}

{% tab title="2. Add Columns" %}
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
**Tip:** The **Is Nullable option** (Yes/No) indicates whether a field (column) in a table or template can accept empty (NULL) values or must always have a value.
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
{% endtab %}
{% endtabs %}















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



[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
