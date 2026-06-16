# Comprehensive QA Testing Project: E-Commerce User Journey & Backend Integrity

This repository contains comprehensive QA engineering artifacts for testing the core user journey, state persistence, and backend data integrity on the e-commerce platform **Practice Software Testing**. 

The project demonstrates advanced manual testing techniques, meticulous test design (Levels 1–3), state/session management validation, database verification, and professional defect reporting aligned with modern QA industry standards.

---

## 🛠 Target System & Environment

*   **System under Test (SUT):** Practice Software Testing (E-commerce web application)
*   **Testing Scope:** End-to-End User Journey (Catalog, Filter & Search, Shopping Cart, User Registration, Authentication, Checkout, and Invoices Integration).
*   **Environment Used for Verification:** macOS / Google Chrome (Desktop)
*   **Key Tools:** Chrome DevTools (Network & Application Tabs), SQL Database Verifier, GitHub Markdown.

---

## 📋 Project Structure & Architecture

All QA deliverables are logically structured into specialized directories covering individual system components. Click the links below to view the detailed test cases and bug reports:

### 👤 1. User Authentication & Profile Management
*   **`registration-form/`** — Validation rules and edge cases for creating a new account.
    *   📄 [level_1_general_validation.md](registration-form/test-cases/level_1_general_validation.md) — Happy Path testing, mandatory field verification, and dropdown behavior.
    *   📄 [level_2_negative_ui_validation.md](registration-form/test-cases/level_2_negative_ui_validation.md) — Advanced front-end field masking, format violations, and 18+ business logic restriction.
    *   📄 [database_verification.md](registration-form/database_verification.md) — Database integration verification suite containing backend SQL integrity tests and SHA-256 password hashing checks.
    *   🐛 [BUG-001_dob_missing_highlight.md](registration-form/BUG-001_dob_missing_highlight.md) — *High-Severity Defect:* Missing field synchronization and visual indicator during Date of Birth validation failure.
*   **`login-form/`** — Authorization security and form validation.
    *   📄 [login_level_1_general.md](login-form/test-cases/login_level_1_general.md) — Happy Path login testing with valid credentials and core UI elements check.
    *   📄 [login_level_2_negative.md](login-form/test-cases/login_level_2_negative.md) — Invalid authentication inputs, error message rendering, and basic brute-force protection.
*   **`account/`** — Post-login customer experience, dashboard behavior, and E2E synchronization.
    *   📄 [account_registration_validation.md](account/test-cases/account_registration_validation.md) — Form state preservation upon validation errors and dynamic password strength indicator.
    *   📄 [account_invoices_integration.md](account/test-cases/account_invoices_integration.md) — Automatic invoice binding after order completion, Detailed Invoice View UI, and Session Timeout (401 Unauthorized) handling.

### 🛒 2. E-Commerce Core & Checkout Funnel
*   **`catalog/`** — Product discovery and filtering engines.
    *   📄 [catalog_level_1_filters.md](catalog/test-cases/catalog_level_1_filters.md) — Top-Down/Bottom-Up checkbox logic, real-time AJAX price range slider, and sort state persistence.
    *   📄 [catalog_level_1_search.md](catalog/test-cases/catalog_level_1_search.md) — Text search query functionality and active filter resetting via the "X" control.
*   **`shopping-cart/`** — Cart state, boundary limitations, and memory lifecycle.
    *   📄 [cart_level_1_general.md](shopping-cart/test-cases/cart_level_1_general.md) — Adding items to the cart, dynamic header badge counter, and toast notifications.
    *   📄 [cart_level_2_negative.md](shopping-cart/test-cases/cart_level_2_negative.md) — Boundary Value Analysis for item quantities (handling 0 and the 99-unit limit).
    *   📄 [cart_level_3_session.md](shopping-cart/test-cases/cart_level_3_session.md) — Data persistence across browser states (F5 reload behavior vs. Session Storage reset upon tab closure).
*   **`checkout/`** — Payment forms and checkout flow processing.
    *   📄 [checkout_level_1_general.md](checkout/test-cases/checkout_level_1_general.md) — Multi-step checkout execution for Guest Users (Credit Card and Cash on Delivery methods).
    *   🐛 [BUG_003_checkout_credit_card_missing_fields.md](checkout/test-cases/bug-reports/BUG_003_checkout_credit_card_missing_fields.md) — *High-Severity Defect:* Missing mandatory field validation leading to submission of empty inputs and server-side "Unknown Error".

---

## 🧠 Key QA Practices & Methodologies Covered

*   **Multi-Level Test Design:** Test cases are strictly categorized from **Level 1** (Happy Path / Basic Functional) to **Level 2** (Negative / Boundary Conditions) and **Level 3** (State, Session & Edge Cases).
*   **Equivalence Partitioning & BVA:** Systematically applied to input field constraints, item quantity caps (0 and 99 units), and age business rules.
*   **State & Session Testing:** Verifying how the application handles data in `SessionStorage` vs. `LocalStorage` during browser reloads, tab closures, and idle time-outs (`401 Unauthorized`).
*   **Backend & DB Integrity:** Documented validation of database states, ensuring user records are correctly inserted into relational tables with appropriately masked/hashed credentials.
*   **UI/UX Defect Synchronicity:** Special focus on capturing mismatch bugs where the system correctly rejects invalid data but fails to provide appropriate visual cues (e.g., missing input field highlighting or generic server errors).
