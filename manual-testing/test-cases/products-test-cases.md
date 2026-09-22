# Products Test Cases — SauceDemo

## Application Under Test

**Application:** SauceDemo  
**URL:** https://www.saucedemo.com/  
**Module:** Products

## Test Scope

The Products module was tested to verify:

- Products page availability
- Product list display
- Product names
- Product descriptions
- Product prices
- Product images
- Add to Cart functionality
- Remove from Cart functionality
- Sort functionality
- Navigation to Cart
- Navigation menu

## Testing Types

- Functional Testing
- Positive Testing
- Negative Testing
- UI Testing
- Validation Testing

## Test Environment

- **Browser:** Google Chrome
- **Operating System:** Windows
- **Application:** SauceDemo
- **Test User:** `standard_user`

---

# Test Case Summary

| ID | Test Case | Type | Status |
|---|---|---|---|
| TC-PRODUCTS-001 | Verify Products page is displayed after login | Positive / Functional | PASS |
| TC-PRODUCTS-002 | Verify products are displayed | Positive / UI | PASS |
| TC-PRODUCTS-003 | Verify product names are displayed | Positive / UI | PASS |
| TC-PRODUCTS-004 | Verify product descriptions are displayed | Positive / UI | PASS |
| TC-PRODUCTS-005 | Verify product prices are displayed | Positive / UI | PASS |
| TC-PRODUCTS-006 | Verify product images are displayed | Positive / UI | PASS |
| TC-PRODUCTS-007 | Add a product to Cart | Positive / Functional | PASS |
| TC-PRODUCTS-008 | Remove a product from Cart | Positive / Functional | PASS |
| TC-PRODUCTS-009 | Sort products | Positive / Functional | PASS |
| TC-PRODUCTS-010 | Navigate to Cart from Products page | Positive / Functional | PASS |

---

# Detailed Test Cases

## TC-PRODUCTS-001 — Verify Products page is displayed after login

**Title:** Verify that the Products page is displayed after successful login

**Preconditions:**
- User is on the SauceDemo login page.
- Valid credentials are available.

**Test Data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Enter `standard_user` into the Username field.
2. Enter `secret_sauce` into the Password field.
3. Click the **Login** button.

**Expected Result:**
- User is successfully logged in.
- Products page is displayed.
- Products are visible to the user.

**Actual Result:**
- User was successfully logged in.
- Products page was displayed.
- Products were visible.

**Status:** PASS

---

## TC-PRODUCTS-002 — Verify products are displayed

**Title:** Verify that products are displayed on the Products page

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Observe the product list.

**Expected Result:**
- Product items are displayed.
- Each product is presented as a separate product item.
- Product information is visible.

**Actual Result:**
- Product items were displayed correctly.
- Product information was visible.

**Status:** PASS

---

## TC-PRODUCTS-003 — Verify product names are displayed

**Title:** Verify that product names are displayed correctly

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Observe the product cards.
3. Check the product names.

**Expected Result:**
- Each product has a visible product name.
- Product names are readable.
- Product names are associated with the correct product.

**Actual Result:**
- Product names were displayed correctly.
- Names were readable and associated with the products.

**Status:** PASS

---

## TC-PRODUCTS-004 — Verify product descriptions are displayed

**Title:** Verify that product descriptions are displayed

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Observe the product cards.
3. Check the product descriptions.

**Expected Result:**
- Product descriptions are displayed.
- Descriptions are readable.
- Descriptions are associated with the corresponding products.

**Actual Result:**
- Product descriptions were displayed correctly.
- Descriptions were readable and associated with the corresponding products.

**Status:** PASS

---

## TC-PRODUCTS-005 — Verify product prices are displayed

**Title:** Verify that product prices are displayed

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Observe the product cards.
3. Check the displayed prices.

**Expected Result:**
- Each product has a visible price.
- Prices are displayed in a consistent format.
- Prices are readable.

**Actual Result:**
- Product prices were displayed correctly.
- Prices were readable and consistently formatted.

**Status:** PASS

---

## TC-PRODUCTS-006 — Verify product images are displayed

**Title:** Verify that product images are displayed correctly

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Observe the product images.
3. Check that images are displayed for the products.

**Expected Result:**
- Product images are displayed.
- Images are visible.
- Images correspond to the displayed products.

**Actual Result:**
- Product images were displayed correctly.
- Images were visible and corresponded to the products.

**Status:** PASS

---

## TC-PRODUCTS-007 — Add a product to Cart

**Title:** Verify that a product can be added to the Cart

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Select any available product.
2. Click the **Add to Cart** button.
3. Observe the Cart icon.

**Expected Result:**
- The selected product is added to the Cart.
- The Cart icon reflects the added item.
- The button state changes appropriately.

**Actual Result:**
- The selected product was successfully added to the Cart.
- The Cart icon reflected the added item.
- The button state changed appropriately.

**Status:** PASS

---

## TC-PRODUCTS-008 — Remove a product from Cart

**Title:** Verify that a product can be removed from the Cart

**Preconditions:**
- User is logged in.
- A product has been added to the Cart.

**Steps:**
1. Add a product to the Cart.
2. Click the **Remove** button for the selected product.
3. Observe the product and Cart icon.

**Expected Result:**
- The selected product is removed from the Cart.
- The Cart count is updated.
- The product is no longer selected for purchase.

**Actual Result:**
- The product was successfully removed.
- The Cart count was updated accordingly.

**Status:** PASS

---

## TC-PRODUCTS-009 — Sort products

**Title:** Verify that products can be sorted

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the product sorting dropdown.
2. Select a sorting option.
3. Observe the product list.
4. Repeat with another available sorting option.

**Expected Result:**
- The sorting dropdown is available.
- Products are reordered according to the selected sorting option.
- The selected sorting option remains displayed.

**Actual Result:**
- The sorting dropdown was available.
- Products were reordered according to the selected option.
- The selected option was displayed correctly.

**Status:** PASS

---

## TC-PRODUCTS-010 — Navigate to Cart from Products page

**Title:** Verify navigation from Products page to Cart

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Open the Products page.
2. Click the **Cart** icon.
3. Observe the opened page.

**Expected Result:**
- User is redirected to the Cart page.
- Cart page is displayed.
- Previously added products are displayed in the Cart.

**Actual Result:**
- User was successfully redirected to the Cart page.
- Cart page was displayed.
- Added products were displayed correctly.

**Status:** PASS

---

# Test Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 10 |
| Passed | 10 |
| Failed | 0 |
| Blocked | 0 |

## Defects Found

No defects were found during the initial Products module testing with the `standard_user` account.

## Conclusion

The SauceDemo Products module was tested using functional, positive, negative, UI, and validation scenarios.

All 10 executed test cases passed successfully.

The tested functionality includes:

- Products page display
- Product information
- Product names
- Product descriptions
- Product prices
- Product images
- Add to Cart functionality
- Remove functionality
- Product sorting
- Navigation to Cart

## Next Steps

Planned testing activities:

- Cart module test cases
- Checkout module test cases
- Checklists
- Regression testing
- Exploratory testing
- Additional user scenarios
