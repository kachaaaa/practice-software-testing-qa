# Test Cases. Level 1: Product Catalog & Category Filtering (UI)

**Target System under Test (SUT):** Practice Software Testing

**Testing Scope:** Side Navigation Filter Panel — Category Checkboxes

## Item 1.1: Bulk selection via Parent Category checkbox (Top-Down Logic)

**Pre-conditions:** 
  
  * The user is on the main Product Catalog page.
  * All filters are cleared, and the sidebar filter panel is visible.

**Steps:**
  
  1. Locate the **"By category"** section in the left sidebar.
  2. Click on the parent checkbox **"Hand Tools"**.
  3. Observe the state of the nested subcategories (*Hammer, Hand Saw, Wrench, Screwdriver, Pliers, Chisels, Measures*).

**Expected Result (UI):**
  
  1. The parent checkbox **"Hand Tools"** becomes checked.
  2. All 7 nested subcategory checkboxes automatically switch to the checked state simultaneously.
  3. The product grid updates to display items belonging to all subcategories under Hand Tools.

---

## Item 1.2: Individual selection of a Subcategory checkbox (Bottom-Up Logic)

**Pre-conditions:**
  
  * The user is on the main Product Catalog page.
  * All filters are cleared.

**Steps:**
  
  1. Locate the **"Hand Tools"** subcategory list.
  2. Click on a single subcategory checkbox, for example, **"Hammer"**.
  3. Observe the state of the parent checkbox **"Hand Tools"**.

**Expected Result (UI):**
  
  1. The selected subcategory checkbox (**"Hammer"**) becomes checked.
  2. The parent checkbox **"Hand Tools"** remains unchanged (unchecked).
  3. The product grid updates dynamically to display *only* products categorized as Hammers.

---

## Item 1.3: Dynamic product filtering via Price Range slider (AJAX)

**Pre-conditions:**
  
  * The user is on the main Product Catalog page.
  * The default price range slider is set to its maximum bounds (e.g., `1 - 200`).
  * Multiple product cards with images and prices are displayed in the grid.

**Steps:**
  
  1. Locate the **"Price Range"** slider in the left sidebar.
  2. Drag the slider handles to narrow down the price interval (e.g., set it to `50 - 150`).
  3. Observe the behavior of the product grid and check if any page reload occurs.

**Expected Result (UI):**
  
  1. The product grid updates dynamically on the fly (real-time AJAX filtering) as the slider moves.
  2. No page reload or submission via an extra "Apply" button is required.
  3. Only products with prices strictly within the newly selected range remain visible in the grid.

---

# Test Cases. Level 2: Combined Filter Logic & Conflict Validation (UI)

## Item 2.1: Combine Text Search with Conflicting Category Filter

**Pre-conditions:**
  
  * The user is on the main Product Catalog page.
  * All filters are initially cleared.

**Steps:**
  
  1. In the search field, type **"Hammer"** and execute the search.
  2. Verify that the product grid updates to show relevant items (Hand Tools).
  3. In the left sidebar under "Power Tools", check the parent checkbox **"Power Tools"** (or any specific subcategory like "Drill").
  4. Observe the product grid and the resulting system message.

**Expected Result (UI):**
  
  1. The system combines the text search and category filter using "AND" logic.
  2. Because no "Hammer" exists inside the "Power Tools" category, the product grid becomes empty.
  3. The system must display the exact alert messages: 
     * `"0 products found for 'Hammer'"`
     * `"There are no products found."`
