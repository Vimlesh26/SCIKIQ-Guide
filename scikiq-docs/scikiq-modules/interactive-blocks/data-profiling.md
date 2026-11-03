---
hidden: true
icon: calendar-lines-pen
---

# Data Profiling

### What is Data Profiling ?

* Data profiling is the process of examining, analyzing, and summarizing data from various sources to understand its structure, quality, and content. The main goal of data profiling is to gain insights into the characteristics and overall health of the data, which is crucial for various data-related tasks such as data integration, data cleansing and data analytics.
* **In** ScikIQ **Data Profiling** tool can help explore the data content, validate it against existing Metadata, and identify Data Quality gaps as well as deficiencies in existing data artifacts, such as logical and physical models, DDL, and model descriptions.
* In the Data Profiling tab, there are various capabilities available, such as performing exploratory data analysis (EDA), generating different versions of tables for future use, tailoring model training to meet specific data requirements, and deploying models for further utilization on new, unseen data.

### **Why is Data profiling needed?**

Data profiling is essential for understanding, assessing, and improving data quality. It supports data integration, analysis, and compliance, aiding decision-making, and risk management. By revealing data issues early, it saves costs and resources, making it a crucial step in effective data management across various industries.

### **Step for the Data Profiling**

**Step 1**: When you click the "Data Profiling" option mentioned above, it will lead you to the following page, providing the opportunity to commence data modeling.

<figure><img src="../../.gitbook/assets/image (969).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (970).png" alt=""><figcaption></figcaption></figure>

**Step 2**: On this page, clicking the Table/Topic icon allows you to retrieve your desired source connections

<figure><img src="../../.gitbook/assets/image (971).png" alt=""><figcaption></figcaption></figure>

**Step 3**: On selecting the Table/Topic icon, drop down box will appear you will can retrieve your desired source connections.



<figure><img src="../../.gitbook/assets/image (972).png" alt=""><figcaption></figcaption></figure>

The dropdown box includes a keyword search to quickly find desired connections.

<figure><img src="../../.gitbook/assets/image (973).png" alt=""><figcaption></figcaption></figure>

**Step 4**: After choosing the desired source connections, users are directed to a page where we can start applying various data profiling functions (located on the left side of the screen) to the data table.

<figure><img src="../../.gitbook/assets/image (974).png" alt=""><figcaption></figcaption></figure>

### Actions via SCIKIQ's Suggestions Menu

ScikIQ data profiling provides a variety of functions tailored to diverse data types, encompassing integers, text and dates. Additionally, it offers functions such as data cleaning, custom fields, data masking and anonymization, detailed further in the document.

<figure><img src="../../.gitbook/assets/image (975).png" alt=""><figcaption></figcaption></figure>

ScikIQ data profiling includes a Default/standard version.<br>

<figure><img src="../../.gitbook/assets/image (976).png" alt=""><figcaption></figcaption></figure>

By clicking the "save" icon on the rightmost side of the page, users can generate a new data version.

<figure><img src="../../.gitbook/assets/image (978).png" alt=""><figcaption></figcaption></figure>

Upon clicking the "save" icon, a dialog box will appear to assist the user in creating a new version.

<figure><img src="../../.gitbook/assets/image (979).png" alt=""><figcaption></figcaption></figure>

Enabling the toggle button allows users to create a new data version.

<figure><img src="../../.gitbook/assets/image (980).png" alt=""><figcaption></figcaption></figure>

A data version created by the user will now be visible in the dropdown menu. Users can create multiple versions in the same manner.

<figure><img src="../../.gitbook/assets/image (981).png" alt=""><figcaption></figcaption></figure>

ScikIQ data profiling provides a function that allows users to set limits while fetching data, helping them control the amount of data retrieved.

<figure><img src="../../.gitbook/assets/image (982).png" alt=""><figcaption></figcaption></figure>

### Data Profiling Functions for Various Data Types

### **Delete Column Function**

Specifically addressing the "Integer" data type, numerous functions are available. One of these functions is the "Delete Column Function." Users can easily select the column they wish to remove, such as the "active" column in the provided example, and execute the function to delete it.

<figure><img src="../../.gitbook/assets/image (983).png" alt=""><figcaption></figcaption></figure>

Upon executing the function, the specified column will be removed.

<figure><img src="../../.gitbook/assets/image (984).png" alt=""><figcaption></figcaption></figure>

ScikIQ Data Profiling also provides an execution history for users to examine and reconsider their actions.

<figure><img src="../../.gitbook/assets/image (985).png" alt=""><figcaption></figcaption></figure>

Users can also clear the execution history to restore previous actions.

<figure><img src="../../.gitbook/assets/image (986).png" alt=""><figcaption></figcaption></figure>

A green flash message will appear, signifying that clearing the history will allow the user to access previously executed actions.

<figure><img src="../../.gitbook/assets/image (987).png" alt=""><figcaption></figcaption></figure>

### **Data Masking Function**

Addressing the "Integer" data type, one of the functions available is Data Masking. Users can easily select columns containing sensitive information that requires masking.

Data Masking Auto Function is an automated data protection mechanism. It identifies and masks sensitive or personally identifiable information (PII), like Social Security numbers, credit card numbers, or email addresses, using predefined rules and algorithms.

<br>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FElopyipDx7AQd5lM0Klz%2Fimage.png?alt=media&#x26;token=67c614fc-958b-4e95-8722-3a897c5c863a" alt=""><figcaption></figcaption></figure>

Data Masking Custom Function is a customizable data security feature. users can define their rules and methods for masking sensitive data, allowing specific control over the process.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FPizLr9MrC8xXYNwRM4CJ%2Fimage.png?alt=media&#x26;token=3f0bd61b-1a5f-410f-8007-94e8e905ebdc" alt=""><figcaption></figcaption></figure>

Data Masking Protegrity Function is a menu showing Protegrity API connections created via data store creation. It facilitates API calls to mask PII data using the Protegrity API connection.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FB9sUCrXR7c8jJlTdVPWd%2Fimage.png?alt=media&#x26;token=8872c377-9108-4cbf-b396-132f52558a29" alt=""><figcaption></figcaption></figure>

### **Calculate Length Function**

* Focusing on the "Integer" data type, one of the functions at your disposal is "Calculate Length."&#x20;
* The "Calculated Length" is a data profiling function used to determine the length of a data field or column in a dataset. It's often applied to text or string data types.&#x20;
* Users can effortlessly choose columns to apply this function. When a user highlights a specific target column, such as "Avg Sale Amt," and initiates the "Calculate Field" function, a new column is automatically generated (with the default name "Avg Sale Amt\_Col\_Value\_Length\_1") to show the desired result.&#x20;
* Users have the flexibility to rename the column according to their preferences.

<figure><img src="../../.gitbook/assets/image (988).png" alt=""><figcaption></figcaption></figure>

### **Data Anonymization Function**&#x20;

* Looking at the "Integer" data type, one of the available functions is Data Anonymization. Data Anonymization is a data profiling function that focuses on protecting the privacy and confidentiality of individuals by replacing personally identifiable information (PII) or sensitive data with anonymized or pseudonymous values.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2F8vP9TEHENNv3TnRNhWAt%2Fimage.png?alt=media&#x26;token=40331ecc-8c8d-4b9b-a2b0-be4ad67ec8a1" alt=""><figcaption></figcaption></figure>

Users can easily select columns to utilize this function. When a user highlights a particular target column, like "Agent Name," and activates the "Data Anonymization" function, the desired outcome is presented.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2F6KQseMZD3FJNKZDAIjjt%2Fimage.png?alt=media&#x26;token=6352d133-2a66-4cd5-b5e6-af9c89d0c610" alt=""><figcaption></figcaption></figure>

### Text Data Type Functions

### **Change to lower case**

Users have the convenience of selecting the column they want to convert to lowercase, as demonstrated in the provided example with the "productcatname" column and can execute this function to accomplish the task.

<figure><img src="../../.gitbook/assets/image (989).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (991).png" alt=""><figcaption></figcaption></figure>

### **Change to Title case**

* Users can conveniently pick the column they desire to convert to title case, just as exemplified with the "productcatname" column in the provided example and execute this function to complete the task.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FAKuf55neRXislwe7SxML%2Fimage.png?alt=media&#x26;token=6975e019-e471-4e59-b91d-516f6c5edd46" alt=""><figcaption></figcaption></figure>

### **Change to upper case**

Users can easily choose the column they wish to convert to uppercase, as shown in the provided example using the "productcatname" column and can execute this function to achieve the desired outcome.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2Fykf37omXr4d8JJieLWjg%2Fimage.png?alt=media&#x26;token=974702d3-2185-4dad-8e94-2bfba830ab2f" alt=""><figcaption></figcaption></figure>

### **Extract part of the Text Function**

The function "Extract part of the Text" in ScikIQ data profiling tool is a feature that allows users to isolate and capture specific portions or segments of text within a given data field or column. \
This function is particularly useful for data preparation and analysis when you need to extract specific information from a larger text string.&#x20;

Users can utilize various combinations when using this function to create a new column with the extracted text. Here are a few examples:

For instance, a user may extract a portion of the text starting from the beginning and ending at the last character to create a new column.

<figure><img src="../../.gitbook/assets/image (992).png" alt=""><figcaption></figcaption></figure>

Alternatively, users can opt for a combination where they choose text from the beginning to a specific index and the end index, resulting in the desired extraction.

<figure><img src="../../.gitbook/assets/image (993).png" alt=""><figcaption></figcaption></figure>

Another option is selecting text from an index to the beginning index, up to a number before the end, and ending at the character 2.

<figure><img src="../../.gitbook/assets/image (994).png" alt=""><figcaption></figcaption></figure>

In a different scenario, users might extract text by choosing from the number before the end to character 2, up to the number before the end and character 0. This results in the desired text extraction.

<figure><img src="../../.gitbook/assets/image (995).png" alt=""><figcaption></figcaption></figure>

### **Search and replace**

The **"Search and replace"** function in a data profiling tool is a feature that allows users to search for specific patterns, words, or characters within a dataset and replace them with another specified pattern.

The following example illustrates the process of replacing "ROOT CATALOG" with "TOOR CATALOG" in the "productcatname" column when creating a new column.

<figure><img src="../../.gitbook/assets/image (996).png" alt=""><figcaption></figcaption></figure>

Additionally, it shows how the word "CATALOG" was substituted with "Root," resulting in the creation of a new column containing "ROOT ROOT

<figure><img src="../../.gitbook/assets/image (997).png" alt=""><figcaption></figcaption></figure>

### **Set as Numeric Function**

When a user triggers the "Set as Numeric" function, it automatically generates a brand-new column and transforms the text column into an integer column.

<figure><img src="../../.gitbook/assets/image (998).png" alt=""><figcaption></figcaption></figure>

### **Number Extraction**

The "Number Extraction" function is a capability that empowers users to retrieve particular sections or segments of numeric data within a given data field or column.

<figure><img src="../../.gitbook/assets/image (999).png" alt=""><figcaption></figcaption></figure>

Here's an example of how users can effortlessly extract numbers from text with just a simple click of this function's button.

<figure><img src="../../.gitbook/assets/image (1000).png" alt=""><figcaption></figcaption></figure>

### **Extract string part**

The function "Extract String Part" allows users to extract a specific portion or segment of a text string based on certain criteria or parameters.

To utilize this function the following example, the target column is 'skq\_created\_by'.

<figure><img src="../../.gitbook/assets/image (1001).png" alt=""><figcaption></figcaption></figure>

The criteria could include specifying the starting point (e.g., the position of the first character you want to extract) and the length of the segment to be extracted, or it could involve searching for a specific substring or pattern within the text and extracting the text around that pattern.

<figure><img src="../../.gitbook/assets/image (1002).png" alt=""><figcaption></figcaption></figure>

### **Split the text in parts URL parts**

* To use this function, users need to specify the number of parts they want to divide a particular text into. In the example below, the user 'TPR\_PLLTD' can split specific text into three parts while specifying the separator as '\_'. The result will be displayed in two consecutive columns, 'TPR' and 'PLLTD'.

<figure><img src="../../.gitbook/assets/image (1003).png" alt=""><figcaption></figcaption></figure>

### **Date Format Function**

It allows user to specify how dates should be displayed or interpreted. This function can be useful when working with date data in various formats and you need to standardize the representation of dates.

<figure><img src="../../.gitbook/assets/image (1004).png" alt=""><figcaption></figcaption></figure>

In below example "dd/mm/yy" is a date format that represents a date with the day, month, and year in a specific order.

<figure><img src="../../.gitbook/assets/image (1005).png" alt=""><figcaption></figcaption></figure>

**Fill the cell with value**

The data profiling function fill the cell with value, allows users to populate an empty or missing cell in a dataset with a specified value.

<figure><img src="../../.gitbook/assets/image (1006).png" alt=""><figcaption></figcaption></figure>

This feature proves particularly valuable when users encounter gaps or missing data points within a dataset and seek to replace those gaps with a designated value. To illustrate this, we've filled the specified column, "mba\_abbr," with the value 0, enhancing data completeness and making it better suited for analysis.

<figure><img src="../../.gitbook/assets/image (1007).png" alt=""><figcaption></figcaption></figure>

This feature additionally assists users in substituting values from a specific column with designated ones.

<figure><img src="../../.gitbook/assets/image (1008).png" alt=""><figcaption></figcaption></figure>

To demonstrate, we've filled the designated column, "mba\_abbr," with values extracted from the "mbv\_id" column, thereby improving data completeness and rendering it more suitable for analysis.

<figure><img src="../../.gitbook/assets/image (1009).png" alt=""><figcaption></figcaption></figure>

### **Fill empty cell with above Function**

The function "Fill empty cell with above Function" in a data profiling tool is a feature that allows users to automatically populate or fill in empty or blank cells within a dataset.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FLtsHDK3Xg8q8C0l8T3Nr%2Fimage.png?alt=media&#x26;token=12d93e97-d89b-4211-a396-01884d1a9755" alt=""><figcaption></figcaption></figure>

As illustrated below, when a user encounters a column of numerical data containing empty cells, they can employ this function to automatically fill those empty cells with the value from the cell directly above. This feature can save time and reduce errors, particularly when working with datasets that contain missing or incomplete information.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FLtsHDK3Xg8q8C0l8T3Nr%2Fimage.png?alt=media&#x26;token=12d93e97-d89b-4211-a396-01884d1a9755" alt=""><figcaption></figcaption></figure>

The above operations pertain to individual columns, whereas there are also suggestions that apply to the entire dataset.

<figure><img src="../../.gitbook/assets/image (1010).png" alt=""><figcaption></figcaption></figure>

1: Delete empty row: Delete empty rows refers to the action of removing rows in a dataset that contain no data or have missing values, leaving only rows with valid information.

2: Remove duplicate rows: Removing duplicate rows involves the process of eliminating identical or redundant rows from a dataset, ensuring that each row in the dataset is unique.

3: Remove white spaces: Removing white spaces means eliminating any extra spaces, tabs, or other whitespace characters from a text or dataset, resulting in a cleaner and more uniform appearance.

### **SMART SUGGESTIONS**

* The ScikIQ data profiling tool includes a suggestion box that serves as a user guide.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2FcpypwvJ2YKkm1oWgj34H%2Fimage.png?alt=media&#x26;token=3eb6b615-fdce-4425-8100-1c520d1786a7" alt=""><figcaption></figcaption></figure>

The suggestion box leverages Scikiq's intelligence to analyze the entire dataset. It then offers recommendations for actions and operations during exploratory data analysis (EDA). These recommendations include tasks such as deleting empty columns, changing column data types, applying masking, and many other suggestions to enhance data quality and insights.

If the same suggestion applies to multiple columns, you can utilize the "Select All" checkbox to choose and apply that recommendation to all the required columns.

<figure><img src="../../.gitbook/assets/image (1011).png" alt=""><figcaption></figcaption></figure>

In the image above, it indicates a strong correlation between these columns. To address this correlation, various options are available. By clicking on the 'i' icon, you can view which columns are related to the selected one.

<figure><img src="../../.gitbook/assets/image (1012).png" alt=""><figcaption></figcaption></figure>

The column shown in the image above contains entirely repeated values. In this case, it's advisable to apply the suggested actions to address this redundancy.

<figure><img src="../../.gitbook/assets/image (1013).png" alt=""><figcaption></figcaption></figure>

The image above reveals the presence of special characters in the column, which can potentially pose issues during exploratory data analysis (EDA). To mitigate this, you can take recommended actions.

<figure><img src="../../.gitbook/assets/image (1014).png" alt=""><figcaption></figcaption></figure>

The column displayed in the image above indicates the presence of duplicate values. In such instances, it's recommended to execute the suggested actions for that column.

<figure><img src="../../.gitbook/assets/image (1015).png" alt=""><figcaption></figcaption></figure>

The column depicted in the image above contains names of specific entities or items. In this context, it's advisable to implement the suggested actions for that column as relevant.

<figure><img src="../../.gitbook/assets/image (1016).png" alt=""><figcaption></figcaption></figure>

The column shown in the above image contains values that are integers but have been interpreted as strings, resulting in their display as "int\_like." In this scenario, it's recommended to carry out the suggested actions for that column.

<figure><img src="../../.gitbook/assets/image (1017).png" alt=""><figcaption></figcaption></figure>

The column shown in the above image contains values that are floats but have been interpreted as strings, resulting in their display as "float\_like." In this scenario, it's recommended to carry out the suggested actions for that column.Comment

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FGyC3in6fubVUF0mncApZ%2Fuploads%2F9kHWhLjClYEGSVvswss7%2Fimage.png?alt=media&#x26;token=ddf67c0f-51d6-47f4-b3fc-b8fd42b63f20" alt=""><figcaption></figcaption></figure>

The column shown in the above image contains values that are date and time but have been interpreted as something different, resulting in their display as "date\_like." In this scenario, it's recommended to carry out the suggested actions for that column.



This suggestion box conveniently offers both previous and next options for users to navigate through the suggestions.

<figure><img src="../../.gitbook/assets/image (1018).png" alt=""><figcaption></figcaption></figure>

