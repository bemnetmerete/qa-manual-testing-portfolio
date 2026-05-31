# Login Feature — Functional Test Cases

**Project:** Sauce Demo E-commerce App
**Module:** Login
**Type:** Functional (Positive)
**Version:** 1.0
**Date:** 25/05/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://www.saucedemo.com/

---

## TC_LOGIN_001 — Verify successful login with valid credentials

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_001 |
| **Feature**      | Login        |
| **Test Type**    | Positive     |
| **Priority**     | High         |

**Preconditions:**

1. Browser is open at https://www.saucedemo.com/
2. User has valid credentials

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter `standard_user` in the Username field
3. Enter `secret_sauce` in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | standard_user |
| Password | secret_sauce |

**Expected Result:**
User redirected to `/inventory.html` and inventory items displayed successfully.

**Actual Result:**
User successfully redirected to `/inventory.html` and all product items displayed correctly.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---
