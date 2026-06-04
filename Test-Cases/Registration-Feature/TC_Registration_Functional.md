# Registration Feature — Functional Test Cases
**Project:** OrangeHRM HR Management App
**Module:** Registration
**Type:** Functional (Positive)
**Version:** 1.0
**Date:** 29/05/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://opensource-demo.orangehrmlive.com
**Login Credentials:** Username: Admin | Password: admin123

---

## TC_REG_001 — Verify successful registration with all valid required fields

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_001 |
| **Feature** | Registration |
| **Test Type** | Positive |
| **Priority** | High |

**Preconditions:**
1. Browser is open at https://opensource-demo.orangehrmlive.com
2. User has valid credentials

**Test Steps:**
1. Navigate to https://opensource-demo.orangehrmlive.com
2. Enter `Admin` in the Username field
3. Enter `admin123` in the Password field
4. Navigate to the **PIM** tab
5. Click the **Add** button
6. Enter the employee's first name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Navigate to the **Admin** tab
11. Click the **Add** button
12. Select **User Role** and choose either `Admin` or `ESS` from the dropdown
13. Select **Employee Name** and type the employee's name
14. Select **Status** and choose either `Enabled` or `Disabled`
15. Enter a valid username in the **Username** field
16. Enter a valid password in the **Password** field
17. Re-enter the password in the **Confirm Password** field
18. Click the **Save** button

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| User Role | Admin / ESS |
| Status | Enabled / Disabled |
| Employee Name | (Full Name) |
| New Username | valid username |
| Password | valid password |

**Expected Result:**
The system should successfully create the employee record and associated user account using the provided valid data.

**Actual Result:**
The employee record and associated user account were successfully created using the provided valid data.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_002 — Verify user is redirected to correct page after successful registration

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_002 |
| **Feature** | Registration |
| **Test Type** | Positive |
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
6. Enter the employee's first name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Observe the page the user is redirected to

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| Employee Name | (Full Name) |

**Expected Result:**
User should be redirected to the appropriate page after successfully saving the employee record.

**Actual Result:**
User was successfully redirected to the appropriate page after saving the employee record.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---

## TC_REG_003 — Verify confirmation message appears after successful registration

| Field | Details |
|---|---|
| **Test Case ID** | TC_REG_003 |
| **Feature** | Registration |
| **Test Type** | Positive |
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
6. Enter the employee's first name
7. Enter the employee's middle name
8. Enter the employee's last name
9. Click the **Save** button
10. Observe the notification message displayed

**Test Data:**
| Field | Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| Employee Name | (Full Name) |

**Expected Result:**
A success notification should be displayed confirming that the record was saved successfully.

**Actual Result:**
Success notification `Successfully Saved` was displayed after the record was created.

**Status:** ✅ Pass
**Defect ID:** —
**Tested By:** Bemnet Merete

---
