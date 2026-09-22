# Test Plan — SauceDemo

## 1. Test Plan Overview

This test plan describes the manual testing activities for the SauceDemo web application.

The purpose of testing is to verify the main user flows, identify defects, and document test results.

---

## 2. Test Objectives

The main objectives are:

- Verify the Login functionality
- Verify the Products page
- Verify product sorting
- Verify Add to Cart functionality
- Verify Cart functionality
- Verify Checkout functionality
- Verify order completion
- Verify input validation
- Verify navigation between pages
- Identify and document defects

---

## 3. Scope

### In Scope

The following features will be tested:

- Login
- Products
- Product sorting
- Add to Cart
- Remove from Cart
- Cart
- Checkout
- Order completion
- Form validation
- Error messages
- Navigation
- Basic UI behavior

### Out of Scope

The following areas are not part of this test cycle:

- Performance testing
- Security testing
- Accessibility testing
- Database testing
- Mobile application testing

API testing will be performed separately.

---

## 4. Test Environment

### Application

SauceDemo

### Platform

Web application

### Browser

Google Chrome

### Test Users

The following users will be used:

- `standard_user`
- `problem_user`

Additional special users may be used during exploratory testing.

---

## 5. Test Data

### Login

Username:

`standard_user`

Password:

`secret_sauce`

### Checkout

First Name:

`Ivan`

Last Name:

`Tester`

ZIP/Postal Code:

`21000`

Invalid and empty values will also be used for validation testing.

---

## 6. Testing Types

The following testing types will be performed:

- Functional Testing
- Positive Testing
- Negative Testing
- Validation Testing
- UI Testing
- Navigation Testing
- End-to-End Testing
- Exploratory Testing

Regression testing will be performed separately after the initial testing cycle.

---

## 7. Test Documentation

The following documentation will be used:

### Test Cases

Location:

`manual-testing/test-cases/`

Test cases cover:

- Login
- Products
- Cart
- Checkout

### Checklists

Location:

`manual-testing/checklists/`

Checklists cover:

- Login
- Products
- Cart
- Checkout

### Bug Reports

Location:

`manual-testing/bug-reports/`

Observed defects will be documented using individual bug reports.

---

## 8. Test Execution

Testing will be performed manually.

The initial test cycle uses `standard_user` to verify the expected application flow.

Special test users will then be used for exploratory testing and defect identification.

Test results will be recorded in the corresponding test cases and checklists.

---

## 9. Defect Management

When a defect is identified, a bug report will be created.

Each bug report should contain:

- Bug ID
- Title
- Environment
- Preconditions
- Steps to Reproduce
- Actual Result
- Expected Result
- Severity
- Priority
- Status

Only defects that are actually observed and reproducible will be documented.

---

## 10. Entry Criteria

Testing can start when:

- The application is accessible
- The test environment is available
- Test users are available
- Test data is prepared
- Test cases and checklists are available

---

## 11. Exit Criteria

The test cycle can be considered complete when:

- Planned test cases have been executed
- Checklists have been completed
- Identified defects have been documented
- Main user flows have been verified
- Test results have been recorded

---

## 12. Test Deliverables

The expected deliverables are:

- Test Plan
- Test Cases
- Checklists
- Bug Reports
- Regression Test Documentation
- Test Results

---

## 13. Risks

Potential risks include:

- Application availability issues
- Browser-specific behavior
- Test environment changes
- Limited test data
- Defects outside the current testing scope

---

## 14. Current Test Status

Initial testing with `standard_user` has been completed for:

- Login
- Products
- Cart
- Checkout

The initial test cases and checklists passed without identified defects.

The next testing phase will focus on special users and exploratory testing to identify potential defects.
