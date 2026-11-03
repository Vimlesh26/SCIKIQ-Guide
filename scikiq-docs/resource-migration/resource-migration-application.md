---
hidden: true
---

# Resource Migration Application

1\. Introduction

The Resource Migration Application (RMA) is designed to streamline and standardize the migration of resources across different environments within the Scikiq Application ecosystem. It ensures that business-critical resources such as ETL jobs, Dashboards, and Logical Data Models (LDMs) are migrated securely and systematically from Development (Dev) → User Acceptance Testing (UAT) → Production (Prod) environments.

The solution follows a request-and-approval model, ensuring governance, traceability, and controlled release of resources.

\---

2\. Objectives

· Provide a centralized platform for resource migration.

· Enable a request-driven migration process to enforce checks and balances.

· Ensure seamless transfer of resources across environments with minimal downtime.

· Maintain auditability and traceability of all migration activities.

· Support environmental consistency and reduce manual errors.

\---

3\. Migration Workflow

The migration process in the Resource Migration Application (RMA) follows a structured, step-by-step workflow to ensure accuracy, control, and governance:

1\. Configuration Setup

· Before starting migration, the source and target environment details must be configured.

· Add the Source Data Source and the Target Data Source.



· Enter the environment URLs (Dev, UAT, Prod, etc.) in the Configuration Tab of the application.

· Validate the configuration. Once validation is successful, proceed to the migration page.

\---

2\. Request Creation

· Navigate to the Migration Page.

· Select the Source Environment (e.g., Dev / UAT) and the Target Environment (e.g., UAT / Prod).

· Provide client-specific details:

o Source Catalog → Select Enterprise Data Catalog.

· Click Next to continue.

\---

3\. Resource Selection

· On the resource selection page:

o Choose the Resource Type (ETL / Dashboard / LDM).

o Select the specific resource(s) from the dropdown list.

· After selection, proceed to the next step.

\---

4\. Resource Validation

· Provide a Name and Description for the migration.

· Run Validation to check resource integrity and dependencies.

· If validation passes:

o Admins → Can directly approve and proceed with migration.

o Data Engineers → Must raise a request to the Admin for approval.
