# Test Cases. Level 2: Negative & Boundary Validation (UI)

**Target System under Test (SUT):** Practice Software Testing (e-commerce platform)

**Testing Scope:** Shopping Cart — Quantity fields and boundary values

## Item 2.1: Decrease item quantity to zero or enter "0" manually

**Pre-conditions:** The shopping cart contains 1 item ("Combination Pliers") with Quantity: 1. User is on the Cart page.

**Steps:**

 1. Locate the quantity input field for "Combination Pliers".
 2. Click the minus (**"-"**) button to decrease the quantity from 1 to 0 (or manually type `0` into the field and press Enter/click outside).

 **Expected Result (UI):**
  
 1. The system displays a toast notification in the top-right corner: **"Product quantity updated."**
 2. The system automatically overrides the invalid value `0` and resets the Quantity field back to **1**.
 3. The Total price remains calculated for 1 item ($14.15), and the product is NOT removed from the cart.


---

## Item 2.2: Complete removal of an item from the cart using the Delete button

**Pre-conditions:** The shopping cart contains 1 item ("Combination Pliers"). User is on the Cart page.

 **Steps:**
  
 1. Locate the Delete button (trash bin icon / "X") at the end of the "Combination Pliers" product row.
 2. Click the Delete button.

 **Expected Result (UI):**
 
 1. The product row "Combination Pliers" completely disappears from the Cart page.
 2. The system displays a confirmation message (e.g., "Product removed from shopping cart").
 3. The cart badge counter in the header drops back to 0 (or disappears).
 4. The page displays an empty state message: **"Your cart is empty"** (or similar).

## Item 2.3: Enter an excessively large value exceeding the maximum limit

**Pre-conditions:** The shopping cart contains 1 item with Quantity. User is on the Cart page.

**Steps:**
 
 1. Locate the quantity input field.
 2. Manually type an extreme value exceeding the allowed limit (e.g., `999`) and press Enter or click outside.

**Expected Result (UI):**

 1. The system displays a specific warning toast notification in the top-right corner: **"You can order at most 99 of this product."**
 2. The system automatically caps the input and sets the Quantity field to the maximum allowed limit: **99**.
 3. The Total price is dynamically and mathematically correctly recalculated for 99 items.

---

## Item 2.4: Complete removal of an item from the cart using the Delete button

 **Pre-conditions:** The shopping cart contains 1 item ("Combination Pliers"). User is on the Cart page.

 **Steps:**
  
 1. Locate the Delete button (trash bin icon / "X") at the end of the "Combination Pliers" product row.
 2. Click the Delete button.

**Expected Result (UI):**

 1. The product row "Combination Pliers" completely disappears from the Cart page.
 2. The system displays a confirmation message (e.g., "Product removed from shopping cart").
 3. The cart badge counter in the header drops back to 0 (or disappears).
 4. The page displays an empty state message: **"Your cart is empty"**.

