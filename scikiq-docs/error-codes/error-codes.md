---
icon: message-exclamation
---

# Error Codes

### Module: Common

#### **SCIK-0001: Page Not Found**

**Explanation:**  The requested page URL could not be located on the server.

**Cause:**

* The URL was entered incorrectly.
* The page no longer exists or has been moved.
* Broken or outdated link.

**Resolution:**

* Double-check the URL for typos.
* Use the application’s navigation or search feature.
* Contact support if the issue persists.

#### **SCIK-0002: Internal Server Error**

**Explanation:** An unexpected system error occurred on the server while processing the request.

**Cause:**

* Server configuration issue.
* Unexpected exception in backend code.
* Resource exhaustion (e.g., memory, CPU).

**Resolution:**

* Retry after some time.
* Contact the administrator or support team.
* Monitor logs for system-level exceptions.

#### **SCIK-0005: API Key is Required**

**Explanation:**\
An API key was not provided in the request.

**Cause:**

* Missing or invalid API key in request headers.
* Client not registered or authenticated.

**Resolution:**

* Provide a valid API key in the request.
* Ensure the API key is active and linked to a valid user.

#### **SCIK-0006: Entity Key is Required**

**Explanation:** The request did not include a required entity key.

**Cause:**

* Client omitted the entity key parameter.
* Mapping configuration is incomplete.

**Resolution:**

* Add the appropriate entity key to your request.
* Review documentation or integration configuration.

#### **SCIK-0010: Technical Error, Please Contact Admin**

**Explanation:** A general technical error occurred during the operation.

**Cause:**

* Backend component failure.
* Invalid system configuration.
* Unexpected exception not handled by the system.

**Resolution:**

* Contact the administrator or support.
* Check system logs for more details.

#### **SCIK-0311: Server is Temporarily Unavailable**

**Explanation:** The {} server is currently down or unreachable.

**Cause:**

* Server maintenance or downtime.
* Network issue or server crash.

**Resolution:**

* Wait for the server to restart.
* Contact the SCIKIQ help desk for further assistance.

#### **SCIK-0332: Debezium CDC Does Not Work on Standalone MongoDB**

**Explanation:** Change Data Capture (CDC) with Debezium is not supported on standalone MongoDB instances.

**Cause:**

* CDC was attempted on a non-replicated MongoDB setup.

**Resolution:**

* Set up MongoDB with replica set configuration.
* Refer to CDC and Debezium integration documentation.

#### **SCIK-0333: Email Server Not Configured Properly**

**Explanation:** The system could not connect to the configured email server.

**Cause:**

* Missing or incorrect email server settings.
* Authentication failure or connectivity issue.

**Resolution:**

* Validate SMTP/email server configuration in admin settings.
* Contact your administrator.

### Module: Admin error codes

**SCIK-0090: Logo updated successfully**\
**Explanation:** The system has successfully updated the logo.\
**Cause:**

* A valid logo file was uploaded.
* No errors during processing.

**Resolution:**

* No action needed.
* Confirm the logo is displaying as expected.

**SCIK-0091: Please choose the file for Logo**\
**Explanation:**\
No logo file was selected for upload.\
**Cause:**

* User did not select any file before submitting.

**Resolution:**

* Select a valid file for upload.
* Retry the upload process.

***

**SCIK-0093: Your Account has been Cancelled**\
**Explanation:** The user account has been cancelled and access revoked.\
**Cause:**

* Account was cancelled by user or admin.
* Policy violation or administrative action.

**Resolution:**

* Contact support or admin for clarification.
* Request reactivation if applicable.

**SCIK-0094: Incorrect Email or Password**\
**Explanation:**\
Login failed due to invalid credentials.\
**Cause:**

* Incorrect email or password entered.
* User may have mistyped credentials.

**Resolution:**

* Verify credentials and try again.
* Use password recovery if needed.

**SCIK-0096: Merchant Name is required**\
**Explanation:** Merchant name field was left empty.\
**Cause:**

* Missing merchant name input.

**Resolution:**

* Enter a valid merchant name before submission.

**SCIK-0097: Merchant Type is required**\
**Explanation:** Merchant type field was not specified.\
**Cause:**

* Missing merchant type input.

**Resolution:**

* Provide a valid merchant type before submission.

**SCIK-0098: Merchant email is required**\
**Explanation:** Merchant email address is mandatory but missing.\
**Cause:**

* Merchant email field left empty.

**Resolution:**

* Enter a valid email address before submitting.

**SCIK-0105: Role is required**\
**Explanation:**\
User role information is required but missing.\
**Cause:**

* Role field was left empty.\
  **Resolution:**
* Specify a valid role before submission.

**SCIK-0106: Id is required**\
**Explanation:** A required identification field is missing.\
**Cause:**

* ID was not provided in the request.

**Resolution:**

* Provide the necessary ID before proceeding.

**SCIK-0108: Role already exist!**\
**Explanation:** The role name entered already exists in the system.\
**Cause:**

* Duplicate role name attempted to be created.

**Resolution:**

* Choose a unique role name.
* Check existing roles before adding new ones.

**SCIK-0234: Data migration deletes not allowed**\
**Explanation:**\
Deletion is not permitted during data migration process.\
**Cause:**

* Attempt to delete data while migration is active.

**Resolution:**

* Wait for migration to complete before deleting.
* Verify migration status before deleting data.

**SCIK-0343: Unable to save admin settings**\
**Explanation:**\
System failed to save administrative settings.\
**Cause:**

* Server or database issue during save operation.
* Invalid input data.

**Resolution:**

* Retry after verifying data correctness.
* Check server and database connectivity.

**SCIK-0344: Unable to fetch admin settings**\
**Explanation:**\
Failed to retrieve admin settings from the system.\
**Cause:**

* Database or network connectivity issues.
* Permission problems.

**Resolution:**

* Check system connectivity.
* Verify user permissions.

**SCIK-0345: Failed to retrieve email configuration list**\
**Explanation:**\
Email configuration list could not be loaded.\
**Cause:**

* Database errors or corrupted data.
* Access permission issues.

**Resolution:**

* Verify database health.
* Check user authorization.

**SCIK-0346: Unable to delete email configuration**\
**Explanation:**\
Failed to delete the specified email configuration.\
**Cause:**

* Dependencies or constraints prevent deletion.
* Database or permission issues.

**Resolution:**

* Ensure no dependent resources exist.
* Verify permissions and retry.

***

**SCIK-0347: Failed to save email configuration**\
**Explanation:**\
System was unable to save the email configuration.\
**Cause:**

* Validation errors or server failure.

**Resolution:**

* Check input data for correctness.
* Retry saving after fixing errors.

**SCIK-0348: Failed to retrieve email templates**\
**Explanation:**\
Unable to fetch email templates from the system.\
**Cause:**

* Database or connectivity issues.
* Permission denied.

**Resolution:**

* Check database connection.
* Verify user rights.

**SCIK-0349: Failed to delete email template**\
**Explanation:**\
System could not delete the selected email template.\
**Cause:**

* Template is in use or locked.
* Insufficient permissions.

**Resolution:**

* Ensure template is not referenced elsewhere.
* Verify permission and try again.

**SCIK-0350: Unable to save email template**\
**Explanation:**\
Saving the email template failed.\
**Cause:**

* Invalid template data or server error.

**Resolution:**

* Correct template content and retry.
* Check server logs for more details.

**SCIK-0351: Failed to retrieve ServiceNow configuration data**\
**Explanation:**\
System could not load ServiceNow integration settings.\
**Cause:**

* Configuration missing or corrupted.
* Network or permission issues.

**Resolution:**

* Verify ServiceNow configuration details.
* Check network connectivity and credentials.

**SCIK-0486: Unable to save logo**\
**Explanation:**\
System failed to save the logo image.\
**Cause:**

* File size or format invalid.
* Storage or permission error.

**Resolution:**

* Use supported image formats and sizes.
* Check file storage permissions.

**SCIK-0487: Unable to save theme settings**\
**Explanation:**\
Saving theme customization failed.\
**Cause:**

* Invalid theme parameters.
* Backend failure or permission issues.

**Resolution:**

* Verify theme data validity.
* Retry after resolving server issues.

**SCIK-0488: Unable to view settings**\
**Explanation:**\
System failed to display the requested settings page.\
**Cause:**

* Permission denied or server error.

**Resolution:**

* Verify user permissions.
* Check system status and logs.

**SCIK-0489: Unable to view admin settings**\
**Explanation:**\
Failed to load the admin settings interface.\
**Cause:**

* Access restrictions or backend failure.

**Resolution:**

* Confirm admin privileges.
* Investigate server or database issues.

**SCIK-0490: Unable to load AWS configuration**\
**Explanation:**\
AWS configuration data could not be loaded.\
**Cause:**

* AWS credentials missing or invalid.
* Connectivity or permissions problem.

**Resolution:**

* Verify AWS configuration and credentials.
* Check network connectivity.

**SCIK-0491: Unable to retrieve updated AWS configuration**\
**Explanation:**\
Failed to fetch the latest AWS configuration.\
**Cause:**

* Sync failure or access issues.

**Resolution:**

* Confirm update process completed successfully.
* Validate AWS access rights.

### Module : API Hub

**SCIK-0293: IP Restrictions**\
**Explanation:**\
Access denied due to IP address restrictions on the API.\
**Cause:**

* Request originated from an IP address not allowed by policy.
* IP whitelist or blacklist settings are in effect.

**Resolution:**

* Verify and update allowed IP addresses in APIHub settings.
* Contact administrator to adjust IP restrictions if necessary.

**SCIK-0294: Token Expired**\
**Explanation:**\
Authentication token used in the request has expired.\
**Cause:**

* Token validity period has elapsed.
* User session timed out or token was revoked.

**Resolution:**

* Re-authenticate to obtain a new token.
* Implement token refresh mechanisms if applicable.

**SCIK-0302: Policy with this name already exists**\
**Explanation:**\
A policy with the specified name already exists in the system.\
**Cause:**

* Duplicate policy name entered during creation.

**Resolution:**

* Use a unique name when creating a new policy.
* Check existing policies before adding.

**SCIK-0303: Policy name cannot be Null**\
**Explanation:**\
Policy creation or update failed due to missing policy name.\
**Cause:**

* Policy name field left empty or null.

**Resolution:**

* Provide a valid policy name before submitting.

**SCIK-0304: Policy description cannot be Null**\
**Explanation:**\
Policy description is mandatory but missing.\
**Cause:**

* Policy description field left empty or null.

**Resolution:**

* Enter a detailed description for the policy.

**SCIK-0318: Token Invalid**\
**Explanation:**\
The authentication token provided is invalid or corrupted.\
**Cause:**

* Token format is incorrect or token has been tampered with.
* Token was generated improperly.

**Resolution:**

* Request a new valid token through authentication.
* Ensure token generation and transmission are secure.

**SCIK-0319: Application configuration not set properly. Please configure file storage location: {}**\
**Explanation:**\
File storage location is not configured properly in the application settings.\
**Cause:**

* Missing or incorrect file storage path configuration.
* Application setup incomplete or corrupted.

**Resolution:**

* Configure the file storage location correctly in the application config.
* Verify configuration files and reload settings.

**SCIK-0339: Unable to retrieve client information**\
**Explanation:**\
System failed to fetch client details.\
**Cause:**

* Database connectivity issues.
* Client ID invalid or missing.

**Resolution:**

* Check database connection status.
* Verify client identifiers and try again.

**SCIK-0340: Unable to retrieve client list**\
**Explanation:**\
System could not fetch the list of clients.\
**Cause:**

* Backend service unavailable.
* Permission or data access issues.

**Resolution:**

* Check service health and user permissions.
* Retry after resolving backend issues.

**SCIK-0403: Unable to attach cloud group policy**\
**Explanation:**\
System failed to attach the specified cloud group policy.\
**Cause:**

* Policy not found or invalid.
* Insufficient permissions or API errors.

**Resolution:**

* Verify the policy ID and user access rights.
* Retry the operation after correcting errors.

**SCIK-0481: Unable to fetch data from API hub**\
**Explanation:**\
System failed to retrieve data from the API hub service.\
**Cause:**

* Network issues or API service downtime.
* Incorrect API endpoint or credentials.

**Resolution:**

* Check network connectivity and API service status.
* Verify API endpoint URLs and authentication credentials.

### Module: Auth

**SCIK-0033: Email already exist**\
**Explanation:**\
The email provided is already registered in the system.\
**Cause:**

* Email address is already used by another user account.
* Duplicate registration attempt.

**Resolution:**

* Use a different email address for registration.
* Recover existing account if you forgot credentials.

**SCIK-0053: Please enter valid verifycode key**\
**Explanation:**\
Verification code entered is invalid or malformed.\
**Cause:**

* Verification code format incorrect.
* Expired or wrong verification code used.

**Resolution:**

* Enter the correct verification code.
* Request a new verification code if expired.

**SCIK-0099: Code required**\
**Explanation:**\
A required code was not provided.\
**Cause:**

* Missing input in code field.

**Resolution:**

* Provide the necessary code before submission.

**SCIK-0101: Code not match**\
**Explanation:**\
Entered code does not match the expected value.\
**Cause:**

* User input error or outdated code.

**Resolution:**

* Re-enter the correct code.
* Request a fresh code if necessary.

**SCIK-0104: Entity is required**\
**Explanation:**\
Entity field is mandatory but missing.\
**Cause:**

* Entity data not provided in request.

**Resolution:**

* Enter the valid entity information.

**SCIK-0111: Entity already exist!**\
**Explanation:**\
The entity you are trying to add already exists.\
**Cause:**

* Duplicate entity creation attempt.

**Resolution:**

* Use a unique entity name or identifier.

**SCIK-0115: Records does not exist.**\
**Explanation:**\
Requested records were not found in the system.\
**Cause:**

* Query for non-existent or deleted records.

**Resolution:**

* Verify query parameters and retry.

**SCIK-0190: Group name already exist**\
**Explanation:**\
The group name is already taken.\
**Cause:**

* Duplicate group name input.

**Resolution:**

* Choose a unique group name.

**SCIK-0192: Group updated**\
**Explanation:**\
Group information has been successfully updated.\
**Cause:**

* Valid update request processed successfully.

**Resolution:**

* No further action needed.

**SCIK-0193: Group deleted**\
**Explanation:**\
Group has been successfully deleted.\
**Cause:**

* Valid delete request processed.

**Resolution:**

* No further action needed.

**SCIK-0196: Application is running...**\
**Explanation:**\
System health check confirms the application is operational.\
**Cause:**

* Application is up and responding to requests.

**Resolution:**

* No action needed.

**SCIK-0272: @{} - your role and entity has been updated by {}. Updated Entity and Roles are:- {}**\
**Explanation:**\
User role and entity have been updated by an administrator.\
**Cause:**

* Administrative changes to user roles/entities.

**Resolution:**

* Review updated roles and entities.
* Contact admin if unexpected.

**SCIK-0337: {} not in allowed domains.**\
**Explanation:**\
The domain of the input is not allowed by policy.\
**Cause:**

* Domain is not in the permitted list.\
  **Resolution:**
* Use an email or domain from the allowed list.
* Request domain addition if necessary.

***

**SCIK-0338: Unable to save merchant details.**\
**Explanation:**\
System failed to save merchant information.\
**Cause:**

* Validation errors or backend failures.\
  **Resolution:**
* Verify merchant data and try again.
* Check system logs for errors.

***

**SCIK-0342: Failed to retrieve application settings.**\
**Explanation:**\
System could not load the application settings.\
**Cause:**

* Database or file access issues.\
  **Resolution:**
* Verify settings source availability.
* Retry after fixing connectivity.

**SCIK-0352: Unable to create group.**\
**Explanation:**\
Group creation process failed.\
**Cause:**

* Validation error or server problem.\
  **Resolution:**
* Check input data and retry.
* Investigate server logs.

**SCIK-0375: Unable to save page settings.**\
**Explanation:**\
Saving page configuration failed.\
**Cause:**

* Incorrect data or backend failure.

**Resolution:**

* Validate page settings input.
* Retry save operation.

**SCIK-0376: Unable to retrieve page settings.**\
**Explanation:**\
Fetching page settings was unsuccessful.\
**Cause:**

* Access issue or backend service down.

**Resolution:**

* Verify permissions.
* Check backend availability.

### Module: User

**SCIK-0050: User already activated**\
**Explanation:**\
The user account has already been activated.\
**Cause:**

* User previously completed the activation process.
* System did not update activation status correctly.
* Duplicate activation request sent by user.

**Resolution:**

* Inform the user that activation is already complete.
* Guide user to login or recover password if needed.
* Avoid repeated activation attempts by disabling the button.

***

**SCIK-0052: User don’t exist**\
**Explanation:**\
The specified user does not exist in the system.\
**Cause:**

* Incorrect or unregistered user ID or email entered.
* User account deleted or never created.
* Typographical errors in the user input.

**Resolution:**

* Verify user details before submission.
* Suggest user registration if no account exists.
* Implement input validation to catch typos.

**SCIK-0054: Please enter your email address**\
**Explanation:**\
Email address input is missing or empty.\
**Cause:**

* User skipped the email input field.
* Form validation did not catch the missing email.
* Email field was cleared due to technical issues.

**Resolution:**

* Prompt user to enter a valid email address.
* Add mandatory field validation on email input.
* Provide email format help or examples.

**SCIK-0055: Please enter registered email address**\
**Explanation:**\
A registered email address is required to proceed.\
**Cause:**

* Email provided does not exist in the user database.
* User attempting to log in with an unregistered email.
* Mistakes or typos in the email input.

**Resolution:**

* Ask user to input an email registered in the system.
* Provide option to register if user is new.
* Check email existence before authentication.

**SCIK-0057: Please enter verify code**\
**Explanation:**\
Verification code input is missing.\
**Cause:**

* User did not enter the verification code.
* Code not generated or sent correctly.
* Verification code expired or invalid.

**Resolution:**

* Prompt user to enter the verification code.
* Allow resending verification code if necessary.
* Validate code format and expiry before acceptance.

**SCIK-0058: Please enter password**\
**Explanation:**\
Password input is missing.\
**Cause:**

* User omitted the password field.
* Form validation missed empty password.
* Password input reset due to technical issues.

**Resolution:**

* Make password field mandatory with validation.
* Prompt user to enter password before submitting.
* Ensure password input is securely handled.

**SCIK-0059: Please enter Confirm Password**\
**Explanation:**\
Confirmation password is required but missing.\
**Cause:**

* User skipped confirming the password.
* Form validation did not enforce confirm password input.
* Browser or client error cleared the field.

**Resolution:**

* Enforce mandatory confirm password field.
* Prompt user to fill confirm password before submitting.
* Match confirm password with original password.

**SCIK-0060: Please provide password and Confirm password same**\
**Explanation:**\
Password and confirmation password do not match.\
**Cause:**

* User typed different strings in password and confirmation fields.
* Copy-paste errors between the two inputs.
* Input field truncation or formatting issues.

**Resolution:**

* Validate passwords match before submission.
* Prompt user with clear error message if mismatched.
* Use show/hide password toggles to reduce input errors.

**SCIK-0061: Please enter valid verification code**\
**Explanation:**\
Entered verification code is invalid or malformed.\
**Cause:**

* Code format does not comply with expected pattern.
* Code expired or already used.
* User mistyped the verification code.

**Resolution:**

* Validate code format on the client side.
* Allow user to request a new verification code.
* Display helpful error messages on invalid code.

**SCIK-0062: Password length must be between 8-20 characters. It must contain a number and a special character.**\
**Explanation:**\
Password does not meet complexity or length requirements.\
**Cause:**

* User chose a password that is too short or too long.
* Password lacks required numeric or special characters.
* Complexity rules not enforced in UI.

**Resolution:**

* Enforce password policy during input.
* Provide real-time feedback on password strength.
* Document password requirements clearly for users.

**SCIK-0063: Confirm password don’t match**\
**Explanation:**\
Confirmation password does not match the original password.\
**Cause:**

* User entered different values in password fields.
* Input field reset or cleared unexpectedly.
* User confusion over input fields.

**Resolution:**

* Perform immediate password match validation.
* Provide clear error messages for mismatches.
* Use visibility toggle to avoid typos.

**SCIK-0065: Unable to reset password. Please contact your Admin!**\
**Explanation:**\
Password reset process failed due to backend or system error.\
**Cause:**

* Backend service unavailable or timeout.
* Invalid password reset token or expired link.
* Database error or inconsistency during reset.

**Resolution:**

* Verify backend services and dependencies are up.
* Validate password reset tokens before processing.
* Provide alternative support contact info.

**SCIK-0066: Please enter valid old password**\
**Explanation:**\
Old password entered is invalid or incorrect.\
**Cause:**

* User typed incorrect current password.
* Password encoding/decoding mismatch.
* User account locked or password expired.

**Resolution:**

* Prompt user to carefully enter correct old password.
* Check password hash and storage logic.
* Provide user support for locked accounts.

**SCIK-0067: Please enter valid old\_password key**\
**Explanation:**\
Old password key or parameter is missing or invalid.\
**Cause:**

* API call missing required old\_password parameter.
* Client-side input key mismatch.
* Backend validation error for parameter.

**Resolution:**

* Ensure API requests include all required keys.
* Validate client form submissions properly.
* Review backend input validation logic.

**SCIK-0068: Please enter new password**\
**Explanation:**\
New password field is missing input.\
**Cause:**

* User omitted new password field.
* Client form did not enforce required fields.
* Input field cleared accidentally.

**Resolution:**

* Make new password field mandatory.
* Prompt users to enter new password before submitting.
* Validate input on client and server side.

**SCIK-0069: Please enter valid new\_password key**\
**Explanation:**\
New password parameter/key is missing or invalid.\
**Cause:**

* API requests missing new\_password parameter.
* Input validation on client or server failed.
* Parameter naming mismatch between client and server.

**Resolution:**

* Ensure new\_password key included in API requests.
* Synchronize client-server parameter naming.
* Implement robust input validation.

**SCIK-0070: Please enter confirm new password**\
**Explanation:**\
Confirm new password input missing.\
**Cause:**

* User skipped confirm new password field.
* Form validation missed the required field.
* Client-side errors cleared the field.

**Resolution:**

* Require confirm new password in forms.
* Validate confirmation matches new password.
* Prompt users on missing confirmation input.

**SCIK-0071: Old password and New password cannot be same**\
**Explanation:**\
New password is identical to the old password, which is not allowed.\
**Cause:**

* User tried to reuse the same password.
* Password policy disallows reuse for security reasons.
* User unaware of password uniqueness requirement.

**Resolution:**

* Enforce password change policies.
* Provide clear messages about password reuse.
* Encourage use of strong, unique passwords.

**SCIK-0073: Failure password save**\
**Explanation:**\
System failed to save the new password.\
**Cause:**

* Database or service failure during save.
* Input validation error causing rejection.
* Concurrency or locking issues in storage.

**Resolution:**

* Verify database and service health.
* Check validation and error logs.
* Retry save operation or alert admin.

**SCIK-0074: Please enter valid first\_name key**\
**Explanation:**\
First name parameter is missing or invalid.\
**Cause:**

* API or form missing first\_name field.
* Input validation rejected invalid names.
* Client-server mismatch on key names.

**Resolution:**

* Ensure first\_name field is included and valid.
* Implement proper input sanitation.
* Synchronize client and API specs.

**SCIK-0075: Please enter valid last\_name key**\
**Explanation:**\
Last name parameter is missing or invalid.\
**Cause:**

* Missing last\_name in request.
* Invalid characters or length in input.
* Validation mismatch between client and server.

**Resolution:**

* Validate last\_name presence and format.
* Sanitize input to prevent errors.
* Ensure client and API are aligned.

**SCIK-0076: Please enter valid gender key**\
**Explanation:**\
Gender parameter is missing or invalid.\
**Cause:**

* API call missing gender field.
* Invalid gender values submitted.
* Client form not enforcing valid options.

**Resolution:**

* Enforce valid gender selection on client side.
* Validate gender values on server.
* Provide acceptable value list to users.

**SCIK-0077: Please enter valid position key**\
**Explanation:**\
Position parameter is missing or invalid.\
**Cause:**

* Missing or empty position field.
* Invalid characters or formats.
* Client-server API mismatch.

**Resolution:**

* Validate position field input and presence.
* Sanitize inputs before saving.
* Align client form and server requirements.

**SCIK-0078: Please enter valid company key**\
**Explanation:**\
Company parameter is missing or invalid.\
**Cause:**

* Company field omitted in submission.
* Invalid company names or formats.
* Mismatch in API expectations.

**Resolution:**

* Validate company input for correctness.
* Provide format guidance to users.
* Synchronize API specs with client forms.

**SCIK-0079: Please enter valid phone\_no key**\
**Explanation:**\
Phone number parameter is missing or invalid.\
**Cause:**

* Phone number omitted or malformed.
* Missing country code or wrong format.
* Validation not enforced client-side.

**Resolution:**

* Enforce phone number format and presence.
* Validate country code inclusion.
* Provide formatting help or masks.

**SCIK-0080: Please enter valid country key**\
**Explanation:**\
Country parameter is missing or invalid.\
**Cause:**

* Missing or invalid country field.
* Unsupported country codes or names.
* Validation mismatch.

**Resolution:**

* Use dropdowns or validated inputs for country.
* Enforce required field on client and server.
* Provide country list reference.

**SCIK-0081: Please enter valid city key**\
**Explanation:**\
City parameter is missing or invalid.\
**Cause:**

* City omitted or invalid format.
* Client-server inconsistency.
* Input length or character issues.

**Resolution:**

* Validate city input for format and length.
* Use autocomplete or controlled inputs.
* Synchronize validation rules.

**SCIK-0082: Please enter valid dob key**\
**Explanation:**\
Date of birth parameter is missing or invalid.\
**Cause:**

* Missing DOB input.
* Invalid date format or future date.
* Input field not validated properly.

**Resolution:**

* Enforce DOB input with date picker.
* Validate date format and logical constraints.
* Prompt user for correct DOB entry.

**SCIK-0083: Please enter valid about key**\
**Explanation:**\
About or bio parameter is missing or invalid.\
**Cause:**

* Missing about field.
* Input exceeds length limits or contains invalid chars.
* Client-server validation mismatch.

**Resolution:**

* Limit about field length and sanitize input.
* Provide guidelines for input content.
* Validate presence if mandatory.

**SCIK-0085: Failure user details update**\
**Explanation:**\
System failed to update user details.\
**Cause:**

* Backend service or database error.
* Validation error rejected inputs.
* Network or permission issues.

**Resolution:**

* Check backend service health and logs.
* Validate all inputs before update.
* Retry or escalate error to admin.

**SCIK-0086: Please enter valid profile\_image key**\
**Explanation:**\
Profile image parameter is missing or invalid.\
**Cause:**

* Missing or corrupted image file input.
* Unsupported file format or size.
* API validation error for image parameter.

**Resolution:**

* Enforce file upload validations.
* Accept only allowed image formats and sizes.
* Validate parameter presence before processing.

**SCIK-0088: Failure user profile image update**\
**Explanation:**\
Failed to update user's profile image.\
**Cause:**

* File upload or storage failure.
* Image format or size issues.
* Permission or server errors.

**Resolution:**

* Verify file upload processes and permissions.
* Enforce file type and size limits.
* Provide meaningful user feedback on failures.

**SCIK-0089: Upload Image with correct Extension, only (.jpg, .jpeg, .png) are allowed.**\
**Explanation:**\
Uploaded image has unsupported file extension.\
**Cause:**

* User tried uploading unsupported image type.
* Client-side file type restrictions missing.
* Server validation rejected unsupported formats.

**Resolution:**

* Restrict file uploads to supported types only.
* Validate file extensions client-side and server-side.
* Inform user about accepted formats clearly.

**SCIK-0092: User not activated**\
**Explanation:**\
User account is not yet activated.\
**Cause:**

* User did not complete activation process.
* Activation email not received or expired.
* System failed to update activation status.

**Resolution:**

* Prompt user to activate account via email link.
* Allow resending activation email.
* Verify activation process backend functionality.

**SCIK-0095: You are not registered User**\
**Explanation:**\
User is attempting action without being registered.\
**Cause:**

* User tries to access system without registration.
* Unregistered email or ID used.
* User deleted or blocked account.

**Resolution:**

* Inform user to register before proceeding.
* Provide registration link or support.
* Restrict access to registered users only.

**SCIK-0100: User Id is required**\
**Explanation:**\
User ID parameter is missing.\
**Cause:**

* API or form missing user ID input.
* Incorrect parameter name or empty field.
* Client-server mismatch.

**Resolution:**

* Enforce user ID field presence.
* Validate and sanitize user ID inputs.
* Ensure consistent parameter naming.

**SCIK-0146: Invalid Username and Password!**\
**Explanation:**\
Authentication failed due to wrong credentials.\
**Cause:**

* Incorrect username or password entered.
* User account locked or disabled.
* Backend authentication service error.

**Resolution:**

* Prompt user to verify credentials.
* Implement account lockout policies.
* Provide password reset option.

**SCIK-0154: Failure user details update**\
**Explanation:**\
User detail update operation failed.\
**Cause:**

* Database or API error during update.
* Invalid or missing input data.
* Permission or authorization failure.

**Resolution:**

* Check backend logs and fix errors.
* Validate inputs before update.
* Ensure user has necessary permissions.

**SCIK-0233: Only one role can be assigned to a user in an Entity({})**\
**Explanation:**\
User cannot have multiple roles in the same entity.\
**Cause:**

* Attempt to assign multiple roles to one user in same entity.
* Business rule enforcing single role per entity.
* Data inconsistency or duplicate assignments.

**Resolution:**

* Restrict role assignment to one per entity per user.
* Validate assignments on client and server.
* Notify user of assignment conflict.

**SCIK-0295: User cannot update ownself**\
**Explanation:**\
User is not permitted to update their own account details.\
**Cause:**

* System rule preventing self-update for security.
* Possible privilege restrictions.
* To avoid accidental or unauthorized changes.

**Resolution:**

* Enforce role-based update permissions.
* Advise user to request admin assistance.
* Document policy on self-update restrictions.

**SCIK-0296: User cannot delete ownself**\
**Explanation:**\
User cannot delete their own account.\
**Cause:**

* Prevent accidental self-deletion.
* Security or audit requirements.
* Administrative policy.

**Resolution:**

* Block self-delete operations.
* Require admin to perform deletions.
* Provide clear error messages.

**SCIK-0336: This user is currently locked. Please contact your admin!**\
**Explanation:**\
User account is locked and access denied.\
**Cause:**

* Account locked due to failed login attempts.
* Manual lock by admin for security reasons.
* Policy enforcement on user locking.

**Resolution:**

* Inform user of locked status.
* Provide admin contact info for unlocking.
* Implement lockout duration and reset policies.

**SCIK-0341: Unable to retrieve user list.**\
**Explanation:**\
System failed to fetch user list data.\
**Cause:**

* Backend database or API failure.
* Network or permission issues.
* Data corruption or timeout.

**Resolution:**

* Check backend service health.
* Verify user permissions.
* Retry operation or escalate error.

**SCIK-0353: Unable to update group details.**\
**Explanation:**\
Group details update operation failed.\
**Cause:**

* Backend failure during update.
* Invalid or incomplete input data.
* Permissions or locking issues.

**Resolution:**

* Validate input data.
* Check system logs for errors.
* Confirm user authorization.

**SCIK-0354: Unable to delete the selected group.**\
**Explanation:**\
Deletion of group failed.\
**Cause:**

* Group linked to dependent records.
* Database constraints preventing delete.
* Permission or role restrictions.

**Resolution:**

* Check group dependencies before delete.
* Provide error feedback on failure reasons.
* Request admin assistance if needed.

**SCIK-0355: Unable to retrieve group details.**\
**Explanation:**\
Failed to fetch specific group details.\
**Cause:**

* Backend or database error.
* Incorrect group identifier.
* Permission issues.

**Resolution:**

* Verify group ID correctness.
* Check backend availability.
* Ensure user has access rights.

**SCIK-0356: Unable to retrieve groups list.**\
**Explanation:**\
Failed to fetch list of groups.\
**Cause:**

* Service downtime or database failure.
* User permission denied.
* Network connectivity issues.

**Resolution:**

* Check backend system status.
* Confirm user access rights.
* Retry or escalate issue.

**SCIK-0357: Unable to validate user token.**\
**Explanation:**\
User authentication token validation failed.\
**Cause:**

* Expired or malformed token.
* Token revoked or blacklisted.
* Backend validation service unavailable.

**Resolution:**

* Prompt user to reauthenticate.
* Refresh or regenerate token.
* Check token validation service health.

***

**SCIK-0358: Failed to register user.**\
**Explanation:**\
User registration process failed.\
**Cause:**

* Database or backend error during save.
* Duplicate user or email detected.
* Validation errors on input data.\
  **Resolution:**
* Check backend logs for errors.
* Validate uniqueness of user data.
* Provide clear user feedback on failure.

**SCIK-0359: Failed to log in.**\
**Explanation:**\
User login attempt failed.\
**Cause:**

* Incorrect credentials.
* Account locked or inactive.
* Backend authentication error.

**Resolution:**

* Verify credentials and retry.
* Check account status.
* Provide password reset option.

**SCIK-0360: Unable to retrieve user profile.**\
**Explanation:**\
Failed to fetch user profile data.\
**Cause:**

* Database or API failure.
* User ID missing or invalid.
* Permission denied.

**Resolution:**

* Validate user ID input.
* Check backend service health.
* Ensure proper user permissions.

**SCIK-0361: Failed to log out.**\
**Explanation:**\
Logout process failed.\
**Cause:**

* Session or token invalidation error.
* Backend service unavailable.
* Network or client issues.

**Resolution:**

* Retry logout operation.
* Verify backend session management.
* Inform user to close browser if needed.

**SCIK-0362: Unable to process forgot password request.**\
**Explanation:**\
Forgot password operation failed.\
**Cause:**

* Backend error sending reset email.
* Invalid or missing user email.
* Service outages or misconfiguration.

**Resolution:**

* Check mail server and service health.
* Validate email input.
* Provide alternative support.

**SCIK-0363: Unable to reset password.**\
**Explanation:**\
Password reset failed during processing.\
**Cause:**

* Invalid or expired reset token.
* Backend database or service error.
* Input validation failure.

**Resolution:**

* Validate token before reset.
* Check backend logs.
* Inform user and allow retry.

**SCIK-0364: Unable to change password.**\
**Explanation:**\
Password change operation failed.\
**Cause:**

* Incorrect old password.
* Backend service or database failure.
* Validation error on new password.

**Resolution:**

* Verify old password correctness.
* Check service availability.
* Provide detailed error feedback.

**SCIK-0365: Unable to update user profile.**\
**Explanation:**\
User profile update failed.\
**Cause:**

* Backend or database error.
* Input validation failed.
* Permissions issue.\
  **Resolution:**
* Validate input data.
* Check backend logs.
* Verify user permissions.

***

**SCIK-0366: Unable to retrieve user activities.**\
**Explanation:**\
Failed to fetch user activity logs.\
**Cause:**

* Backend API failure.
* Missing user identifier.
* Permission restrictions.\
  **Resolution:**
* Confirm user ID input.
* Verify backend service status.
* Check user permissions.

***

**SCIK-0368: Unable to save user details.**\
**Explanation:**\
Saving new or updated user data failed.\
**Cause:**

* Database write failure.
* Validation error on data.
* Permission or concurrency issues.\
  **Resolution:**
* Check data validity.
* Verify database availability.
* Ensure proper permissions.

***

**SCIK-0369: Unable to update user details.**\
**Explanation:**\
User detail update operation failed.\
**Cause:**

* Backend or DB error.
* Input validation failure.
* Permissions issues.\
  **Resolution:**
* Validate inputs thoroughly.
* Check backend logs.
* Confirm authorization.

***

**SCIK-0370: Failed to reactivate user.**\
**Explanation:**\
User reactivation process failed.\
**Cause:**

* Backend error during update.
* User already active or invalid status.
* Validation or permission failures.\
  **Resolution:**
* Verify user status before reactivation.
* Check backend service health.
* Inform admin for manual intervention.

***

**SCIK-0371: Unable to retrieve user details.**\
**Explanation:**\
Failed to fetch user information.\
**Cause:**

* Missing or invalid user ID.
* Backend failure or timeout.
* Permission restrictions.\
  **Resolution:**
* Validate user ID input.
* Check backend service availability.
* Verify access permissions.

***

**SCIK-0372: Failed to retrieve user folder path.**\
**Explanation:**\
Unable to get user-specific folder path.\
**Cause:**

* Backend file system or database failure.
* Missing user ID or mapping.
* Configuration issues.\
  **Resolution:**
* Validate user ID.
* Check folder mapping logic.
* Confirm storage service availability.

***

**SCIK-0373: Unable to delete user.**\
**Explanation:**\
User deletion process failed.\
**Cause:**

* User has active dependencies.
* Permission denied.
* Backend failure.\
  **Resolution:**
* Validate dependencies before delete.
* Check permission levels.
* Review backend error logs.

***

**SCIK-0374: Unable to retrieve user list.**\
**Explanation:**\
Fetching user list failed.\
**Cause:**

* Database or service error.
* Permission issues.
* Input validation failure.\
  **Resolution:**
* Retry after verifying backend.
* Confirm user role has access.
* Provide fallback error message.

***

**SCIK-0377: Unable to change user lock status.**\
**Explanation:**\
System failed to lock or unlock user.\
**Cause:**

* Permission or role-based restrictions.
* Backend failure.
* Invalid user ID.\
  **Resolution:**
* Validate input data.
* Ensure proper access rights.
* Retry or escalate issue.

***

**SCIK-0380: Unable to retrieve user email list.**\
**Explanation:**\
Fetching user emails failed.\
**Cause:**

* Backend service issue.
* Database connectivity problems.
* Access restriction.\
  **Resolution:**
* Check service and database logs.
* Validate user role permissions.
* Retry operation safely.

***

**SCIK-0381: Unable to create user activity record.**\
**Explanation:**\
Failed to log user activity.\
**Cause:**

* Logging service unavailable.
* Input data invalid or missing.
* Permission or backend error.\
  **Resolution:**
* Verify logging service status.
* Validate inputs before logging.
* Retry or store locally for retry.

***

**SCIK-0415: Unable to retrieve user activities report.**\
**Explanation:**\
User activity report generation failed.\
**Cause:**

* Report service offline.
* Data missing or invalid filters.
* Permission denied.\
  **Resolution:**
* Confirm data availability and filters.
* Check report generation backend.
* Ensure user has access rights.

### Module: Auth

#### SCIK-0033: Email already exist

**Explanation:**\
Attempt to register or add an email that is already in the system.

**Cause:**

* User tries to register with an email that is already taken.
* Duplicate entry due to system sync or concurrency issues.
* Email validation logic not properly filtering duplicates.

**Resolution:**

* Inform user that the email is already registered.
* Implement email uniqueness checks before registration.
* Provide "forgot password" or account recovery options.

***

#### SCIK-0053: Please enter valid verifycode key

**Explanation:**\
Verification code provided is invalid or malformed.

**Cause:**

* User enters incorrect or expired verification code.
* Verification key format does not match expected pattern.
* Backend verification service or database issue.

**Resolution:**

* Prompt user to enter the correct verification code.
* Validate code format on client and server side before processing.
* Ensure verification code expiration and regeneration are handled correctly.

***

#### SCIK-0099: Code required

**Explanation:**\
Verification or authorization code is missing in the request.

**Cause:**

* User or client did not provide the required code.
* Frontend or API failed to send the code parameter.
* Input validation missed this required field.

**Resolution:**

* Make the code field mandatory on the frontend.
* Add validation checks in API for missing parameters.
* Provide clear error messages to guide the user.

***

#### SCIK-0101: Code not match

**Explanation:**\
Provided verification code does not match expected code.

**Cause:**

* User entered incorrect verification code.
* Code expired or has already been used.
* Backend mismatch due to timing or data sync issues.

**Resolution:**

* Inform user that the code is incorrect and allow retry.
* Implement code expiration and regeneration logic.
* Ensure backend and frontend are synchronized with the current valid codes.

***

#### SCIK-0104: Entity is required

**Explanation:**\
Required entity information is missing from the request.

**Cause:**

* Client request missing entity ID or name.
* API or form validation not enforcing this requirement.
* Miscommunication or documentation gaps on required fields.

**Resolution:**

* Make entity input mandatory on client side.
* Validate entity presence before processing on backend.
* Update API docs to clearly state entity requirements.

***

#### SCIK-0111: Entity already exist!

**Explanation:**\
Attempt to create an entity that already exists in the system.

**Cause:**

* Duplicate entity creation request.
* Backend entity uniqueness validation missed or failed.
* Race condition causing concurrent creation of same entity.

**Resolution:**

* Validate entity uniqueness before creation.
* Return user-friendly message when duplication detected.
* Implement locking or transactional logic to prevent race conditions.

***

#### SCIK-0115: Records does not exist.

**Explanation:**\
Requested records or data not found in the database.

**Cause:**

* Querying non-existent record ID or parameters.
* Data deletion or archival occurred before request.
* Backend search/filter criteria too restrictive or incorrect.

**Resolution:**

* Validate input parameters and handle empty results gracefully.
* Inform user when no records match the request.
* Review data lifecycle and retention policies.

***

#### SCIK-0190: Group name already exist

**Explanation:**\
Attempt to create or rename group with a name already used.

**Cause:**

* Duplicate group names allowed or missed check.
* User unaware of existing group names.
* Concurrency issues with group creation.

**Resolution:**

* Enforce unique group names in database.
* Provide user feedback about existing groups.
* Lock or queue creation requests to prevent race conditions.

***

#### SCIK-0192: Group updated

**Explanation:**\
Group details successfully updated.

**Cause:**

* User submitted valid changes to group.
* Backend processed update without errors.
* No validation or permission issues encountered.

**Resolution:**

* Confirm update to user with success message.
* Log update actions for audit.
* Refresh group views to show updated info.

***

#### SCIK-0193: Group deleted

**Explanation:**\
Group successfully deleted from the system.

**Cause:**

* User or admin requested deletion.
* No dependencies blocking delete action.
* Backend completed operation without errors.

**Resolution:**

* Inform user of successful deletion.
* Remove group references in UI or other components.
* Log deletion for audit and recovery if needed.

***

#### SCIK-0196: Application is running...

**Explanation:**\
Health check message indicating the Auth module is operational.

**Cause:**

* Health check endpoint invoked successfully.
* Backend services responding as expected.
* No critical errors detected at this time.

**Resolution:**

* Use as monitoring signal for uptime.
* Investigate if health check fails.
* Keep health check lightweight and reliable.

***

#### SCIK-0272: @{} - your role and entity has been updated by {}. Updated Entity and Roles are:- {}

**Explanation:**\
Notification message about user’s role and entity update.

**Cause:**

* Admin or system updated user role/entity.
* Role changes require notifying the affected user.
* Audit trail or compliance requirements.

**Resolution:**

* Send notification to affected user promptly.
* Log the change for audit.
* Verify user permissions after update.

***

#### SCIK-0337: {} not in allowed domains.

**Explanation:**\
Provided domain is not on the list of allowed domains.

**Cause:**

* User tries to register or login with disallowed email domain.
* Allowed domain list not updated or synced.
* Policy restricting access to certain domains.

**Resolution:**

* Inform user of allowed domain policy.
* Update domain whitelist as needed.
* Validate domains both client and server side.

***

#### SCIK-0338: Unable to save merchant details.

**Explanation:**\
Saving merchant data failed.

**Cause:**

* Database write failure or validation error.
* Missing or invalid merchant data.
* Backend service or network issues.

**Resolution:**

* Validate merchant data before saving.
* Check database and service logs for errors.
* Provide user-friendly error feedback.

***

#### SCIK-0342: Failed to retrieve application settings.

**Explanation:**\
Could not fetch app configuration or settings.

**Cause:**

* Backend service or DB failure.
* Incorrect query parameters or authorization.
* Network or timeout issues.

**Resolution:**

* Verify service health and database connection.
* Validate user permissions.
* Retry or fallback to default settings if applicable.

***

#### SCIK-0352: Unable to create group.

**Explanation:**\
Group creation operation failed.

**Cause:**

* Validation failure on input data.
* Database or backend service error.
* Permission or quota restrictions.

**Resolution:**

* Validate group creation inputs thoroughly.
* Check backend error logs.
* Ensure user has create permissions.

***

#### SCIK-0375: Unable to save page settings.

**Explanation:**\
Failed to save configuration for a page.

**Cause:**

* Backend validation or save error.
* Missing or invalid page setting data.
* Permission issues.

**Resolution:**

* Validate inputs before saving.
* Check backend logs for errors.
* Confirm user authorization.

***

#### SCIK-0376: Unable to retrieve page settings.

**Explanation:**\
Could not fetch saved page configurations.

**Cause:**

* Backend service or DB failure.
* User lacks permission.
* Incorrect request parameters.

**Resolution:**

* Verify backend service availability.
* Check user access rights.
* Validate request parameters.

### Module: Dashboard

#### **SCIK-0012: Failure dashboard update**

**Explanation:**\
Failed to update the dashboard due to internal error or invalid data.\
**Cause:**

* Incorrect or missing input data.
* Backend service failure or timeout.\
  **Resolution:**
* Verify all required dashboard data is correct.
* Check service logs and retry the update operation.

***

#### **SCIK-0013: Failure Report delete**

**Explanation:**\
Failed to delete the specified report.\
**Cause:**

* Report is in use or linked to other components.
* Insufficient user permissions.\
  **Resolution:**
* Ensure the report is not linked to any dashboard or active process.
* Verify user privileges for report deletion.

***

#### **SCIK-0018: Failure Reshape Dimensions and Matrix**

**Explanation:**\
Failed to reshape the dimension matrix structure.\
**Cause:**

* Invalid matrix configuration or size mismatch.
* Data inconsistency in input structure.\
  **Resolution:**
* Check the matrix dimensions and format.
* Ensure the reshaping logic aligns with input structure.

***

#### **SCIK-0021: Failure get all reports**

**Explanation:**\
Unable to retrieve the list of all reports.\
**Cause:**

* Backend service error.
* Database connection issue.\
  **Resolution:**
* Retry fetching after some time.
* Verify backend service health and logs.

***

#### **SCIK-0026: Please enter your custom formula!**

**Explanation:**\
Custom formula field is empty or not provided.\
**Cause:**

* User skipped formula input.\
  **Resolution:**
* Enter a valid custom formula before proceeding.

***

#### **SCIK-0027: Calculated field is not correct!**

**Explanation:**\
Provided calculated field expression is invalid.\
**Cause:**

* Syntax error in formula.
* Unsupported operations or references.\
  **Resolution:**
* Validate the formula structure and syntax.
* Use only supported fields and operators.

***

#### **SCIK-0028: Expression is invalid!**

**Explanation:**\
Invalid expression entered in input field.\
**Cause:**

* Malformed expression or logical error.\
  **Resolution:**
* Use a valid expression format.
* Refer to documentation for allowed syntax.

***

#### **SCIK-0029: report\_id key is not valid**

**Explanation:**\
Provided report\_id is missing or incorrect.\
**Cause:**

* Invalid or deleted report identifier.\
  **Resolution:**
* Check and input a valid report\_id.
* Ensure the report exists in the system.

***

#### **SCIK-0030: Dashboard id is not valid**

**Explanation:**\
Provided dashboard ID is incorrect or does not exist.\
**Cause:**

* Typo or invalid dashboard reference.\
  **Resolution:**
* Re-check the dashboard ID.
* Ensure it matches an existing dashboard.

#### **SCIK-0113: Object does not exist**

**Explanation:**\
The requested object could not be found in the system.\
**Cause:**

* Object may have been deleted or never existed.
* Incorrect or outdated reference used.\
  **Resolution:**
* Verify the object identifier.
* Ensure the object has not been removed or renamed.

***

#### **SCIK-0116: Data not found**

**Explanation:**\
No data is available for the specified query or filter.\
**Cause:**

* Data filters returned an empty result.
* Dataset may not have been loaded or is missing.\
  **Resolution:**
* Adjust filters or parameters.
* Confirm that the data source contains the expected records.

***

#### **SCIK-0117: Error in loadStandardReport**

**Explanation:**\
An error occurred while attempting to load a standard report.\
**Cause:**

* Corrupt or incomplete report template.
* System failure or configuration issue.\
  **Resolution:**
* Validate the report template configuration.
* Check backend logs for additional error details.

***

#### **SCIK-0118: Please choose right mapping for RFM-analysis**

**Explanation:**\
RFM-analysis cannot proceed without proper mapping selection.\
**Cause:**

* Required mapping fields are not selected.\
  **Resolution:**
* Select correct customer, frequency, and monetary fields.

***

#### **SCIK-0124: Dashboard name already exist**

**Explanation:**\
The specified dashboard name is already in use.\
**Cause:**

* Duplicate dashboard name entered during creation.\
  **Resolution:**
* Use a unique dashboard name.
* Check existing dashboards for name conflicts.

***

#### **SCIK-0230: Template id is not valid**

**Explanation:**\
Provided template ID does not match any existing template.\
**Cause:**

* Typo in template ID.
* Template may have been deleted.\
  **Resolution:**
* Use a valid and existing template ID.
* Check template availability in the system.

***

#### **SCIK-0236: Dashboard key is not valid**

**Explanation:**\
The dashboard key provided is incorrect or invalid.\
**Cause:**

* Key mismatch or reference error.\
  **Resolution:**
* Ensure a valid dashboard key is used.
* Recheck dashboard metadata.

***

#### **SCIK-0237: Report name already exist**

**Explanation:**\
The report name is already in use.\
**Cause:**

* Duplicate report name detected during creation.\
  **Resolution:**
* Provide a unique name for the new report.
* Review existing reports to avoid duplication.

***

#### **SCIK-0252: Date format not valid**

**Explanation:**\
The date format provided is incorrect.\
**Cause:**

* Format mismatch (e.g., using MM/DD/YYYY instead of YYYY-MM-DD).\
  **Resolution:**
* Use the expected date format as per system configuration.
* Refer to input guidelines.

***

#### **SCIK-0253: Sales mapping not provided**

**Explanation:**\
Required sales mapping data is missing.\
**Cause:**

* Mapping fields for sales not configured.\
  **Resolution:**
* Provide valid sales data mapping.
* Complete the configuration before proceeding.

#### **SCIK-0416: Unable to retrieve dashboard calculated columns list**

**Explanation:**\
System failed to fetch the list of calculated columns for the dashboard.\
**Cause:**

* Backend query failure or missing metadata.
* Permissions issue or misconfigured dashboard.\
  **Resolution:**
* Check if the dashboard has valid calculated fields.
* Verify user access and backend service logs.

***

#### **SCIK-0417: Unable to create dashboard calculated column**

**Explanation:**\
Failed to create a new calculated column in the dashboard.\
**Cause:**

* Invalid formula or field references.
* System error during save operation.\
  **Resolution:**
* Validate the formula syntax and field names.
* Retry creation after verifying dependencies.

***

#### **SCIK-0418: Unable to retrieve inventory list**

**Explanation:**\
Could not load the inventory list from the system.\
**Cause:**

* Data source unavailable or misconfigured.
* Backend fetch error.\
  **Resolution:**
* Ensure the inventory source is properly connected.
* Check logs for inventory service errors.

***

#### **SCIK-0419: Unable to search inventory**

**Explanation:**\
Inventory search operation failed.\
**Cause:**

* Query syntax error.
* Search index not updated or available.\
  **Resolution:**
* Refine search parameters.
* Rebuild or re-index the inventory search data.

***

#### **SCIK-0420: Unable to fetch inventory data**

**Explanation:**\
System failed to retrieve detailed inventory data.\
**Cause:**

* Timeout or server error during data fetch.
* Missing inventory records.\
  **Resolution:**
* Verify data exists for selected filters.
* Retry or check inventory service status.

***

#### **SCIK-0421: Unable to fetch order lifecycle data**

**Explanation:**\
Could not retrieve lifecycle information for the selected order.\
**Cause:**

* Missing or incomplete order records.
* Backend service or database error.\
  **Resolution:**
* Confirm order ID and data integrity.
* Retry after ensuring backend services are running.

***

#### **SCIK-0423: Unable to save dashboard component**

**Explanation:**\
Dashboard component could not be saved.\
**Cause:**

* Missing mandatory fields.
* Validation failure or server-side error.\
  **Resolution:**
* Complete all required fields.
* Check logs for component-level issues and retry.

***

#### **SCIK-0424: Unable to generate PDF**

**Explanation:**\
Failed to generate the PDF version of the dashboard/report.\
**Cause:**

* Rendering service failure.
* Unsupported content or format.\
  **Resolution:**
* Simplify dashboard layout or content.
* Retry or contact system administrator.

***

#### **SCIK-0425: Unable to fetch dashboard parameters**

**Explanation:**\
System failed to retrieve configuration parameters for the dashboard.\
**Cause:**

* Misconfigured dashboard setup.
* Database or API issue.\
  **Resolution:**
* Ensure parameters are properly defined.
* Review logs or contact support team.

***

#### **SCIK-0426: Unable to retrieve drilldown data**

**Explanation:**\
Drilldown data could not be loaded.\
**Cause:**

* Missing links or invalid configuration for drilldown.
* Data source error.\
  **Resolution:**
* Verify drilldown path and data availability.
* Reconfigure drilldown if necessary.

#### **SCIK-0427: Unable to retrieve component drilldown data**

**Explanation:**\
Failed to load drilldown data for the dashboard component.\
**Cause:**

* Component configuration error.
* Missing linked data source or parameters.\
  **Resolution:**
* Verify drilldown setup in component settings.
* Check related dataset connections.

***

#### **SCIK-0428: Unable to edit dashboard**

**Explanation:**\
The dashboard could not be edited.\
**Cause:**

* Lock on dashboard by another session or user.
* Permission or validation error.\
  **Resolution:**
* Ensure the dashboard is not being edited elsewhere.
* Confirm edit permissions and resolve validation issues.

***

#### **SCIK-0429: Unable to create dashboard**

**Explanation:**\
Dashboard creation failed.\
**Cause:**

* Missing required fields or invalid input.
* System error during save operation.\
  **Resolution:**
* Complete all required fields.
* Retry with valid configuration.

***

#### **SCIK-0430: Unable to upload dashboard logo**

**Explanation:**\
System was unable to upload the logo image for the dashboard.\
**Cause:**

* Unsupported file format or size limit exceeded.
* Upload path error or permission issue.\
  **Resolution:**
* Use supported image formats (e.g., PNG, JPG).
* Ensure image size is within the limit and retry.

***

#### **SCIK-0431: Unable to upload dashboard image**

**Explanation:**\
Dashboard image upload failed.\
**Cause:**

* File too large or incorrect format.
* Storage or API issue.\
  **Resolution:**
* Resize or reformat the image.
* Check connectivity and retry.

***

#### **SCIK-0432: Unable to view dashboard**

**Explanation:**\
Dashboard preview or rendering failed.\
**Cause:**

* Rendering engine failure.
* Broken or missing layout components.\
  **Resolution:**
* Reconfigure dashboard components.
* Check for frontend rendering issues.

***

#### **SCIK-0433: Unable to view dashboard asset**

**Explanation:**\
Dashboard asset (e.g., images or files) could not be displayed.\
**Cause:**

* Asset missing or improperly linked.\
  **Resolution:**
* Verify asset paths and availability.
* Re-upload or relink assets.

***

#### **SCIK-0434: Unable to load dashboard in iframe**

**Explanation:**\
Embedding the dashboard in an iframe failed.\
**Cause:**

* Cross-origin resource sharing (CORS) restrictions.
* Misconfigured iframe settings.\
  **Resolution:**
* Adjust server headers for CORS.
* Use correct embedding parameters.

***

#### **SCIK-0435: Unable to retrieve dashboard list**

**Explanation:**\
System failed to fetch the list of dashboards.\
**Cause:**

* Backend service error or timeout.
* Access or permission issue.\
  **Resolution:**
* Retry after a short period.
* Check user permissions and server status.

***

#### **SCIK-0436: Unable to delete dashboard component**

**Explanation:**\
Failed to remove a component from the dashboard.\
**Cause:**

* Component locked or in use.
* System permissions issue.\
  **Resolution:**
* Ensure component is not in active use.
* Verify deletion rights.

***

#### **SCIK-0437: Unable to delete dashboard**

**Explanation:**\
Dashboard deletion process failed.\
**Cause:**

* Dashboard has dependencies or restricted access.
* Backend failure.\
  **Resolution:**
* Remove dependencies before deletion.
* Retry with appropriate permissions.

***

#### **SCIK-0439: Unable to generate collapsible tree**

**Explanation:**\
The system could not create a collapsible tree view.\
**Cause:**

* Data structure invalid for tree generation.
* Logic error in component configuration.\
  **Resolution:**
* Ensure hierarchical data is correctly structured.
* Check for null or circular references.

***

#### **SCIK-0440: Unable to identify intent**

**Explanation:**\
System failed to determine user intent from the input.\
**Cause:**

* Ambiguous or unclear input command.\
  **Resolution:**
* Use a more specific or standard query.
* Follow input syntax guidelines.

***

#### **SCIK-0441: Unable to create dashboard token**

**Explanation:**\
Failed to generate a token for dashboard access.\
**Cause:**

* Authentication error.
* Token service issue.\
  **Resolution:**
* Retry login and token request.
* Check token service configuration.

***

#### **SCIK-0442: Unable to retrieve dashboard token**

**Explanation:**\
Token fetch failed for the dashboard session.\
**Cause:**

* Token expired or not found.\
  **Resolution:**
* Request a new token.
* Validate existing token status.

***

#### **SCIK-0443: Unable to delete dashboard token**

**Explanation:**\
Token deletion operation failed.\
**Cause:**

* Invalid or expired token reference.\
  **Resolution:**
* Ensure token exists before deletion.
* Check for session dependencies.

***

#### **SCIK-0444: Unable to process dashboard source relation**

**Explanation:**\
Source relation setup in dashboard could not be completed.\
**Cause:**

* Invalid relation mapping between sources.
* Schema mismatch.\
  **Resolution:**
* Review source schema definitions.
* Fix mapping configuration.

***

#### **SCIK-0445: Unable to create dashboard sheet**

**Explanation:**\
Failed to create a new sheet in the dashboard.\
**Cause:**

* Sheet name conflict or missing inputs.\
  **Resolution:**
* Use a unique sheet name.
* Provide all required sheet properties.

***

#### **SCIK-0446: Unable to rename dashboard sheet**

**Explanation:**\
Dashboard sheet rename operation failed.\
**Cause:**

* Sheet name already in use.
* Sheet is locked or not found.\
  **Resolution:**
* Choose a unique name.
* Unlock sheet and retry.

***

#### **SCIK-0447: Unable to duplicate dashboard sheet**

**Explanation:**\
Dashboard sheet duplication process failed.\
**Cause:**

* Duplicate name or internal error.\
  **Resolution:**
* Rename new copy or resolve duplication conflict.

***

#### **SCIK-0448: Unable to delete dashboard sheet**

**Explanation:**\
The selected sheet could not be deleted.\
**Cause:**

* Sheet contains active components or references.\
  **Resolution:**
* Remove dependencies before deletion.
* Retry with proper access rights.

***

#### **SCIK-0449: Unable to retrieve dashboard sheets**

**Explanation:**\
Failed to load available sheets for the dashboard.\
**Cause:**

* Sheet metadata retrieval error.\
  **Resolution:**
* Recheck dashboard configuration.
* Contact support if error persists.

***

#### **SCIK-0450: Unable to update sheet status**

**Explanation:**\
System could not update the sheet's status (e.g., active/inactive).\
**Cause:**

* Invalid sheet ID or permission issue.\
  **Resolution:**
* Ensure the sheet exists and is editable.
* Verify API status update permissions.

***

#### **SCIK-0451: Unable to save dashboard as copy**

**Explanation:**\
Copying the dashboard failed.\
**Cause:**

* Name conflict or internal save error.\
  **Resolution:**
* Use a unique name for the copy.
* Ensure all components are valid.

#### **SCIK-0492: Unable to reshape dimension for matrix**

**Explanation:**\
Matrix transformation failed due to incompatible dimensions.\
**Cause:**

* Input data shape mismatch.
* Incorrect parameters passed for reshaping.\
  **Resolution:**
* Validate input dimensions.
* Adjust reshaping logic to match data structure.

***

#### **SCIK-0493: Unable to delete report**

**Explanation:**\
System could not delete the selected report.\
**Cause:**

* Report is linked to dashboards or scheduled tasks.
* Insufficient user permissions.\
  **Resolution:**
* Remove all dependencies first.
* Retry with proper access rights.

***

#### **SCIK-0494: Unable to list report**

**Explanation:**\
Failed to load available reports.\
**Cause:**

* Backend error or report table inaccessible.
* Permission restrictions.\
  **Resolution:**
* Check report service status.
* Confirm user roles allow report listing.

***

#### **SCIK-0495: Unable to create report**

**Explanation:**\
Report creation process failed.\
**Cause:**

* Missing required fields.
* System error while saving report.\
  **Resolution:**
* Provide valid report parameters.
* Retry after correcting any configuration issues.

***

#### **SCIK-0496: Unable to edit report**

**Explanation:**\
System failed to apply changes to the report.\
**Cause:**

* Report locked or already published.
* User lacks edit rights.\
  **Resolution:**
* Unlock report and verify permissions.
* Reapply changes after resolving conflicts.

***

#### **SCIK-0497: Unable to get table data**

**Explanation:**\
Could not fetch table data for the report/dashboard.\
**Cause:**

* Query execution error.
* Source table unavailable.\
  **Resolution:**
* Verify table existence and structure.
* Check backend logs for SQL or API errors.

***

#### **SCIK-0498: Unable to retrieve filtered data**

**Explanation:**\
Data filtering operation failed.\
**Cause:**

* Invalid filter condition or missing field.\
  **Resolution:**
* Review filter criteria.
* Ensure field mappings are correct.

***

#### **SCIK-0499: Unable to publish report**

**Explanation:**\
Publishing of the report was unsuccessful.\
**Cause:**

* Report has validation issues.
* Backend error during deployment.\
  **Resolution:**
* Resolve all validation errors.
* Retry publishing after system check.

***

#### **SCIK-0500: Unable to view IFrame component of report**

**Explanation:**\
IFrame component rendering failed in report.\
**Cause:**

* Cross-origin policy or broken link.\
  **Resolution:**
* Validate IFrame source and domain settings.
* Fix or replace the embedded URL.

***

#### **SCIK-0501: Unable to view components of report**

**Explanation:**\
Report components could not be retrieved.\
**Cause:**

* Incomplete or corrupted report structure.\
  **Resolution:**
* Rebuild or reimport components.
* Check for missing references.

***

#### **SCIK-0502: Unable to get JSON string data of the report**

**Explanation:**\
System failed to generate JSON data for the report.\
**Cause:**

* Report configuration error or circular reference.\
  **Resolution:**
* Validate report structure.
* Retry export or generation process.

***

#### **SCIK-0503: Unable to retrieve dimension metrics of the dataset**

**Explanation:**\
Failed to get dimension and metric details from dataset.\
**Cause:**

* Dataset schema not accessible or invalid.\
  **Resolution:**
* Check dataset mapping and schema.
* Ensure backend services are operational.

***

#### **SCIK-0504: Unable to retrieve report information**

**Explanation:**\
System was unable to fetch the metadata of the report.\
**Cause:**

* Report ID does not exist or is corrupted.\
  **Resolution:**
* Use a valid report reference.
* Recheck report registry or metadata table.

***

#### **SCIK-0505: Unable to retrieve report data**

**Explanation:**\
Data loading failed for the report.\
**Cause:**

* Report query failed or dataset missing.\
  **Resolution:**
* Verify dataset connection.
* Check and debug report query logic.

***

#### **SCIK-0506: Unable to delete calculated field**

**Explanation:**\
System could not remove the calculated field.\
**Cause:**

* Field is used in active reports or dashboards.\
  **Resolution:**
* Remove references before deletion.
* Reattempt deletion afterward.

***

#### **SCIK-0507: Unable to get calculated field**

**Explanation:**\
Failed to retrieve the calculated field details.\
**Cause:**

* Field not found or data retrieval error.\
  **Resolution:**
* Verify field name and location.
* Ensure backend fetch is working properly.

***

#### **SCIK-0508: Unable to add calculated field**

**Explanation:**\
Adding a new calculated field failed.\
**Cause:**

* Invalid formula or unsupported operation.\
  **Resolution:**
* Validate expression syntax.
* Recheck available fields and functions.

***

#### **SCIK-0509: Unable to view report classification list**

**Explanation:**\
Could not display the list of report classifications.\
**Cause:**

* Classification metadata missing.\
  **Resolution:**
* Ensure classifications are configured.
* Reload or reinitialize classification module.

***

#### **SCIK-0510: Unable to save report classification list**

**Explanation:**\
Saving report classifications failed.\
**Cause:**

* Database error or validation issue.\
  **Resolution:**
* Recheck input data.
* Retry after correcting format or constraints.

***

#### **SCIK-0511: Unable to save report classification category**

**Explanation:**\
Failed to save a category within the classification system.\
**Cause:**

* Category name duplication or missing input.\
  **Resolution:**
* Provide a unique name.
* Ensure all required fields are filled.

***

#### **SCIK-0512: Unable to view report classified list**

**Explanation:**\
System could not retrieve the list of classified reports.\
**Cause:**

* Classification tags missing or corrupted.\
  **Resolution:**
* Re-tag reports correctly.
* Ensure backend classification module is operational.

### Module: Data dictionarty

#### **SCIK-0277: These headers are missing from the uploaded file {}**

**Explanation:**\
The uploaded file does not contain one or more required headers.\
**Cause:**

* The file format is incorrect or headers are not aligned with expected schema.
* Headers are misspelled or missing entirely.
* File might be corrupted or improperly exported from the source.\
  **Resolution:**
* Review the required headers for the upload process.
* Ensure that all mandatory headers are included and spelled correctly.
* Re-export or reformat the file according to the provided template or specification.

### Module: Data Product Factory

#### **SCIK-0114: Product List is not correct.**

**Explanation:**\
The product list provided is invalid or incorrectly formatted.\
**Cause:**

* Missing mandatory product attributes.
* Data inconsistency or invalid entries.\
  **Resolution:**
* Validate the product list against expected format.
* Correct data and retry the operation.

***

#### **SCIK-0452: Unable to deploy data product.**

**Explanation:**\
Deployment of the selected data product failed.\
**Cause:**

* Configuration or environment issues.
* Backend deployment service error.\
  **Resolution:**
* Check deployment logs for errors.
* Ensure the environment and configurations are valid.

***

#### **SCIK-0453: Unable to save data product.**

**Explanation:**\
System failed to save the data product configuration.\
**Cause:**

* Missing required fields or metadata.
* Database write failure.\
  **Resolution:**
* Provide complete and valid data.
* Retry after confirming backend connectivity.

***

#### **SCIK-0454: Unable to update product bundle.**

**Explanation:**\
Updating the product bundle was unsuccessful.\
**Cause:**

* Bundle references outdated or incorrect.
* User does not have permission.\
  **Resolution:**
* Verify bundle details and update dependencies.
* Check user roles and access privileges.

***

#### **SCIK-0455: Unable to remove product bundle.**

**Explanation:**\
Product bundle deletion failed.\
**Cause:**

* Bundle is in use or linked to active products.
* System constraint preventing removal.\
  **Resolution:**
* Detach dependencies before deletion.
* Retry after confirming no usage conflicts.

***

#### **SCIK-0456: Unable to retrieve data product list.**

**Explanation:**\
The list of data products could not be fetched.\
**Cause:**

* Backend service timeout or unresponsive.
* Insufficient access rights.\
  **Resolution:**
* Retry after checking system health.
* Confirm proper access roles.

***

#### **SCIK-0457: Unable to delete data product.**

**Explanation:**\
The selected data product could not be deleted.\
**Cause:**

* Product is linked to active use cases.
* Permission or internal error.\
  **Resolution:**
* Remove associations before deletion.
* Ensure user has delete rights.

***

#### **SCIK-0458: Failed to retrieve data product.**

**Explanation:**\
Data product details could not be loaded.\
**Cause:**

* Invalid product ID or missing entry.
* Backend error.\
  **Resolution:**
* Verify product ID.
* Retry after ensuring backend availability.

***

#### **SCIK-0459: Unable to register data product.**

**Explanation:**\
Registration of new data product failed.\
**Cause:**

* Missing metadata or identifier conflict.
* System constraint violation.\
  **Resolution:**
* Fill all mandatory registration fields.
* Ensure product ID is unique.

***

#### **SCIK-0460: Unable to update product pricing.**

**Explanation:**\
Updating pricing for the product was not successful.\
**Cause:**

* Invalid pricing format or missing values.
* System error during update operation.\
  **Resolution:**
* Provide valid pricing data.
* Retry after backend validation.

***

#### **SCIK-0461: Unable to retrieve product bundle.**

**Explanation:**\
Fetching specific product bundle failed.\
**Cause:**

* Bundle ID not found or deleted.
* Retrieval logic error.\
  **Resolution:**
* Reconfirm bundle reference.
* Refresh and retry operation.

***

#### **SCIK-0462: Unable to retrieve product bundles list.**

**Explanation:**\
System failed to list all available product bundles.\
**Cause:**

* Network or API service issue.
* Data inconsistency.\
  **Resolution:**
* Check service logs.
* Retry after backend confirmation.

***

#### **SCIK-0463: Unable to save usecase.**

**Explanation:**\
System could not persist the use case configuration.\
**Cause:**

* Missing fields or invalid inputs.
* Save operation error.\
  **Resolution:**
* Ensure all required fields are completed.
* Retry saving after validation.

***

#### **SCIK-0464: Failed to retrieve saved usecases list.**

**Explanation:**\
Saved use cases could not be listed.\
**Cause:**

* Backend service failure or user access restriction.\
  **Resolution:**
* Check backend logs.
* Verify access permissions.

***

#### **SCIK-0465: Unable to delete saved usecase.**

**Explanation:**\
Deletion of the selected saved use case failed.\
**Cause:**

* Use case is linked to active products or dashboards.
* Permission issue or backend failure.\
  **Resolution:**
* Detach dependencies.
* Retry deletion with proper permissions.



### Module: Dataset

#### **SCIK-0014: Dataset not found.**

**Explanation:**\
The specified dataset could not be located in the system.\
**Cause:**

* Dataset ID is invalid or does not exist.
* Dataset may have been deleted or never created.\
  **Resolution:**
* Verify dataset ID.
* Ensure dataset exists in the system.

***

#### **SCIK-0015: Model name already exist!**

**Explanation:**\
A dataset with the same model name already exists.\
**Cause:**

* Duplicate model name entry during creation.\
  **Resolution:**
* Use a unique model name for the dataset.
* Check existing entries before saving.

***

#### **SCIK-0016: Unable to save data set!**

**Explanation:**\
The system failed to save the dataset.\
**Cause:**

* Missing mandatory fields.
* Database or system error.\
  **Resolution:**
* Ensure all required fields are populated.
* Retry after checking backend status.

***

#### **SCIK-0020: dim\_mat\_name or dataset\_id or column\_type is not valid**

**Explanation:**\
One or more input fields for dimensions are invalid.\
**Cause:**

* Incorrect or null values for dimension matrix name, dataset ID, or column type.\
  **Resolution:**
* Validate all input parameters.
* Ensure fields match expected format and values.

***

#### **SCIK-0031: dataset\_id key is not valid.**

**Explanation:**\
The provided dataset ID key is invalid.\
**Cause:**

* Key is missing, malformed, or not found in the database.\
  **Resolution:**
* Check and correct the dataset\_id value.
* Ensure the key exists and is active.

***

#### **SCIK-0119: No dashboard found, please select any dataset**

**Explanation:**\
Operation requires a dataset to proceed, but none was selected.\
**Cause:**

* Dataset selection was skipped.\
  **Resolution:**
* Select a valid dataset before proceeding.

***

#### **SCIK-0121: Error: Please select any of dataset**

**Explanation:**\
A dataset must be selected to continue the operation.\
**Cause:**

* No dataset selected by the user.\
  **Resolution:**
* Choose a dataset from the available list.

***

#### **SCIK-0122: No dashboard found, please select any dataset**

**Explanation:**\
System couldn't find an associated dashboard as no dataset was selected.\
**Cause:**

* Missing dataset selection in the mapping operation.\
  **Resolution:**
* Select a dataset before initiating dashboard mapping.

***

#### **SCIK-0123: No dashboard found, please select any dataset**

**Explanation:**\
No dataset selected while trying to update mapping.\
**Cause:**

* Dataset association not provided.\
  **Resolution:**
* Select an appropriate dataset for the update.

***

#### **SCIK-0126: DataSet key is not valid**

**Explanation:**\
Invalid dataset key was used in the request.\
**Cause:**

* Dataset key is missing or corrupted.\
  **Resolution:**
* Verify dataset key format and source.

***

#### **SCIK-0127: Failure DataSet delete**

**Explanation:**\
The dataset could not be deleted.\
**Cause:**

* Dataset is linked to dependent components.
* System error during deletion.\
  **Resolution:**
* Remove dependencies before deletion.
* Retry after confirming dataset status.

***

#### **SCIK-0129: Dataset data missing**

**Explanation:**\
No data available for the selected dataset.\
**Cause:**

* Dataset is empty or failed to load.\
  **Resolution:**
* Confirm data source is valid.
* Reload or repopulate the dataset.

***

#### **SCIK-0131: Dataset id is required**

**Explanation:**\
Dataset ID is mandatory but was not provided.\
**Cause:**

* Missing dataset ID in request.\
  **Resolution:**
* Ensure dataset ID is passed as part of the request.

***

#### **SCIK-0244: Dataset is not approved asset({}).**

**Explanation:**\
The dataset has not been approved for use.\
**Cause:**

* Asset approval pending or rejected.\
  **Resolution:**
* Complete dataset approval process.
* Contact administrator if needed.

***

#### **SCIK-0246: Please pass filter in correct format**

**Explanation:**\
The filter parameters are incorrectly formatted.\
**Cause:**

* Syntax or structure error in filter query.\
  **Resolution:**
* Format the filters according to API requirements.
* Use supported operators and structure.

***

#### **SCIK-0438: Unable to retrieve dataset data.**

**Explanation:**\
Failed to load or fetch dataset records.\
**Cause:**

* Dataset source inaccessible or empty.\
  **Resolution:**
* Verify data connectivity and source availability.

***

#### **SCIK-0467: Unable to fetch dataset.**

**Explanation:**\
Dataset could not be retrieved.\
**Cause:**

* Backend timeout or invalid ID.\
  **Resolution:**
* Check dataset ID and retry.
* Ensure services are up.

***

#### **SCIK-0468: Failed to preview dataset.**

**Explanation:**\
Preview of the dataset could not be generated.\
**Cause:**

* Data inconsistency or rendering issue.\
  **Resolution:**
* Validate data structure.
* Retry after fixing formatting issues.

***

#### **SCIK-0469: Unable to update dataset token.**

**Explanation:**\
System couldn't update the token associated with the dataset.\
**Cause:**

* Invalid or expired token reference.\
  **Resolution:**
* Regenerate a new token if required.
* Check permissions.

***

#### **SCIK-0470: Unable to generate dataset token.**

**Explanation:**\
Token creation for dataset failed.\
**Cause:**

* System error or missing dataset ID.\
  **Resolution:**
* Retry with valid dataset reference.

***

#### **SCIK-0471: Unable to retrieve dataset token list.**

**Explanation:**\
Failed to fetch existing tokens for the dataset.\
**Cause:**

* Token records missing or corrupted.\
  **Resolution:**
* Verify dataset and backend token service.

***

#### **SCIK-0472: Unable to fetch dataset token.**

**Explanation:**\
Unable to fetch a specific token related to the dataset.\
**Cause:**

* Token not found or expired.\
  **Resolution:**
* Reissue the token.
* Validate token status.

***

#### **SCIK-0473: Unable to retrieve dataset metadata.**

**Explanation:**\
Failed to load metadata associated with the dataset.\
**Cause:**

* Metadata missing or access issue.\
  **Resolution:**
* Revalidate metadata definitions.
* Retry after backend fix.

***

#### **SCIK-0474: Unable to read table data.**

**Explanation:**\
Reading data from the source table failed.\
**Cause:**

* Source table inaccessible or empty.\
  **Resolution:**
* Confirm table permissions and availability.

***

#### **SCIK-0475: Unable to verify data dictionary.**

**Explanation:**\
Validation of data dictionary failed.\
**Cause:**

* Incorrect dictionary structure or format.\
  **Resolution:**
* Review dictionary template.
* Ensure correct mapping with dataset.

***

#### **SCIK-0476: Unable to delete dataset.**

**Explanation:**\
System failed to delete the dataset.\
**Cause:**

* Dataset in use or locked.\
  **Resolution:**
* Remove dependencies.
* Retry with proper permissions.

***

#### **SCIK-0477: Unable to create dataset.**

**Explanation:**\
Creation of new dataset failed.\
**Cause:**

* Missing fields or validation error.\
  **Resolution:**
* Fill mandatory data.
* Retry creation.

***

#### **SCIK-0478: Unable to edit dataset.**

**Explanation:**\
Dataset update operation failed.\
**Cause:**

* Invalid update fields or locked dataset.\
  **Resolution:**
* Verify editable fields.
* Retry with correct parameters.

***

#### **SCIK-0479: Unable to retrieve dataset list.**

**Explanation:**\
Failed to load the list of datasets.\
**Cause:**

* Backend issue or access restriction.\
  **Resolution:**
* Ensure access rights.
* Retry after system check.

***

#### **SCIK-0480: Unable to access dataset data via API.**

**Explanation:**\
API failed to deliver dataset content.\
**Cause:**

* Unauthorized access or bad endpoint.\
  **Resolution:**
* Check API token and dataset permissions.

***

#### **SCIK-0482: Unable to fetch dataset columns.**

**Explanation:**\
System could not retrieve column details of the dataset.\
**Cause:**

* Dataset schema undefined or corrupted.\
  **Resolution:**
* Refresh schema metadata.
* Retry fetch operation.

***

#### **SCIK-0483: Unable to get dataset metadata.**

**Explanation:**\
Metadata fetch failed for dataset.\
**Cause:**

* Metadata reference missing.\
  **Resolution:**
* Verify dataset schema linkage.

***

#### **SCIK-0484: Unable to update dataset metadata.**

**Explanation:**\
Failed to modify dataset metadata.\
**Cause:**

* Schema lock or invalid metadata structure.\
  **Resolution:**
* Use correct metadata format.
* Retry after schema unlock.

### Module: Datasource

#### **SCIK-0048: connection\_id is required**

**Explanation:**\
The system requires a connection ID to proceed.\
**Cause:**

* `connection_id` parameter is missing in the request.\
  **Resolution:**
* Ensure `connection_id` is supplied when calling the API or UI flow.

***

#### **SCIK-0138: Up to date**

**Explanation:**\
The data source or object is already current.\
**Cause:**

* No updates needed; the system is already synchronized.\
  **Resolution:**
* No action required; simply confirm the state.

***

#### **SCIK-0140: Empty**

**Explanation:**\
A required field or file is empty.\
**Cause:**

* User did not provide necessary input or upload.\
  **Resolution:**
* Provide the expected input or file before proceeding.

***

#### **SCIK-0143: Connection already exists**

**Explanation:**\
A connection with the same parameters is already present.\
**Cause:**

* Duplicate connection created by the user.\
  **Resolution:**
* Use the existing connection or delete the duplicate and recreate.

***

#### **SCIK-0145: Location Does Not exist!**

**Explanation:**\
The specified location parameter is invalid.\
**Cause:**

* Incorrect or missing location value.
* Location not recognized in the system.\
  **Resolution:**
* Provide a valid location identifier or value.

***

#### **SCIK-0147: File name already exists**

**Explanation:**\
The uploaded file has a duplicate name in the system.\
**Cause:**

* Naming conflict with an existing file.\
  **Resolution:**
* Rename the file before uploading.

***

#### **SCIK-0148: Unable to delete connection.**

**Explanation:**\
The system failed to remove the specified connection.\
**Cause:**

* Connection in use or internal deletion error.\
  **Resolution:**
* Ensure connection is not active; then retry deletion.

***

#### **SCIK-0149: Error in getAllDb**

**Explanation:**\
System error occurred while fetching all databases.\
**Cause:**

* Backend service unavailable.\
  **Resolution:**
* Retry after confirming database service is operational.

***

#### **SCIK-0150: Connection id key is not valid**

**Explanation:**\
Provided connection ID is incorrect or invalid.\
**Cause:**

* Typo or non-existent connection reference.\
  **Resolution:**
* Verify and supply a valid connection ID.

***

#### **SCIK-0151: Connection already deleted.**

**Explanation:**\
The targeted connection has already been removed.\
**Cause:**

* Duplicate deletion request.\
  **Resolution:**
* Confirm deletion status; refresh connection list.

***

#### **SCIK-0152: Connection not established!**

**Explanation:**\
The connection could not be established with the data source.\
**Cause:**

* Network issues or incorrect credentials.\
  **Resolution:**
* Check credentials and network configuration; retry.

***

#### **SCIK-0153: Failure MySQL server schema creation**

**Explanation:**\
Failed to create MySQL schema on target server.\
**Cause:**

* Insufficient privileges or schema conflict.\
  **Resolution:**
* Ensure user has privileges and schema does not already exist.

***

#### **SCIK-0156: Please select file with format csv/xls.**

**Explanation:**\
Only CSV or XLS files are allowed for upload.\
**Cause:**

* Invalid file format selected.\
  **Resolution:**
* Upload a supported CSV or XLS file.

***

#### **SCIK-0157: Please select file less than 5 mb.**

**Explanation:**\
File size exceeds the 5 MB upload limit.\
**Cause:**

* File is too large.\
  **Resolution:**
* Compress or split file to under 5 MB.

***

#### **SCIK-0158: Invalid data selected, please check correct format with correct delimiter.**

**Explanation:**\
Uploaded file has formatting or delimiter issues.\
**Cause:**

* Incorrect delimiter or malformed rows.\
  **Resolution:**
* Adjust file format and delimiter to match specification.

***

#### **SCIK-0159: Error fileupload edit page metadata not found**

**Explanation:**\
Metadata needed for editing file upload page is unavailable.\
**Cause:**

* Backend failed to provide necessary configuration.\
  **Resolution:**
* Check metadata availability; retry UI load.

***

#### **SCIK-0160: Please select file with pdf format**

**Explanation:**\
Only PDF format is accepted for this operation.\
**Cause:**

* Incorrect file format selected.\
  **Resolution:**
* Upload a valid PDF file.

***

#### **SCIK-0161: File not found!**

**Explanation:**\
Specified file does not exist or cannot be accessed.\
**Cause:**

* File path incorrect or file deleted.\
  **Resolution:**
* Verify file path or re-upload the file.

***

#### **SCIK-0162: Failed to update Connection.**

**Explanation:**\
The system couldn’t apply updates to the connection.\
**Cause:**

* Invalid update data or backend error.\
  **Resolution:**
* Check input values and retry; validate service health.

***

#### **SCIK-0163: Access Denied, please check your credentials!**

**Explanation:**\
Invalid credentials were supplied for the data source.\
**Cause:**

* Wrong username or password.\
  **Resolution:**
* Correct credentials and attempt reconnection.

***

#### **SCIK-0164: Server is unavailable or Does Not Exist!**

**Explanation:**\
Target data server is unreachable or undefined.\
**Cause:**

* Server down or host name invalid.\
  **Resolution:**
* Validate server endpoint; check connectivity.

***

#### **SCIK-0174: Data Source already deleted or wrong parameter provided. Please contact Admin!**

**Explanation:**\
Data source cannot be found or parameter is invalid.\
**Cause:**

* Data source was removed or request malformed.\
  **Resolution:**
* Confirm data source status; escalate to admin.

***

#### **SCIK-0217: Connection Name already exists!**

**Explanation:**\
The name chosen for the connection is already in use.\
**Cause:**

* Duplicate name attempt during creation/edit.\
  **Resolution:**
* Provide a unique connection name.

***

#### **SCIK-0220: Unable to upload {} file!**

**Explanation:**\
File upload failed for the specified file name.\
**Cause:**

* I/O error or backend upload failure.\
  **Resolution:**
* Retry upload; verify file integrity.

***

#### **SCIK-0221: Glossary not found for the table {}**

**Explanation:**\
No glossary metadata exists for the selected table.\
**Cause:**

* Missing glossary entry for that table.\
  **Resolution:**
* Add glossary entry or correct table reference.

***

#### **SCIK-0222: Connection not found!**

**Explanation:**\
Requested connection does not exist.\
**Cause:**

* Incorrect connection ID or deleted entry.\
  **Resolution:**
* Confirm connection exists; refresh list.

***

#### **SCIK-0245: Kafka connection already exists with this name!**

**Explanation:**\
A Kafka connection with that name is already configured.\
**Cause:**

* Duplicate naming for Kafka connector.\
  **Resolution:**
* Choose a different name for the connection.

***

#### **SCIK-0249: Follow the link to get authenticate**

**Explanation:**\
User must authenticate via a provided link.\
**Cause:**

* SSO or OAuth flow not completed.\
  **Resolution:**
* Click on the link and complete authentication process.

***

#### **SCIK-0250: Unable to generate token**

**Explanation:**\
Token creation for the operation failed.\
**Cause:**

* Backend service error or missing data.\
  **Resolution:**
* Retry after checking service availability.

***

#### **SCIK-0251: File with this name already exists**

**Explanation:**\
Cannot upload — filename conflicts with existing file.\
**Cause:**

* Duplicate name in storage.\
  **Resolution:**
* Rename file before attempting upload again.

***

#### **SCIK-0297: Connection used in the admin settings cannot be deleted**

**Explanation:**\
This connection is required for admin-level configurations.\
**Cause:**

* Connection is referenced in system settings.\
  **Resolution:**
* Remove dependency or update admin config first.

***

#### **SCIK-0301: Unable to fetch datasource table list.**

**Explanation:**\
Failed to list tables from the data source.\
**Cause:**

* Permission denied or fetch timeout.\
  **Resolution:**
* Verify connection permissions; retry fetch.

***

#### **SCIK-0321: Unable to fetch schema details for the topic: {}.**

**Explanation:**\
Schema information for the given topic could not be retrieved.\
**Cause:**

* Topic name invalid or schema registry error.\
  **Resolution:**
* Validate topic exists and retry schema fetch.

***

#### **SCIK-0410: Failed to get Glue jobs list.**

**Explanation:**\
System couldn’t retrieve AWS Glue jobs.\
**Cause:**

* AWS permissions/configuration invalid.\
  **Resolution:**
* Confirm IAM permissions and AWS endpoints.

***

#### **SCIK-0411: Failed to get Glue crawler list.**

**Explanation:**\
Could not fetch AWS Glue crawler configurations.\
**Cause:**

* Glue service unavailable or permission lacking.\
  **Resolution:**
* Check AWS settings and retry crawler list retrieval.

***

#### **SCIK-0422: Unable to fetch AWS image.**

**Explanation:**\
Failed to retrieve an image/resource from AWS.\
**Cause:**

* S3 ACL or path misconfiguration.\
  **Resolution:**
* Validate AWS path and access rights.

### Module:  Discovery

#### **SCIK-0278: RESOURCE\_DISCOVERY\_SUCCESS**

**Message:**\
`{resource_type}: '{resource_name}' is discovered in background`\
**Explanation:**\
The system successfully found a resource (e.g., database, table, or service) in the background discovery process.\
**Cause:**\
Discovery process completed without errors.\
**Resolution:**\
No action needed; the resource is now available for further operations.

***

#### **SCIK-0279: RESOURCE\_DISCOVERY\_FAIL**

**Message:**\
`{resource_type}: '{resource_name}' discovery failed`\
**Explanation:**\
Discovery process failed to find or access the specified resource.\
**Cause:**

* Network issue
* Incorrect resource name or inaccessible resource
* Permission denied\
  **Resolution:**
* Check connectivity and permissions for the resource.
* Verify resource identifier correctness.

***

#### **SCIK-0280: FOUND\_TABLE\_ADDED**

**Message:**\
`A new table '{table}' found in {resource_type}: '{resource_name}'`\
**Explanation:**\
A new table was detected in the specified resource during discovery.\
**Cause:**

* New table added since last discovery.\
  **Resolution:**
* Optionally update metadata or inform users of the new table.

***

#### **SCIK-0281: FOUND\_TABLE\_DELETED**

**Message:**\
`A table '{table}' found deleted in {resource_type}: '{resource_name}'`\
**Explanation:**\
A previously discovered table was removed from the resource.\
**Cause:**

* Table deleted or dropped externally.\
  **Resolution:**
* Update metadata; handle impacts on dependent processes.

***

#### **SCIK-0282: FOUND\_BULK\_TABLE\_ADDED**

**Message:**\
`Tables {table} found in {resource_type}: '{resource_name}'`\
**Explanation:**\
Multiple new tables detected during discovery in the specified resource.\
**Cause:**

* Bulk addition of tables.\
  **Resolution:**
* Update system metadata or notify stakeholders.

***

#### **SCIK-0283: FOUND\_BULK\_TABLE\_DELETED**

**Message:**\
`Tables {table} found deleted in {resource_type}: '{resource_name}'`\
**Explanation:**\
Multiple tables were removed from the resource.\
**Cause:**

* Bulk deletion of tables.\
  **Resolution:**
* Sync metadata; review impact on data consumers.

***

#### **SCIK-0284: FOUND\_COLUMN\_ADDED**

**Message:**\
`A column '{column}' added found in table '{table}' '{resource_type}': '{resource_name}'`\
**Explanation:**\
A new column was added to an existing table.\
**Cause:**

* Schema change by adding a column.\
  **Resolution:**
* Update schema metadata accordingly.

***

#### **SCIK-0285: FOUND\_BULK\_COLUMNS\_ADDED**

**Message:**\
`Columns {columns} added found in table '{table}' '{resource_type}': '{resource_name}'`\
**Explanation:**\
Multiple columns added to a table.\
**Cause:**

* Bulk schema alteration.\
  **Resolution:**
* Update metadata to reflect new columns.

***

#### **SCIK-0286: FOUND\_COLUMN\_ALTERED**

**Message:**\
`Column '{column}' {property} modified from {from} to {to} found in table '{table}' '{resource_type}': '{resource_name}'`\
**Explanation:**\
A column’s property (e.g., datatype, length) was changed.\
**Cause:**

* Schema alteration operation on column property.\
  **Resolution:**
* Synchronize metadata with the updated column definition.

***

#### **SCIK-0287: FOUND\_BULK\_COLUMN\_ALTERED**

**Message:**\
`Columns '{column}' {property} modified from {from} to {to} found in table '{table}' '{resource_type}': '{resource_name}'`\
**Explanation:**\
Multiple columns were altered in the table.\
**Cause:**

* Bulk column modifications.\
  **Resolution:**
* Update all relevant metadata.

***

#### **SCIK-0289: FOUND\_ALTERED\_LINEAGE\_AFFECTED**

**Message:**\
`{lineage_affected_stmt} Column '{column}' {property} modified from {from} to {to} found in table '{table}' '{resource_type}': '{resource_name}'`\
**Explanation:**\
A column alteration impacted data lineage or dependencies.\
**Cause:**

* Column change affecting lineage.\
  **Resolution:**
* Update lineage metadata and notify relevant owners.

***

#### **SCIK-0290: FOUND\_COLUMN\_DELETED**

**Message:**\
`A column delete found in '{resource_type}' '{resource_name}' table {table}, deleted column: '{column}'`\
**Explanation:**\
A column was deleted from a table.\
**Cause:**

* Column dropped or removed.\
  **Resolution:**
* Remove column metadata and handle impact on data flows.

***

#### **SCIK-0291: FOUND\_BULK\_COLUMN\_DELETED**

**Message:**\
`A bulk column delete found in {resource_type} {resource_name} table {table}, deleted columns: {columns}`\
**Explanation:**\
Multiple columns were deleted.\
**Cause:**

* Bulk column deletions.\
  **Resolution:**
* Sync schema metadata accordingly.

***

#### **SCIK-0292: FOUND\_DELETED\_LINEAGE\_AFFECTED**

**Message:**\
`{lineage_affected_stmt} column delete found in '{resource_type}' '{resource_name}' table {table}, deleted column: '{column}'`\
**Explanation:**\
Column deletion affecting data lineage.\
**Cause:**

* Column removal impacts lineage tracking.\
  **Resolution:**
* Update lineage metadata and communicate changes.

***

#### **SCIK-0379: MSG\_DISC\_REQ\_ERROR**

**Message:**\
`Unable to initiate discovery request.`\
**Explanation:**\
The discovery service failed to start the resource scan.\
**Cause:**

* Configuration error, permission issue, or service down.\
  **Resolution:**
* Verify discovery service health and permissions; retry request.

### Module: DQ

**SCIK-0254: Relationship already exists**\
**Explanation:**\
Attempt to create a relationship that already exists in the observability data quality module.\
**Cause:**

* Duplicate entry of an existing relationship.
* Attempt to re-add a previously created relationship.\
  **Resolution:**
* Verify existing relationships before creating new ones.
* Avoid duplicating relationships; edit existing ones if needed.

***

**SCIK-0255: At least one column required**\
**Explanation:**\
Operation requires at least one column to be specified but none was provided.\
**Cause:**

* No columns selected when defining the observability table relationship.
* Missing mandatory fields in the configuration.\
  **Resolution:**
* Ensure at least one column is selected before proceeding.
* Validate required fields during input.

***

**SCIK-0256: Select required columns**\
**Explanation:**\
Columns required for the operation were not selected.\
**Cause:**

* User did not select necessary columns in the observability table.
* Missing input in column selection step.\
  **Resolution:**
* Review and select all mandatory columns.
* Enforce validation on column selection.

***

**SCIK-0257: Selected Column not mapped**\
**Explanation:**\
One or more selected columns have not been mapped to any target field.\
**Cause:**

* Column mapping step incomplete or missed.
* Data mapping definitions missing for selected columns.\
  **Resolution:**
* Map all selected columns appropriately before proceeding.
* Check the mapping configuration for completeness.

***

**SCIK-0266: Observability Relation doesn't exist**\
**Explanation:**\
Referenced observability relation was not found in the system.\
**Cause:**

* Relation was deleted or never created.
* Incorrect relation identifier used.\
  **Resolution:**
* Verify relation existence before reference.
* Create the required relation if missing.

***

**SCIK-0267: Selected date already commented. Edit Comments**\
**Explanation:**\
User tried to add a comment on a date that already has an existing comment.\
**Cause:**

* Duplicate commenting on the same date entry.\
  **Resolution:**
* Edit the existing comment instead of adding a new one.
* Prevent duplicate comments by checking for existing entries.

***

**SCIK-0408: Unable to retrieve data quality operator list**\
**Explanation:**\
Failed to fetch the list of data quality operators.\
**Cause:**

* Backend service error or unavailability.
* Network issues or permissions restricting access.\
  **Resolution:**
* Check backend service status and connectivity.
* Verify user permissions to access operator lists.

### Module: Entity

**SCIK-0044: Cant delete client entity**\
**Explanation:**\
The system prevented deletion of a client entity due to constraints or dependencies.\
**Cause:**

* The client entity is linked to other records or transactions preventing deletion.
* Permissions do not allow the deletion of this entity.
* System rules restrict deletion to maintain data integrity.\
  **Resolution:**
* Check for dependent records or links to the client entity and remove or update them first.
* Confirm user has the necessary permissions to delete the entity.
* Review business rules regarding entity deletion and follow the correct process.

***

**SCIK-0367: Unable to update selected entity.**\
**Explanation:**\
The update operation on the selected entity failed.\
**Cause:**

* Validation errors or incorrect data in the update request.
* Entity may be locked or currently in use by another process.
* Backend system or database issues during update operation.\
  **Resolution:**
* Verify the data being submitted for update meets validation requirements.
* Ensure the entity is not locked or being edited by someone else.
* Check system and database status, retry after resolving any issues.

### Module: Governance

**SCIK-0049: System error, please contact Administrator!**\
**Explanation:**\
A general system error occurred in the Governance module preventing the operation from completing.\
**Cause:**

* Unexpected backend failure or exception.
* Configuration or environment issue impacting system functionality.\
  **Resolution:**
* Contact the system administrator for detailed investigation.
* Review system logs to identify root cause.
* Ensure proper system configuration and resource availability.

***

**SCIK-0175: Unable to send mail to Approver!**\
**Explanation:**\
Failed to deliver email notification to the designated approver.\
**Cause:**

* Email server down or misconfigured.
* Incorrect email address or network issues.
* Email service restrictions or spam filters.\
  **Resolution:**
* Check mail server connectivity and configurations.
* Verify approver email address correctness.
* Review email service logs and retry sending.

***

**SCIK-0177: Unable to update asset!**\
**Explanation:**\
Asset update operation failed in the Governance module.\
**Cause:**

* Validation errors or incomplete data during update.
* Asset locked or accessed by another process.
* Database or backend update failure.\
  **Resolution:**
* Validate input data before updating.
* Confirm asset is not locked or in use.
* Check backend service status and retry.

***

**SCIK-0185: Asset not found!**\
**Explanation:**\
Requested asset does not exist in the system.\
**Cause:**

* Asset ID or name is incorrect or missing.
* Asset was deleted or never created.\
  **Resolution:**
* Verify asset identifiers before querying.
* Confirm asset creation or restore if deleted.

***

**SCIK-0186: Invalid Asset type!**\
**Explanation:**\
Provided asset type is not recognized or supported.\
**Cause:**

* Typo or incorrect asset type supplied.
* Asset type not configured in system.\
  **Resolution:**
* Use valid and supported asset types.
* Update system configuration to include new asset types if necessary.

***

**SCIK-0187: Asset name already exist**\
**Explanation:**\
An asset with the given name already exists, preventing duplicates.\
**Cause:**

* Attempt to create or rename asset to an existing name.\
  **Resolution:**
* Use a unique name for each asset.
* Check for existing assets before naming.

***

**SCIK-0200: Pipeline with this name already exists!**\
**Explanation:**\
Duplicate pipeline name detected, which is not allowed.\
**Cause:**

* Creating or renaming a pipeline to an already used name.\
  **Resolution:**
* Choose a unique pipeline name.
* Verify existing pipeline names before saving.

***

**SCIK-0223: {} is {} by {}**\
**Explanation:**\
An asset or resource was successfully approved or changed by a user.\
**Cause:**

* Approval or status change action performed.\
  **Resolution:**
* No action needed. This is an informational success message.

***

**SCIK-0224: {} is Rejected by {}**\
**Explanation:**\
An asset or request was rejected by the specified user.\
**Cause:**

* Rejection action taken during approval workflow.\
  **Resolution:**
* Review rejection reason and update or resubmit if appropriate.

***

**SCIK-0225: {} - Delegated by {}, New Approver - {}**\
**Explanation:**\
Approval request was delegated from one approver to another.\
**Cause:**

* Approval delegation process initiated.\
  **Resolution:**
* New approver to take action as required.

***

**SCIK-0228: DataSource is not approved.**\
**Explanation:**\
The data source referenced has not received approval, restricting further actions.\
**Cause:**

* Pending or failed approval for the data source.\
  **Resolution:**
* Complete the approval process for the data source before proceeding.

***

**SCIK-0235: {} with this name already exists!**\
**Explanation:**\
Duplicate name conflict detected for an entity or asset.\
**Cause:**

* Creating or updating an entity with an existing name.\
  **Resolution:**
* Use a unique name.
* Verify existing names to avoid duplicates.

***

**SCIK-0238: MetaData does not exist for tables {}**\
**Explanation:**\
Metadata is missing for the specified tables, impacting governance operations.\
**Cause:**

* Metadata extraction or registration was not performed.\
  **Resolution:**
* Generate or import metadata for the missing tables.
* Validate metadata presence before operations.

***

**SCIK-0258: @{}, Please take an action on the ASSET Created by {}**\
**Explanation:**\
Notification requesting the mentioned user to take action on an asset created by another user.\
**Cause:**

* Pending approval or review needed on the asset.\
  **Resolution:**
* Approver or user to review and act on the asset.

***

**SCIK-0259: {}- Modify Request is Approved**\
**Explanation:**\
Modification request for the asset or entity was approved.\
**Cause:**

* Successful approval of requested changes.\
  **Resolution:**
* Proceed with implementing the approved changes.

***

**SCIK-0260: {}- Modify Request is Rejected by {}**\
**Explanation:**\
Modification request was rejected by the specified user.\
**Cause:**

* Rejection during modification approval workflow.\
  **Resolution:**
* Review rejection reason and adjust modification request accordingly.

***

**SCIK-0261: {}- Modify Request - Delegated by {}, New Approver - {}**\
**Explanation:**\
Modification approval request delegated from one approver to another.\
**Cause:**

* Delegation initiated during approval process.\
  **Resolution:**
* New approver to take necessary actions.

***

**SCIK-0262: {}- Asset Request Access is Approved by {}**\
**Explanation:**\
Access request to an asset was approved by a user.\
**Cause:**

* Successful approval of access request.\
  **Resolution:**
* Grant access as per approval.

***

**SCIK-0263: {}- Asset Request Access is Rejected by {}**\
**Explanation:**\
Access request to an asset was rejected by a user.\
**Cause:**

* Denial during access approval workflow.\
  **Resolution:**
* Notify requester of rejection and provide next steps if applicable.

***

**SCIK-0264: {}- Asset Request Access - Delegated by {}, New Approver - {}**\
**Explanation:**\
Access request approval delegated to another user.\
**Cause:**

* Delegation in approval workflow.\
  **Resolution:**
* New approver to review and approve or reject.

***

**SCIK-0265: {}- Asset Query sent by {}**\
**Explanation:**\
A query related to the asset was sent by a user.\
**Cause:**

* User initiated a query operation on the asset.\
  **Resolution:**
* Respond to or process the asset query as needed.

***

**SCIK-0268: {}- Asset is Auto Approved**\
**Explanation:**\
The asset was automatically approved by the system based on predefined rules.\
**Cause:**

* Asset met auto-approval criteria.\
  **Resolution:**
* Proceed with asset usage following auto-approval.

***

**SCIK-0271: {} - owner changed from {} to {}**\
**Explanation:**\
Ownership of an asset or entity was transferred from one user to another.\
**Cause:**

* Owner change operation completed successfully.\
  **Resolution:**
* Notify involved parties and update ownership records.

***

**SCIK-0275: Approval workflow is not configured. Please contact your Admin**\
**Explanation:**\
Approval process for the requested resource is missing or incomplete.\
**Cause:**

* Missing approval workflow configuration for the resource.\
  **Resolution:**
* Admin to configure approval workflows before proceeding.

***

**SCIK-0276: Department already exist!**\
**Explanation:**\
Attempt to create or add a department that already exists.\
**Cause:**

* Duplicate department name or identifier.\
  **Resolution:**
* Use a unique department name.
* Check existing departments before creating new ones.

***

**SCIK-0314: {}- Request Access is Approved by {}**\
**Explanation:**\
Access request was approved by a user.\
**Cause:**

* Successful approval action on access request.\
  **Resolution:**
* Grant access and notify the requester.

***

**SCIK-0315: {}- Request Access is Rejected by {}**\
**Explanation:**\
Access request was rejected by a user.\
**Cause:**

* Denial in access approval workflow.\
  **Resolution:**
* Inform requester and advise on next steps.

***

**SCIK-0316: {} - {} already exist**\
**Explanation:**\
An entity with the specified type and name already exists.\
**Cause:**

* Duplicate entry of entity and type combination.\
  **Resolution:**
* Ensure entity uniqueness before creation or update.

***

**SCIK-0325: Asset of this resource already exist witn name : {}**\
**Explanation:**\
Resource already has an asset registered with the given name.\
**Cause:**

* Duplicate asset name for the same resource.\
  **Resolution:**
* Choose a unique asset name or update existing asset.

***

### Module: MLMS

**SCIK-0331: error while getting data from whatif- {}**\
**Explanation:**\
An error occurred when attempting to retrieve data from the "whatif" component or module in the MLMS system.\
**Cause:**

* Connectivity issues between MLMS and the WhatIf service.
* Data source or API failure within the WhatIf module.
* Incorrect or malformed request parameters.\
  **Resolution:**
* Verify network connectivity and service availability for WhatIf.
* Check logs and error messages from the WhatIf service for details.
* Validate request parameters and retry the operation.
* Contact system admin if the issue persists.

### Module: Parameter

**SCIK-0139: param\_id\_is\_not\_correct**\
**Explanation:**\
The provided parameter ID is invalid or does not match any existing parameter.\
**Cause:**

* Typo or incorrect parameter ID supplied in the request.
* Parameter ID does not exist or has been deleted.\
  **Resolution:**
* Verify and correct the parameter ID before resubmitting.
* Ensure parameter ID exists in the system.

***

**SCIK-0202: Parameter values are not correct.**\
**Explanation:**\
One or more values supplied for the parameter are invalid or out of expected range.\
**Cause:**

* Data type mismatch or format error in parameter values.
* Values do not meet validation criteria or business rules.\
  **Resolution:**
* Review and correct parameter values as per specification.
* Validate parameter inputs before submission.

***

**SCIK-0203: Parameter name already exist.**\
**Explanation:**\
An attempt to create or rename a parameter to a name that already exists in the system.\
**Cause:**

* Duplicate parameter name conflicts with existing entries.\
  **Resolution:**
* Use unique names for parameters.
* Check existing parameter names before adding or renaming.

***

**SCIK-0206: Parameter empty is not allowed.**\
**Explanation:**\
The parameter value was left empty where a value is required.\
**Cause:**

* Mandatory parameter field was left blank.\
  **Resolution:**
* Provide valid, non-empty values for required parameters.

***

**SCIK-0209: Parameter mapping is not correct.**\
**Explanation:**\
Mapping between parameters or to external data is incorrect or incomplete.\
**Cause:**

* Missing or invalid mapping configuration.
* Incorrect references or links between parameters and data fields.\
  **Resolution:**
* Verify and correct the parameter mapping setup.
* Ensure all mappings are valid and complete before proceeding.

\
Module: Pipeline

**SCIK-0166: Error while executing ETL Job!**\
**Explanation:**\
The ETL (Extract, Transform, Load) job failed during execution.\
**Cause:**

* ETL job script errors or data issues.
* Resource constraints or connectivity problems.
* External system failures impacting ETL processing.\
  **Resolution:**
* Review ETL job logs to identify failure point.
* Validate ETL scripts and data inputs.
* Ensure system resources and external dependencies are operational.

***

**SCIK-0168: Error while saving ETL Job!**\
**Explanation:**\
Failed to save the ETL job configuration or metadata.\
**Cause:**

* Database or storage issues preventing save operation.
* Validation errors in ETL job details.\
  **Resolution:**
* Check database connectivity and permissions.
* Validate ETL job parameters and retry saving.

***

**SCIK-0170: Error while updating ETL Job!**\
**Explanation:**\
Update operation for an existing ETL job failed.\
**Cause:**

* Conflicts or validation errors during update.
* ETL job may be locked or in use.\
  **Resolution:**
* Verify update data and resolve conflicts.
* Ensure job is not running or locked during update.

***

**SCIK-0171: ETL Job Already Existed!**\
**Explanation:**\
Attempt to create an ETL job with a name or ID that already exists.\
**Cause:**

* Duplicate ETL job name or identifier.\
  **Resolution:**
* Use a unique name or ID for the ETL job.

***

**SCIK-0172: ETL Job Does Not Exist!**\
**Explanation:**\
Referenced ETL job could not be found.\
**Cause:**

* Incorrect ETL job identifier or deleted job.\
  **Resolution:**
* Verify the ETL job ID and ensure the job exists.

***

**SCIK-0210: Error While Saving Pipeline!**\
**Explanation:**\
Failed to save pipeline configuration or metadata.\
**Cause:**

* Database errors or validation failures.\
  **Resolution:**
* Check system and database status.
* Validate pipeline configuration before saving.

***

**SCIK-0213: Error While Deleting Pipeline!**\
**Explanation:**\
Pipeline deletion operation failed.\
**Cause:**

* Pipeline in use or locked.
* Database or permission issues.\
  **Resolution:**
* Ensure pipeline is not running or referenced.
* Verify permissions and try again.

***

**SCIK-0215: Error While Updating Pipeline!**\
**Explanation:**\
Failed to update existing pipeline configuration.\
**Cause:**

* Validation errors or conflicts.
* Pipeline locked or in use.\
  **Resolution:**
* Validate update data and resolve conflicts.
* Ensure pipeline is available for editing.

***

**SCIK-0466: Unable to execute API pipeline.**\
**Explanation:**\
API-triggered pipeline execution failed.\
**Cause:**

* API errors or misconfiguration.
* Pipeline runtime issues or dependencies missing.\
  **Resolution:**
* Check API request and pipeline configuration.
* Review logs for runtime errors and resolve.

***

**SCIK-0485: Unable to check JSON differences.**\
**Explanation:**\
Failed to perform JSON comparison, possibly for configuration or data validation.\
**Cause:**

* Malformed JSON or parsing errors.
* Missing or corrupted data.\
  **Resolution:**
* Validate JSON formats.
* Ensure required data is available and well-formed.

### Module: Scheduler

**SCIK-0036: Invalid schedule type**\
**Explanation:**\
The schedule type provided is not valid or supported.\
**Cause:**

* Incorrect or unsupported schedule type specified during job creation or update.\
  **Resolution:**
* Use a valid schedule type from the supported list.
* Refer to documentation for allowed schedule types.

***

**SCIK-0037: Creating job date-time must be greater than dependent job date-time.**\
**Explanation:**\
The scheduled start time of a job is set before its dependent job’s completion time.\
**Cause:**

* Scheduling conflict where dependent job finishes after the scheduled start time.\
  **Resolution:**
* Adjust job creation time to be after the dependent job’s scheduled completion.

***

**SCIK-0038: schedule removed**\
**Explanation:**\
A schedule was successfully deleted from the system.\
**Cause:**

* User or system requested schedule deletion.\
  **Resolution:**
* No action required; informational message confirming deletion.

***

**SCIK-0039: Jobs does not exist in scheduler**\
**Explanation:**\
The scheduler does not have any jobs configured or the requested job is missing.\
**Cause:**

* No jobs created or job ID referenced does not exist.\
  **Resolution:**
* Create the necessary jobs or verify the job ID.

***

**SCIK-0040: You have selected an invalid action**\
**Explanation:**\
The action requested on the scheduler or job is invalid or unsupported.\
**Cause:**

* Incorrect or unsupported user input for scheduler operation.\
  **Resolution:**
* Select a valid action from the supported operations list.

***

**SCIK-0041: Exception occured while play/pause/resume/stop schedule :**\
**Explanation:**\
An unexpected error occurred while performing schedule control operations.\
**Cause:**

* Internal system error, race condition, or resource issue during control command.\
  **Resolution:**
* Check system logs for detailed error.
* Retry the operation or contact admin if persistent.

***

**SCIK-0243: Scheduler name already exist.**\
**Explanation:**\
A scheduler with the specified name already exists in the system.\
**Cause:**

* Duplicate scheduler name conflict during creation or rename.\
  **Resolution:**
* Use a unique scheduler name to avoid conflict.

***

**SCIK-0313: No logs found**\
**Explanation:**\
No log entries are available for the requested scheduler or job.\
**Cause:**

* Scheduler or job has not generated logs yet or logs were purged.\
  **Resolution:**
* Confirm scheduler or job execution.
* Check logging configuration.

***

**SCIK-0335: Orchestrator Disabled. Please contact your admin!**\
**Explanation:**\
The orchestrator service required for scheduling is disabled or unavailable.\
**Cause:**

* Orchestrator service stopped, disabled, or misconfigured.\
  **Resolution:**
* Contact system administrator to enable and verify orchestrator service.

**SCIK-0019: Key is not valid.**\
**Explanation:**\
The provided key does not match the expected format or does not exist.\
**Cause:**

* Typo in the key input.
* Key expired, deleted, or invalid.\
  **Resolution:**
* Verify the key value and format.
* Generate or request a new valid key if needed.

***

**SCIK-0022: Empty Destination**\
**Explanation:**\
The destination field is empty or undefined.\
**Cause:**

* Required destination input missing during configuration or data transfer.\
  **Resolution:**
* Provide a valid destination value before proceeding.

***

**SCIK-0032: Please enter valid id key**\
**Explanation:**\
The ID key entered is not valid or recognized.\
**Cause:**

* Invalid or malformed ID key.
* The ID does not exist in the system.\
  **Resolution:**
* Confirm the correctness of the ID key.
* Use an existing, valid ID from the system.

***

**SCIK-0035: Exception occurred**\
**Explanation:**\
A general error or exception was triggered during the process.\
**Cause:**

* Backend failure or unexpected runtime issue.
* Invalid input or system misbehavior.\
  **Resolution:**
* Check system logs for the exception details.
* Retry the operation or contact admin for troubleshooting.

***

**SCIK-0045: Multitenancy Table Name is required**\
**Explanation:**\
A multitenancy-enabled operation requires a table name, which is missing.\
**Cause:**

* Multitenancy configuration not completed properly.\
  **Resolution:**
* Provide a valid multitenancy table name in the configuration.

***

**SCIK-0046: Multitenancy Column Name is required**\
**Explanation:**\
Column name for multitenancy setup is missing.\
**Cause:**

* Multitenancy column field left blank.\
  **Resolution:**
* Specify the correct multitenancy column name.

***

**SCIK-0047: Multitenancy Value is required**\
**Explanation:**\
A required value for multitenancy context is not provided.\
**Cause:**

* Missing tenant-specific identifier or context.\
  **Resolution:**
* Supply the multitenancy value (e.g., tenant ID) before proceeding.

***

**SCIK-0132: Action ID is required**\
**Explanation:**\
An operation is missing the action ID, which is mandatory.\
**Cause:**

* Action ID parameter not passed.\
  **Resolution:**
* Ensure action ID is included in the request.

***

**SCIK-0134: Action is required**\
**Explanation:**\
The requested operation requires a defined action, which is not provided.\
**Cause:**

* Missing or null action field in the input.\
  **Resolution:**
* Provide a valid action type to proceed with the request.

***

**SCIK-0137: Action Not Possible**\
**Explanation:**\
The selected action cannot be performed under current conditions.\
**Cause:**

* Action conflicts with current state of the resource.
* User does not have permission to perform the action.\
  **Resolution:**
* Validate action feasibility.
* Check resource status and user privileges.

***

**SCIK-0176: Unable to save approver details!**\
**Explanation:**\
Saving approver information failed during submission.\
**Cause:**

* Database or validation error.
* Missing required approver data.\
  **Resolution:**
* Confirm all approver details are provided and valid.
* Retry after checking system status.

***

**SCIK-0195: You don't have sufficient privilege to modify this resource. Please contact admin.**\
**Explanation:**\
The user attempted to modify a resource without the required permissions.\
**Cause:**

* Insufficient user role or privileges.\
  **Resolution:**
* Contact the administrator to request access.
* Modify user roles if appropriate permissions are needed.



**SCIK-0300: Extract Email parts suggestion cannot be applied to the selected column.**\
**Explanation:**\
The system was unable to apply the "Extract Email Parts" suggestion (e.g., extracting username or domain from email) to the selected column.\
**Cause:**

* The selected column does not contain valid email-formatted data.
* The data type or format is incompatible with the suggestion logic.\
  **Resolution:**
* Ensure the column contains properly formatted email addresses (e.g., `user@example.com`).
* Choose a different column with valid email data.
* Validate and clean data before applying the suggestion.
