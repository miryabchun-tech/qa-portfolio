# Cart Test Cases — SauceDemo

## Application Under Test

**Application:** SauceDemo  
**URL:** https://www.saucedemo.com/  
**Module:** Cart

## Test Scope

The Cart module was tested to verify:

- Adding products to the Cart
- Displaying added products
- Product names in the Cart
- Product prices in the Cart
- Adding multiple products
- Removing products from the Cart
- Cart item count
- Navigation between Products and Cart
- Continue Shopping functionality
- Proceeding from Cart to Checkout

## Testing Types

- Functional Testing
- Positive Testing
- UI Testing
- Validation Testing
- Navigation Testing

## Test Environment

- **Browser:** Google Chrome
- **Operating System:** Windows
- **Application:** SauceDemo
- **Test User:** `standard_user`

---

# Test Case Summary

| ID | Test Case | Type | Status |
|---|---|---|---|
| TC-CART-001 | Add one product to Cart | Positive / Functional | PASS |
| TC-CART-002 | Verify added product is displayed in Cart | Positive / UI | PASS |
| TC-CART-003 | Verify product name in Cart | Positive / UI | PASS |
| TC-CART-004 | Verify product price in Cart | Positive / UI | PASS |
| TC-CART-005 | Add multiple products to Cart | Positive / Functional | PASS |
| TC-CART-006 | Remove a product from Cart | Positive / Functional | PASS |
| TC-CART-007 | Verify Cart item count | Positive / Validation | PASS |
| TC-CART-008 | Navigate from Cart back to Products | Positive / Navigation | PASS |
| TC-CART-009 | Verify Continue Shopping functionality | Positive / Navigation | PASS |
| TC-CART-010 | Proceed from Cart to Checkout | Positive / Functional | PASS |

---

# Detailed Test Cases

## TC-CART-001 — Add one product to Cart

**Title:** Verify that one product can be added to the Cart

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Select any available product.
2. Click the **Add to Cart** button.
3. Click the Cart icon.

**Expected Result:**
- The selected product is added to the Cart.
- Cart page is displayed.
- The selected product is visible in the Cart.

**Actual Result:**
- The selected product was successfully added to the Cart.
- Cart page was displayed.
- The selected product was visible in the Cart.

**Status:** PASS

---

## TC-CART-002 — Verify added product is displayed in Cart

**Title:** Verify that the added product is displayed in the Cart

**Preconditions:**
- User is logged in.
- At least one product has been added to the Cart.

**Steps:**
1. Add a product to the Cart.
2. Open the Cart.
3. Observe the Cart contents.

**Expected Result:**
- The added product is displayed in the Cart.
- The product appears as a Cart item.
- Product information is visible.

**Actual Result:**
- The added product was displayed correctly.
- Product information was visible.

**Status:** PASS

---

## TC-CART-003 — Verify product name in Cart

**Title:** Verify that the correct product name is displayed in the Cart

**Preconditions:**
- User is logged in.
- A product has been added to the Cart.

**Steps:**
1. Add a product to the Cart.
2. Open the Cart.
3. Compare the product name in the Cart with the product selected on the Products page.

**Expected Result:**
- The product name in the Cart matches the selected product.
- Product name is displayed correctly and is readable.

**Actual Result:**
- The product name matched the selected product.
- The name was displayed correctly and was readable.

**Status:** PASS

---

## TC-CART-004 — Verify product price in Cart

**Title:** Verify that the correct product price is displayed in the Cart

**Preconditions:**
- User is logged in.
- A product has been added to the Cart.

**Steps:**
1. Open the Products page.
2. Note the price of a selected product.
3. Add the product to the Cart.
4. Open the Cart.
5. Compare the displayed price with the price observed on the Products page.

**Expected Result:**
- The product price in the Cart matches the product price on the Products page.
- The price is displayed correctly and is readable.

**Actual Result:**
- The product price in the Cart matched the price on the Products page.
- The price was displayed correctly.

**Status:** PASS

---

## TC-CART-005 — Add multiple products to Cart

**Title:** Verify that multiple products can be added to the Cart

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Select the first product.
2. Click **Add to Cart**.
3. Select a second product.
4. Click **Add to Cart**.
5. Open the Cart.

**Expected Result:**
- Both selected products are added to the Cart.
- Both products are displayed in the Cart.
- The Cart contains the correct number of products.

**Actual Result:**
- Both products were successfully added.
- Both products were displayed in the Cart.
- The Cart contained the correct number of products.

**Status:** PASS

---

## TC-CART-006 — Remove a product from Cart

**Title:** Verify that a product can be removed from the Cart

**Preconditions:**
- User is logged in.
- At least one product has been added to the Cart.

**Steps:**
1. Add a product to the Cart.
2. Open the Cart.
3. Click the **Remove** button for the selected product.
4. Observe the Cart.

**Expected Result:**
- The selected product is removed from the Cart.
- The product is no longer displayed.
- The Cart count is updated accordingly.

**Actual Result:**
- The selected product was successfully removed.
- The product was no longer displayed.
- The Cart count was updated.

**Status:** PASS

---

## TC-CART-007 — Verify Cart item count

**Title:** Verify that the Cart item count is updated correctly

**Preconditions:**
- User is logged in.
- Products page is open.

**Steps:**
1. Add one product to the Cart.
2. Observe the Cart icon.
3. Add another product to the Cart.
4. Observe the Cart icon again.
5. Remove one product.
6. Observe the Cart icon.

**Expected Result:**
- Cart count increases when a product is added.
- Cart count reflects the number of products currently in the Cart.
- Cart count decreases when a product is removed.

**Actual Result:**
- Cart count increased after adding products.
- Cart count reflected the selected products.
- Cart count decreased after removing a product.

**Status:** PASS

---

## TC-CART-008 — Navigate from Cart back to Products

**Title:** Verify navigation from Cart back to Products page

**Preconditions:**
- User is logged in.
- Cart page is open.

**Steps:**
1. Open the Cart.
2. Click the **Continue Shopping** button.
3. Observe the opened page.

**Expected Result:**
- User is redirected to the Products page.
- Products are displayed.
- The user can continue shopping.

**Actual Result:**
- User was successfully redirected to the Products page.
- Products were displayed.
- User was able to continue shopping.

**Status:** PASS

---

## TC-CART-009 — Verify Continue Shopping functionality

**Title:** Verify that Continue Shopping allows the user to continue shopping

**Preconditions:**
- User is logged in.
- Cart contains at least one product.

**Steps:**
1. Open the Cart.
2. Click **Continue Shopping**.
3. Select another product.
4. Click **Add to Cart**.
5. Open the Cart again.

**Expected Result:**
- User is redirected to the Products page.
- User can select another product.
- The new product can be added to the Cart.
- Previously added products remain in the Cart.

**Actual Result:**
- User was redirected to the Products page.
- Another product was successfully added.
- Previously added products remained in the Cart.

**Status:** PASS

---

## TC-CART-010 — Proceed from Cart to Checkout

**Title:** Verify navigation from Cart to Checkout

**Preconditions:**
- User is logged in.
- At least one product has been added to the Cart.

**Steps:**
1. Open the Cart.
2. Verify that the selected product is displayed.
3. Click the **Checkout** button.
4. Observe the opened page.

**Expected Result:**
- User is redirected to the Checkout page.
- Checkout information fields are displayed.
- The user can continue the checkout process.

**Actual Result:**
- User was successfully redirected to the Checkout page.
- Checkout information fields were displayed.
- The checkout process could be continued.

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

No defects were found during the initial Cart module testing with the `standard_user` account.

## Conclusion

The SauceDemo Cart module was tested using functional, positive, UI, validation, and navigation scenarios.

All 10 executed test cases passed successfully.

The tested functionality includes:

- Adding products to Cart
- Displaying products in Cart
- Product name verification
- Product price verification
- Adding multiple products
- Removing products
- Cart item count
- Navigation between Products and Cart
- Continue Shopping functionality
- Navigation to Checkout

## Next Steps

Planned testing activities:

- Checkout module test cases
- Complete checkout flow
- Checklists
- Regression testing
- Exploratory testing
- Testing with `problem_user`
- Bug reporting
