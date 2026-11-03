---
icon: circle-user
---

# User Login

### Azure Entra App Registration and Configuration Guide

1.  <mark style="color:blue;">**App Registration in Microsoft Entra**</mark>    \
    To register an application in Microsoft Entra (formerly Azure AD):

    1. Go to the Microsoft Entra admin center.
    2. Navigate to Identity > Applications > App registrations.
    3. Click on '+ New registration'.
    4. Fill in the application details (Name, Redirect URI, etc.).
    5. Click 'Register' to create the application.

    <figure><img src="../../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>
2.  <mark style="color:blue;">**App Overview**</mark>    \
    After registration, you'll see an overview of your app including:

    1. Application (client) ID
    2. Directory (tenant) ID
    3. Redirect URIs
    4. Supported account types

    <figure><img src="../../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure>
3.  <mark style="color:blue;">**Creating Client Secrets**</mark>    \
    To authenticate your app with a token:

    1. Go to 'Certificates & secrets'.
    2. Click on '+ New client secret'.
    3. Add a description and expiration.
    4. Click 'Add'.
    5. Copy and store the secret value securely.

    <figure><img src="../../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>
4.  <mark style="color:blue;">**Assigning Microsoft Graph API Permissions**</mark>    \
    To configure Graph API permissions:

    1. Navigate to 'API permissions'.
    2. Click on '+ Add a permission'.
    3. Choose 'Microsoft Graph'.
    4. Select the required delegated or application permissions.
    5. Click 'Grant admin consent' for organization-wide access.

    <figure><img src="../../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure>

### **Logs into ScikIQ via Microsoft**

* Go to your ScikIQ instance (e.g., `https://dev4.scikiq.com`).
* On the login screen, click **Login with Microsoft**.

<figure><img src="../../.gitbook/assets/image (1366).png" alt=""><figcaption></figcaption></figure>

* Enter **email or phone**, then click **Next**.

<figure><img src="../../.gitbook/assets/image (1367).png" alt=""><figcaption></figcaption></figure>

* Enter the **password**, then click **Next**.

<figure><img src="../../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

* You're now signed into ScikIQ using Microsoft credentials.

<figure><img src="../../.gitbook/assets/image (1369).png" alt=""><figcaption></figcaption></figure>
