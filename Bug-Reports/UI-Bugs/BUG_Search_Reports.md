# Search Feature — Bug Reports
**Project:** OpenCart E-commerce App
**Module:** Search
**Version:** 1.0
**Date:** 25/06/2026
**Reported by:** Bemnet Merete
**Application URL:** https://demo.opencart.com/

---

## BUG_SEARCH_001 — Search result count is missing from the search results page

| Field | Details |
|---|---|
| **Bug ID** | BUG_SEARCH_001 |
| **Test Case ID** | TC_SEARCH_019 |
| **Feature** | Search |
| **Severity** | Medium |
| **Priority** | Low |
| **Status** | 🔴 Open |

**Bug Title:**
Search result count is missing from the search results page

**Steps to Reproduce:**
1. Navigate to https://demo.opencart.com/
2. Locate the top search bar
3. Enter `MacBook` in the search input field
4. Click the Search button (magnifying glass icon)
5. Observe the search results page layout under the header `Products meeting the search criteria`

**Expected Result:**
The search results page should display a total result count summary such as `Showing 1 to 3 of 3 (1 Pages)` or `3 product(s) found` to inform the user of the total number of matching items.

**Actual Result:**
The total result count is completely missing from the UI above or near the product grid. Users have no way of knowing how many products matched their search without manually counting.

**Screenshots:**
- `BUG_SEARCH_001_missing_count.png`

---

## Bug Summary

| Bug ID | Title | Severity | Priority | Status | Linked TC |
|---|---|---|---|---|---|
| BUG_SEARCH_001 | Search result count missing from results page | Medium | Low | 🔴 Open | TC_SEARCH_019 |

---
