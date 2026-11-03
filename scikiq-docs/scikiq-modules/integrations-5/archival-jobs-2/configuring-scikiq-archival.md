---
hidden: true
icon: scale-unbalanced-flip
---

# Configuring SCIKIQ Archival

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Configuring **SCIKIQ Archival** involves a series of structured steps to ensure secure, compliant, and efficient data archiving.&#x20;

The process begins with establishing a connection to the source database, followed by configuring table classification to identify and categorize the data. The required compliance framework is then configured, and compliance policies are defined to specify data retention, archival, and deletion rules.

Next, the AWS storage environment is configured to store archived data. Once the setup is complete, an archival job is created and deployed to move data from the source system to archival storage.&#x20;

Finally, archived data can be viewed for retrieval and analysis, and deleted when it is no longer required, ensuring complete lifecycle management of archived information.

***

### Procedure

The expandable panels below tabs detailed instructions for completing each step.

{% tabs %}
{% tab title="Prerequisites" %}
The following are the prerequisites for configuring SCIKIQ Archival:

<table><thead><tr><th valign="top">System Requirements</th><th valign="top">Cloud Requirements</th></tr></thead><tbody><tr><td valign="top"><ul><li>Active access to the SCIKIQ platform</li><li>Administrative privileges</li><li>Valid database connection details</li><li>Network connectivity between SCIKIQ and AWS</li></ul></td><td valign="top"><p>An AWS account enables with the following services:</p><ul><li>Amazon S3</li><li>IAM Roles</li><li>CloudWatch Monitoring</li><li>Lifecycle Policies</li></ul></td></tr><tr><td valign="top"></td><td valign="top"></td></tr></tbody></table>
{% endtab %}

{% tab title="Connect SCIKIQ to Source Database" %}
**Overview**

The purpose of connecting the application with the Source Database while configuring the archival process is to establish secure access to the original data so it can be identified, filtered, and archived accurately. The process consists of the following steps: Select a New Data Source, Configure Connection Details, Add Metadata, Discovery, Configuration, and Review & Submit.

***

**Procedure**

* Refer to [Creating a Data Source Connection](../../images-and-media-1/creating-a-data-source-connection.md) to view the procedure.
{% endtab %}

{% tab title="Configure Table Classification " %}
**Overview**

Table classification helps identify which tables contain archival data by analyzing factors such as data age, usage frequency, and business relevance. It enables organizations to distinguish between active and historical data, ensuring that only appropriate tables are selected for archival.

This structured identification improves the efficiency of the archival process and prevents unnecessary data movement. As a result, it supports better storage management, system performance, and compliance with data retention policies.

***

**Procedure**

Table classification can be configured in two methods: Auto Table Classification and Manual Table Classification.

Refer to [Table Classification](../../integrations/meta-data-manager/table-classification.md) for the procedure.
{% endtab %}

{% tab title="Create Compliance Framework" %}
**Overview**

Configuring compliance rules ensures that archived data meets both legal and organizational requirements by enforcing defined data retention, security, and access policies. It helps organizations adhere to regulatory standards while maintaining proper governance over stored data. This also reduces the risk of non-compliance, penalties, and data misuse.

***

**Procedure**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under **SCIKIQ Archival**, expand **Compliance**, and then click **Regulatory Compliance**.

<figure><img src="../../../.gitbook/assets/image (211).png" alt="Regulatory Compliance Menu Item"><figcaption><p>Regulatory Compliance Menu Item</p></figcaption></figure>

The Regulatory Compliance Frameworks page is displayed.

3. On the **Regulatory Compliance Frameworks** page, click the **Add Framework** button.

The Add Framework  dialogue-box is displayed.

4. On the **Add Framework** dialogue-box:

A. Specify the **Framework Code, Version, Framework Name, Description, Jurisdiction, Effective Date, Regulatory Authority,** and **Mapped Policy Types.**&#x20;

> <mark style="color:red;">**Note:**</mark> Refer to the below table for the description of the above.

**Add Framework Dialogue Box Field Description**

| Field                | Description                                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Framework Code       | A unique identifier assigned to the compliance framework for easy reference and tracking                           |
| Version              | Indicates the specific version of the framework, helping manage updates and changes over time                      |
| Framework Name       | The official name of the compliance framework (e.g., GDPR, HIPAA, etc.)                                            |
| Description          | A brief summary explaining the purpose, scope, and key objectives of the framework                                 |
| Jurisdiction         | Specifies the geographic region or legal authority where the framework is applicable (e.g., India, EU, US)         |
| Effective Date       | The date from which the framework becomes applicable and enforceable                                               |
| Regulatory Authority | The governing body or organization responsible for defining and enforcing the framework                            |
| Mapped Policy Types  | The categories of internal policies (e.g., data retention, security, privacy) that are aligned with this framework |

B. Click the **Add Framework**  button.

<figure><img src="../../../.gitbook/assets/1 (1).png" alt=""><figcaption><p>Add Framework Dialogue Box</p></figcaption></figure>

The Framework added successfully message box appears and the framework is displayed on the Regulatory Compliance Frameworks page.&#x20;

<figure><img src="../../../.gitbook/assets/image (212).png" alt=""><figcaption><p>Regulatory Compliance Frameworks</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> * To view the details of a framework, click the View Framework ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAdCAYAAABWk2cPAAAB9ElEQVR4AeyUS0iUYRSG328gbVligl2gFgkVhIumm0wEipsKqk1E0KJSQmrRommgmGgomKZFi0JCq0UQ0UYFdSMKonh3IYIKulC8gvell4XO863nn/kQHV3MD4fDezn/O5w5/L7JmaWtdD7k+bQPTyZ0T5eeWe/BWO/6xqaaWnv09NUnFd0p17Vbz2wHw6O7/lKn/3RkbEKPKsJ6/6Vaw6Pjyss9quLAJdvB8Oj4XIJThnb0DqriTUwzcws6nJ2lWPiFan5H9TH03HYwPDo+/KmCk4ZOz80r+u2P1tY37Hse3itV4YUChWNVun67zHYwPAZ8+JkDe5VnaPx7rP91zVpcXrWz2VmHFLhaqJb2PjW39QmdDoZHx4ifOXRwovIMTWTeLc4z1BijB3dLlJtzxGZxne3dA/ED8qvkhl/GGNuLA37Bo2PEz5wxBpiwPENxn8zPU+jlY3tA4H+1TRoYGlUkWK7OhmrbwfDoHBR+5sBelTSUoaLLF1X5OagT+cfsQQUj33X/SUjvoj9sB3NA6PjwM5esUoYyfO7saf2tjOjD6zKdLzij+cWV+EH12w6GR8eHP1U5hfISrrP05hX9+vpWHfVV6mr8aTsYHh2fSzmHurzM1ZMJdd3UjnyZ9e5oba5D+7feqdllpavYhu/U8Rylu7YBAAD//4yl+SAAAAAGSURBVAMAM0t71otIidwAAAAASUVORK5CYII=) icon corresponding to it.
> * To update a framework, click the Edit  ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAfCAYAAADwbH0HAAABb0lEQVR4AeyXO0sDQRSFz64pRDtBEB+F4L+wVXwgWJio4AMsjIWNhSiSSkW0VpQUghDQygeCgsFOEH+AhZUgLkkQURQVwRRx7sBACAlzdzOZapc9M7PD3PvNPczCrvuceSvYVkFcLsTV0doEWxI4eUuwHFluQrA1w0OrfVstXkkcnaYxOpvAk5djx1dt9f3DI5KpM3jZFyyubrPhgcFU6fnVDf7yeawtxRGJ1CGTewVthFN2IDBBD0/S2NpJYWVjD40N9VhfnsNCfBxDvd0cLnyDFXT34FgCvn9+kdhMoq2lGWPDPXAcR87rGl/gUqhKPh0bRFdnu3pk9WxwJej8TBQTI33sStWuWGDTUIJrwbWAssAX17dQB4kCSEHtpVglbcUfn19qrexNQCmRFkyLlExBKZ8WPBUbwN3lvtRktN/36SVIOWnB5YJMzIVgEy6ycoRWs2wysUha7WXfxaeLHalNu7b+mYo5BJcV08C2/gEAAP//xpp8GgAAAAZJREFUAwDipTrWX77UzgAAAABJRU5ErkJggg==) icon corresponding to it.
> * To delete a framework, click the Delete ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB0AAAAeCAYAAADQBxWhAAABCUlEQVR4AexQzQoBURj9shdZKrGgzM7CxjN4DQuvgGSFspEVRdl5A9lRfjIL4hnIlMKCrJkzi6mZuZo7V8bm3u659Z3zfd/pnsBLP4fTVX/9uwH6w5GmPw1dxuuI9/540lzd0XS5oXKjS7l8wQRq8NDR5xi2EdzxaucL1Vp9qjR7NFttLWtQg4eOPovIKLhN08k4DTtVqpeKHwEdfQwfC8VtiqmFujd+il+xAB19bvBk6raMV5emvEkJ9cl4hWLjHfIUbzajUDgUZO4GD50p2khPpkoqQZNRm9bjgQPgodv2M0tPpswNAqQ0FQiNf0TGy5+VQKcZ71G7kV8wTGPRCPkJw1Qgoa9G3gAAAP//vLyoLQAAAAZJREFUAwBdvxjYSxTHgwAAAABJRU5ErkJggg==) icon corresponding to it.
{% endtab %}

{% tab title="Create Compliance Policy" %}
**Overview**

Creating a compliance policy as part of an archival process is essential to ensure that archived data is handled in accordance with regulatory, security, and business requirements.

Importance of creating a creating a compliance policy:

* **Regulatory Compliance:** Ensures that data is retained, protected, and deleted in line with regulations (e.g., GDPR, SOX, DORA), avoiding legal penalties.
* **Defined Retention Rules:** Specifies how long data should be stored (e.g., 7 years), preventing both premature deletion and unnecessary storage.
* **Data Protection & Security:** Enforces controls such as encryption, access restrictions, and immutability to safeguard sensitive data.
* **Audit & Traceability:** Maintains proper audit logs and evidence to support audits, investigations, and reporting requirements.
* **Risk Management:** Minimizes risks related to data breaches, non-compliance, and operational failures.

***

**Procedure**

In the SCIKIQ application, the process of archival involves a series of steps including inputting Policy Basic Details, specifying Data Retention Settings and Data Security Settings, configuring Access Control Settings, Setting up Audit Logging, Data Privacy Settings, Incident response Settings, and Conflict Resolution Settings.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Input Policy Basic Details</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, under **SCIKIQ Archival,** expand **Compliance**, and then click **Compliance Policies**.&#x20;

<figure><img src="../../../.gitbook/assets/image (213).png" alt="" width="563"><figcaption><p>Compliance Policies Menu Item </p></figcaption></figure>

2. The Compliance Policies page is displayed.&#x20;
3. On the **Compliance Policies** page, click the **Create Policy** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (214).png" alt=""><figcaption><p>Compliance Policies Page</p></figcaption></figure>

4. The Create New Policy dialogue box is displayed.&#x20;
5. On the **Create New Policy** dialogue box:

<figure><img src="../../../.gitbook/assets/image (215).png" alt="" width="563"><figcaption><p>Create New Policy Dialogue Box</p></figcaption></figure>

6. Specify the **Policy Title, Description, Policy Category, Data Classification, Effective Date, Version,** and **Policy Domain.** &#x20;
7. From the **Attach Frameworks** drop-down box, select the **applicable framework**.&#x20;

> <mark style="color:red;">**Note:**</mark> See the below table for the description of the frameworks.    &#x20;

**Description of Frameworks**

| Basel III – Basel III Accord                                | A global regulatory framework that strengthens bank capital requirements, risk management, and liquidity to improve financial system stability                                                                                                      |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BMR – Benchmark Regulation                                  | An EU regulation that ensures the accuracy, reliability, and integrity of financial benchmarks like interest rates and indices                                                                                                                      |
| CSDR – Central Securities Depositories Regulation           | An EU regulation aimed at improving the safety, efficiency, and transparency of securities settlement and central securities depositories                                                                                                           |
| CASS – Client Assets Sourcebook                             | A UK regulatory framework that governs how firms must safeguard and manage client money and assets.                                                                                                                                                 |
| DORA – Digital Operational Resilience Act                   | An EU regulation that ensures financial institutions can withstand, respond to, and recover from ICT (technology-related) disruptions and cyber threats                                                                                             |
| Dodd-Frank – Dodd-Frank Act                                 | A U.S. financial reform law designed to increase transparency, reduce systemic risk, and prevent another financial crisis after 2008                                                                                                                |
| DODD\_FRANK – Dodd-Frank Wall Street Reform Act             | A comprehensive U.S. regulation (same core law as above) focused on stricter oversight of financial institutions, derivatives, and consumer protection                                                                                              |
| EMIR\_REFIT – EMIR Refit                                    | An updated version of EMIR that simplifies reporting requirements and reduces regulatory burdens while maintaining transparency in derivatives markets                                                                                              |
| EMIR – European Market Infrastructure Regulation            | An EU regulation that improves transparency and reduces risk in over-the-counter (OTC) derivatives through reporting, clearing, and risk mitigation rules.                                                                                          |
| FCA\_HANDBOOK – FCA Handbook                                | A detailed set of rules and guidance issued by the UK regulator governing financial firms’ conduct and compliance obligations.                                                                                                                      |
| FCA – Financial Conduct Authority                           | The UK regulatory body responsible for overseeing financial markets, protecting consumers, and ensuring fair competition                                                                                                                            |
| GDPR – General Data Protection Regulation                   | An EU regulation that governs how organizations collect, process, and protect personal data while ensuring individuals’ privacy rights                                                                                                              |
| IFPR – Investment Firms Prudential Regime                   | A UK regulatory framework that sets capital, liquidity, and risk management requirements specifically for investment firms                                                                                                                          |
| MAR – Market Abuse Regulation                               | An EU regulation aimed at preventing insider trading, market manipulation, and ensuring market integrity and transparency                                                                                                                           |
| MiFID II – Markets in Financial Instruments Directive       | An EU directive that regulates investment services and financial markets to enhance transparency, investor protection, and competition                                                                                                              |
| MiFID\_II – Markets in Financial Instruments Directive II   | Another reference to MiFID II, emphasizing the same EU framework governing trading, reporting, and investor safeguards in financial markets                                                                                                         |
| MiFID\_III – Markets in Financial Instruments Directive III | A proposed or evolving extension of MiFID II expected to further refine market transparency, investor protection, and regulatory oversight in EU financial markets                                                                                  |
| NIS2 – Network and Information Security Directive 2         | An EU directive that strengthens cybersecurity requirements and incident reporting obligations for critical and digital service providers                                                                                                           |
| PSD2 – Payment Services Directive 2                         | An EU regulation that enhances payment security, promotes open banking, and increases competition by enabling third-party access to banking data                                                                                                    |
| SOX – Sarbanes-Oxley Act                                    | A U.S. law that enforces strict financial reporting, internal controls, and corporate governance standards to prevent fraud                                                                                                                         |
| SFTR – Securities Financing Transactions Regulation         | An EU regulation that improves transparency in securities financing markets (like repos and securities lending) through detailed reporting requirements                                                                                             |
| SMCR – Senior Managers & Certification Regime               | A UK framework that holds senior financial services staff accountable for their conduct and ensures employees are fit and proper for their roles                                                                                                    |
| SDR – Settlement Discipline Regime                          | An EU regime under CSDR that enforces timely securities settlement through penalties and mandatory buy-ins for settlement failures                                                                                                                  |
| SEC – SOC 2                                                 | A compliance framework (developed by AICPA and often associated with SEC-regulated environments) that evaluates how organizations manage customer data based on security, availability, processing integrity, confidentiality, and privacy controls |
| SFDR – Sustainable Finance Disclosure Regulation            | An EU regulation requiring financial firms to disclose how they integrate environmental, social, and governance (ESG) factors into investment decisions                                                                                             |
| UK\_DPA\_2018 – UK Data Protection Act 2018                 | A UK law that complements UK GDPR by setting out how personal data must be processed, protected, and handled within the UK                                                                                                                          |
| UK\_EMIR – UK European Market Infrastructure Regulation     | The UK version of EMIR that governs derivatives reporting, clearing, and risk mitigation post-Brexit                                                                                                                                                |
| UK\_GDPR – UK General Data Protection Regulation            | The UK’s adaptation of EU GDPR that regulates personal data protection and privacy rights within the UK                                                                                                                                             |
| UK\_LISTING\_RULES – UK Listing Rules                       | A set of regulations governing how companies list and maintain securities on UK stock exchanges, ensuring transparency and investor protection                                                                                                      |
| UK\_MAR – UK Market Abuse Regulation                        | A UK regulation that prevents insider trading, market manipulation, and unlawful disclosure to ensure fair and transparent financial markets                                                                                                        |
| UK\_MIFIR – UK Markets in Financial Instruments Regulation  | The UK version of MiFIR that sets rules for trade transparency, reporting, and market structure for financial instruments post-Brexit                                                                                                               |

</details>

<details>

<summary><strong>2.Specify Data Retention Settings</strong></summary>

1. In the **Policy Domains** section, select the **Data Retention panel**.

&#x20;     The Data Retention panel is expanded.

2. On the **Data Retention panel**, specify the **retention period** for **each storage tier** by selecting the appropriate **unit** choosing from **Days, Months,** or **Years**.
3. Specify the **Start date (From)** and **End date (To).**&#x20;
4. From the **Action** drop-down box, **retain** the default selections—**Move for Hot, Warm, and Cold storage tiers, and Archive for the Deep Cold storage tier**.

<figure><img src="../../../.gitbook/assets/image (216).png" alt=""><figcaption><p>Data Retention Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>3.Specify Data Security Settings</strong></summary>

1. In the **Policy Domains** section, select the **Data Security panel**.

&#x20;     The Data Security panel is expanded.

2. In the expanded **Data Security panel**, select the **Encryption at Rest** and **Encryption at Rest** checkboxes.

<figure><img src="../../../.gitbook/assets/image (217).png" alt=""><figcaption><p>Data Security Settings</p></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> You can select either or both of the **Encryption at Rest** and **Encryption in Transit checkboxes.**
>
> Here is the description of these:
>
> * **Encryption at Rest:** Protects data stored on disks or storage systems by encrypting it so unauthorized users cannot access it even if the storage is compromised.
> * **Encryption in Transit:** Protects data as it moves between systems over networks by encrypting it to prevent interception or eavesdropping during transmission.

</details>

<details>

<summary><strong>4.Configure Access Control Settings</strong></summary>

**Overview**&#x20;

Configuring access control settings defines which users, data owners, and roles are authorized to access specific resources. It ensures that only approved entities can view, modify, or manage data in accordance with security and compliance requirements.&#x20;

The following section provides step-by-step instructions to help you set up and manage access control.

**Procedure**

The following step-by-step instructions guide you through the process.

1. In the **Policy Domains** section, select the **Access Control panel.**

&#x20;     The Access Control panel is expanded.

2. On the expanded **Access Control panel,** specify the **Users, Data Owner Group,** and **Allowed Roles.**
3. Select the **Approval Required checkbox** based on the requirement.

<figure><img src="../../../.gitbook/assets/image (218).png" alt=""><figcaption><p>Access Control Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>5.Setup Audit Logging</strong></summary>

**Overview**&#x20;

Configuring Audit Logging enables you to define the level of detail captured in system logs and the duration for which these logs are retained. These settings support regulatory compliance and audit requirements by ensuring that relevant activities are recorded and preserved for the required retention period.&#x20;

**Procedure**

The following section provides step-by-step instructions to help you set up audit logging.

1. In the **Policy Domains** section, select the **Audit Logging** panel.

&#x20;     The Audit Logging panel is expanded.

2. On the expanded **Audit Logging** panel, from the **Log Level** drop-down box, select the required **audit level** choosing from **Full (All Operations), Changes Only, Critical Only,** or **Minimal.**&#x20;

{% hint style="info" %}
**Tip:** **Description of Log Levels**

* **Full (All Operations):** Logs every action performed in the system (read, write, update, delete, etc.); provides maximum visibility but generates high log volume&#x20;
* **Changes Only:** Logs only actions that modify data or configurations (e.g., create, update, delete), excluding read/view operations
* **Critical Only:** Logs only high-risk or sensitive actions (e.g., admin changes, access control updates, security events)
* **Minimal:** Logs only essential system events, reducing storage and performance overhead but offering limited traceability
{% endhint %}

3. In the **Audit Retention** days field, specify how long audit logs should be stored and retained before deletion or archival.
4. Select the **Immutable Logs (Cannot be modified)** checkbox based on requirement.

> <mark style="color:red;">**Note:**</mark> Immutable Logs (Cannot be modified) is an option that ensures once audit logs are written, they cannot be altered, deleted, or overwritten, even by administrators.

<figure><img src="../../../.gitbook/assets/image (219).png" alt=""><figcaption><p>Audit Log Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>6.Setup Data Privacy Settings</strong></summary>

**Overview**&#x20;

Data Privacy Settings allow you to enable controls for protecting sensitive personal data and ensuring compliance with privacy regulations such as GDPR. When enabled, you can select the required options—PII Masking, Data Anonymization, Consent Requirement, and Right to Erasure—based on your data protection and compliance needs.&#x20;

The following section provides step-by-step instructions to help you set up data privacy settings.

**Procedure**

1. In the **Policy Domains** section, select the **Data Privacy** panel.

&#x20;     The Data Privacy panel is expanded.

2. On the expanded **Data Privacy** panel, select the required options choosing from **PII Masking, Data Anonymization, Consent Requirement,** and **Right to Erasure.**

{% hint style="info" %}
**Tip: Description of Data Privacy options**

* **PII Masking Enabled:** Masks sensitive personally identifiable information (PII), such as names or account numbers, to prevent unauthorized visibility while still allowing limited use of the data
* **Data Anonymization:** Transforms data in a way that individuals cannot be identified, ensuring privacy while allowing the data to be used for analysis or reporting
* **Consent Required:** Ensures that user consent is obtained and recorded before collecting or processing their personal data, in line with privacy regulations
* **Right to Erasure (GDPR):** Allows individuals to request deletion of their personal data, ensuring compliance with GDPR’s “right to be forgotten” requirement
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (220).png" alt=""><figcaption><p>Data Privacy Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>7.Setup Incident Response Settings</strong></summary>

**Overview**&#x20;

Configuring Incident Response settings allows you to define the Incident Detection SLA and Notification SLA in hours, ensuring timely identification and communication of incidents. These settings are essential for maintaining operational resilience and meeting compliance requirements.

The following section provides step-by-step instructions to help you set up incident response settings.

**Procedure**

1. In the **Policy Domains** section, select the **Incident Response** panel.

&#x20;     The Incident Response panel is expanded.

2. On the expanded **Incident Response** panel, specify the **Incident Detection SLA** and **Notification SLA in hours.**

{% hint style="info" %}
**Tip: Description of Incident Response panel options**

* **Incident Detection SLA (In Hours)**: Specifies the maximum time allowed to detect or identify an incident after it occurs
* **Notification SLA (hours):** Defines the maximum time within which relevant stakeholders must be notified after an incident is detected
{% endhint %}

3. Select the **Escalation Required** checkbox to enable automatic escalation workflows if SLA thresholds are breached.

<figure><img src="../../../.gitbook/assets/image (221).png" alt=""><figcaption><p>Incident Response Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>8.Setup Conflict Resolution Settings</strong></summary>

**Overview**&#x20;

Configuring the Conflict Resolution Settings determines how the system handles situations where multiple policies apply to the same data and produce conflicting outcomes. It defines which policy takes precedence—such as the most restrictive, least restrictive, first match. Or Custom —ensuring consistent and predictable enforcement of rules across the system.

The following section provides step-by-step instructions to help you set up conflict resolution settings.

**Procedure**

1. From the **Conflict Resolution Strategy** drop-down box, select the appropriate option choosing from **Most Restrictive, Least Restrictive, First Match** or **Custom.**&#x20;

{% hint style="info" %}
**Tip:** **Conflict Resolution Strategy Options**

* **Incident Detection SLA (In Hours)**: Choosing this option applies the strictest rule among all matching policies. You can use this option when compliance and data security are the highest priority.
* **Least Restrictive:** Choosing this option applies the most lenient rule among conflicting policies. You can use this option when ease of access and operational flexibility are more important.
* **First Match:** Choosing this option applies the first policy that matches, based on priority or order. You can use this option when policies are designed in a specific order of precedence.
* **Custom:** This option allows you to define your own conflict resolution logic. You can use this option when standard strategies don’t meet your business requirements.
{% endhint %}

2. Select the **Inherit Settings from Framework** checkbox if you want to Apply framework-level configurations automatically.
3. Finally, click the **Create Policy** button.

<figure><img src="../../../.gitbook/assets/image (222).png" alt=""><figcaption><p>Conflict Resolution Strategy Settings</p></figcaption></figure>

4. The policy is created and displayed on the Compliance Policies page. See the below image.

<figure><img src="../../../.gitbook/assets/image (223).png" alt=""><figcaption><p>Compliance Policies Page</p></figcaption></figure>

{% hint style="info" %}
Tip:&#x20;

To view details of a policy, click the View  ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACkAAAAoCAYAAABjPNNTAAADMklEQVR4AeyYe0hTURzHv7uuzJQi0zR7UhYs0KAyfBTVDE0tygw1w6hcSSVTs+jh1oQoTa2MEs1EK6Sihln9odiDEqE006LS3ilpaabiCx/YbOfgrg1i7m6DJd0Lv3PPPb/fOb/P/Z7HxmUGR8HFYOj6+q0V5rQhjL/eWEjineFkC3MYya3LtCB1BZrTx0OaSn1eSV5JUylgqnGMWpPqHyu0tXeirPINHpZWoPr9F/T09pmKjR3HIEgCkqcsgk+IFP5hsYiRn0F8YiYiYo9DHLQXW/YoUF5VDZVqkE1kTIUzZM2HWoRHJSA9V4mu7h5Yj7fCBr8VkEqC4bXUlbJ8rmtAtOw05CcvoKOzm7YZU3CCJNMpjT+Fhu/NNOdKz0XIz0nCwahwbA70QapCipw0GRzsbUEusgSIwuRlyLOhpjdk448WJKRkU/VIsmlT7al6Tc2tCI2UwSNAAkXKRfVvvwNidoVCIBCQMFS8rMH5nJsYGPhFnw0p9IIkG+R6wT31v6QmNoeryBmTbSci88ot1NU30vbiR2W4X1IO1wXOcHK0o22kuFtcispX70jVINMLsrevH59qG7QSTLGbhP7+AbR3dGm1/2xtxxihEBNsrNl2lUql7l/PPnOt6AVpNc4Sweu9wTDD4W8/1sHCggFZl5qkNtZW8HRzQXNLm5bqs6Y7wnu5myaM83046whdPRa7YJ3PMjbq2YsaPH3+GmEbfZGedAAJ+yXIPSvH/DkzcePOA3btMuoXi9waCKI825ljRW9IodAC0TtDELDai6YgU3g0OQt5ykKI5s2G7yp3MAIGsqRM3C4qoTGkjyx2u5ba1MGx0BuSjEum/Uj0NsTtDoPl2DF0x2Zczgc5wMnuDoo4hMdPqkgoyBRnpR6Gn9iD3enUYUDBCZKMzzACbForRuG1NCjiJFiyUETPRXI2kmPJ39sTBO5qxjGqMOljrHGG1CQkqq4Ru+PciTgUXEqmpsxOhHzfDriI5oK8jCbW2LvBkMYm5tL/X4HUycxD6pSHg5NXkoNYOkN5JXXKw8E5+pQ016e/kURllTTHJ78/c+oCZSF1BZnbx0OaagZ4Jf8rJX8DAAD//2kYVkgAAAAGSURBVAMA1+E+y+iyUJwAAAAASUVORK5CYII=) icon corresponding to it.

To update a policy, click the Edit ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAlCAYAAAAuqZsAAAABi0lEQVR4AeyYPUgDMRTH/3QTBVE3wdVJ0EFw0cnJWRwFB1Fw93MSLYKCOJUufgyurqLTuSh1OVBwEFdBRLBaRKtDr94LRO7s0bskl6aFhHtJyNf73f89MiRTbdKSQZMWCyYamJBij09FmLQgfAiMJvp6u2HCyHfQasCCkyb7FkxUfauYVSxOgfL3Dy6uXLyXPuKWRs5ryTGC2skdY20rj1XfXt9Kkc7rDaYO5nlVfH6V8fxSZH5v7h6wsXsAgmUDCatUwch5du8Q5841NpfnMDTQzzAItlLxWD9plRoYQVH4zpwCckcnf3DTUxNYX5xFR3tbUia2LhUwDkVKsVP9iuCcSxcLM5Po6er0R8Q+ZbAoKEKgMI6PDVNXypTA6kFlV+allOJ/IQ2mE4rgpMB0Q0mBNQJKCsy9vWdXAW3mRomumlP8LN5KhZJvplYHFJ2rBKYLSgpsdGQQhdN9ZvntJbkrgTzHmJJiMWcrTVswUfmsYlYxUQVE17dOjpl6hvqvaEgxE89PQZ9BuF8AAAD//0RjOAMAAAAGSURBVAMArCjbwpAnZcMAAAAASUVORK5CYII=) icon corresponding to it.

To delete a policy, click the Delete ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACkAAAAoCAYAAABjPNNTAAABf0lEQVR4AeyYwSsEYRjGn8a2y02rjUT+AQdysJTmIEobKclF2tMmN6W54OKi/Q8o/4NWERfFkgOXPTg5EuWgJOGws3wO22i+t+b75qvP1Dv11PS9z7zvb56ZmulzGgk4HCTgYEhTDymU5P3jC2xKdmMhSGHq7c7ChsRsmaSQMqPNNYY0lT4nyUmqJuD7DdRu73B6cdPUw9OzahvSr/1Ofnx+YbO8i9mih8LiKpa9Mta3d5paKG1gZmntt75/dEYCRCloQwabZ9JpdOayf5TraIfjGGkP7S5trRmsFOfgjgwiP9RPan56HIWJ0eA9KZ9rQ4pJr2/vODiponJ8TuryuoZ63Rd2bcWC1J6qeCFDKgZG2jlJMhrFAiepGBhp/y9JkoCiEAuyr6cLY/kB0UeqVKoFk+4wxNdJaoi4GAtSDN/ySrg63JOqWvn5AZlyI6LQtliQdFuzFYY0lScnyUmaSsBUn+S+k7a2/qjkQ0na2PILzpSBhiBlJttrDGnqCXwDAAD//5KIW10AAAAGSURBVAMAzIG0vChw33wAAAAASUVORK5CYII=) icon corresponding to it.
{% endhint %}

</details>
{% endtab %}

{% tab title="Configure Storage" %}
**Overview**

Setting up AWS S3 for storing archived data provides a scalable, secure, and cost-effective storage solution for long-term data retention. After the AWS S3 set up, data can be archived through a structured pipeline that moves data from the source system to S3 based on defined rules.

***

**Procedure**

The AWS setup configuration process consists of four steps: Basic Configuration, Storage and Data Configuration, Compute Configuration, and Review Compute Configuration.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Basic Configuration</strong></summary>

**Overview**

As part of the basic configuration, you need to input **Configuration name, Environment, AWS Access Key, AWS Secret Key, AWS Region,** and **Resource Prefix**.&#x20;

The following step-by-step instructions guide you through the process.

**Procedure**

1. On the **SCIKIQ Left Navigation Bar,** go to **SCIKIQ Archival**.&#x20;
2. Under **SCIKIQ Archival**, expand **Storages** , and then click **Configure Storage**. See the image below:

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

3. The AWS Infrastructure Configuration Wizard page is displayed.
4. In the **Basic Configuration** section, select either an **existing pre-configuration** or c**reate a new one.**

**Selecting an existing configuration**

* From the **Load from Existing AWS Configuration** drop-down box, select an **existing configuration.**

Once the existing configuration is selected, the Configuration name, Environment, Glue Connection, and Description are prepopulated.

**Creating a new configuration**

* In the **Basic Configuration** section, specify **Configuration name, Environment, Glue Connection,** and **Description.**

> <mark style="color:red;">**Note:**</mark> For description of the above fields, refer to the below AWS Basic Configuration – Field Descriptions table.

**AWS Basic Configuration – Field Descriptions**

| **Field**          | **Purpose**                                                                                                                  |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Configuration Name | A unique name to identify and manage the AWS configuration within the system.                                                |
| Environment        | Specifies the deployment context (e.g., Dev, Test, Prod) to separate and manage resources appropriately.                     |
| Glue Connection    | A configured connection used by AWS Glue to securely access and process data from source systems during archival operations. |
| **Description**    | A brief description used to provide additional details or context about the AWS configuration.                               |

<figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Once the Basic Configuration is completed, the Storage and Data Configuration section is highlighted.

</details>

<details>

<summary><strong>2.Storage &#x26; Data Configuration</strong></summary>

**Overview**

The purpose of Storage & Data Configuration is to define how and where archived data will be stored across different storage tiers based on its access frequency and retention needs. It ensures that data is placed in the most appropriate storage class (hot, warm, cold, or archival) to balance performance and cost.

**Procedure**

As part of Storage & Data Configuration, you need to define the a**ccess tiers, including S3 Hot Storage (Frequent Access), S3 Warm Storage (Infrequent Access), S3 Cold Storage (Rare Access), and S3 Archival Storage (Deep Cold).**

The following step-by-step instructions guide you through the process.

Step-by-Step Instructions

**1.Defining S3 Hot Storage (Frequent Access)**

* If you want to select an **existing bucket**, then from the **Select or Create Bucket** drop-down box, select an **existing bucket**.
* If you want to select a new bucket, then from the **Select or Create Bucket** drop-down box, select **Create New**, and then enter the **bucket name** in the **New Bucket Name** field.

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Defining Hot Storage</p></figcaption></figure>

**2.Defining S3 Warm Storage (Infrequent Access)**

* In the **S3 Warm Storage (Infrequent Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select the **storage class** choosing from **S3 Standard - 1A or S3 One Zone - 1A.**

{% hint style="info" %}
**Tip:**&#x20;

* **Standard-IA:** Use **Standard-IA** when data is important but rarely accessed
* **One Zone-I:** Use **One Zone-IA** when data is less critical and cost saving is a priority
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption><p>Defining Warm Storage</p></figcaption></figure>

**3.Defining S3 Cold Storage (Rare Access)**

* In the **S3 Cold Storage (Rare Access)** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select **S3 Glacier Instant Retrieval**.

{% hint style="info" %}
**Tip: S3 Glacier Instant Retrieval** is an AWS S3 storage class designed for archival data that is rarely accessed but needs immediate (milliseconds) retrieval when required
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (54).png" alt=""><figcaption><p>Defining S3 Cold Storage (Rare Access)</p></figcaption></figure>

**4.Defining S3 Archival Storage (Deep Cold)**

* In the **S3 Archival Storage (Deep Cold),** section, select an **existing bucket** or **create a new one.**
* From the **Storage Class** drop-down box, select either **S3 Glacier Flexible Retrieval** or **S3 Glacier Deep Archive.**

{% hint style="info" %}
**Tip:**&#x20;

* Use **Flexible Retrieval** when you may need data occasionally
* Use **Deep Archive** when data is rarely needed and cost saving is the top priority
{% endhint %}

* From the **Select Glacier Vault** drop-down box, select either **lse\_glacier\_vault** or **create a new one.**

{% hint style="info" %}
**Tip:** A Glacier Vault is a storage container in Amazon Glacier (legacy archival service) used to store and manage long-term archived data.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption><p>Defining Deep Cold Storage</p></figcaption></figure>

**5.Defining AWS Glue Data Catalog & ETL**

* In the **AWS Glue Data Catalog & ETL** section, select either an **existing catalogue database or create a new one.**

{% hint style="info" %}
**Tip:**&#x20;

* **Glue Data Catalog** → Stores information about your data
* **Glue ETL** → Moves and transforms your data
* **Catalogue Database** → Organizes metadata tables into logical groups
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (56).png" alt=""><figcaption><p>Defining AWS Glue Data Catalog &#x26; ETL</p></figcaption></figure>

**6.Defining Amazon Athena**

* In the **Amazon Athena** section, enter the **Work Group Name** and **Results Bucket**.

{% hint style="info" %}
**Tip:**

* **Amazon Athena** is a serverless query service that allows you to run SQL queries directly on data stored in Amazon S3—without setting up or managing any database servers.
* A **Workgroup** in Athena is a way to organize and manage query execution.
* The **Results Bucket** is an S3 location where Athena stores the output of queries.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption><p>Defining Amazon Athena</p></figcaption></figure>

**7.Configuring KMS (Key Management Service)**

* In the **KMS Configuration** section, select the applicable **KMS Key Alias**.

{% hint style="info" %}
Tip:&#x20;

* **KMS Configuration** defines the selection and management of encryption keys in AWS to secure data and control access through centralized key management.
* **KMS key alias** is a user-defined, human-readable name that maps to a KMS key, simplifying key identification and management.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (58).png" alt=""><figcaption><p>Configuring KMS</p></figcaption></figure>

8. Finally, click the **Next** button.
9. The Review Configuration section is highlighted.

</details>

<details>

<summary><strong>3.Review Configuration</strong></summary>

1. In the **Review Configuration** section, review the configuration, and then click the **Finish** button.

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption><p>Review Configuration</p></figcaption></figure>

2. The configuration is saved and displayed on the AWS Infrastructure Management page.

</details>
{% endtab %}

{% tab title="Setup Deployment Platform" %}
**Overview**

The purpose of setting up a deployment platform such as Amazon ECS Cluster or Kubernetes Pod while creating an archival job is to provide the runtime environment where the archival processes are executed. It enables scalable and efficient handling of large volumes of data by distributing workloads across containers. This setup ensures high availability, fault tolerance, and better resource utilization during data archiving.

Overall, it improves performance, reliability, and operational control of the archival process.

***

**Procedure**

As part of setting up the deployment platform, you can setup either Amazon ECS Cluster or Kubernetes Pod.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup Deployment on Amazon ECS Cluster</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival,** and then expand **Archival Jobs.**
2. On the expanded menu, click **Deployment Config.**

<figure><img src="../../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

3. The Deployment Configuration page displayed. Click on **"+New Configuration"** Button

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

4. On the **Deployment Configuration** page, specify the **Configuration Name, Description,** and **select Amazon ECS Cluster.**

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

The Amazon ECS Cluster fields are displayed.

5. In the **Amazon ECS Cluster** fields, fill the required details, and then click the **Save Configuration** button.

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

The config is Created.

</details>

<details>

<summary><strong>2.Setup Deployment on Kubernetes POD</strong></summary>

1. On the **Deployment Configuratio**n page, specify the **Configuration Name, Description,** and **select Kubernetes POD.**&#x20;

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

The Kubernetes POD Configuration fields are displayed.

2. &#x20;In the **Kubernetes POD Configuration** fields, specify **CPU Units, Memory,** and then click the **Save Configuration** button.&#x20;

<figure><img src="../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

The config is created.

</details>
{% endtab %}

{% tab title="Create Archival Job" %}
**Overview**

Creating an archival job is to automate the process of moving inactive or historical data from primary systems to long-term storage. It helps improve application performance by reducing the load on active databases. An archival job ensures that data is stored securely while meeting compliance and retention requirements.

***

**Procedure**

The process involves a series of sequential steps, which includes Setup Data Source, Define Data Selection, Select Compliance Policy, Enable PII Detection, Setup Partitioning, Apply Data Filters, Define Retention Schedule, POD Management, and Review & Save.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Setup</strong> <strong>Data Source</strong></summary>

**Overview**

As part of selecting the Data Source, you need to select **Data Source Type, Connection,** and **Tables.** The purpose of selecting these is to clearly define what data to archive and from where. Each element plays a specific role.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Create Archival Job**.

<figure><img src="../../../.gitbook/assets/image (1631).png" alt=""><figcaption></figcaption></figure>

The **Archival Configuration** page is displayed.

3. On the **Archival Configuration** page, in the **Data Source** section:

A. From the **Source Type** drop-down box, select the **data source**. For example, ORACEL-EBS.

{% hint style="info" %}
**Tip:** Selecting the **data source** identifies the type of system from which the data will be archived.
{% endhint %}

B. From the **Connection** drop-down box, select the applicable **connection.** For example, ORACEL-EBS.

{% hint style="info" %}
**Tip:** Selecting the connection defines the actual link to the data source.
{% endhint %}

C. From the **Module** drop-down box, select the applicable module. For example, _AR – Accounts Receivable_. Click on **Load Tables.**

{% hint style="info" %}
**Tip:** Selecting the module ensures that the archival process is scoped to the relevant business area.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1657).png" alt=""><figcaption></figcaption></figure>

D. From the **Selected Tables** list, select the required **tables**.

{% hint style="info" %}
**Tip:**  Selecting the tables specifies the tables that are to be archived.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1659).png" alt=""><figcaption></figcaption></figure>

**a. Table Selection and Grouping for Archival**

1. To begin, clicking on the **Advanced Search** button to search table by name.

<figure><img src="../../../.gitbook/assets/image (1661).png" alt=""><figcaption></figcaption></figure>

2. Provide the name of the table you want to search for. For example, enter a table name like **“BANK”** in the search field.
3. If matching text is found, the system will display all relevant tables associated with your search term.

<figure><img src="../../../.gitbook/assets/image (1663).png" alt=""><figcaption></figcaption></figure>

4. The matching tables (e.g., all tables related to “BANK”) will then be appended to the existing table list.

<figure><img src="../../../.gitbook/assets/image (1664).png" alt=""><figcaption></figcaption></figure>

**b. Managing Table Groups**

1. Click on **“Add Row”** to create multiple groups.
2. Each group allows you to organize and assign different tables as needed.
3. Click on **Add Row.**

<figure><img src="../../../.gitbook/assets/image (1668).png" alt=""><figcaption></figcaption></figure>

**c. Assigning Modules**

1. You can assign selected tables to specific groups based on different modules.
2. Choose the desired module from the dropdown menu available for each group.

<figure><img src="../../../.gitbook/assets/image (1666).png" alt=""><figcaption></figcaption></figure>

**d. Archival Flexibility**

* The system supports archiving tables across multiple modules within a single archival job.
* This allows you to efficiently manage and process data from different modules together.

</details>

<details>

<summary><strong>2.Define Data Selectio</strong>n</summary>

**Overview**

As part of data selection, data profiling is performed. Data profiling is the process of analyzing data to understand its structure, quality, and content before it is used, migrated, or archived.

SCIKIQ performs data profiling by:

* Scanning tables automatically
* Generating profiling reports
* Highlighting data quality issues

**Procedure**

The below instructions guide you through the process:

**Step-by-Step Instructions**

1. In the **Profiling** column, click the toggle or action icon

<figure><img src="../../../.gitbook/assets/image (1636).png" alt=""><figcaption></figcaption></figure>

2. On the **Data Selection** page, click **each table** to perform data profiling.

<figure><img src="../../../.gitbook/assets/image (1638).png" alt=""><figcaption></figcaption></figure>

3. After completion of data profiling, click the **Close** button.

<figure><img src="../../../.gitbook/assets/image (1639).png" alt=""><figcaption></figcaption></figure>

&#x20;  4\. The Compliance columns is highlighted.

</details>

<details>

<summary><strong>3.Select Compliance Policy</strong></summary>

**Overview**

The purpose of selecting a compliance policy while creating an archival job is to ensure that the archived data adheres to legal, regulatory, and organizational requirements.&#x20;

The compliance policy defines rules such as Data retention period, Data Security, Access Control, Audit Logging, Data Privacy, and Incident Response.

**Procedure**

The following step-by-step instructions guide you through the process.

**Step-by-Step Instructions**

1.  In the **Compliance** column, click the action option.



    <figure><img src="../../../.gitbook/assets/image (1633).png" alt=""><figcaption></figcaption></figure>


2. select the required **policy** from the **Compliance Policy** drop-down to apply compliance rules to the first table.

The selected compliance policy details appear below.&#x20;

2. If you want to apply **same compliance policy** to all tables, then select ![](<../../../.gitbook/assets/unknown (36).png>)to apply the same compliance policy to all tables.

The selected compliance policy details appear below.

3.  If not, select the required table, and then select the required policy from the **Compliance Policy** drop-down box.



    <figure><img src="../../../.gitbook/assets/image (1641).png" alt=""><figcaption></figcaption></figure>
4. Finally, click the **Save** button.

</details>

<details>

<summary><strong>4.Enable PII Detection</strong></summary>

**Overview**

PII Detection is the process of identifying personally identifiable information within data to ensure it is securely handled and compliant with regulations. PII detection scans data (tables, files, databases) to:

* Locate sensitive personal information
* Classify it appropriately
* Enable security and compliance actions

**Procedure**

As part of enabling PII Detection, you need to:

* **Define protection settings** to establish how sensitive data should be handled and protected.
* **Identify PII patterns** through scanning to automatically detect sensitive data within tables or datasets.
* **Specify appropriate masking methods** to define how the identified sensitive data should be protected or hidden.

The following sections explain how to configure each of these.

**a. Define Protection Settings**

1.  In the **PII Detection** column, click the action option.



    <figure><img src="../../../.gitbook/assets/image (1642).png" alt=""><figcaption></figcaption></figure>
2.  On the **PII Detection** page, click the **PII Protection Settings** button.



    <figure><img src="../../../.gitbook/assets/image (1643).png" alt=""><figcaption></figcaption></figure>

The PII Protection Settings screen is displayed.

1. On the **PII Protection Settings** screen, select the **Enable PI** checkbox.
2. From the **Detection Patterns** List, select the **required patterns.**&#x20;
3. From the **Masking Method** drop- down box, select the applicable **masking method**.&#x20;

<figure><img src="../../../.gitbook/assets/image (1644).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Tip:** Refer to the below table for the description of masking methods:
{% endhint %}

&#x20;                                                     **Masking Methods Description**

| Field                     | Purpose                                                                    | Example                                             | Purpose                                                                        |
| ------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------ |
| Partial Masking (Default) | Only a portion of the data is hidden, while the rest remains visible       | 98XXXX3210                                          | Allows partial visibility for identification while protecting sensitive parts. |
| Full Redaction            | Completely hides the data                                                  | \*\*\*\*\*\*\*\*\*\*6                               | Maximum security when data should not be visible at all.                       |
| Masking Character         | Replaces the data with a specific character (like \*, X, or #)             | john.doe@email.com → \*\*\*\*\*\*\*\*\*\*\*\*\*\*\* | Simple and consistent masking format.                                          |
| Custom Pattern            | Applies a user-defined masking format                                      | Shows first 2 and last 2 characters → ABXXXXYZ      | Flexible masking based on business requirements.                               |
| Hashing                   | Converts data into a fixed-length encrypted value (non-reversible)         | password → 5f4dcc3b5aa765d61d8327deb882cf99         | Secure storage where original data cannot be retrieved.                        |
| Encryption                | Transforms data into an unreadable format that can be decrypted with a key | 12345 → Encrypted text                              | Secure storage with the ability to restore original data when needed.          |
| Tokenization              | Replaces sensitive data with a non-sensitive placeholder (token)           | 1234-5678-9012-3456 → TKN-982734                    | Keeps original data safe while allowing reference via tokens.                  |

4. Finally, click the **OK** button.
5. The PII protection settings are defined.

**b. Identify PII patterns**&#x20;

1. On the **PII Detection** page, select the **Table**, and then click the **Scan for PII Patterns** button.

<figure><img src="../../../.gitbook/assets/image (1645).png" alt=""><figcaption></figcaption></figure>

2. The detected PII patterns are displayed. See the below image.

<figure><img src="../../../.gitbook/assets/image (1646).png" alt=""><figcaption></figcaption></figure>

**c. Specify Masking Methods**

1. On the **PII Detection** page, from the **Masking Method** drop-down box, select the required **masking method**.
2. Follow the same procedure for all the detected patterns.
3. Apply the same procedure for all the tables.
4. Click the **Save** button.

<figure><img src="../../../.gitbook/assets/image (1647).png" alt=""><figcaption></figcaption></figure>

5. The partitioning column is highlighted.

</details>

<details>

<summary><strong>5. Set Storage Configuration</strong></summary>

**Overview**

The **Set Storage Configuration** step allows you to define how and where the data will be stored in AWS. It includes selecting the storage configuration and specifying the partitioning column to optimize data storage and retrieval.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

1. In the **Storage Config** column, click the action option.

<figure><img src="../../../.gitbook/assets/image (1648).png" alt=""><figcaption></figcaption></figure>

**a. Select Partitioning method**&#x20;

1. On the **Partitioning** page, select **Date Based** or **Range Based** to choose the partitioning method.

{% hint style="info" %}
Tip:&#x20;

**Tip: Here is the description for partitioning methods:**

* **Date-Based Partitioning:** Divides data based on time intervals such as day, month, or year.
* **Range-Based Partitioning:** Divides data into partitions based on defined value ranges of a column.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (1649).png" alt=""><figcaption></figcaption></figure>

**b. Select Configuration Parameters**

1. From the **AWS Storage Configuration** drop-down box, select the **AWS Config**, which you have already created.
2. From the **Partition Column** drop-down box, select the **required partition column**.
3. If you want to apply **same AWS config for al**l to all tables, then select ![](<../../../.gitbook/assets/image (1652).png>)to apply the same **AWS Config** to all tables.

{% hint style="info" %}
**Tip: Here is the description for AWS Configuration parameters:**

* AWS Storage Configuration: Defines the storage location and tiering strategy for archived data in AWS.
* Partition Column: Specifies the column used to divide data into partitions for efficient storage and processing.
{% endhint %}

> <mark style="color:red;">**Note:**</mark> Make sure to select the Configuration Parameters for all the tables.

<figure><img src="../../../.gitbook/assets/image (1650).png" alt=""><figcaption></figcaption></figure>

4. Click on **Save** button.&#x20;

</details>

<details>

<summary>6<strong>.Setup Partitioning</strong></summary>

**Overview**

Partitioning is the process of dividing data into smaller segments based on defined criteria, enabling efficient storage across different tiers and optimizing performance, cost, and lifecycle management.&#x20;

As part of partitioning, you need to specify Partitioning method, Configuration Parameters, Hot Storage Settings, Warm Storage Settings, Cold Storage settings, and Deep Archive Storage Settings.

Partitioning range can be defined at two levels:

* **Global Level** – Applies the same date range across all tables and storage tiers
* **Table Level** – Allows defining a specific date range for an individual table

This flexibility helps in managing data efficiently based on business and storage requirements.

&#x20;**Procedure**

The step-by-step instructions below help you understand the partitioning process.

**a. Configure Global Partitioning Range**

1. At the **top of the page**, locate the **Global Date Partitioning** option.

<figure><img src="../../../.gitbook/assets/image (1669).png" alt=""><figcaption></figcaption></figure>

2. Select the required **Storage Tier** (Hot, Warm, Cold, Deep Archive).
   1. Enter the **Date Range**:
   2. Specify the **Start Date**
   3. Specify the **End Date**
3. Click **Apply**.&#x20;
   1. Confirmation message: **“Applied: \[Start Date] to \[End Date] across all tables."**

<figure><img src="../../../.gitbook/assets/image (1670).png" alt=""><figcaption></figcaption></figure>

**b. Configure Table-Level Partitioning Range**

1. In the **Partitioning** column, click the **Action** option.

<figure><img src="../../../.gitbook/assets/image (1654).png" alt=""><figcaption></figcaption></figure>

2. A list of all **selected tables** will appear in a **drop-down selection list**.
3. From this list, you can:
   1. View all selected tables
4. The selected tables details appear below.&#x20;
   1. If you want to apply **same date ranges** to all tables, then select to ![](<../../../.gitbook/assets/image (1677).png>)  apply the same date ranges to all tables.

<figure><img src="../../../.gitbook/assets/image (1676).png" alt=""><figcaption></figcaption></figure>

**c. Define Hot Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Hot Storage for frequently accessed and critical data that requires fast retrieval. For example, Current year transactions, frequently accessed customer data, etc.

1. In the **Hot Storage Settings** section, select the **Enable Hot Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1672).png" alt=""><figcaption></figcaption></figure>

**d. Define Warm Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Warm Storage for moderately accessed data that is not needed instantly but still accessed occasionally. For example, Data from the last 6–12 months, Periodic reporting data, etc.

1. In the **Warm Storage Settings** section, select the **Warm Storage** checkbox.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1673).png" alt=""><figcaption></figcaption></figure>

**e. Define Cold Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Cold Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the **Cold Storage Settings** section, select the **Cold Storage** checkbox.
2. Specify the **From Date, To Date**, and **Retention Period**.

<figure><img src="../../../.gitbook/assets/image (1674).png" alt=""><figcaption></figcaption></figure>

**f. Define Deep Archive Storage Settings**

> <mark style="color:red;">**Note:**</mark> You can use the Deep Archive Storage to store rarely accessed data for long-term retention. For example, Data older than 1–3 years, Audit or compliance records, etc.

1. In the Deep **Archive Storage Settings** section, select the  **Deep Archive Storage checkbox**.
2. Specify the **From Date, To Date,** and **Retention Period.**

<figure><img src="../../../.gitbook/assets/image (1675).png" alt=""><figcaption></figcaption></figure>

3. After completing all the configuration, finally, click the **Save** button.

</details>

<details>

<summary><strong>6.Apply Data Filters</strong></summary>

**Overview**

As part of defining conditions, you need to configure Date-based filtering, which is used to select specific data for archiving based on a date or time condition. You can use the Quick Presets to specify the date ranges.

**Procedure**

The step-by-step instructions below help you understand the process of configuring date-based filtering.

1.  In the **Data Filter** column, click the **Action** option.



    <figure><img src="../../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>


2. From the **Date Column** drop-down box, select the required **column**.
3. From the **Quick Presets**, select the **required quick preset** choosing from L**ast 30 days, Last 90 days, Last 6 Months, Last Year,** and **Custom Range.**  For example, Last 6 Months.

> <mark style="color:red;">**Note:**</mark> Quick Presets are shortcut options that allow you to select commonly used date ranges quickly and accurately. Once a Quick Preset is selected, the Start Date and End Date fields are populated automatically.
>
> For example, if you want to archive data for the last 6 months, simply select the “Last 6 Months” Quick Preset. Alternatively, you can use the “Custom Range” Quick Preset to manually specify the required date range.

4. Finally, click the **Save** button. See the below image.

<figure><img src="../../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Define Retention Schedule</strong></summary>

**Overview**

The purpose of configuring a retention schedule for automated data archival enforcement is to define how long data should be retained and to ensure that archival (and eventual deletion, if applicable) happens automatically based on predefined rules.

For example, if a retention schedule is set to 12 months, any data older than 12 months will be automatically archived as per the defined schedule—without needing manual action.

**Procedure**

The step-by-step instructions below help you understand the process of configuring a retention schedule.

1.  In the **Retention Job** column, click the action option.



    <figure><img src="../../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>


2. On the **Retention Job Schedule** page, select the **table**.

&#x20;  The selected table name is populated in the Schedule Name field.

1. From the **Schedule Type** drop-down box, select the **required schedule type** choosing from **Daily, Weekly,** or **Monthly.** For example, Daily.&#x20;
2. In the **Description** field, enter an **appropriate description** for the retention schedule.
3. In the **Schedule Time** field, specify the schedule time by clicking the **Show Time Picker** ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAXCAYAAAALHW+jAAACGklEQVR4AexTO2tqQRD+SIqQQEgRkjRiY2trZWEh2IggKoqF+AA7C0UtBAXBShEtfSAogliICoKg2AlW/gsRRUEQfOLr3jsL58Tjg9uku/fA7M5+8+13Zmd2H3798PeAH/7+C34XdLFYoFKpwOfzQa1Ww+/3o1qtYrVafZNueDdrWCwWIRKJYLfbcTqdIJPJcDweYbPZIBaLmfANLQZdCVJWVqsVwWAQ0+kUiUQC4XCYzZPJBB6PBwaDAZ1OhwlcDgLB2WwGp9PJxOiILy8vmM/nSKfTbB+t6Uculwv00+12y/DzQSBYKBTw/v7OMuJI54IcFo/HsdvtUKvVOIifBYK9Xg8ajQaPj4884Zbz9PQElUqFbrd7FRYILpdLvL6+XpHW6zUOh4MAp+YMBgMBRguB4NfXF0ajEeG8EaZUKiGVSlEul/Hn6bPYeDzG5+cn888HgaBcLke73cZ+v+c5z8/PSKVSaDabaDQayOfz2Gw2aLVaUCgUPI9zBIJmsxnUuVAoxMX5WSKRsAwdDgfcbjers8lk4uOcIxB8e3tDJpNBNBpFLBZjmXBEmqnGgUAA2WwWdCPoGhF+bgJBCuj1etBLiUQioPp5vV52jejufXx8IJfLoV6vsy4T/9IeLgFaWywWDIdDtpmeXr/fB2VTKpVAndVqtUS7aTcFiUnHNxqNSCaTrCFUAp1OB2oSxe/ZXcF7G/6G/4OCvwEAAP//9KQKeQAAAAZJREFUAwCc7BLu3kqjGgAAAABJRU5ErkJggg==) icon.
4. In the **Notify on Failure** field, enter the **email IDs** of the recipients who should be notified in the event of a failure. You can enter multiple email IDs separated by commas.

<figure><img src="../../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

5. Finally, click the **Save** button.

</details>

<details>

<summary><strong>8.Deployment Configuration</strong></summary>

**Overview**

While creating an archival job, the purpose of a POD (in Kubernetes) is to act as the execution unit where the archival process runs. A POD contains one or more containers that perform tasks such as data extraction, transformation, and movement to archival storage.

**Procedure**

The step-by-step instructions below help you understand the process.

1. From the **Deployment Configuration** drop-down box, select **Kubernetes**.

<figure><img src="../../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

2. After selecting the deployment configuration
3. PODs are **automatically assigned at the Group level.**
4. When multiple groups are created, **separate PODs are automatically assigned to each group**

<figure><img src="../../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>9.Specify Batch Size Settings</strong></summary>

**Overview**

**Batch Size** specifies the number of records processed in a single batch during the archival operation. As part of specifying batch size, you can also define parallel processing.

**Procedure**

The step-by-step instructions below help you understand the process of specifying batch size.

1. On the **Archival Configuration** page (See the below image):

* From the **Deployment Configuration** drop-down box, select either **Amazon ECS Cluster** or  **Kubernetes**.
* Specify the **Batch Size, File Size (MB), Max Records/File, Parallel (Yes or No)**, and **Max Parallel**.

Here is the description for the above fields:

<table><thead><tr><th width="175.66668701171875">Field</th><th>Description</th></tr></thead><tbody><tr><td>Batch Size</td><td>This field specifies the <strong>number</strong> of records processed in each batch</td></tr><tr><td>File Size (MB)</td><td>This field specifies the <strong>maximum number</strong> of archived records stored in a single output file.</td></tr><tr><td>Max Records/File</td><td>This field specifies the <strong>maximum size</strong> of each archived file</td></tr><tr><td>Parallel (Yes or No)</td><td>This field enables to specify whether multiple batches are processed simultaneously or not. If the <strong>Yes</strong> option is selected, then <strong>Parallel</strong> processing is enabled.</td></tr><tr><td>Max Parallel</td><td>This field specifies the <strong>number of batches</strong> run in parallel.For example, if you enter <strong>5</strong> in the Max Parallel field, the system processes up to <strong>5 batches</strong> in parallel.</td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (2378).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>10.Resource Approval Rules for Archival Job</strong></summary>

**Overview**

Resource Approval Rules define the approval workflow required before an archival job is executed. These rules ensure that the appropriate stakeholders review and approve the job based on their roles and responsibilities.

For archival jobs, the approval workflow is typically configured with roles such as:

* **Data Steward** – Recommends the archival request.
* **Data Owner** – Provides final approval.

These rules are configured in the **Admin Settings module** under the Resource Approval section by selecting the **Resource Type as Archival Job**. Once defined, the configured rules automatically appear in the Archival Job creation screen.

When creating an archival job, users must select the appropriate users mapped to each role (for example, Data Steward and Data Owner). These users will be responsible for reviewing, recommending, and approving the archival request.

**Procedure**

The step-by-step instructions to Configure and Use Resource Approval Rules for Archival Job

**a. Configure Resource Approval Rules**

1. Navigate to **Admin Settings**.
2. Open the **Resource Approval Rules** section.
3. Select **Resource Type** as **Archival Job**.

<figure><img src="../../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

4. Define the approval workflow:
   1. **Role: Data Steward**
      1. Action: Recommend
      2. Accept Status: Recommended
      3. Reject Status: Rejected
      4. Is Required: Yes
      5. Priority: 1
   2. **Role: Data Owner**
      1. Action: Approve
      2. Accept Status: Approved
      3. Reject Status: Rejected
      4. Is Required: Yes
      5. Priority: 2

<figure><img src="../../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

**b. Assign Approvers During Archival Job Creation**

1. Navigate to the **Archival Job Creation** screen.
2. Scroll to the **Approval Section**:

<figure><img src="../../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

3. The system automatically displays approval roles based on configured rules.
4. For each role:
   1. **Data Steward** → Select a user from dropdown
   2. **Data Owner** → Select a user from dropdown

<figure><img src="../../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>11.Configuration name</strong></summary>

**Overview**

Archival Configuration is used to define and save all required setup details for the archival process. After entering the necessary information

**Procedure**

The below step-by-step instructions guide you through the procedure.

1. In the **Configuration Name** field, enter a **name** for the archival job.
2. In the **Description** field, enter a **description** relevant to the archival job.
3. Click the **Validate and Save** button.

<figure><img src="../../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

4. **Validate and Review Configuration** screen is displayed with all detailes.&#x20;

</details>

<details>

<summary><strong>12.Validate and Review Configuration</strong></summary>

**Overview**

The purpose of reviewing and saving an archival job after completing all configurations is to validate the setup and securely store it so the job can be executed accurately and consistently.

**Procedure**

The below step-by-step instructions guide you through the procedure.

1. On the **Validate and Review Configuration** page, select each **table,** and review the configuration.
2. In the **Configuration Name** field, enter a **name** for the archival job.
3. In the **Description** field, enter a **description** relevant to the archival job.
4. Click the **Save Configuration** button.

<figure><img src="../../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

5. The configuration is saved and displayed on the Archival Configuration List page. See the below image.

<figure><img src="../../../.gitbook/assets/image (1678).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Deploy Archival Job" %}
**Overview**

Deploying the archival job is to activate and run the job in the designated execution environment. Deployment ensures that all configurations, such as data sources, policies, and storage settings, are applied and executed correctly. It initiates the actual process of moving data from primary systems to archival storage.

***

**Procedure**

As part of deploying an archival configuration, you need to click the **Deploy** button corresponding to it on the Configuration List page. Once confirmed, the configuration is successfully deployed, and its status is updated to **Submitted**.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Access Archival Job</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, go to **SCIKIQ Archival.**&#x20;
2. Under S**CIKIQ Archival,** expand **Archival Jobs**, and then click **Existing Jobs**.

<figure><img src="../../../.gitbook/assets/1 (2).png" alt=""><figcaption><p>SCIKIQ Archival - Existing Jobs</p></figcaption></figure>

3. The **Archival Configuration** **List** page is displayed.

</details>

<details>

<summary><strong>2.View Details</strong></summary>

**Overview**

The **View Details (Eye Icon)** option allows you to view the complete information of an archival configuration without editing it. This provides a read-only view of both high-level metadata and detailed configuration settings.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Locate the required archival configuration.
2. Click on the **Eye Icon (View Details)** corresponding to the configuration.
3. The **Archival Job Details** screen is displayed.

<figure><img src="../../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

**Archival Job Details Screen**

**a. Configuration Information**

This section displays the basic details of the configuration:

* **Configuration Key:** Unique identifier for the archival configuration.
* **Name: E**xample: _Customer Table Archival_
* **Source Type:** Example: _ORACLE-EBS_
* **Connection Name:** Example: _ORACLE EBS AR_
* **Status:** Example: _DRAFT / SUBMITTED /_

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

***

**b. Configuration Details**

This section provides a structured breakdown of the archival setup:

* **Selected Tables:** Displays the list of tables selected for archival.
* **Partitioning:** Shows partition logic (if configured) used to segment data for archival.
* **Filters:** Displays conditions applied to identify which data should be archived.
* **Retention Job Configuration:** Defines how long archived data is retained and any associated deletion rules.
* **Compliance:** Displays compliance-related settings such as policies or regulatory requirements.
* **AWS Configuration:** Shows cloud storage details such as:
  * S3 bucket configuration
  * Storage path
  * Region details

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>3.Expand Icon – View Detailed Configuration</strong></summary>

**Overview**

The **Expand Icon ( > )** allows users to view complete archival job execution details, including request metadata, approval workflow, resource allocation, table-level configurations, partitioning strategy, retention policy, and storage settings.

This section provides a **read-only, consolidated view** of everything configured before deployment.

**Procedure**

The following step-by-step instructions guide you through the process.

**Expand the Configuration**

1. Navigate to the **Configuration List** page.
2. Locate the required configuration.
3. Click the **Expand Icon ( > ).**

<figure><img src="../../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

4. The **Detailed View Panel** is displayed.

<figure><img src="../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>4.Approval Workflow Execution</strong></summary>

**Overview**

Before deployment, the configuration may require approval based on predefined workflow rules.

**Procedure**

The following step-by-step instructions guide you through the process.

**Data Steward** Action

1. Login with **Data Steward** role
2. Go to the **Resource Approval screen**
3. The request is routed to the selected **Data Steward**.
4. The Data Steward can:
   1. **Recommend** → Moves request to next level
   2. **Reject** → Workflow stops
5. Click on the **Recommend** moving next level.&#x20;

<figure><img src="../../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

**Data Owner** Action

1. **Login with Data Owner role**
2. Go to the **Resource Approval screen**
3. After the Data Steward selects **Recommend**, the request is routed to the **Data Owner**
4. **Under Data Owner Action:** The request is assigned to the selected Data Owner.
5. **The Data Owner can:**
   1. **Approve** → Final approval; the request is completed
   2. **Reject** → Workflow stops
6. Click Approve Final approval the request is completed

<figure><img src="../../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

7. Once approved in the configured list, when the job status is set to Approved, the job becomes eligible for execution.

<figure><img src="../../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>5.Run Archival Job</strong></summary>

1. On the **Archival Configuration** **List** page, click the **Run** icon corresponding to the required archival configuration.

<figure><img src="../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

2. The Confirm Deployment message box is displayed.
3. On the **Confirm Run** message box, click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

4. A **Deployment request submitted successfully** message is displayed, and the configuration status is updated to **Submitted** on the Configuration Lists page.&#x20;

<figure><img src="../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (115).png" alt="" width="124"><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>6.Reconciliation Report</strong></summary>

**Overview**

The Reconciliation Report is automatically generated after an archival job is successfully deployed and executed. It validates the accuracy of the archival process by comparing source data with the archived data.

This report helps ensure that:

* All intended records are archived correctly
* No data loss or mismatch occurs during the process
* The archival job execution is complete and accurate

It provides a clear status of whether the data is fully matched, partially matched, or failed.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Deploy and execute the **Archival Job**.
2. Once execution is completed, the system automatically triggers the **Reconciliation process**.
3. Locate and open the **Reconciliation Report** section.

<figure><img src="../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

5. Review the report details:
   * Total source records
   * Total archived records
   * Failed or mismatched records
   * Overall reconciliation status
6. To download repot click "**Download XLSX"** Button.&#x20;

<figure><img src="../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>7.Delete Archival Job</strong></summary>

**Overview**

The Delete Archival Configuration option allows users to permanently remove an existing archival configuration from the system. This action is irreversible and should be performed only when the configuration is no longer required.

For example, when deleting **Archived GL Tables**, the system prompts for confirmation to prevent accidental deletion.

**Procedure**

The following step-by-step instructions guide you through the process.

1. Locate the configuration you want to delete (for example, **Archived GL Tables**).
2. Click on the **Delete** (🗑) icon associated with the configuration.

<figure><img src="../../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

The **Confirm Delete Configuration** dialog is displayed with the message:

* _“Are you sure you want to delete this configuration?”_
* _“This action cannot be undone.”_

5. Click **Confirm/Delete** to proceed.
   * Click **Cancel** to abort the action.
6. Upon confirmation, the configuration is permanently deleted from the system.

<figure><img src="../../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

</details>
{% endtab %}

{% tab title="Validate Archived Data" %}
**Overview**

Validation is the next step after successfully archiving data through SCIKIQ. As part of this process, you must verify the archived data in AWS S3 to ensure its integrity and completeness. This includes checking that the data is correctly stored, properly structured, and accessible across all configured storage tiers. Validation helps confirm that archival policies have been applied accurately and that the data can be retrieved when required. Overall, this step ensures reliability, compliance, and readiness for future access or audits.

***

**Procedure**

As part of validating the archived data, you need to first login to AWS Console and access the archived data. Once done, you can validate it.

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Login to AWS Console</strong></summary>

1.Open **AWS Console** in browser.

The IAM User Login page is displayed.

2.On the **IAM User Login** page, enter your **IAM User Name, Password**, and click the **Sign in** button.

<figure><img src="../../../.gitbook/assets/image (1597).png" alt=""><figcaption><p><strong>AWS Console</strong></p></figcaption></figure>

The **AWS Console Home** page page is displayed.

</details>

<details>

<summary><strong>2.Validate Parquet File</strong></summary>

1. On the **AWS Console Home** page, click **S3** in the **Recently Visited** section.

<figure><img src="../../../.gitbook/assets/image (1598).png" alt=""><figcaption><p>AWS Console Home - S3</p></figcaption></figure>

&#x20; The Buckets page is displayed.

2. On the **Buckets** page, in the **Search** field, enter the **Search Key** word.
3. From the **Search Results**, locate the **bucket** and click it.

<figure><img src="../../../.gitbook/assets/image (1599).png" alt=""><figcaption><p>AWS Console Home - S3</p></figcaption></figure>

The Objects page is displayed.&#x20;

4. On the **Objects** page, click the required **table**.

<figure><img src="../../../.gitbook/assets/image (1600).png" alt=""><figcaption><p>Objects Page</p></figcaption></figure>

The Storage Tier page is displayed.

5. On the Storage Tier page, click the **Parquet** file.

<figure><img src="../../../.gitbook/assets/image (1601).png" alt=""><figcaption><p>Storage Tier</p></figcaption></figure>

The Parquet page is displayed.

6. On the **Parquet** page, click the **Download** button.

<figure><img src="../../../.gitbook/assets/image (1602).png" alt=""><figcaption><p>Parquet page - Download Button</p></figcaption></figure>

The Parquet file is downloaded in the local system.

7. In your local system, browse to the **Downloads** location, and then **open** the Parquet file.

<figure><img src="../../../.gitbook/assets/image (1603).png" alt=""><figcaption></figcaption></figure>

&#x20;   The Parquet page is displayed.&#x20;

8. On the **Parquet** page, verify the **data.**

<figure><img src="../../../.gitbook/assets/image (1604).png" alt=""><figcaption><p>Parquet Page</p></figcaption></figure>

</details>

<details>

<summary>3<strong>.Validate AWS Glue</strong></summary>

1. In the **AWS Search** field, enter **glue**, and then on the **Services** menu, click **AWS Glue**.

<figure><img src="../../../.gitbook/assets/image (1605).png" alt=""><figcaption><p>AWS Services Page</p></figcaption></figure>

The AWS Glue page is displayed.

2. On the **AWS Glue** **page**, click **Databases** on the left navigation bar.

<figure><img src="../../../.gitbook/assets/image (1606).png" alt=""><figcaption><p>AWS Glue Page</p></figcaption></figure>

&#x20;   The Databases page is displayed. See the next slide.

3. On the **Databases** page, click **Table Data.**

<figure><img src="../../../.gitbook/assets/image (1607).png" alt=""><figcaption><p>Table Data </p></figcaption></figure>

&#x20;   The View Data message box is displayed.

4. On the **View Data** message box, click the **Proceed** button.

<figure><img src="../../../.gitbook/assets/image (1608).png" alt=""><figcaption><p>View Data Message Box</p></figcaption></figure>

The Athena Query Editor is displayed.

5. On the **Athena Query Editor**, make the required changes to the **Athena Query**, and then click the **Run** button.

<figure><img src="../../../.gitbook/assets/image (1609).png" alt=""><figcaption><p>Athena Query Editor</p></figcaption></figure>

The Query Results tab is displayed with the records.

6. On the **Query Results** tab, click the **Download Results CSV** button if you wish to download the results CSV format.

<figure><img src="../../../.gitbook/assets/image (1610).png" alt=""><figcaption><p><strong>Download Results CSV</strong> </p></figcaption></figure>

</details>
{% endtab %}
{% endtabs %}

***

## Related Topics

*
