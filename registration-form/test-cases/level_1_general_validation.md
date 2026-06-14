# Test Cases. Level 1: General Form Validation and Filling in Required Fields

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Testing Scope:** User Registration (Sign Up) Form

---

## Item 1.1 Successful registration when all fields are filled with valid data
* **Test Data:**
  1. First Name : John
  2. Last Name : Doe 
  3. DoB : 1990-05-15
  4. Address : 123 Main Street 
  5. Postcode : 10001
  6. City/State : New York 
  7. Country : United States
  8. Phone: 12125550199
  9. Email : `john.doe.test@gmail.com`
  10. Password : `Qwerty12345!`

**Expected Result (UI)**: The fields accept values ​​without validation errors **(no red highlights or error text)**. After clicking the **"Register"** button, a successful redirect to the profile page occurs.

**Item 1.2**: Negative test: Form validation when submitted with empty required fields 

**Steps**: 

1. Fill in the First Name, Last Name, Email, and Password fields with valid information.
2. Leave the Date of Birth and Address fields completely blank.
3. Click the **"Register"** button.

**Expected Result (UI)**: The form is blocked from submission ,and registration fails.Empty fields are highlighted in red, and error message appear underneath them (e.g., "Please enter a valid date in YYYY-MM-DD format.Date of Birth is required').

**Item 1.3**: Interaction with special interface elements (Drop-down list) 

**Steps:** 

1. Click on the Country field.
2. Select the country from the drop-down list.

**Expected Result:** A drop-down list of countries opens, containing available options (including United States); the selected country is fixed in the field.

