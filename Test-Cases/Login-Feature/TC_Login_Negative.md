# Login Feature — Negative, Boundary, Security & UI Test Cases

**Project:** Sauce Demo E-commerce App
**Module:** Login
**Type:** Negative | Boundary | Security | UI
**Version:** 1.0
**Date:** 25/05/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://www.saucedemo.com/

---

## TC_LOGIN_002 — Verify login fails with incorrect password

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_002 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | High         |

**Preconditions:**

1. User account exists
2. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter valid username in the Username field
3. Enter wrong password in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | standard_user |
| Password | wrong_password |

**Expected Result:**
Error message shown: `Invalid username or password`

**Actual Result:**
Error message shown: `Epic sadface: Username and password do not match any user in this service`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_003 — Verify login fails with empty username

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_003 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | Medium       |

**Preconditions:**

1. User account exists
2. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Leave the Username field empty
3. Enter `secret_sauce` in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | (empty) |
| Password | secret_sauce |

**Expected Result:**
Error message shown: `Username is required`

**Actual Result:**
Error message `Epic sadface: Username is required` is displayed.

**Status:** ✅ Pass
**Defect ID:** BUG_001 (Closed)
**Tested By:** Bemnet Merete

---

## TC_LOGIN_004 — Verify login fails with empty password

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_004 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | Medium       |

**Preconditions:**

1. User account exists
2. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter `standard_user` in the Username field
3. Leave the Password field empty
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | standard_user |
| Password | (empty) |

**Expected Result:**
Error message shown: `Password is required`

**Actual Result:**
Error message `Epic sadface: Password is required` is displayed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_005 — Verify login fails with locked out account

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_005 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | Medium       |

**Preconditions:**

1. Locked account exists
2. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter locked out username in the Username field
3. Enter locked out password in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | locked_out_user |
| Password | secret_sauce |

**Expected Result:**
Error message shown: `Account is locked`

**Actual Result:**
Error message `Epic sadface: Sorry, this user has been locked out.` is displayed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_006 — Verify login fails with both username and password empty

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_006 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | High         |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Leave all fields empty
3. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | (empty) |
| Password | (empty) |

**Expected Result:**
Error message shown: `Username is required`

**Actual Result:**
Error message `Epic sadface: Username is required` is displayed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_007 — Verify login page is protected against SQL injection attack

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_007 |
| **Feature**      | Login        |
| **Test Type**    | Security     |
| **Priority**     | High         |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter SQL injection string in the Username field
3. Enter SQL injection string in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | `' OR '1'='1` |
| Password | `' OR '1'='1` |

**Expected Result:**
Error message shown: `Invalid username or password`

**Actual Result:**
Error message shown: `Epic sadface: Username and password do not match any user in this service`

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_008 — Login with very long username and password

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_008 |
| **Feature**      | Login        |
| **Test Type**    | Boundary     |
| **Priority**     | Medium       |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Enter 65-character username in the Username field
3. Enter 65-character password in the Password field
4. Click the **Login** button

**Test Data:**
| Field | Value |
|---|---|
| Username | `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` (65 a's) |
| Password | `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb` (65 b's) |

**Expected Result:**
Login should fail — system should either show an error or reject the input gracefully without crashing.

**Actual Result:**
Error message shown: `Epic sadface: Username and password do not match any user in this service`

**Status:** ✅ Pass
**Defect ID:** BUG_002 (Closed)
**Tested By:** Bemnet Merete

---

## TC_LOGIN_009 — Verify password field masks input characters

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_009 |
| **Feature**      | Login        |
| **Test Type**    | UI           |
| **Priority**     | High         |

**Preconditions:**

1. User is on SauceDemo login page
2. Password must exist

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Click on the Password field
3. Enter `secret_sauce` in the Password field
4. Observe the characters in the Password field

**Test Data:**
| Field | Value |
|---|---|
| Password | secret_sauce |

**Expected Result:**
Each character typed in the Password field is immediately masked and displayed as dots (••••••••••••)

**Actual Result:**
User password is masked and invisible.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_010 — Verify login button behavior on multiple rapid clicks

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_010 |
| **Feature**      | Login        |
| **Test Type**    | Negative     |
| **Priority**     | Medium       |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Leave all fields empty
3. Click the **Login** button rapidly 5 times in succession
4. Observe the system response

**Test Data:**
| Field | Value |
|---|---|
| Username | (empty) |
| Password | (empty) |

**Expected Result:**
Error message shown: `Username is required`

**Actual Result:**
Error message `Epic sadface: Username is required` is displayed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_011 — Verify tab navigation between fields

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_011 |
| **Feature**      | Login        |
| **Test Type**    | UI           |
| **Priority**     | Medium       |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Click on the Username field
3. Press the **Tab** key on the keyboard
4. Observe which field receives focus next
5. Press **Tab** again
6. Observe which field receives focus

**Test Data:**
| Field | Value |
|---|---|
| Test Data | None |

**Expected Result:**
Focus moves from Username → Password → Login button in logical order when Tab key is pressed.

**Actual Result:**
Tab navigation was successful.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_LOGIN_012 — Verify login page is responsive across different screen sizes

| Field            | Details      |
| ---------------- | ------------ |
| **Test Case ID** | TC_LOGIN_012 |
| **Feature**      | Login        |
| **Test Type**    | UI           |
| **Priority**     | Medium       |

**Preconditions:**

1. User is on SauceDemo login page

**Test Steps:**

1. Navigate to https://www.saucedemo.com/
2. Right click on empty space on the page
3. Click **Inspect** tab
4. Click **Toggle device emulation** icon on top-left of screen
5. Enter `standard_user` in the Username field
6. Enter `secret_sauce` in the Password field
7. Resize tab for **Mobile**, **Tablet**, and **Laptop** screen sizes

**Test Data:**
| Field | Value |
|---|---|
| Username | standard_user |
| Password | secret_sauce |

**Expected Result:**
Login page layout adjusts correctly for Mobile, Tablet, and Desktop screen sizes. All fields and buttons remain visible and usable.

**Actual Result:**
Login page displayed correctly on Mobile (375px), Tablet (768px), and Desktop (1280px). All elements visible and functional.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---
