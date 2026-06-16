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

---

## Item 1.2: Verification of Invoice Detailed View UI and Metadata (Level 2)

**Pre-conditions:**

  * The user has at least one generated invoice in their account history.
  * The user is on the "My Invoices" page.

**Steps:**
  
  1. Click the **"Details"** button on a specific invoice row (e.g., `INV-2026000008`).
  2. Verify the layout and matching data within three sections: **General Information**, **Payment Information**, and **Billing Address**.
  3. Verify the **Products** table layout (Quantity, Product name, Unit Price, Total).
  4. Ensure all total calculations match the main invoice table.

**Expected Result (UI):**
  
  1. **General Info** correctly displays: Invoice Number, Invoice date, and Total.
  2. **Payment Info** states the exact method used (e.g., `Cash on Delivery Method`).
  3. **Billing Address** displays complete fields: Street, Postal Code, City, State, and Country.
  4. **Products Table** explicitly lists the correct item details (`Combination Pliers`), correct quantity (`1`), and the final price summation matches perfectly.
