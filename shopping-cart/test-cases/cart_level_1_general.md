# Test Cases. Level 1: General Functional & Happy Path (UI)

* **Target System under Test (SUT):** Practice Software Testing (e-commerce platform)
* **Testing Scope:** Shopping Cart — Adding items and core total calculations

## Item 1.1: Add a single item to an empty shopping cart

* **Pre-conditions:** The shopping cart is completely empty (badge icon shows no number).
* **Steps:**
  
 1. Go to the Home page of the website.
 2. Click on the product card **"Combination Pliers"** (or any available tool).
 3. On the product details page, click the **"Add to cart"** button.
 4. Look at the shopping cart icon in the top right header and the pop-up notification.
 5. Click on the shopping cart icon to navigate to the Cart page.

* **Expected Result (UI):**

 1. In Step 3, a toast notification appears in the top-right corner with the text: **"Product added to shopping cart."**
 2. In Step 4, the cart badge counter dynamically changes to **1**.
 3. On the Cart page, the selected item is displayed with the correct Name ("Combination Pliers"), Price, Quantity (1), and the Total price perfectly matches the product price.
