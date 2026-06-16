# Test Cases. Level 1 & 2: Customer Registration Form Validation (UI)

**Target System under Test (SUT):** Practice Software Testing

**Testing Scope:** Customer Registration Form Fields (`account/test-cases/`)

## Item 1.1: Successful preservation of form data upon validation error (Level 2)

**Pre-conditions:**

  * The user is on the "Customer registration" page.
  * The form is completely blank.

**Steps:**

  1. Fill in all personal data fields with valid inputs (First name: `Alex`, Last Name: `Ford`, Date of Birth).
  2. Input valid Country, Postal Code, and House Number to trigger address auto-completion.
  3. Enter a valid strong password matching all criteria (e.g., `Qwerty!987`).
  4. In the **Email Address** field, enter an invalid format string: `alex.ford_test.net` (missing `@` symbol).
  5. Click the registration/submit button at the bottom of the form.
  6. Observe the form state, inputs, and error messages.

**Expected Result (UI):**

  1. The form submission is blocked due to validation failure.
  2. The **Email Address** field is highlighted, and the exact error message `"email format is invalid"` appears directly below it.
  3. **Form State Persistence:** All other entered data (First name, Last name, phone, password, and auto-completed address details) remain intact inside their respective input fields. The form does NOT clear or reset.

---

## Item 1.2: Password Strength Indicator and Rules Verification (UI)

**Pre-conditions:**

  * The user is on the "Customer registration" page.
  * The password field is empty.

**Steps:**

  1. Locate the **"Your Password"** input field and the password rules list beneath it.
  2. Start typing a password that satisfies all conditions: at least 8 chars, uppercase, lowercase, number, and special symbol (e.g., `Qwerty!987`).
  3. Verify the behavior of the eye icon (Show/Hide password) by clicking it.
  4. Observe the dynamic **"Password strength"** indicator.

**Expected Result (UI):**
  
  1. The eye icon toggles the visibility of the password text between masked dots and plain text.
  2. As the password meets all criteria, the checklist indicators update accordingly.
  3. The **Password strength** indicator dynamically updates its state (e.g., switches to *Strong*, *Very Strong*, or *Excellent* based on entropy).
