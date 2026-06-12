# BUG-001: No red highlighting in the "Date of Birth" field due to an age validation error

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Priority:** Medium (as this directly impacts the UX of the registration form)
* **Severity:** Minor 
* **Environment:** macOS, Google Chrome (Desktop), Practice Software Testing (Web)

---

## Summary
When the business age validation is triggered, the error text `"Customer must be 18 years old"` is displayed on the screen, but the `Date of Birth` input field itself is not visually highlighted in red (there is no UI indication of the error on a specific field).

## Steps to Reproduce 
1. Open the registration page on the test bench.
2. Fill in all required fields with valid data.
3. In the **Date of Birth** field, enter an invalid date (under 18 or a future date).
   * *Test Data:* `2027-01-01`
4. Click the **"Register"** button.

## Actual Result 
Registration is blocked. The error text appears below the form, but the `Date of Birth` field border remains a neutral gray (there is no visual focus or red highlight on the erroneous field).

## Expected Result 
The form is blocked, the error text is displayed on the screen, and the `Date of Birth` field frame **must be visually highlighted in red** (similar to the system's behavior when submitting an empty form), indicating to the user in which field the error was made.
