# Comprehensive QA Testing Project: User Registration Form

This repository contains comprehensive QA engineering artifacts for testing the **User Registration (Sign Up) Form** on the e-commerce platform **Practice Software Testing**.

The project demonstrates manual testing techniques, professional documentation version control, front-end validation logic analysis, and alignment with modern QA industry standards.

---

## 🛠 Target System & Environment
* **System under Test (SUT):** Practice Software Testing (E-commerce web application)
* **Testing Scope:** User Registration / Account Creation Workflow
* **Environment Used for Verification:** macOS / Google Chrome (Desktop)
* **Key Tools:** Chrome DevTools (Network Tab), GitHub Markdown

---

## 📋 Project Structure & Artifacts

All QA deliverables are logically structured into specialized directories. Click the links below to view the detailed documentation:

* 📂 **[registration-form/test-cases/](./registration-form/test-cases/)**
  * 📄 [level_1_general_validation.md](./registration-form/test-cases/level_1_general_validation.md) — Happy Path testing, mandatory field verification, and basic UI element behavior.
  * 📄 [level_2_negative_ui_validation.md](./registration-form/test-cases/level_2_negative_ui_validation.md) — Advanced front-end field masking, boundary value analysis, and password complexity criteria.
* 📂 **[registration-form/](./registration-form/)**
  * 📄 [BUG-001_dob_missing_highlight.md](./registration-form/BUG-001_dob_missing_highlight.md) — Defect report detailing missing field synchronization during age validation errors.
  * 📄 [database_verification.md](./registration-form/database_verification.md) — Database integration verification suite containing backend SQL integrity tests and password hashing checks based on Item 1.1.

---

## 🧠 Key QA Practices Covered
* **Equivalence Partitioning & BVA:** Systematically applied to field lengths and age/date inputs to optimize test coverage.
* **UI/UX Error Synchronization:** Tracking cases where backend/business rules block submissions but the client interface fails to render field highlights correctly.
