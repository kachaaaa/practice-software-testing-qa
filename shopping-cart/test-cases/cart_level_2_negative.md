# Test Cases. Level 2: Negative & Boundary Validation (UI)

**Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
**Testing Scope:** Shopping Cart — Quantity fields and boundary values

## Item 2.1: Decrease item quantity to zero or enter "0" manually

**Pre-conditions:** The shopping cart contains 1 item ("Combination Pliers") with Quantity: 1. User is on the Cart page.

**Steps:**

 1. Locate the quantity input field for "Combination Pliers".
 2. Click the minus (**"-"**) button to decrease the quantity from 1 to 0 (or manually type `0` into the field and press Enter/click outside).

* **Expected Result (UI):**
  
 1. The system displays a toast notification in the top-right corner: **"Product quantity updated."**
 2. The system automatically overrides the invalid value `0` and resets the Quantity field back to **1**.
 3. The Total price remains calculated for 1 item ($14.15), and the product is NOT removed from the cart.
