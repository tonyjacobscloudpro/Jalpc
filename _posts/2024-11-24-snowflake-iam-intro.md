---
layout: post
title: "Introduction to Snowflake IAM"
date: 2020-11-24
desc: "Introduction to Snowflake IAM"
keywords: "Snowflake, IAM"
categories: [Snowflake]
tags: [Snowflake, IAM]
icon: icon-html
---

## Introduction to Snowflake Identity and Access Management (IAM)

Snowflake provides robust **Identity and Access Management (IAM)** capabilities to ensure secure and efficient user and resource management. Its IAM system is built to handle authentication, authorization, and auditing with fine-grained control over data and operations.

Here’s an overview:

---

### Key Components of Snowflake IAM

#### 1. **Authentication**
Authentication verifies the identity of users or services accessing Snowflake.

- **Supported Authentication Methods**:
  - **Username and Password**: Default method for user login.
  - **Multi-Factor Authentication (MFA)**: Adds an extra security layer using apps like Google Authenticator.
  - **OAuth**: Supports third-party providers like Google and Okta.
  - **Key Pair Authentication**: Secures programmatic access (e.g., SnowSQL, Python).
  - **Federated Authentication**: Enables SSO integration using SAML 2.0 with providers like Azure AD.
  - **External Functions Authentication**: Secures interactions with external services.

---

#### 2. **Authorization**
Authorization determines what actions authenticated users can perform.

- **Role-Based Access Control (RBAC)**:
  - Snowflake uses **roles** to manage permissions.
  - Each role is granted specific privileges on **objects** like databases, schemas, and warehouses.
  - Users are assigned one or more roles.

- **Hierarchy of Roles**:
  - **System-Defined Roles**:
    - `ACCOUNTADMIN`: Full administrative access.
    - `SYSADMIN`: Manages databases and objects.
    - `SECURITYADMIN`: Manages roles and access.
    - `PUBLIC`: Default role for all users.
  - **Custom Roles**:
    - Created to provide tailored access for teams or projects.

- **Granting Privileges**:
  - Common privileges include `SELECT`, `INSERT`, `USAGE`, and `OWNERSHIP`.

---

#### 3. **Object-Level Access Control**
Snowflake offers fine-grained access control for:
- **Databases and Schemas**: Controlled via `USAGE` privilege.
- **Tables and Views**: Controlled via `SELECT`, `INSERT`, etc.
- **Warehouses**: Controlled via `USAGE` privilege.

---

#### 4. **Data Access Governance**
- **Row-Level Security**:
  - Policies restrict access to specific rows in a table.
- **Dynamic Data Masking**:
  - Masks sensitive data dynamically for unauthorized users.
- **Time Travel and Data Retention**:
  - Enables historical data access, restricted to authorized roles.

---

#### 5. **Auditing and Monitoring**
- **Query History**: Tracks user queries.
- **Access History**: Records user logins and resource access.
- **Usage Views**: Provides insights into resource and role utilization.

---

### Best Practices for Snowflake IAM
1. Follow the **Principle of Least Privilege** to minimize unnecessary access.
2. Create **custom roles** for different teams or functions.
3. Enable **MFA** for all users to enhance security.
4. Regularly **audit and monitor** using `ACCESS_HISTORY`.
5. Integrate with **SSO** for simplified user management.

---

### Example Use Case: Managing Roles and Access

The following example demonstrates creating a custom role and assigning it to a user:

```sql
-- Create a role for data analysts
CREATE ROLE DATA_ANALYST;

-- Grant read-only access to a database and schema
GRANT USAGE ON DATABASE SALES_DB TO ROLE DATA_ANALYST;
GRANT USAGE ON SCHEMA SALES_DB.PUBLIC TO ROLE DATA_ANALYST;
GRANT SELECT ON ALL TABLES IN SCHEMA SALES_DB.PUBLIC TO ROLE DATA_ANALYST;

-- Assign the role to a user
GRANT ROLE DATA_ANALYST TO USER john_doe;

/* You can run the above SQL commands in:

1. Snowflake Web Interface: Navigate to the Worksheet tab and execute the SQL.


2. SnowSQL CLI: Connect and execute commands programmatically.


3. Third-party tools: Use tools like DBeaver or DataGrip for SQL execution.


4. Programmatic Access: Automate using the Snowflake Python connector or APIs.
*/

