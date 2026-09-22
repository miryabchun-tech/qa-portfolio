# Regression Test Cases

## Application

SauceDemo — https://www.saucedemo.com/

## Test Type

Regression Testing

## Test Objective

Verify that the core application functionality remains stable during a simulated post-change regression cycle.

## Test Environment

- Application: SauceDemo
- Browser: Google Chrome
- Testing type: Manual
- Primary user: `standard_user`
- Password: `secret_sauce`

## Regression Scope

The regression suite covers the following critical areas:

- Login
- Products
- Product sorting
- Shopping cart
- Checkout
- Order completion
- Navigation

---

## Regression Test Cases

| ID | Test Case | Preconditions | Expected Result | Status |
|---|---|---|---|---|
| REG-001 | Login with valid credentials | User is on Login page | User is successfully logged in and Products page is displayed | PASS |
| REG-002 | Login validation with empty fields | User is on Login page | Validation message is displayed | PASS |
| REG-003 | Products page loads correctly | User is logged in | Products page is displayed without critical UI issues | PASS |
| REG-004 | Product information is displayed | User is on Products page | Product names, descriptions and prices are displayed | PASS |
| REG-005 | Product sorting works | User is on Products page | Products are reordered according to selected sorting option | PASS |
| REG-006 | Add product to cart | User is on Products page | Selected product is added to cart | PASS |
| REG-007 | Remove product from cart | Product is added to cart | Product is removed from cart | PASS |
| REG-008 | Cart badge is updated | Product is added to cart | Cart badge displays correct item count | PASS |
| REG-009 | Multiple products can be added | User is on Products page | Multiple selected products are added to cart | PASS |
| REG-010 | Cart displays correct product information | Products are added to cart | Product name and price are displayed correctly | PASS |
| REG-011 | Continue Shopping works | User is on Cart page | User is returned to Products page | PASS |
| REG-012 | Proceed to Checkout works | User has products in cart | Checkout information page is displayed | PASS |
| REG-013 | Checkout required field validation | User is on Checkout page | Required field validation messages are displayed | PASS |
| REG-014 | Checkout with valid information | User is on Checkout page | User can continue to Overview page | PASS |
| REG-015 | Checkout Overview is displayed | Valid checkout information was entered | Order overview page is displayed | PASS |
| REG-016 | Product price is displayed on Overview | User is on Overview page | Product price is displayed correctly | PASS |
| REG-017 | Order Summary is displayed | User is on Overview page | Payment and shipping information is displayed | PASS |
| REG-018 | Order can be completed | User is on Overview page | Order is successfully completed | PASS |
| REG-019 | Order confirmation is displayed | Order was completed | Confirmation message is displayed | PASS |
| REG-020 | Navigation after checkout works | Order was completed | User can navigate using available navigation controls | PASS |

---

## Regression Entry Criteria

Regression testing can start when:

- A new build or application change is available.
- Critical defects have been fixed or changes have been implemented.
- Test environment is available.
- Required test data is available.

## Regression Exit Criteria

Regression testing can be completed when:

- All critical regression test cases have been executed.
- No new critical defects are identified.
- Fixed defects are verified.
- Test results are documented.

---

## Regression Test Execution

### Execution Type

Simulated Regression Cycle

### Execution Date

2026-09-22

### Test Environment

- Application: SauceDemo
- Browser: Google Chrome
- User: `standard_user`
- Testing type: Manual Regression Testing

### Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 20 |
| Passed | 20 |
| Failed | 0 |
| Blocked | 0 |
| Not Run | 0 |

### Result

All 20 regression test cases passed successfully during the simulated regression cycle.

No new defects were identified during this test execution with `standard_user`.

### Important Note

SauceDemo is a publicly available demo application, and no new application build or release was available for this portfolio exercise.

Therefore, this regression cycle simulates a post-change regression run using the existing application.

The regression suite is designed to be executed after future application changes or defect fixes.

---

## Notes

This document represents the regression test suite for the SauceDemo application.

The test cases cover the core user flow from login to order completion.

The regression suite includes functional checks for login, products, sorting, cart, checkout, order completion, and navigation.

The simulated regression cycle was executed with `standard_user`, and all 20 test cases passed successfully.
