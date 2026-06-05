# Test Plan — OrangeHRM HR Management Application
**Document ID:** TP_OrangeHRM_v1.0
**Version:** 1.0
**Date:** 29/05/2026
**Prepared by:** Bemnet Merete
**Application URL:** https://opensource-demo.orangehrmlive.com
**Status:** Active

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Test Objectives](#2-test-objectives)
3. [Scope of Testing](#3-scope-of-testing)
4. [Test Approach](#4-test-approach)
5. [Features to be Tested](#5-features-to-be-tested)
6. [Features Not to be Tested](#6-features-not-to-be-tested)
7. [Test Types](#7-test-types)
8. [Test Environment](#8-test-environment)
9. [Test Data](#9-test-data)
10. [Test Schedule](#10-test-schedule)
11. [Entry and Exit Criteria](#11-entry-and-exit-criteria)
12. [Defect Management](#12-defect-management)
13. [Risks and Mitigation](#13-risks-and-mitigation)
14. [Deliverables](#14-deliverables)
15. [Approval](#15-approval)

---

## 1. Introduction

### 1.1 Purpose
This Test Plan document describes the testing strategy, scope, approach, resources, and schedule for testing the **OrangeHRM HR Management Application**. It serves as a guide for the QA team to ensure the application meets the specified requirements and delivers a reliable, high-quality user experience.

### 1.2 Project Overview
OrangeHRM is an open-source Human Resource Management (HRM) system that provides a wide range of HR functionalities including employee management, user registration, leave management, recruitment, and reporting. This test plan covers the testing of the OrangeHRM demo application available at https://opensource-demo.orangehrmlive.com.

### 1.3 Application Overview

| Item | Details |
|---|---|
| **Application Name** | OrangeHRM HR Management System |
| **Application Type** | Web Application |
| **Application URL** | https://opensource-demo.orangehrmlive.com |
| **Admin Login** | Username: Admin / Password: admin123 |
| **Platform** | Browser-based |
| **Purpose** | Human Resource Management |

### 1.4 Document References

| Document | Description |
|---|---|
| TC_OrangeHRM_Registration_v1.0 | Registration feature test cases |
| TC_OrangeHRM_Login_v1.0 | Login feature test cases |
| TC_SauceDemo_Login_v1.0 | SauceDemo login test cases |

---

## 2. Test Objectives

The primary objectives of this testing effort are:

- ✅ Verify that all core HR functionalities work as specified
- ✅ Ensure the application handles valid and invalid inputs correctly
- ✅ Confirm that error messages are clear, accurate, and helpful
- ✅ Validate that the application is secure against common attacks such as SQL injection and XSS
- ✅ Verify the application is responsive across different screen sizes and devices
- ✅ Ensure data integrity is maintained across all modules
- ✅ Confirm that navigation and user flows work correctly end to end
- ✅ Identify and document any defects before the application is used in production

---

## 3. Scope of Testing

### 3.1 In Scope

The following modules and features are included in this testing effort:

| Module | Features |
|---|---|
| **Authentication** | Login, Logout, Session management |
| **Registration** | Add Employee, Add User account |
| **Employee Management** | View, Edit, Delete employee records |
| **User Management** | Add, Edit, Delete user accounts |
| **Leave Management** | Apply for leave, Approve/Reject leave |
| **Search** | Employee search, Filter and sort results |
| **Navigation** | Menu navigation, Tab switching, Breadcrumbs |
| **UI / Responsiveness** | Layout, Styling, Mobile and Tablet views |
| **Security** | SQL injection, XSS, Unauthorized access |

### 3.2 Out of Scope

The following are explicitly excluded from this testing effort:

- Backend server configuration and infrastructure testing
- Database performance under extreme load
- Third-party integrations not available in the demo environment
- Payroll and compensation modules (not available in demo)
- Mobile native application testing
- Email notification delivery testing

---

## 4. Test Approach

### 4.1 Testing Methodology

This project follows a **manual testing** approach using structured test cases. Testing will progress in the following order:

```
Step 1: Review requirements and understand application behavior
Step 2: Write test cases covering all scenarios
Step 3: Execute test cases on the demo application
Step 4: Record actual results and compare with expected results
Step 5: Log defects for any failures found
Step 6: Retest after defect resolution
Step 7: Produce test summary report
```

### 4.2 Testing Levels

| Level | Description | Responsibility |
|---|---|---|
| **Functional Testing** | Verify each feature works as expected | QA Engineer |
| **Negative Testing** | Verify error handling for invalid inputs | QA Engineer |
| **Boundary Value Testing** | Verify behavior at input limits | QA Engineer |
| **Security Testing** | Verify protection against common attacks | QA Engineer |
| **UI Testing** | Verify visual layout and responsiveness | QA Engineer |
| **Regression Testing** | Re-verify existing features after changes | QA Engineer |

### 4.3 Test Design Techniques

The following test design techniques will be applied:

| Technique | Applied To |
|---|---|
| **Equivalence Partitioning** | Input fields with defined valid/invalid ranges |
| **Boundary Value Analysis** | Username length, Password length, numeric inputs |
| **Decision Table Testing** | Complex business rules (e.g. leave approval logic) |
| **Exploratory Testing** | Navigation, edge cases, unexpected user behavior |
| **Use Case Testing** | End-to-end user workflows |

---

## 5. Features to be Tested

### 5.1 Authentication Module

| Feature | Test Scenarios |
|---|---|
| Login | Valid credentials, Invalid credentials, Empty fields, Locked account |
| Logout | Successful logout, Session cleared after logout |
| Session | Session expires after inactivity |

### 5.2 Registration Module

| Feature | Test Scenarios |
|---|---|
| Add Employee | Valid data, Empty required fields, Boundary values |
| Add User Account | Valid data, Duplicate username, Password mismatch |
| Field Validation | Required fields, Character limits, Format validation |

### 5.3 Employee Management Module

| Feature | Test Scenarios |
|---|---|
| View Employees | Employee list displayed correctly |
| Edit Employee | Update valid data, Validation on edit |
| Delete Employee | Successful deletion, Confirmation prompt |
| Search Employee | Search by name, Filter by status |

### 5.4 User Management Module

| Feature | Test Scenarios |
|---|---|
| View Users | User list displayed correctly |
| Edit User | Update valid data, Validation on edit |
| Delete User | Successful deletion, Confirmation prompt |

### 5.5 Leave Management Module

| Feature | Test Scenarios |
|---|---|
| Apply for Leave | Valid dates, Overlapping dates, Insufficient balance |
| Approve Leave | Admin approves pending leave request |
| Reject Leave | Admin rejects with reason |

### 5.6 Search Module

| Feature | Test Scenarios |
|---|---|
| Employee Search | Valid name, Partial name, No results, Special characters |
| Filter Results | Filter by department, Status, Employment type |

### 5.7 Navigation

| Feature | Test Scenarios |
|---|---|
| Menu Navigation | All menu items navigate to correct pages |
| Tab Navigation | Keyboard Tab order is logical and complete |
| Breadcrumbs | Correct path shown, Back navigation works |

### 5.8 Security

| Feature | Test Scenarios |
|---|---|
| SQL Injection | Login field, Search field, Username field |
| XSS Attack | Name fields, Description fields |
| Unauthorized Access | Direct URL access without login |
| Password Security | Password masking, Minimum length enforcement |

---

## 6. Features Not to be Tested

| Feature | Reason Excluded |
|---|---|
| Payroll Module | Not available in demo environment |
| Report Generation | Out of scope for current testing cycle |
| Email Notifications | Cannot verify email delivery in demo |
| Backend APIs | Outside scope of manual testing phase |
| Database Layer | Direct DB access not available in demo |
| Performance Under Load | Requires dedicated performance testing tools |
| Third-party Integrations | Not configured in demo environment |

---

## 7. Test Types

### 7.1 Functional Testing
Verify that each feature performs its intended function correctly according to requirements.

**Row Color in Test Cases:** 🔵 Light Blue / ⚪ White

### 7.2 Negative Testing
Verify that the application handles incorrect, invalid, or unexpected inputs gracefully.

**Row Color in Test Cases:** 🔴 Light Red

### 7.3 Boundary Value Testing
Verify application behavior at the exact minimum and maximum limits of input fields.

**Row Color in Test Cases:** 🟠 Light Orange

### 7.4 Security Testing
Verify that the application is protected against common web attacks and unauthorized access.

**Row Color in Test Cases:** 🟣 Light Purple

### 7.5 UI / Visual Testing
Verify that the application displays correctly across different browsers and screen sizes.

**Row Color in Test Cases:** 🟡 Light Yellow

### 7.6 Regression Testing
Re-execute previously passed test cases after bug fixes or new feature additions to ensure no existing functionality is broken.

---

## 8. Test Environment

### 8.1 Hardware

| Component | Specification |
|---|---|
| **Computer** | Windows PC (low-end) |
| **RAM** | Available system memory |
| **Storage** | Sufficient for screenshots and reports |

### 8.2 Software

| Component | Details |
|---|---|
| **Operating System** | Windows |
| **Primary Browser** | Google Chrome (latest version) |
| **Secondary Browser** | Microsoft Edge (latest version) |
| **Code Editor** | Visual Studio Code |
| **Terminal** | Git Bash |
| **Version Control** | Git and GitHub |
| **Test Documentation** | Google Sheets, Markdown |
| **Screenshot Tool** | Windows Snipping Tool (Win + Shift + S) |

### 8.3 Test Application Access

| Item | Details |
|---|---|
| **Application URL** | https://opensource-demo.orangehrmlive.com |
| **Admin Username** | Admin |
| **Admin Password** | admin123 |
| **Environment Type** | Public demo — shared environment |
| **Data Reset** | Demo data may reset periodically |

### 8.4 Browser Compatibility

| Browser | Version | Priority |
|---|---|---|
| Google Chrome | Latest | Primary — all tests run here first |
| Microsoft Edge | Latest | Secondary — key tests verified here |
| Mozilla Firefox | Latest | Optional — if time allows |

---

## 9. Test Data

### 9.1 Valid Test Data Examples

| Field | Valid Value |
|---|---|
| Admin Username | Admin |
| Admin Password | admin123 |
| Employee First Name | John |
| Employee Last Name | Doe |
| New Username | testuser1 |
| New Password | Admin@1234 |
| Confirm Password | Admin@1234 |

### 9.2 Invalid Test Data Examples

| Field | Invalid Value | Purpose |
|---|---|---|
| Username | (empty) | Empty field validation |
| Password | Test@ | Below minimum length |
| Username | `' OR '1'='1` | SQL injection test |
| First Name | `<script>alert('XSS')</script>` | XSS attack test |
| Username | `aaaa` | Below minimum 5 characters |
| Username | 41 character string | Above maximum 40 characters |

### 9.3 Boundary Test Data

| Field | Min Limit | Max Limit | Below Min | At Min | At Max | Above Max |
|---|---|---|---|---|---|---|
| Username | 5 chars | 40 chars | 4 chars | 5 chars | 40 chars | 41 chars |
| Password | 7 chars | N/A | 6 chars | 7 chars | N/A | N/A |

### 9.4 Test Data Management Notes

- Demo environment data may be reset by OrangeHRM periodically
- Always verify test data exists before executing dependent test cases
- Create fresh test data at the start of each test session if needed
- Do not use real personal information as test data

---

## 10. Test Schedule

### 10.1 Testing Phases

| Phase | Activity | Status |
|---|---|---|
| Phase 1 | Login Feature Testing | ✅ Completed |
| Phase 2 | Registration Feature Testing | ✅ Completed |
| Phase 3 | Search Feature Testing | ⏳ In Progress |
| Phase 4 | Checkout / Navigation Testing | ⏳ Pending |
| Phase 5 | Employee Management Testing | ⏳ Pending |
| Phase 6 | Leave Management Testing | ⏳ Pending |
| Phase 7 | Regression Testing | ⏳ Pending |
| Phase 8 | Test Closure and Reporting | ⏳ Pending |

### 10.2 Daily Workflow

```
1. Open application and verify environment is available
2. Review test cases for the session
3. Execute test cases one by one
4. Fill in Actual Result and Status immediately after each test
5. Take screenshot for each test result
6. Log any bugs found
7. Commit test cases and screenshots to GitHub
8. Update test schedule with progress
```

---

## 11. Entry and Exit Criteria

### 11.1 Entry Criteria
Testing will begin when all of the following conditions are met:

- ✅ Application is accessible at the test URL
- ✅ Admin login credentials are working
- ✅ Test cases have been written and reviewed
- ✅ Test environment is confirmed and stable
- ✅ Test data has been prepared
- ✅ GitHub portfolio repository is set up and ready

### 11.2 Exit Criteria
Testing will be considered complete when all of the following conditions are met:

- ✅ All planned test cases have been executed
- ✅ All High priority test cases have passed
- ✅ All Critical and High severity bugs have been resolved and verified
- ✅ Test summary report has been completed
- ✅ All screenshots have been committed to GitHub
- ✅ All Markdown files have been committed to GitHub

### 11.3 Suspension Criteria
Testing will be suspended if:

- ❌ Application is completely inaccessible
- ❌ Admin login credentials stop working
- ❌ Demo environment data is reset mid-testing session
- ❌ Critical blocker bug prevents further test execution

---

## 12. Defect Management

### 12.1 Bug Severity Levels

| Severity | Definition | Example |
|---|---|---|
| **Critical** | Application crashes or data loss occurs | Cannot login at all |
| **High** | Major feature completely broken | Registration form does not save |
| **Medium** | Feature partially broken but workaround exists | Validation message missing for one field |
| **Low** | Minor cosmetic or UI issue | Button slightly misaligned |

### 12.2 Bug Priority Levels

| Priority | Definition |
|---|---|
| **High** | Fix immediately — blocks release or critical user flow |
| **Medium** | Fix in current sprint — important but not blocking |
| **Low** | Fix when time allows — minor impact |

### 12.3 Bug Life Cycle

```
Open → In Progress → Ready for Retest → Verified → Closed

Special cases:
Reopened  → Bug was fixed but still exists after retest
Deferred  → Acknowledged but postponed to future release
Won't Fix → Team decided not to fix this bug
```

### 12.4 Bug Report Format

Each bug report must include:

| Field | Description |
|---|---|
| **Bug ID** | Unique identifier e.g. BUG_001 |
| **Test Case ID** | Which test case found this bug |
| **Feature** | Which module or feature |
| **Bug Title** | Clear one-line description |
| **Severity** | Critical / High / Medium / Low |
| **Priority** | High / Medium / Low |
| **Steps to Reproduce** | Numbered step-by-step instructions |
| **Expected Result** | What should have happened |
| **Actual Result** | What actually happened |
| **Status** | Open / In Progress / Closed etc. |
| **Screenshot** | Evidence of the bug |

---

## 13. Risks and Mitigation

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Demo environment reset by OrangeHRM | Medium | High | Re-create test data at start of each session |
| Admin credentials change | Low | High | Re-check credentials before each session |
| Demo site goes offline | Low | High | Note last tested date — resume when available |
| Internet connection interruption | Medium | Medium | Use mobile hotspot as backup |
| Power outage during testing | Medium | Medium | Use UPS device to maintain power |
| Screenshots not saved properly | Low | Medium | Verify each screenshot before moving to next test |
| Test data conflicts with other users | Medium | Medium | Use unique usernames with timestamps e.g. testuser_20260529 |

---

## 14. Deliverables

The following documents and files will be produced as part of this testing effort:

### 14.1 Test Documentation

| Deliverable | Format | Location |
|---|---|---|
| Test Plan | `.md` | `Test-Plans/` |
| Login Test Cases | `.md` | `Test-Cases/Login-Feature/` |
| Registration Test Cases | `.md` | `Test-Cases/Registration-Feature/` |
| Search Test Cases | `.md` | `Test-Cases/Search-Feature/` |
| Checkout Test Cases | `.md` | `Test-Cases/Checkout-Feature/` |
| Bug Reports | `.md` | `Bug-Reports/[Feature]-Bugs/` |
| Test Summary Reports | `.md` | `Test-Reports/` |

### 14.2 Evidence

| Deliverable | Format | Location |
|---|---|---|
| Test execution screenshots | `.png` | `Screenshots/` |
| Excel test case files | `.xlsx` | `Test-Cases/[Feature]-Feature/` |

### 14.3 GitHub Repository Structure

```
qa-manual-testing-portfolio/
│
├── README.md
├── Test-Plans/
│   └── Test_Plan_OrangeHRM.md          ← This document
├── Test-Cases/
│   ├── Login-Feature/
│   ├── Registration-Feature/
│   ├── Search-Feature/
│   └── Checkout-Feature/
├── Bug-Reports/
│   ├── Login-Bugs/
│   ├── Registration-Bugs/
│   └── UI-Bugs/
├── Test-Reports/
└── Screenshots/
```

---

## 15. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| **QA Engineer** | Bemnet Merete | Bemnet Merete | 29/05/2026 |
| **Reviewer** | — | — | — |

---

## Document History

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 29/05/2026 | Bemnet Merete | Initial version created |

---

*This test plan is a living document and will be updated as testing progresses.*
