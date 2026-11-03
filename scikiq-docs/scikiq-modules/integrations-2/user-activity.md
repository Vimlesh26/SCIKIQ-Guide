---
icon: poll-people
---

# User Activity

The **User Activity Logs** module in ScikIQ helps administrators and users keep track of all actions performed by individuals within the system. Whether it’s a page view, login attempt, or a password change, this module records detailed information. The purpose of this documentation is to provide a clear and step-by-step guide on how to use the **User Activity Logs** feature in ScikIQ, including practical examples.

### **1. Purpose of User Activity Logs in ScikIQ**

The **User Activity Logs** module in ScikIQ is crucial for monitoring user interactions with the system. This module helps to ensure that all activities, such as logging in, navigating pages, and changing passwords, are properly recorded and available for audit. The logs serve multiple purposes:

* **Security Monitoring**: Ensures all user actions are traceable to detect any unauthorized access or changes.
* **Troubleshooting**: Helps system administrators diagnose issues related to user access and system behavior.
* **Compliance**: Maintains an audit trail for regulatory and compliance purposes, ensuring transparency and accountability.
* **User Behavior Analysis**: Provides insights into how users are interacting with the system, which can help optimize the user experience.

By capturing and organizing this data, administrators can monitor and respond to potential security incidents or troubleshoot issues effectively.

### **2. Module Overview**

The **User Activity Logs** module in ScikIQ includes three main components:

* **User Page View Logs**: Tracks which pages users visit and when.
* **Login History**: Records all login events, session durations, and browser/host information.
* **Change Password Logs**: Tracks any password changes made by users.

<figure><img src="../../.gitbook/assets/image (1311).png" alt=""><figcaption></figcaption></figure>

Each of these components allows you to filter logs by different attributes (e.g., name, email, time), providing a flexible and detailed audit trail.

### **2.1. User Page View Logs**

The **User Page View Logs** component records every page a user visits within the system. It allows administrators to see which pages are frequently accessed and when, helping to identify popular features and detect any unauthorized or suspicious access.

**Step-by-Step Guide**

1. **Accessing the User Activity Logs**:
   * First, log into the ScikIQ  with client Admin role.
   * In the navigation menu, go to the **User Activity Logs** section.

<figure><img src="../../.gitbook/assets/image (1301).png" alt=""><figcaption></figcaption></figure>

1. **Viewing User Page View Logs**:
   * In the **User Activity Logs** section, click on **User Page View Logs**.
   * You will see the option to filter the results by **Name**, **Email**, **Page**, and **Time**.

<figure><img src="../../.gitbook/assets/image (1303).png" alt=""><figcaption></figcaption></figure>

1. **Applying Filters**:
   * In the **Search** panel, you can enter search parameters to narrow down the results:
     * **Name**: The user’s name (e.g., John Doe).
     * **Email**: The user’s email address (e.g., vimlesh.singh@scikiq.com).
     * **Page**: The page that the user visited (e.g., Dashboard, Settings).
     * **Time**: The time when the page was visited.

<figure><img src="../../.gitbook/assets/image (1304).png" alt=""><figcaption></figcaption></figure>

1. **Viewing the Logs**:
   * After entering your filter criteria, the system will display a list of page view logs that match your search.
   * The logs will show details about the user, the page they visited, and the time of the visit.

<figure><img src="../../.gitbook/assets/image (1302).png" alt=""><figcaption></figcaption></figure>

### **2.2. Login History**

**Use Case**

The **Login History** component tracks every login and logout event within the system. This log is useful for security auditing, as it shows which users logged in, when, and from which device (host and browser). It also helps administrators monitor session durations.

**Step-by-Step Guide**

1. **Accessing Login History**:
   * In the **User Activity Logs** section of the ScikIQ Admin portal, click on **Login History**.

<figure><img src="../../.gitbook/assets/image (1306).png" alt=""><figcaption></figcaption></figure>

1. **Filtering Login History**:
   * You can filter the login history logs by:
     * **Name**: The user’s name (e.g., Vimlesh).
     * **Email**: The user’s email address (e.g., vimlesh.singh@scikiq.com).
     * **Event**: The type of login event (e.g., successful login).
     * **Login Time**: The time the user logged in.
     * **Logout Time**: The time the user logged out.
     * **Session Duration**: The length of time the user stayed logged in.
     * **Logout Type**: Whether the user logged out manually or automatically.
     * **Host**: The device from which the user logged in.
     * **Browser**: The browser used to log in.

<figure><img src="../../.gitbook/assets/image (1307).png" alt=""><figcaption></figcaption></figure>

1. **Viewing the Login History**:
   * After applying the filters, the system will display all login events based on the criteria you’ve set.

<figure><img src="../../.gitbook/assets/image (1308).png" alt=""><figcaption></figcaption></figure>

### **2.3. Change Password Logs**

The **Change Password Logs** capture any instance when a user changes their password. This log is particularly important for security audits, as it allows administrators to track password changes and detect any unauthorized password reset requests.

**Step-by-Step Guide**

1. **Accessing Change Password Logs**:
   * From the **User Activity Logs** section in the Admin portal, click on **Change Password Logs**.

<figure><img src="../../.gitbook/assets/image (1309).png" alt=""><figcaption></figcaption></figure>

1. **Filtering Change Password Logs**:
   * In the **Search** panel, filter the logs by:
     * **Name**: The user’s name (e.g., vimlesh).
     * **Email**: The user’s email address (e.g., vimlessingh@scikiq.com).
     * **Event**: The "Password Change" event.
     * **Password Change Date/Time**: The time the password was changed.
2. **Viewing the Change Password Logs**:
   * After applying the filters, you’ll see the list of users who changed their passwords, along with the time and date of the change.

<figure><img src="../../.gitbook/assets/image (1310).png" alt=""><figcaption></figcaption></figure>

### **3. Managing Password Expiry, Reset, Forgotten Password, and Changing Password**

### **3.1 Managing Password Expiry Settings**

The **Password Expiry Settings** ensure that user passwords are periodically updated, which enhances system security. As an administrator, you can set up reminders and expiration periods to manage password changes.

#### **Steps: Setting Password Expiry Days**

1. **Login as Admin**: Log into the ScikIQ with client Admin role.
2. **Navigate to Admin Settings**: Go to the **Admin Settings** section from the main dashboard.

<figure><img src="../../.gitbook/assets/image (1314).png" alt=""><figcaption></figcaption></figure>

3. **Select Password Settings**: Under **Password Policy**, click on **Password Expiry Settings**.

<figure><img src="../../.gitbook/assets/image (1315).png" alt=""><figcaption></figcaption></figure>

4. **Set Expiry Days**: Enter the number of **Password Expiry Days** (e.g., 90 days) in the corresponding field.
5. **Configuring Password Change Reminder 1-Set First Reminder**: In the **Password Change Reminder 1** field, enter the number of days before password expiration when the first reminder should be sent (e.g., 14 days).
6. **Set Second Reminder**: In the **Password Change Reminder 2** field, enter the number of days before password expiration when the second reminder should be sent (e.g., 7 days).

<figure><img src="../../.gitbook/assets/image (1316).png" alt=""><figcaption></figcaption></figure>

7. **Save Configuration**: Click **Update** to apply the changes.

<figure><img src="../../.gitbook/assets/image (1317).png" alt=""><figcaption></figcaption></figure>

8. user will receive Reminder 1, 14 days before the registered milestone, as shown in the attached screenshot.

<figure><img src="../../.gitbook/assets/image (268).png" alt=""><figcaption></figcaption></figure>

### **3.2 Changing Your Password**

The **Change Password** feature allows users to update their passwords if they are logged in and wish to change it to a new one.

**Steps**:

1. **Login to Your Account**: Open ScikIQ and log into your account using your current password.
2. **Navigate to Profile Settings**: Click on your username or profile icon in the top right corner of the dashboard and select **Profile** from the dropdown.

<figure><img src="../../.gitbook/assets/image (1318).png" alt=""><figcaption></figcaption></figure>

3. **Select Reset Password Option**: On your profile page, click on **Reset Password** (or **Change Password**).

<figure><img src="../../.gitbook/assets/image (1319).png" alt=""><figcaption></figcaption></figure>

4. **Enter Current Password**: In the **Current Password** field, enter the password you are currently using.
5. **Enter New Password**: Enter your **New Password** in the **New Password** field. Ensure it meets the system’s password complexity requirements (e.g., minimum length, special characters).
6. **Confirm New Password**: Re-enter the **New Password** in the **Confirm New Password** field to ensure it matches.

<figure><img src="../../.gitbook/assets/image (1320).png" alt=""><figcaption></figcaption></figure>

7. **Save New Password**: Click **update password** to apply the new password.

<figure><img src="../../.gitbook/assets/image (1321).png" alt=""><figcaption></figcaption></figure>

8. After clicking the 'Update Password' button, you will be directly redirected to the login screen to re-authenticate your account

<figure><img src="../../.gitbook/assets/image (1322).png" alt=""><figcaption></figcaption></figure>

> **Note**: After changing your password, make sure to update any saved passwords in your browser or password manager to avoid login issues.

### **3.3 Forgotten Password Recovery**

The **Forgot Password** feature allows users to recover their account by resetting their password if they have forgotten it.

**Steps**:

1. **Navigate to Login Page**: On the ScikIQ login page, click the **Forgot Password** link below the login form.

<figure><img src="../../.gitbook/assets/image (1323).png" alt=""><figcaption></figcaption></figure>

2. **Enter Email Address**: Enter the **email address** associated with your account and click **Submit**.

<figure><img src="../../.gitbook/assets/image (1324).png" alt=""><figcaption></figcaption></figure>

3. **Receive Reset Code**: Check your inbox for a **Password Reset Email** containing a code to reset your password.

<figure><img src="../../.gitbook/assets/image (1326).png" alt=""><figcaption></figcaption></figure>

4. **Select Reset Code:** Copy the reset code provided in the password reset email and paste it on the password reset page.
5. **Enter New Password**: Enter your **New Password** in the designated field, ensuring it meets the security criteria (e.g., minimum length, uppercase, numbers).
6. **Confirm New Password**: Re-enter the new password in the confirmation field to ensure it matches.

<figure><img src="../../.gitbook/assets/image (1327).png" alt=""><figcaption></figcaption></figure>

6. **Submit**: Click the **Submit** button to update your password. Upon successful reset, you will receive a confirmation email stating **"Password Reset Succeeded."**

<figure><img src="../../.gitbook/assets/image (1330).png" alt=""><figcaption></figcaption></figure>

7. **Login**: You can now log in to your account using the new password.

<figure><img src="../../.gitbook/assets/image (1329).png" alt=""><figcaption></figcaption></figure>



***

