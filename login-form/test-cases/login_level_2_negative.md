**Item 2.1**: Attempt to submit an empty login form

**Steps** : 

1. Go to the Sign In page.
2. Leave both the **Email** and **Password** fields completely blank.
3. Click the **"Login"** button.


**Expected Result (UI):**

1. The form blocks submission (the page does not reload, there is no redirect).
2. Individual fields are NOT highlighted in red.
3. A single, unified error message appears on the screen : **"Invalid email or password"**.


**Item 2.2**: Attempt to login with valid Email and empty Password

**Test Data:**

1. Email: `john.doe.test@gmail.com`
2. Password: **(leave completely blank)**

**Steps:**

1. Go to the Sign In page.
2. Enter the valid email `john.doe.test@gmail.com` into the Email field.
3. Leave the Password field completely blank.
4. Click the **"Login"** button.

**Expected Result (UI):**

1. The form blocks submission.
2. The system displays a specific validation error message: **"Password is required"**.


**Item 2.3**: Attempt to login with empty Email and valid Password

**Test Data**: 
1. Email: **(leave completely blank)**
2. Password : `J0hnDoe_Test2026!`

**Steps**: 

1. Go to the Sign In page.
2. Leave the Email field completely blank.
3. Enter the valid password `Qwerty12345!` into the Password field.
4. Click the **"Login"** button.

**Expected Result (UI):**

1. The form blocks sybmission.
2. The system displays a specific validation error message: **"Email is required"**.


**Item 2.4**: Attempt to login with invalid Email format (Field Mask Validation) 

**Test Scenarios:** 

1. **Missing "@" symbol:** `john.doe.testgmail.com`
2. **Missing domain extension:** `john.doe.test@`

 **Steps**:

 1. Go to the Sign In page.
 2. Enter an invalid email format into the Email field according to the scenarios above.
 3. Enter the valid password `J0hnDoe_Test2026!`.
 4. Click the **Login** button.

**Expected Result (UI):**

1. The form blocks submission.
2. The system displays the specific validation error message: **"Email format is invalid"**.


**Item 2.5**: Attempt to login with incorrect credentials (Non-existing user / Wrong password)

**Test Scenarios:**

1. **Wrong Password:** Enter registered email `john.doe.test@gmail.com` and an incorrect password `WrongPassword123!`.
2. **Non-existing User:** Enter an unregistered email `not.exist.qa@gmail.com` and any password.

**Steps:**

1. Go to the Sign In page.
2. Enter the data according to the scenarios above.
3. Click the **"Login"** button.

**Expected Result:**

1. The form blocks submission.
2. The system displays a generic error message: **"Invalid email or password"** (protecting the system from user enumeration attacs).
