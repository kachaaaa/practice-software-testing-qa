# Test Case. Level 2: Negative UI and Field Validation (Front-end)

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Testing Scope:** User Registration (Sign Up) Form - Negative Scenarios & Validation

---

## Item 2.1: Attempt to submit an empty registration form
* **Steps:** Go to the registration page, leave all fields blank and click the "Register" button. 
* **Expected Result (UI):** 1. The form is not submitted (the page does not reload, there is no redirect).
  2. All required fields are highlighted in red.
  3. Clear error text appears under each required field or at the top of the form (e.g., "First name is required" or "Email is required").

---

## Section 2.2: Validate the Email field for the correct format
* **Test Data:** Email: `test.com`
* **Steps:** 1. In the Email field, enter `test.com`.
  2. Fill in the remaining fields with valid data from Item 1.1.
  3. Click "Register."
* **Expected Result:** 1. The form is blocked from submission.
  2. The Email field is highlighted as invalid.
  3. An "Email format is invalid" message appears.

---

## Item 2.3: Positive test: Checking registration with a password that fully complies with all security requirements
* **Input Data:** `P@ssword1`
* **Compliance Check:** * Length: 9 characters (condition >= 8 met)
  * Case: Includes uppercase P and lowercase ssword (condition met)
  * Numbers: Includes "1" (condition met)
  * Special characters: Includes @ (condition met)
* **Steps:** 1. Fill in all other required fields (Email, Name, etc.) with valid data.
  2. In the Password field, enter the value: `P@ssword1`
  3. Click the Register button.
* **Expected Result:** The system successfully accepts the password. The form is submitted without validation errors, and the user is successfully registered.

---

## Item 2.4: Negative Test: Checking password validation without using special characters
* **Input Data (Test Value):** `Password123`
* **Requirements Coverage Analysis:** * Length: 11 characters (condition >= 8 met)
  * Case: Uppercase P and lowercase assword (condition met)
  * Numbers: 123 (condition met)
  * Special characters: None (requirement violated)
* **Steps:** 1. Fill in all other required fields with valid data.
  2. In the Password field, enter the value: `Password123`.
  3. Click the registration button.
* **Expected Result:** The system blocks the form submission. A clear warning appears under the Password field: "Your password must have at least one special character (e.g., @, #, $, etc.)." The field is highlighted in red.

---

## Item 2.5: Negative tests: Validation of password composition (no numbers/no case)
* **Test Scenarios:** 1. **No number:** Enter `P@ssword` $\rightarrow$ A corresponding password violation message is displayed.
  2. **No capital letters:** Enter `p@ssword1` $\rightarrow$ A corresponding password violation message is displayed.
  3. **Too short:** Enter `P@ss1` (7 characters) $\rightarrow$ A corresponding password violation message is displayed.

---

## Item 2.6: Positive Test: Enter a valid date of birth in the required format
* **Input Data (Test Value):** `1995-10-25`
* **Conformance Check:** YYYY-MM-DD format is respected, the date is valid.
* **Steps:** 1. Fill in all fields with valid data.
  2. In the Date of Birth field, enter `1995-10-25`.
  3. Click Register.
* **Expected Result:** The red highlight and error disappear. The system successfully accepts the date, and the form is ready to be submitted.

---

## Item 2.7: Negative tests: Validation of incorrect format and unrealistic dates
* **Test Scenarios:** 1. **Format error (dots instead of hyphens):** Enter `10.25.1995` or `1995.10.25`
  2. **Format error (insufficient digits):** Enter `10-25-95` (two-digit year)
  3. **Non-existent date (calendar logical error):** Enter `02-31-1995` (February 31) or `10-13-1995` (13th month)
* **Expected Result:** In all scenarios, the system locks the form, the field is highlighted in red, and the request is displayed: "Please enter a valid date in YYYY-MM-DD format."

---

## Item 2.8: Negative Test: Age Business Logic Check (Restriction 18+)
* **Test Scenarios:** 1. Entering a date from the future: Enter `2027-01-01`
  2. Entering a date when the user is under 18 years old (for example, the current year minus 5 years)
* **Steps:** 1. Fill in all other fields with valid data.
  2. In the Date of Birth field, enter a future date (e.g., `2027-01-01`).
  3. Click the "Register" button.
* **Expected Result:** The system is blocking registration. An error message appears below the form: "Customer must be 18 years old."
