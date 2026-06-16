# Test Cases. Level 1: Product Catalog — Text Search Functionality (UI)

**Target System under Test (SUT):** Practice Software Testing

**Testing Scope:** Search Field and Controls (`Search` and `X` buttons)

## Item 1.1: Clear active search query using the "X" button

**Pre-conditions:**

  * The user is on the main Product Catalog page.
  * The product grid is in its default state.

**Steps:**

  1. Click inside the **Search** input field in the left sidebar.
  2. Type a valid search term (e.g., `"Hammer"`) and click the **"Search"** button directly beneath the input field.
  3. Verify that the grid filters and displays only items matching the query.
  4. Click the **"X"** button located next to the Search button.
  5. Observe the text input field and the product grid.

**Expected Result (UI):**

  1. Clicking the **"X"** button completely clears the text from the search input field.
  2. The active search filter is removed, and the product grid dynamically updates to restore the full list of products.
