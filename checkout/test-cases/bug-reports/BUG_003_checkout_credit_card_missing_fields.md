# Bug Report: Missing Validation for Credit Card Fields Leads to "Unknown Error"

**Bug ID:** BUG-003

**Severity:** High

**Priority:** High

**Component:** Checkout / Payment Form

## Summary
The **"Confirm"** button becomes active when only the Credit Card number is filled, allowing the user to submit the form with empty Expiration Date, CVV, and Card Holder Name fields, which results in an **"Unknown Error"** from the server.

## Pre-conditions
1. User is on the Payment step of the checkout process.
2. The "Credit Card" payment method is selected.

## Steps to Reproduce
1. Enter a valid 16-digit card number with hyphens into the **Credit Card** field (e.g., `1111-2222-3333-4444`).
2. Leave the **Expiration Date**, **CVV**, and **Card Holder Name** fields completely blank.
3. Observe the state of the **Confirm** button.
4. Click the active **Confirm** button.

## Actual Result (UI)
* In Step 3: The **Confirm** button dynamically unlocks and turns active despite mandatory fields being empty.
* In Step 4: After clicking, the system fails to complete the order and displays a generic red error message at the bottom: `"Unknown Error"`.

## Expected Result (UI)
1. The **Confirm** button must remain disabled (greyed out) until *all* mandatory credit card fields (Card Number, Expiration Date, CVV, Card Holder Name) are filled and validated.
2. Inline validation errors (e.g., *"CVV is required"*) should appear under the empty mandatory fields.
