---
icon: user-group-simple
---

# User Activity

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

The **User Activity Logs** module in ScikIQ is crucial for monitoring user interactions with the system. This module helps to ensure that all activities, such as logging in, navigating pages, and changing passwords, are properly recorded and available for audit. The logs serve multiple purposes:

* **Security Monitoring**: Ensures all user actions are traceable to detect any unauthorized access or changes.
* **Troubleshooting**: Helps system administrators diagnose issues related to user access and system behavior.
* **Compliance**: Maintains an audit trail for regulatory and compliance purposes, ensuring transparency and accountability.
* **User Behavior Analysis**: Provides insights into how users are interacting with the system, which can help optimize the user experience.

By capturing and organizing this data, administrators can monitor and respond to potential security incidents or troubleshoot issues effectively.

***

### **User Activities**

The expandable panels below guide you through the user activities.

<details>

<summary><strong>Accessing User Activity Page</strong></summary>

1. **Accessing the User Activity Logs**
   1. First, log into the ScikIQ with client Admin role.
   2. In the navigation menu, go to the **User Activity Logs** section.

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Viewing User Page View Logs</strong></summary>

**Overview**

The **User Page View Logs** component records every page a user visits within the system. It allows administrators to see which pages are frequently accessed and when, helping to identify popular features and detect any unauthorized or suspicious access.

1. **Viewing User Page View Logs**
   1. In the **User Activity Logs** section, click on **User Page View Logs**.
   2. You will see the option to filter the results by **Name**, **Email**, **Page**, and **Time**.

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

2. **Search Option**
   1. In the **Search** panel, you can enter search parameters to narrow down the results:
   2. **Name**: The user’s name (e.g., John Doe).
   3. **Email**: The user’s email address (e.g., vimlesh.singh@scikiq.com).
   4. **Page**: The page that the user visited (e.g., Dashboard, Settings).
   5. **Time**: The time when the page was visited.

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

3. **Viewing the Logs**
   1. After entering your filter criteria, the system will display a list of page view logs that match your search.
   2. The logs will show details about the user, the page they visited, and the time of the visit.

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Viewing Login History</strong></summary>

**Overview**&#x20;

The **Login History** component tracks every login and logout event within the system. This log is useful for security auditing, as it shows which users logged in, when, and from which device (host and browser). It also helps administrators monitor session durations.

**Procedure**<br>

1. **Accessing Login History**:
   1. In the **User Activity Logs** section of the ScikIQ Admin portal, click on **Login History**.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

2. **Filtering Login History**
   1. You can filter the login history logs by:
      1. **Name**: The user’s name (e.g., Vimlesh).
      2. **Email**: The user’s email address (e.g., vimlesh.singh@scikiq.com).
      3. **Event**: The type of login event (e.g., successful login).
      4. **Login Time**: The time the user logged in.
      5. **Logout Time**: The time the user logged out.
      6. **Session Duration**: The length of time the user stayed logged in.
      7. **Logout Type**: Whether the user logged out manually or automatically.
      8. **Host:** The device from which the user logged in.
      9. **Browser**: The browser used to log in.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

3. **Viewing the Login History**
   1. After applying the filters, the system will display all login events based on the criteria you’ve set.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary><strong>Viewing Change Password Logs</strong></summary>

**Overview**

The **Change Password Logs** capture any instance when a user changes their password. This log is particularly important for security audits, as it allows administrators to track password changes and detect any unauthorized password reset requests.**Step-by-Step Guide**

**Procedure**

1. **Viewing Change Password Logs**
   1. From the **User Activity Logs** section in the Admin portal, click on **Change Password Logs**.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

2. **Filtering Change Password Logs**
   1. In the **Search** panel, filter the logs by:
   2. **Name**: The user’s name (e.g., vimlesh).
   3. **Email**: The user’s email address (e.g., vimlessingh@scikiq.com).
   4. **Event**: The "Password Change" event.
   5. **Password Change Date/Time**: The time the password was changed.

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

3. **Viewing the Change Password Logs**
   1. After applying the filters, you’ll see the list of users who changed their passwords, along with the time and date of the change.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

</details>

### Related Topics

* [**Admin Settings**](admin-settings.md)
