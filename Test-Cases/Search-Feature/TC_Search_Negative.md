# Search Feature — Negative, Boundary, Security & UI Test Cases
**Project:** OpenCart E-commerce App
**Module:** Search
**Type:** Negative | Boundary | Security | UI
**Version:** 1.0
**Date:** 25/06/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://demo.opencart.com/

---

## TC_SEARCH_006 — Verify search shows no results message for invalid product name

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_006 |
| **Feature** | Search |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `xyzxyzxyz123` in the search field
3. Click the Search button
4. Observe the page response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | xyzxyzxyz123 (non-existent product) |

**Expected Result:**
Search results page displays a message indicating no products were found.

**Actual Result:**
Search results page displayed the message `There is no product that matches the search criteria.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_007 — Verify search fails gracefully with empty search field

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_007 |
| **Feature** | Search |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Leave the search field completely empty
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | (empty) |

**Expected Result:**
System should handle empty search gracefully — either show all products or display a message prompting the user to enter a search term.

**Actual Result:**
Search results page displayed the message `There is no product that matches the search criteria.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_008 — Verify search handles special characters without crashing

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_008 |
| **Feature** | Search |
| **Test Type** | Negative |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter special characters in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | @#$%^&*() |

**Expected Result:**
System should handle special characters without crashing — display no results or a relevant message.

**Actual Result:**
Search results page displayed the message `There is no product that matches the search criteria.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_009 — Verify search handles numbers only input

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_009 |
| **Feature** | Search |
| **Test Type** | Negative |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter numbers only in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | 123456 |

**Expected Result:**
System should handle numeric input — display matching products or show a no results message without crashing.

**Actual Result:**
Search results page displayed the message `There is no product that matches the search criteria.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_010 — Verify search handles very long input text

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_010 |
| **Feature** | Search |
| **Test Type** | Negative |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter a very long string of text in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` (64 a's) |

**Expected Result:**
System should handle very long input gracefully — display no results or truncate input without crashing.

**Actual Result:**
Search results page displayed the message `There is no product that matches the search criteria.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_011 — Verify search with single character input

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_011 |
| **Feature** | Search |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter a single character in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | a (single character) |

**Expected Result:**
System should process single character input and display matching results or a no results message.

**Actual Result:**
System processed single character input and displayed matching results.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_012 — Verify search with exactly maximum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_012 |
| **Feature** | Search |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter a string of exactly 128 characters in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | 128 character string: `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` |

**Expected Result:**
System should accept the maximum character input and process the search without errors.

**Actual Result:**
System accepted the 128 character input and processed the search without crashing.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_013 — Verify search with input above maximum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_013 |
| **Feature** | Search |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter a string of 129 or more characters in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | 129 character string: `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` |

**Expected Result:**
System should either truncate input to the maximum allowed length or display a validation message.

**Actual Result:**
System truncated the input to 128 characters and processed the search without crashing.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_014 — Verify search field rejects SQL injection attempt

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_014 |
| **Feature** | Search |
| **Test Type** | Security |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter SQL injection string in the search field
3. Click the Search button
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | `' OR '1'='1` |

**Expected Result:**
System should safely handle SQL injection input without exposing database data or causing unexpected behavior.

**Actual Result:**
System handled SQL injection input safely — no database data was exposed and no unexpected behavior was observed. Search results page displayed the message `Sorry you have been blocked.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** SQL injection attempt was blocked by the application's security layer — no unauthorized data access observed.

---

## TC_SEARCH_015 — Verify search field rejects XSS script input

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_015 |
| **Feature** | Search |
| **Test Type** | Security |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter XSS script in the search field
3. Click the Search button
4. Observe whether the script executes

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | `<script>alert('XSS')</script>` |

**Expected Result:**
System should safely handle XSS input without executing the script.

**Actual Result:**
System handled XSS input safely — no JavaScript alert or popup was executed. Search results page displayed the message `Sorry you have been blocked.`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** XSS script was blocked by the application's security layer — no script execution was observed.

---

## TC_SEARCH_016 — Verify search bar is visible and accessible on homepage

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_016 |
| **Feature** | Search |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Observe the homepage layout
3. Locate the search bar
4. Verify the search bar is clearly visible
5. Verify the search button is accessible

**Test Data:**
| Field | Value |
|---|---|
| Test Data | N/A — visual observation only |

**Expected Result:**
Search bar should be clearly visible at the top of the homepage with a search input field and search button.

**Actual Result:**
Search bar was clearly visible at the top of the homepage with an input field and search button.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_017 — Verify search results page displays correct layout

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_017 |
| **Feature** | Search |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `MacBook` in the search field
3. Click the Search button
4. Observe the layout of the search results page

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | MacBook |

**Expected Result:**
Search results page should display products in a clean grid or list layout with consistent spacing, visible product names, images, and prices.

**Actual Result:**
Search results page displayed products in a clean and consistent grid layout with visible product names, images, and prices.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_018 — Verify search is responsive across different screen sizes

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_018 |
| **Feature** | Search |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible
3. Chrome DevTools is available

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Press **F12** to open Chrome DevTools
3. Click the **Toggle device emulation** icon
4. Set screen size to Mobile (375px)
5. Observe the search bar layout
6. Set screen size to Tablet (768px)
7. Observe the search bar layout
8. Set screen size to Desktop (1280px)
9. Observe the search bar layout

**Test Data:**
| Screen Size | Resolution |
|---|---|
| Mobile | 375 x 667 |
| Tablet | 768 x 1024 |
| Desktop | 1280 x 800 |

**Expected Result:**
Search bar and search results should remain fully visible and usable across all screen sizes without overlapping or disappearing.

**Actual Result:**
Search bar and results page remained fully visible and usable across Mobile, Tablet, and Desktop screen sizes.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_019 — Verify search result count is displayed correctly

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_019 |
| **Feature** | Search |
| **Test Type** | UI |
| **Priority** | Low |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `MacBook` in the search field
3. Click the Search button
4. Observe whether a result count is displayed on the page

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | MacBook |

**Expected Result:**
Search results page should display the total number of results found for the search keyword.

**Actual Result:**
Search results page did not display a result count indicating the total number of matching products found.

**Status:** ❌ Fail
**Defect ID:** BUG_SEARCH_001
**Tested By:** Bemnet Merete
**Notes:** Expected result count summary (e.g., "Showing 1 to 3 of 3") was missing from the UI.

---
