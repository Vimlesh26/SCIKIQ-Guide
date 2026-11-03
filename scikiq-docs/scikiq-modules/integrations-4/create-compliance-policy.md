# Create Compliance Policy

**Contents**

* [**Instructions for Using this Page**](create-compliance-policy.md#instructions-for-using-this-page)
* [**Overview**](create-compliance-policy.md#overview)
* [**Procedure**](create-compliance-policy.md#procedure)
* [**Related Topics**](create-compliance-policy.md#related-topics)

***

## Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* Hover over an italicized annotated term (italic, blue, dotted and underlined) to view its meaning. Here is an example: [_<mark style="color:blue;">**Host Name**</mark>_](#user-content-fn-1)[^1]_<mark style="color:blue;">**.**</mark>_
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

## Overview

Creating a compliance policy as part of an archival process is essential to ensure that archived data is handled in accordance with regulatory, security, and business requirements.

Importance of creating a creating a compliance policy:

* **Regulatory Compliance:** Ensures that data is retained, protected, and deleted in line with regulations (e.g., GDPR, SOX, DORA), avoiding legal penalties.
* **Defined Retention Rules:** Specifies how long data should be stored (e.g., 7 years), preventing both premature deletion and unnecessary storage.
* **Data Protection & Security:** Enforces controls such as encryption, access restrictions, and immutability to safeguard sensitive data.
* **Audit & Traceability:** Maintains proper audit logs and evidence to support audits, investigations, and reporting requirements.
* **Risk Management:** Minimizes risks related to data breaches, non-compliance, and operational failures.

***

## Procedure

In the SCIKIQ application, the process of archival involves a series of steps including inputting Policy Basic Details, specifying Data Retention Settings and Data Security Settings, configuring Access Control Settings, Setting up Audit Logging, Data Privacy Settings, Incident response Settings, and Conflict Resolution Settings.&#x20;

The expandable panels below guide you through the process.

<details>

<summary><strong>1.Input Policy Basic Details</strong></summary>

1. On the **SCIKIQ Left Navigation Bar**, under **SCIKIQ Archival,** expand **Compliance**, and then click **Compliance Policies**.&#x20;

<figure><img src="../../.gitbook/assets/image (213).png" alt="" width="563"><figcaption><p>Compliance Policies Menu Item </p></figcaption></figure>

The Compliance Policies page is displayed.&#x20;

2. On the **Compliance Policies** page, click the **Create Policy** button.&#x20;

<figure><img src="../../.gitbook/assets/image (214).png" alt=""><figcaption><p>Compliance Policies Page</p></figcaption></figure>

The Create New Policy dialogue box is displayed.&#x20;

3. On the **Create New Policy** dialogue box:

<figure><img src="../../.gitbook/assets/image (215).png" alt="" width="563"><figcaption><p>Create New Policy Dialogue Box</p></figcaption></figure>

* Specify the **Policy Title, Description, Policy Category, Data Classification, Effective Date, Version,** and **Policy Domain.** &#x20;
* From the **Attach Frameworks** drop-down box, select the **applicable framework**.&#x20;

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

<figure><img src="../../.gitbook/assets/image (216).png" alt=""><figcaption><p>Data Retention Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>3.Specify Data Security Settings</strong></summary>

1. In the **Policy Domains** section, select the **Data Security panel**.

&#x20;     The Data Security panel is expanded.

2. In the expanded **Data Security panel**, select the **Encryption at Rest** and **Encryption at Rest** checkboxes.

<figure><img src="../../.gitbook/assets/image (217).png" alt=""><figcaption><p>Data Security Settings</p></figcaption></figure>

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

Procedure

1. In the **Policy Domains** section, select the **Access Control panel.**

&#x20;     The Access Control panel is expanded.

2. On the expanded **Access Control panel,** specify the **Users, Data Owner Group,** and **Allowed Roles.**
3. Select the **Approval Required checkbox** based on the requirement.

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption><p>Access Control Settings</p></figcaption></figure>

</details>

<details>

<summary><strong>5.Setup Audit Logging</strong></summary>

**Overview**&#x20;

Configuring Audit Logging enables you to define the level of detail captured in system logs and the duration for which these logs are retained. These settings support regulatory compliance and audit requirements by ensuring that relevant activities are recorded and preserved for the required retention period.&#x20;

The following section provides step-by-step instructions to help you set up audit logging.

**Procedure**

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

<figure><img src="../../.gitbook/assets/image (219).png" alt=""><figcaption><p>Audit Log Settings</p></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (220).png" alt=""><figcaption><p>Data Privacy Settings</p></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (221).png" alt=""><figcaption><p>Incident Response Settings</p></figcaption></figure>

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

<figure><img src="../../.gitbook/assets/image (222).png" alt=""><figcaption><p>Conflict Resolution Strategy Settings</p></figcaption></figure>

The policy is created and displayed on the Compliance Policies page. See the below image.

<figure><img src="../../.gitbook/assets/image (223).png" alt=""><figcaption><p>Compliance Policies Page</p></figcaption></figure>

{% hint style="info" %}
Tip:&#x20;

To view details of a policy, click the View  ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACkAAAAoCAYAAABjPNNTAAADMklEQVR4AeyYe0hTURzHv7uuzJQi0zR7UhYs0KAyfBTVDE0tygw1w6hcSSVTs+jh1oQoTa2MEs1EK6Sihln9odiDEqE006LS3ilpaabiCx/YbOfgrg1i7m6DJd0Lv3PPPb/fOb/P/Z7HxmUGR8HFYOj6+q0V5rQhjL/eWEjineFkC3MYya3LtCB1BZrTx0OaSn1eSV5JUylgqnGMWpPqHyu0tXeirPINHpZWoPr9F/T09pmKjR3HIEgCkqcsgk+IFP5hsYiRn0F8YiYiYo9DHLQXW/YoUF5VDZVqkE1kTIUzZM2HWoRHJSA9V4mu7h5Yj7fCBr8VkEqC4bXUlbJ8rmtAtOw05CcvoKOzm7YZU3CCJNMpjT+Fhu/NNOdKz0XIz0nCwahwbA70QapCipw0GRzsbUEusgSIwuRlyLOhpjdk448WJKRkU/VIsmlT7al6Tc2tCI2UwSNAAkXKRfVvvwNidoVCIBCQMFS8rMH5nJsYGPhFnw0p9IIkG+R6wT31v6QmNoeryBmTbSci88ot1NU30vbiR2W4X1IO1wXOcHK0o22kuFtcispX70jVINMLsrevH59qG7QSTLGbhP7+AbR3dGm1/2xtxxihEBNsrNl2lUql7l/PPnOt6AVpNc4Sweu9wTDD4W8/1sHCggFZl5qkNtZW8HRzQXNLm5bqs6Y7wnu5myaM83046whdPRa7YJ3PMjbq2YsaPH3+GmEbfZGedAAJ+yXIPSvH/DkzcePOA3btMuoXi9waCKI825ljRW9IodAC0TtDELDai6YgU3g0OQt5ykKI5s2G7yp3MAIGsqRM3C4qoTGkjyx2u5ba1MGx0BuSjEum/Uj0NsTtDoPl2DF0x2Zczgc5wMnuDoo4hMdPqkgoyBRnpR6Gn9iD3enUYUDBCZKMzzACbForRuG1NCjiJFiyUETPRXI2kmPJ39sTBO5qxjGqMOljrHGG1CQkqq4Ru+PciTgUXEqmpsxOhHzfDriI5oK8jCbW2LvBkMYm5tL/X4HUycxD6pSHg5NXkoNYOkN5JXXKw8E5+pQ016e/kURllTTHJ78/c+oCZSF1BZnbx0OaagZ4Jf8rJX8DAAD//2kYVkgAAAAGSURBVAMA1+E+y+iyUJwAAAAASUVORK5CYII=) icon corresponding to it.

To update a policy, click the Edit ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAlCAYAAAAuqZsAAAABi0lEQVR4AeyYPUgDMRTH/3QTBVE3wdVJ0EFw0cnJWRwFB1Fw93MSLYKCOJUufgyurqLTuSh1OVBwEFdBRLBaRKtDr94LRO7s0bskl6aFhHtJyNf73f89MiRTbdKSQZMWCyYamJBij09FmLQgfAiMJvp6u2HCyHfQasCCkyb7FkxUfauYVSxOgfL3Dy6uXLyXPuKWRs5ryTGC2skdY20rj1XfXt9Kkc7rDaYO5nlVfH6V8fxSZH5v7h6wsXsAgmUDCatUwch5du8Q5841NpfnMDTQzzAItlLxWD9plRoYQVH4zpwCckcnf3DTUxNYX5xFR3tbUia2LhUwDkVKsVP9iuCcSxcLM5Po6er0R8Q+ZbAoKEKgMI6PDVNXypTA6kFlV+allOJ/IQ2mE4rgpMB0Q0mBNQJKCsy9vWdXAW3mRomumlP8LN5KhZJvplYHFJ2rBKYLSgpsdGQQhdN9ZvntJbkrgTzHmJJiMWcrTVswUfmsYlYxUQVE17dOjpl6hvqvaEgxE89PQZ9BuF8AAAD//0RjOAMAAAAGSURBVAMArCjbwpAnZcMAAAAASUVORK5CYII=) icon corresponding to it.

To delete a policy, click the Delete ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACkAAAAoCAYAAABjPNNTAAABf0lEQVR4AeyYwSsEYRjGn8a2y02rjUT+AQdysJTmIEobKclF2tMmN6W54OKi/Q8o/4NWERfFkgOXPTg5EuWgJOGws3wO22i+t+b75qvP1Dv11PS9z7zvb56ZmulzGgk4HCTgYEhTDymU5P3jC2xKdmMhSGHq7c7ChsRsmaSQMqPNNYY0lT4nyUmqJuD7DdRu73B6cdPUw9OzahvSr/1Ofnx+YbO8i9mih8LiKpa9Mta3d5paKG1gZmntt75/dEYCRCloQwabZ9JpdOayf5TraIfjGGkP7S5trRmsFOfgjgwiP9RPan56HIWJ0eA9KZ9rQ4pJr2/vODiponJ8TuryuoZ63Rd2bcWC1J6qeCFDKgZG2jlJMhrFAiepGBhp/y9JkoCiEAuyr6cLY/kB0UeqVKoFk+4wxNdJaoi4GAtSDN/ySrg63JOqWvn5AZlyI6LQtliQdFuzFYY0lScnyUmaSsBUn+S+k7a2/qjkQ0na2PILzpSBhiBlJttrDGnqCXwDAAD//5KIW10AAAAGSURBVAMAzIG0vChw33wAAAAASUVORK5CYII=) icon corresponding to it.
{% endhint %}

</details>

***

## Related Topics

* [Connect SCIKIQ to Source Database](/broken/pages/1miPFvCEFxfy7uZat3C4)
* [Configure Table Classification](/broken/pages/fy1vjHIN7Nys8uAuddaO)
* [Create Compliance Framework](/broken/pages/J0o8JvIQ5NXn822xZNDA)
* [Create Compliance Policy](/broken/pages/5gBXOCk95Uv7C11YfBLO)
* [Configure AWS Setup](/broken/pages/26PZ6KCui7ZjC3abzdND)
* [Create Archival Job](/broken/pages/54s7haLhTK625sePPPzh)
* [Setup Deployment Platform](/broken/pages/qpdRebf35FBbmvMZlRTo)
* [Deploy Archival Job](/broken/pages/hEN0BpaQWg865JKIDrtG)
* [Manage Deployment Configurations](/broken/pages/ctJKSQVRrDMRLHYUvlWy)
* [Validate Archived Data](/broken/pages/RWHaxNCgJded7Q8xd9FP)
* [View Archived Data](/broken/pages/6xWaChqxS1moikwvFJk7)
* [Delete Archived Data](/broken/pages/oXzQfmDzcrDAFOL2TO5w)

[^1]: **Host Name** refers to the **address** of the computer/server where your database is located.
