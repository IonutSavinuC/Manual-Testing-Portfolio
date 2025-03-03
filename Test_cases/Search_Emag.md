# Test Cases for Search Functionality

## Test Case: Search Displays Relevant Products
**Description:** This test case verifies that when a user searches for a specific product, the system returns relevant results containing the search term.

### Test Data:
- **Search term:** "laptop"

### Steps to Reproduce:
1. Navigate to [eMAG](https://www.emag.ro).
2. Enter "laptop" in the search bar.
3. Click the search button or press **Enter**.

### Expected Result:
- The search results page displays products that include the term **"laptop"** in their title or description (e.g., laptops, laptop accessories).
- Products unrelated to laptops (e.g., refrigerators, shoes) should **not** appear in the results.

### Pre-conditions:
- The search functionality is enabled.
- The database contains products related to **"laptop"**.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Functional
- **Automation:** Manual

---

## Test Case: Search Bar Provides Autocomplete Suggestions
**Description:** This test case ensures that the search bar suggests autocomplete results based on user input after a certain number of characters.

### Test Data:
- **Search term:** "telef"

### Steps to Reproduce:
1. Navigate to [eMAG](https://www.emag.ro).
2. Start typing **"telef"** in the search bar.
3. Observe the autocomplete suggestions provided by the system.

### Expected Result:
- The search bar suggests product names that start with or contain the entered characters (**"telef"**).
- Products that are not relevant to the entered term should not be suggested.

#### Example of valid suggestions:
✅ "telefon" (valid, starts with **"telef"**)
✅ "telefoane mobile" (valid, contains **"telef"**)

#### Example of invalid suggestions:
❌ "teleferic" (invalid, unless it is a relevant product category)

### Pre-conditions:
- The search autocomplete functionality is enabled.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Functional
- **Automation:** Manual

---

## Test Case: Searching for a Non-Existent Product Returns Alternative Suggestions
**Description:** This test case verifies that the search system provides proper feedback when a user searches for a term, even if the term is irrelevant or returns results that are not directly related to the query.

### Test Data:
- **Search term:** "abcdefgh1234567892" (irrelevant search term)

### Steps to Reproduce:
1. Navigate to [eMAG](https://www.emag.ro).
2. Enter **"abcdefgh1234567892"** in the search bar.
3. Observe the search suggestions that appear under the search bar.
4. Click the search button or press **Enter**.

### Expected Result:
- The system displays suggestions regardless of relevance to the search term.
- After pressing **Enter**, the system shows irrelevant products (e.g., fiction books or unrelated categories).
- The system does not show error messages and operates without crashes.

### Pre-conditions:
- The search functionality and suggestion system are enabled.
- The system should not show error messages or crash when irrelevant terms are searched.

### Additional Information:
- **Severity:** Normal
- **Priority:** Low
- **Type:** Functional
- **Automation:** Manual

---

## Test Case: Verify Search Functionality with Special Characters
**Description:** This test case verifies that when a user searches for a term containing special characters (e.g., @, #, %, &), the system ignores these characters and returns relevant results based on the valid portion of the term.

### Test Data:
- **Search term:** "@lap@top!#!@# ##" (containing special characters)

### Steps to Reproduce:
1. Navigate to [eMAG](https://www.emag.ro).
2. Enter **"@lap@top!#!@# ##"** in the search bar.
3. Click the search button or press **Enter**.

### Expected Result:
- The system should ignore the special characters and treat the search term as **"laptop"**.
- The system displays relevant results related to **"laptop"** (e.g., laptops or laptop accessories).
- No error messages or broken layouts should occur.
- The search should function as if the special characters were not included in the query.

### Pre-conditions:
- The search bar is functional.
- The search system is designed to ignore special characters and return results based on the main term.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Functional
- **Automation:** Manual
