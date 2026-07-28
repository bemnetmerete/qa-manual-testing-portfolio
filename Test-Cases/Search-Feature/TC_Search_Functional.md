# Search Feature — Functional Test Cases
**Project:** OpenCart E-commerce App
**Module:** Search
**Type:** Functional (Positive)
**Version:** 1.0
**Date:** 25/06/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://demo.opencart.com/

---

## TC_SEARCH_001 — Verify search returns correct results for valid product name

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_001 |
| **Feature** | Search |
| **Test Type** | Positive |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Locate the search bar at the top of the homepage
3. Enter `MacBook` in the search field
4. Click the Search button (magnifying glass icon)

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | MacBook |

**Expected Result:**
Search results page displays products matching "MacBook" with correct product names, images, and prices.

**Actual Result:**
Search results page displayed products related to "MacBook" with correct names, images, and prices.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_002 — Verify search works with partial product name

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_002 |
| **Feature** | Search |
| **Test Type** | Positive |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Locate the search bar at the top of the homepage
3. Enter `Mac` in the search field
4. Click the Search button

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | Mac (partial name) |

**Expected Result:**
Search results page displays all products containing "Mac" in their name.

**Actual Result:**
Search results page displayed all products containing "Mac" in their names.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_003 — Verify search is case insensitive

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_003 |
| **Feature** | Search |
| **Test Type** | Positive |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `macbook` (all lowercase) in the search field
3. Click the Search button
4. Note the results displayed
5. Clear the search field
6. Enter `MACBOOK` (all uppercase) in the search field
7. Click the Search button
8. Compare results from both searches

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword 1 | macbook (all lowercase) |
| Search Keyword 2 | MACBOOK (all uppercase) |

**Expected Result:**
Both searches return identical results regardless of letter case.

**Actual Result:**
Both searches returned identical results — search is case insensitive.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_004 — Verify search results display product name, image and price

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_004 |
| **Feature** | Search |
| **Test Type** | Positive |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `MacBook` in the search field
3. Click the Search button
4. Observe each product card in the results page

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | MacBook |

**Expected Result:**
Each product card in the search results displays:
- Product name
- Product image
- Product price

**Actual Result:**
Each product card displayed the product name, image, and price correctly.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_SEARCH_005 — Verify clicking a search result navigates to correct product page

| Field | Details |
|---|---|
| **Test Case ID** | TC_SEARCH_005 |
| **Feature** | Search |
| **Test Type** | Positive |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://demo.opencart.com/
2. Application is accessible

**Test Steps:**
1. Navigate to https://demo.opencart.com/
2. Enter `MacBook` in the search field
3. Click the Search button
4. Click on the first product in the search results
5. Observe the page the user is navigated to

**Test Data:**
| Field | Value |
|---|---|
| Search Keyword | MacBook |

**Expected Result:**
User is navigated to the correct product detail page matching the clicked result.

**Actual Result:**
User was navigated to the correct product detail page after clicking the search result.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---
