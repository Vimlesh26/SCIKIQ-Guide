---
icon: page
---

# Validating Data

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

Validation is the next step after successfully archiving data through SCIKIQ. As part of this process, you must verify the archived data in AWS S3 to ensure its integrity and completeness. This includes checking that the data is correctly stored, properly structured, and accessible across all configured storage tiers.&#x20;

Validation helps confirm that archival policies have been applied accurately and that the data can be retrieved when required. Overall, this step ensures reliability, compliance, and readiness for future access or audits.

***

### Procedure

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

***

### Related Topics

* [**Creating a Table Archival Job**](creating-a-table-archival-job.md)
* [**Creating a File Archival Job**](creating-a-file-archival-job.md)
* [**Managing Existing Jobs**](managing-existing-jobs.md)
* [**Retrieving Data**](retrieving-data.md)
* [**Managing Deployment Configs**](managing-deployment-configs.md)
* [**Deleting Archived Data**](deleting-archived-data.md)
* [**Managing Retention Schedules**](managing-retention-schedules.md)
* [**Using Archival Dashboard**](using-archival-dashboard.md)
* [**Using Cube Manager**](using-cube-manager.md)
* [**Using Cube Viewer**](using-cube-viewer.md)
