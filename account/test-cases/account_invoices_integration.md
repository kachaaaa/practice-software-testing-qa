# Test Cases. Level 1 & 2: My Account — Invoices and Checkout Integration (E2E)

**Target System under Test (SUT):** Practice Software Testing

**Testing Scope:** My Invoices Dashboard and Session Integration 

## Item 1.1: Automatic invoice binding to registered customer profile after Checkout

**Pre-conditions:**

  * The user is logged in as a registered customer (e.g., `Alex Ford`).
  * The "My Invoices" section is initially empty (for a brand-new account).

**Steps:**

  1. Navigate to the Product Catalog, add any item to the cart, and click on the dynamic Cart icon to proceed to Checkout.
  2. Verify that the system displays the session message: `"Hello Alex Ford, you are already logged in. You can proceed to checkout."`
  3. Complete the billing details (manually entering the House Number if it is missing from the profile pre-fill).
  4. Advance through all Checkout steps, choose a payment method, and confirm the order.
  5. Note the generated invoice number on the success screen (e.g., `INV-2026000008`).
  6. Return to the main **"My Account"** dashboard and click on the **"Invoices"** (or **"My Invoices"**) section.
  7. Verify the presence and columns of the updated invoice table.

**Expected Result (UI & Data):**

  1. The system correctly pulls the active user session into the Checkout module.
  2. After a successful purchase, a unique invoice ID is generated (e.g., `INV-2026000008`).
  3. **Data Integration:** The newly created invoice instantly populates the table in the user's personal account.
  4. The invoice row displays accurate metadata: **Invoice Number**, **Billing Address**, **Invoice Date**, and **Total** price (e.g., `$14.15`).
  5. A functional **"Details"** button is present for each row to allow deep-diving into individual order items.
