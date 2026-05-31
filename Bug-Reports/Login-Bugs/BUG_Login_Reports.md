# Login Feature — Bug Reports
**Project:** Sauce Demo E-commerce App
**Module:** Login
**Version:** 1.0
**Date:** 25/05/2026
**Reported by:** Bemnet Merete
**Application URL:** https://www.saucedemo.com/

---

## BUG_001 — Error message not displayed properly when fields are empty

| Field | Details |
|---|---|
| **Bug ID** | BUG_001 |
| **Test Case ID** | TC_LOGIN_003 |
| **Feature** | Login |
| **Severity** | Medium |
| **Priority** | High |
| **Status** | ✅ Closed |

**Bug Title:**
Error message not displayed properly when fields are empty

**Steps to Reproduce:**
1. Navigate to SauceDemo login page
2. Leave all fields empty
3. Click the **Login** button

**Expected Result:**
Validation error messages shown for all required fields

**Actual Result:**
Error message `Epic sadface: Username is required` is displayed

**Resolution Notes:**
> Not a bug — expected behavior. App validates the Username field first when both fields are empty. This is the correct system behavior. TC_LOGIN_006 updated to Pass accordingly.

---

## BUG_002 — Error message not displayed properly when character limit is reached

| Field | Details |
|---|---|
| **Bug ID** | BUG_002 |
| **Test Case ID** | TC_LOGIN_008 |
| **Feature** | Login |
| **Severity** | Medium |
| **Priority** | High |
| **Status** | ✅ Closed |

**Bug Title:**
Error message not displayed properly when fields character limit is reached

**Steps to Reproduce:**
1. Navigate to SauceDemo login page
2. Enter `standard_user12345@Standard_User` in the Username field
3. Enter `secret_sauce12345@Secret_Sauce` in the Password field
4. Click the **Login** button

**Expected Result:**
Validation error message shown for character limit exceeded

**Actual Result:**
Error message shown: `Epic sadface: Username and password do not match any user in this service`

**Resolution Notes:**
> Not a bug — expected behavior. SauceDemo has no defined character limit for input fields. Long input is treated as unrecognized credentials and the system correctly returns an invalid credentials error. TC_LOGIN_008 updated to Pass accordingly.

---

## Bug Summary

| Bug ID | Title | Severity | Priority | Status | Linked TC |
|---|---|---|---|---|---|
| BUG_001 | Error message not displayed properly when fields are empty | Medium | High | ✅ Closed | TC_LOGIN_003 |
| BUG_002 | Error message not displayed when character limit reached | Medium | High | ✅ Closed | TC_LOGIN_008 |

---
