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
