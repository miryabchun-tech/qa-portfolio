# Login Test Cases — SauceDemo

## Application Under Test

**Application:** SauceDemo  
**URL:** https://www.saucedemo.com/  
**Module:** Login

## Test Scope

The Login module was tested to verify:

- Login with valid credentials
- Login with invalid credentials
- Required field validation
- Username and password input fields
- Password masking
- Error message handling
- Retry login after a failed attempt

## Testing Types

- Functional Testing
- Positive Testing
- Negative Testing
- Validation Testing
- UI Testing

## Test Environment

- **Browser:** Google Chrome
- **Operating System:** Windows
- **Application:** SauceDemo
- **Test User:** `standard_user`
- **Password:** `secret_sauce`

---

## Test Case Summary

| ID | Test Case | Type | Status |
|---|---|---|---|
| TC-LOGIN-001 | Login with valid credentials | Positive / Functional | PASS |
| TC-LOGIN-002 | Login with invalid password | Negative / Functional | PASS |
| TC-LOGIN-003 | Login with invalid username | Negative / Functional | PASS |
| TC-LOGIN-004 | Login with empty username | Negative / Validation | PASS |
| TC-LOGIN-005 | Login with empty password | Negative / Validation | PASS |
| TC-LOGIN-006 | Login with both fields empty | Negative / Validation | PASS |
| TC-LOGIN-007 | Enter text into username and password fields | Positive / UI | PASS |
| TC-LOGIN-008 | Verify password masking | Positive / UI | PASS |
| TC-LOGIN-009 | Verify error message after failed login | Negative / Functional | PASS |
| TC-LOGIN-010 | Retry login after failed attempt | Positive / Functional | PASS |

---

# Detailed Test Cases

## TC-LOGIN-001 — Login with valid credentials

**Title:** Verify successful login with valid credentials

**Preconditions:**
- User is on the SauceDemo login page.
- Valid test credentials are available.

**Test Data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Enter `standard_user` into the Username field.
3. Enter `secret_sauce` into the Password field.
4. Click the **Login** button.

**Expected Result:**
- User is successfully logged in.
- Products page is displayed.

**Actual Result:**
- User was successfully logged in.
- Products page was displayed.

**Status:** PASS

---

## TC-LOGIN-002 — Login with invalid password

**Title:** Verify login behavior with an invalid password

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `wrong_password`

**Steps:**
1. Open the SauceDemo login page.
2. Enter `standard_user` into the Username field.
3. Enter an incorrect password.
4. Click the **Login** button.

**Expected Result:**
- Login is unsuccessful.
- An appropriate error message is displayed.
- User remains on the login page.

**Actual Result:**
- Login was unsuccessful.
- An error message was displayed.
- User remained on the login page.

**Status:** PASS

---

## TC-LOGIN-003 — Login with invalid username

**Title:** Verify login behavior with an invalid username

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `wrong_user`
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Enter an incorrect username.
3. Enter `secret_sauce` into the Password field.
4. Click the **Login** button.

**Expected Result:**
- Login is unsuccessful.
- An appropriate error message is displayed.
- User remains on the login page.

**Actual Result:**
- Login was unsuccessful.
- An error message was displayed.
- User remained on the login page.

**Status:** PASS

---

## TC-LOGIN-004 — Login with empty username

**Title:** Verify validation when Username field is empty

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: empty
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Leave the Username field empty.
3. Enter `secret_sauce` into the Password field.
4. Click the **Login** button.

**Expected Result:**
- Login is unsuccessful.
- A validation message indicating that the Username field is required is displayed.

**Actual Result:**
- Login was unsuccessful.
- A required-field validation message was displayed for Username.

**Status:** PASS

---

## TC-LOGIN-005 — Login with empty password

**Title:** Verify validation when Password field is empty

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: empty

**Steps:**
1. Open the SauceDemo login page.
2. Enter `standard_user` into the Username field.
3. Leave the Password field empty.
4. Click the **Login** button.

**Expected Result:**
- Login is unsuccessful.
- A validation message indicating that the Password field is required is displayed.

**Actual Result:**
- Login was unsuccessful.
- A required-field validation message was displayed for Password.

**Status:** PASS

---

## TC-LOGIN-006 — Login with both fields empty

**Title:** Verify validation when both Username and Password fields are empty

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: empty
- Password: empty

**Steps:**
1. Open the SauceDemo login page.
2. Leave the Username field empty.
3. Leave the Password field empty.
4. Click the **Login** button.

**Expected Result:**
- Login is unsuccessful.
- A validation message is displayed.
- The system identifies the required Username field first.

**Actual Result:**
- Login was unsuccessful.
- The Username required-field message was displayed first.

**Status:** PASS

**Note:**
- The application validates the Username field before the Password field when both fields are empty.

---

## TC-LOGIN-007 — Enter text into username and password fields

**Title:** Verify that users can enter text into Username and Password fields

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Click the Username field.
3. Enter `standard_user`.
4. Click the Password field.
5. Enter `secret_sauce`.

**Expected Result:**
- Text can be entered into both fields.
- Entered username is displayed in the Username field.
- Password characters are accepted in the Password field.

**Actual Result:**
- Text was successfully entered into both fields.
- Username was displayed correctly.
- Password was accepted by the Password field.

**Status:** PASS

---

## TC-LOGIN-008 — Verify password masking

**Title:** Verify that the password is masked during input

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Click the Password field.
3. Enter `secret_sauce`.
4. Observe the password field.

**Expected Result:**
- Password characters are masked.
- The actual password value is not displayed as plain text.

**Actual Result:**
- Password characters were masked.
- The password was not displayed as plain text.

**Status:** PASS

---

## TC-LOGIN-009 — Verify error message after failed login

**Title:** Verify that an appropriate error message is displayed after failed login

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `wrong_password`

**Steps:**
1. Open the SauceDemo login page.
2. Enter `standard_user` into the Username field.
3. Enter an incorrect password.
4. Click the **Login** button.
5. Observe the error message.

**Expected Result:**
- Login attempt fails.
- An error message is displayed.
- The error message is visible to the user.

**Actual Result:**
- Login attempt failed.
- An error message was displayed and was visible to the user.

**Status:** PASS

---

## TC-LOGIN-010 — Retry login after failed attempt

**Title:** Verify that the user can successfully retry login after a failed attempt

**Preconditions:**
- User is on the SauceDemo login page.

**Test Data:**

First attempt:
- Username: `standard_user`
- Password: `wrong_password`

Second attempt:
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Open the SauceDemo login page.
2. Enter `standard_user`.
3. Enter an incorrect password.
4. Click the **Login** button.
5. Verify that an error message is displayed.
6. Replace the incorrect password with `secret_sauce`.
7. Click the **Login** button again.

**Expected Result:**
- The first login attempt fails.
- An error message is displayed.
- The user can correct the password.
- The second login attempt is successful.
- The Products page is displayed.

**Actual Result:**
- The first login attempt failed as expected.
- An error message was displayed.
- The password was corrected.
- The second login attempt was successful.
- The Products page was displayed.

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

No defects were found during the initial Login module testing with the `standard_user` account.

## Conclusion

The SauceDemo Login module was tested using positive, negative, validation, functional, and UI scenarios.

All 10 executed test cases passed successfully.

The tested functionality includes:

- Successful login
- Invalid username handling
- Invalid password handling
- Required field validation
- Empty field validation
- Username and password input
- Password masking
- Error message display
- Retry after failed login

## Next Steps

Planned testing activities:

- Products module test cases
- Cart module test cases
- Checkout module test cases
- Login checklist
- Regression testing
- Exploratory testing
- Testing with additional SauceDemo users
