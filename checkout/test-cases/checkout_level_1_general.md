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
  4. Verify that the system displays the text: `"continuing as guests: [First name] [Last name] ([Email])"`.
  5. Click the **"proceed to checkout"** button.
  6. On the Billing Address step, select the country and enter a valid **Postal code** (e.g., `10001`) and **House number** (e.g., `123`).
  7. Wait for the Address Autocomplete feature to fill in *street, city, and state*.
  8. Click the green **"proceed to checkout"** button.
  9. On the Payment step, select the **"Cash on Delivery"** payment method.
  10. Verify that the notification `"payment was successful"` appears and the **"confirm"** button becomes active.
  11. Click the **"confirm"** button to finalize the order.

**Expected Result (UI):**

  1. The system successfully processes the order.
  2. The page displays the success message: **"Thanks for your order!"**
  3. The system generates and displays a unique invoice number in the format: **"Your invoice number is INV-2026XXXXXX."**
  4. The shopping cart data is completely cleared, and the "Cart" tab disappears from the main navigation bar.
