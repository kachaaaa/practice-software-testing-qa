
# Test Cases. Level 3: State & Session Persistence (UI)

**Target System under Test (SUT):** Practice Software Testing
**Testing Scope:** Shopping Cart — Data persistence across browser states (Guest Mode)

## Item 3.1: Page refresh behavior (F5 / Cmd+R)

**Pre-conditions:** User is a Guest (not logged in). The shopping cart contains 2 items. User is on the Cart page.

**Steps:**

  1. Refresh the browser page (press F5 or click the Refresh button).
  2. Observe the cart badge counter and the product list on the Cart page.

**Expected Result (UI):**

  1. The page reloads successfully.
  2. All items remain in the shopping cart with their respective quantities and correctly calculated totals. Data is preserved.

---


## Item 3.2: Browser tab closure behavior (Session Storage Reset & Dynamic UI)

**Pre-conditions:** User is a Guest (not logged in). The shopping cart contains items, and the "Cart" tab is visible in the main navigation bar.

**Steps:**
  
  1. Copy the website base URL.
  2. Close the current browser tab where the session was active.
  3. Open a completely new, clean browser tab.
  4. Paste the URL and navigate to the website.
  5. Check the main navigation bar (header menu) next to "Home", "Categories", "Contact", "Sign in".

**Expected Result (UI):**
  
  1. The guest session data is completely wiped from Session Storage upon tab closure.
  2. The **"Cart" link/tab completely disappears** from the main navigation bar. 
  3. The navigation bar displays only default links: "Home", "Categories", "Contact", "Sign in". The user cannot access the Cart page until a product is added again.
