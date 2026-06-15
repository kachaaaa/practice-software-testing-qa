# Test Cases. Level 1: General Functional & Happy Path (UI)

**Target System under Test (SUT):** Practice Software Testing

**Testing Scope:** Checkout Process — Guest Mode Purchase with Cash on Delivery

## Item 1.1: Complete a successful purchase as a Guest via Cash on Delivery

**Pre-conditions:** * The shopping cart contains at least 1 item.
  * The "Cart" tab is visible in the navigation bar.
  * The user is on the Cart page and is NOT logged in (Guest Mode).

**Steps:**

  1. On the Cart page, click the **"Proceed to checkout"** button.
  2. On the authentication step, select the **"Continue as guests"** tab.
  3. Fill in the required fields with valid data: *Email address, First name, Last name* and click the button.
  4. Verify that the system displays the text: `"continuing as guests: [First name] [Last name] [Email]"`.
  5. Click the **"proceed to checkout"** button.
  6. On the Billing Address step, select the country and enter a valid **Postal code** (e.g., `10001`) and **House number** (e.g., `123`).
  7. Wait for the Address Autocomplete feature to fill in *street, city, and state*.
  8. Click the green **"proceed to checkout"** button.
  9. On the Payment step, select the **"Cash on Delivery"** payment method.
  10. Verify that the notification `"payment was successful"` appears and the **"confirm"** button becomes active.
  11. Click the **"confirm"** button to finalize the order.

---

## Item 1.2: Manually edit automatically filled address fields
**Pre-conditions:** User is in Guest Mode and has proceeded to the "Billing Address" step.
**Steps:**
  
  1. Select a country, enter a valid **Postal code** (e.g., `10001`) and **House number** (e.g., `123`) to trigger the Address Autocomplete.
  2. Wait for the system to fill in the *street, city, and state* fields.
  3. Click inside the **street** or **city** field, clear a part of the text, and manually type custom characters (e.g., change the street name).
  4. Check the availability of the "proceed to checkout" button.

**Expected Result (UI):**

  1. The automatically filled fields (*street, city, state*) are fully editable and not restricted to Read-only mode.
  2. The user can successfully modify the text inside these fields.
  3. The **"proceed to checkout"** button remains active (green) and clickable, allowing the user to advance with the manually adjusted address.

 ---
 
## Item 1.3: Complete a successful purchase as a Guest via Credit Card

**Pre-conditions:** * The shopping cart contains at least 1 item.
  * The user is on the Cart page in Guest Mode.

**Steps:**

  1. Advance through the checkout steps to the Payment stage using Guest Mode.
  2. Select the **"Credit Card"** payment method.
  3. Fill in all credit card fields with validly formatted dummy data:

     *Credit Card:* `1111-2222-3333-4444` (including hyphens)
     *Expiration Date:* Any future date
     *CVV:* `123`
     *Card Holder Name:* `IVAN IVANOV`
     
  5. Verify that the notification `"payment was successful"` appears and the **"Confirm"** button becomes active.
  6. Click the **"Confirm"** button.

**Expected Result (UI):**

  1. The system processes the credit card payment successfully.
  2. The page displays the success message: **"Thanks for your order!"**
  3. A unique invoice number is generated (e.g., `INV-2026XXXXXX`).

**Expected Result (UI):**

  1. The system successfully processes the order.
  2. The page displays the success message: **"Thanks for your order!"**
  3. The system generates and displays a unique invoice number in the format: **"Your invoice number is INV-2026XXXXXX."**
  4. The shopping cart data is completely cleared, and the "Cart" tab disappears from the main navigation bar.

---

# Test Cases. Level 2: Negative & Boundary Validation (UI)

## Item 2.1: Enter invalid data (letters) into the Postal Code field

**Pre-conditions:** User is in Guest Mode, has items in the cart, and has proceeded to the "Billing Address" step.

**Steps:**

  1. Select any country.
  2. In the **Postal code** field, manually enter an invalid string containing only letters (e.g., `sgsdgs`).
  3. In the **House number** field, enter a valid number (e.g., `213`).
  4. Observe the remaining address fields (*street, city, state*) and the status of the "proceed to checkout" button.

**Expected Result (UI):**

  1. The Address Autocomplete feature is NOT triggered (no automatic data is filled into street, city, or state).
  2. The fields *street, city, and state* remain blank.
  3. The **"proceed to checkout"** button remains disabled (greyed out) and unclickable, preventing the user from advancing with an invalid address.

---

## Item 2.2: Leave required address fields empty (Boundary Test)

**Pre-conditions:** User is in Guest Mode on the "Billing Address" step.
**Steps:**

  1. Leave the **Postal code** and **House number** fields completely blank.
  2. Attempt to click the **"proceed to checkout"** button.

**Expected Result (UI):**

  1. The **"proceed to checkout"** button is strictly disabled.
  2. The system blocks the transition to the Payment step, requiring all mandatory location data to be present.

---

## Item 1.2: Manually edit automatically filled address fields

**Pre-conditions:** User is in Guest Mode and has proceeded to the "Billing Address" step.

**Steps:**

  1. Select a country, enter a valid **Postal code** (e.g., `10001`) and **House number** (e.g., `123`) to trigger the Address Autocomplete.
  2. Wait for the system to fill in the *street, city, and state* fields.
  3. Click inside the **street** or **city** field, clear a part of the text, and manually type custom characters (e.g., change the street name).
  4. Check the availability of the "proceed to checkout" button.

**Expected Result (UI):**

  1. The automatically filled fields (*street, city, state*) are fully editable and not restricted to Read-only mode.
  2. The user can successfully modify the text inside these fields.
  3. The **"proceed to checkout"** button remains active (green) and clickable, allowing the user to advance with the manually adjusted address.
