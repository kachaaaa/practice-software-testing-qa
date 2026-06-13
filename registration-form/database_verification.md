# Database Integration Verification (Backend Testing)

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Testing Scope:** User Registration Form Data Flow & Database Integrity
* **Database Type:** Relational (SQL-based structure, e.g., PostgreSQL / MySQL)

## Overview
This artifact describes the end-to-end database integration verification for the User Registration process. Testing at the database layer ensures that data captured by the frontend form is accurately processed by the backend and safely stored in the system's relational tables.

---

## DB-001: Verification of successful user creation and data integrity (Happy Path Data)

* **Objective:** Ensure that a newly registered user profile is successfully inserted into the database with exact matching data attributes from the Level 1 Happy Path test case (Item 1.1).
* **Pre-conditions:** A user has just successfully completed the registration form with the data from **Item 1.1** (Email: `john.doe.test@gmail.com`).

### Test SQL Query:
```sql
SELECT id, first_name, last_name, email, phone, city, password 
FROM users 
WHERE email = 'john.doe.test@gmail.com';

Expected Result (Data Integrity Checklist):
1.Row Count: The query returns exactly 1 row.
2.Field Correspondence:
 - first_name matches exactly with Item 1.1 input (John).
 - last_name matches exactly with Item 1.1 input (Doe).
 - email matches exactly with Item 1.1 input (john.doe.test@gmail.com).
 - phone matches exactly with Item 1.1 input (+12125550199).
3.Primary Key Generation: The id field is automatically generated, unique, and serves as the internal identifier.
