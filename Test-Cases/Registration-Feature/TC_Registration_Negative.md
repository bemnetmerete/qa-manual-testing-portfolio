# Registration Feature — Negative, Boundary, Security & UI Test Cases
**Project:** OrangeHRM HR Management App
**Module:** Registration
**Type:** Negative | Boundary | Security | UI
**Version:** 1.0
**Date:** 29/05/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://opensource-demo.orangehrmlive.com
**Login Credentials:** Username: Admin | Password: admin123

---

## TC_REG_004 — Verify registration fails with empty full name field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_004 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Leave the **Employee Name** field empty
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Enter a valid username in the **Username** field
10. Enter a valid password in the **Password** field
11. Re-enter the password in the **Confirm Password** field
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (empty) |
| Status | Enabled / Disabled |
| Username | valid username |
| Password | valid password |

**Expected Result:**
System should prevent submission and display a validation message indicating that the Employee Name field is required.

**Actual Result:**
Validation message `Required` was displayed below the Employee Name field and record creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_005 — Verify registration fails with empty username field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_005 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Select **Employee Name** and type the employee's name
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Leave the **Username** field empty
10. Enter a valid password in the **Password** field
11. Re-enter the password in the **Confirm Password** field
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (Full Name) |
| Status | Enabled / Disabled |
| Username | (empty) |
| Password | valid password |

**Expected Result:**
System should prevent submission and display a validation message indicating that the Username field is required.

**Actual Result:**
Validation message `Required` was displayed below the Username field and record creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_006 — Verify registration fails with empty password field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_006 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Select **Employee Name** and type the employee's name
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Enter a valid username in the **Username** field
10. Leave the **Password** field empty
11. Re-enter the password in the **Confirm Password** field
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (Full Name) |
| Status | Enabled / Disabled |
| Username | valid username |
| Password | (empty) |

**Expected Result:**
System should prevent submission and display a validation message indicating that the Password field is required.

**Actual Result:**
Validation message `Required` was displayed below the Password field and record creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_007 — Verify registration fails with empty confirm password field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_007 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Select **Employee Name** and type the employee's name
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Enter a valid username in the **Username** field
10. Enter a valid password in the **Password** field
11. Leave the **Confirm Password** field empty
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (Full Name) |
| Status | Enabled / Disabled |
| Username | valid username |
| Password | valid password |
| Confirm Password | (empty) |

**Expected Result:**
System should prevent submission and display a validation message indicating that Confirm Password is required.

**Actual Result:**
Validation message `Passwords do not match` was displayed and record creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_008 — Verify registration fails when passwords do not match

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_008 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Select **Employee Name** and type the employee's name
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Enter a valid username in the **Username** field
10. Enter a valid password in the **Password** field
11. Enter a different password in the **Confirm Password** field
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (Full Name) |
| Status | Enabled / Disabled |
| Username | valid username |
| Password | Admin@1234 |
| Confirm Password | Admin@9999 |

**Expected Result:**
System should prevent submission and display a validation message indicating that `Passwords do not match`.

**Actual Result:**
Validation message `Passwords do not match` was displayed when the entered passwords were different.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_009 — Verify registration fails with duplicate username

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_009 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page
4. A user account with the duplicate username already exists

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
7. Select **Employee Name** and type the employee's name
8. Select **Status** and choose either `Enabled` or `Disabled`
9. Enter an already existing username in the **Username** field
10. Enter a valid password in the **Password** field
11. Re-enter the password in the **Confirm Password** field
12. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Employee Name | (Full Name) |
| Status | Enabled / Disabled |
| Username | Admin (already exists) |
| Password | valid password |
| Confirm Password | valid password |

**Expected Result:**
System should prevent account creation and display a message indicating that the username already exists.

**Actual Result:**
Validation message `Already Exists` was displayed and account creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_010 — Verify registration fails with all fields empty

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_010 |
| **Feature** | Registration |
| **Test Type** | Negative |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **Admin** tab
5. Click the **Add** button
6. Leave all fields empty
7. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| All other fields | (empty) |

**Expected Result:**
System should prevent submission and display validation messages for all mandatory fields.

**Actual Result:**
Validation messages were displayed for all mandatory fields and record creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_011 — Verify registration fails with username below minimum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_011 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a username below the minimum character limit in the **Username** field
16. Enter a valid password in the **Password** field
17. Re-enter the password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| New Username | `user` (4 characters — below minimum of 5) |

**Expected Result:**
System should reject usernames shorter than the minimum allowed length and display an appropriate validation message.

**Actual Result:**
Validation message `Should be at least 5 characters` was displayed and account creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_012 — Verify registration succeeds with username at minimum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_012 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a username that matches the exact minimum character limit in the **Username** field
16. Enter a valid password in the **Password** field
17. Re-enter the password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| New Username | `user1` (exactly 5 characters — minimum limit) |

**Expected Result:**
System should accept a username that exactly matches the minimum allowed character length.

**Actual Result:**
Username containing exactly 5 characters was accepted and the account was successfully created.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_013 — Verify registration succeeds with username at maximum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_013 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a username that matches the exact maximum character limit in the **Username** field
16. Enter a valid password in the **Password** field
17. Re-enter the password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| New Username | `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` (exactly 40 characters — maximum limit) |

**Expected Result:**
System should accept a username that exactly matches the maximum allowed character length.

**Actual Result:**
Username containing exactly 40 characters was accepted and the account was successfully created.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_014 — Verify registration fails with username above maximum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_014 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a username above the maximum character limit in the **Username** field
16. Enter a valid password in the **Password** field
17. Re-enter the password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| New Username | `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa` (41 characters — above maximum limit) |

**Expected Result:**
System should reject usernames exceeding the maximum allowed character length and display an appropriate validation message.

**Actual Result:**
Validation message `Should not exceed 40 characters` was displayed and account creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_015 — Verify registration fails with password below minimum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_015 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a valid username in the **Username** field
16. Enter a password below the minimum character limit in the **Password** field
17. Re-enter the same password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| Password | `Test@` (6 characters — below minimum of 7) |
| Confirm Password | `Test@` |

**Expected Result:**
System should reject passwords shorter than the minimum allowed length and display an appropriate validation message.

**Actual Result:**
Validation message `Should have at least 7 characters` was displayed and account creation was prevented.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_016 — Verify registration succeeds with password at minimum character limit

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_016 |
| **Feature** | Registration |
| **Test Type** | Boundary |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials
3. User is on the correct registration page

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's full name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a valid username in the **Username** field
16. Enter a password that matches the exact minimum character limit in the **Password** field
17. Re-enter the same password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| Password | `Test@12` (exactly 7 characters — minimum limit) |
| Confirm Password | `Test@12` |

**Expected Result:**
System should accept a password that meets the minimum character requirement and satisfies password policy rules.

**Actual Result:**
Password containing exactly 7 characters was accepted and the account was successfully created.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_017 — Verify registration rejects SQL injection in username field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_017 |
| **Feature** | Registration |
| **Test Type** | Security |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid admin credentials
3. User is on Admin → Add User page

**Test Steps:**
1. Login as Admin
2. Navigate to **Admin → Add**
3. Select **User Role** from the dropdown
4. Select **Employee Name** from the field
5. Select **Status** from the dropdown
6. Enter SQL injection string in the **Username** field
7. Enter a valid password in the **Password** field
8. Re-enter the password in the **Confirm Password** field
9. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | ESS |
| Employee Name | (existing employee name) |
| Username | `' OR '1'='1` |
| Password | Test123! |
| Confirm Password | Test123! |

**Expected Result:**
System should safely handle SQL injection input without causing unauthorized access, database manipulation, or unexpected system behavior.

**Actual Result:**
Application accepted the input and stored it as the username. No unauthorized access, authentication bypass, or unexpected behavior was observed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Input was treated as plain text and did not appear to affect application functionality or database operations.

---

## TC_REG_018 — Verify registration rejects XSS script in first name field

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_018 |
| **Feature** | Registration |
| **Test Type** | Security |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User is logged in
3. User is on PIM → Add Employee page

**Test Steps:**
1. Navigate to **PIM → Add Employee**
2. Enter XSS script in the **First Name** field
3. Fill all remaining required fields with valid data
4. Click the **Save** button
5. Observe whether the script executes

**Test Data:**
| Field | Value |
|---|---|
| First Name | `<script>alert('XSS')</script>` |
| Last Name | TestUser |

**Expected Result:**
Application should safely handle script input without executing JavaScript code or affecting system functionality.

**Actual Result:**
Application accepted the script as plain text and no JavaScript execution or unexpected behavior was observed.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Application did not execute the injected script. Input appears to be treated as plain text.

---

## TC_REG_019 — Verify password field masks input characters

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_019 |
| **Feature** | Registration |
| **Test Type** | Security |
| **Priority** | High |

**Preconditions:**
1. User is on Admin → Add User page

**Test Steps:**
1. Click on the **Password** field
2. Enter password in the **Password** field
3. Observe the displayed characters in the Password field
4. Click on the **Confirm Password** field
5. Enter password in the **Confirm Password** field
6. Observe the displayed characters in the Confirm Password field

**Test Data:**
| Field | Value |
|---|---|
| Password | Test123! |
| Confirm Password | Test123! |

**Expected Result:**
Password and Confirm Password fields should display masked characters (●●●●● or ••••••) instead of plain text.

**Actual Result:**
Password and Confirm Password fields displayed masked characters and did not expose the entered values.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** If password is visible in plain text, create a Critical Severity bug.

---

## TC_REG_020 — Verify all required fields are marked with an asterisk (*)

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_020 |
| **Feature** | Registration |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User is logged in as Admin
3. User is on the Admin → Add User page

**Test Steps:**
1. Login as Admin
2. Navigate to **Admin → Add User**
3. Observe all input fields on the form
4. Identify fields that are mandatory
5. Verify whether mandatory fields have a visual indicator such as a red asterisk (*)

**Test Data:**
| Field | Value |
|---|---|
| Test Data | N/A — observation test only |

**Expected Result:**
All mandatory fields should clearly display a required-field indicator (e.g., red asterisk *) so users can easily identify which fields must be completed.

**Actual Result:**
All mandatory fields displayed a visible required-field indicator (*), allowing users to easily identify required inputs.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Capture a screenshot if any required field lacks a visual indicator.

---

## TC_REG_021 — Verify tab navigation works correctly between all fields

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_021 |
| **Feature** | Registration |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User is logged in as Admin
3. User is on the Admin → Add User page

**Test Steps:**
1. Place cursor in the first input field
2. Press the **Tab** key repeatedly
3. Observe the order in which focus moves through fields
4. Continue until all fields and buttons are reached
5. Verify focus is visible on each field

**Test Data:**
| Field | Value |
|---|---|
| Test Data | N/A — keyboard navigation test only |

**Expected Result:**
Keyboard focus should move sequentially through all form fields and buttons without skipping elements. The active field should always be visibly highlighted.

**Actual Result:**
Keyboard focus moved sequentially through all fields and remained visible throughout navigation.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Create a bug if focus skips fields, gets trapped, or becomes invisible.

---

## TC_REG_022 — Verify registration form is responsive across different screen sizes

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_022 |
| **Feature** | Registration |
| **Test Type** | UI |
| **Priority** | Medium |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User is logged in as Admin
3. User is on the Admin → Add User page

**Test Steps:**
1. Open the registration form
2. View the page in desktop resolution
3. Resize browser to tablet width
4. Resize browser to mobile width
5. Observe layout, fields, buttons, and text at each size
6. Verify usability at each screen size

**Test Data:**
| Screen Size | Resolution |
|---|---|
| Desktop | 1920 × 1080 |
| Tablet | 768 × 1024 |
| Mobile | 375 × 667 |

**Expected Result:**
The registration form should remain fully usable on all screen sizes. No text, fields, or buttons should overlap, disappear, or become inaccessible.

**Actual Result:**
Registration form remained fully functional across desktop, tablet, and mobile screen sizes without layout or usability issues.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Take screenshots if layout breaks, elements overlap, or horizontal scrolling occurs.

---

## TC_REG_023 — Verify error messages display in correct position and styling

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_023 |
| **Feature** | Registration |
| **Test Type** | UI |
| **Priority** | Low |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User is logged in as Admin
3. User is on the Admin → Add User page

**Test Steps:**
1. Open the registration form
2. Leave one or more mandatory fields blank
3. Click the **Save** button
4. Observe displayed validation messages
5. Verify message location, readability, and styling

**Test Data:**
| Field | Value |
|---|---|
| Required fields | Leave empty |

**Expected Result:**
Validation messages should appear next to the corresponding fields, be clearly readable, and accurately describe the input error. Styling should remain consistent across all validation messages.

**Actual Result:**
Validation messages were displayed next to the corresponding fields and remained clear, readable, and consistently styled.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete
**Notes:** Create a bug if messages are unclear, misplaced, inconsistent, or fail to appear.

---
