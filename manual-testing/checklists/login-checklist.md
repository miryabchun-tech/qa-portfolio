# Login Checklist — SauceDemo

## Application Under Test

**Application:** SauceDemo  
**URL:** https://www.saucedemo.com/  
**Module:** Login

## Test Environment

- Browser: Google Chrome
- Operating System: Windows
- Test User: `standard_user`

---

## Login Page

- [ ] Login page is accessible
- [ ] Username field is displayed
- [ ] Password field is displayed
- [ ] Login button is displayed
- [ ] Application logo is displayed
- [ ] Username field has a clear/understandable placeholder
- [ ] Password field has a clear/understandable placeholder

---

## Username Field

- [ ] User can enter a valid username
- [ ] User can enter an invalid username
- [ ] Username field accepts text input
- [ ] Username field can be cleared
- [ ] Empty username is validated
- [ ] Required field message is displayed for empty username

---

## Password Field

- [ ] User can enter a valid password
- [ ] User can enter an invalid password
- [ ] Password field accepts text input
- [ ] Password characters are masked
- [ ] Password field can be cleared
- [ ] Empty password is validated
- [ ] Required field message is displayed for empty password

---

## Login Functionality

- [ ] Login with valid username and password
- [ ] Login with invalid username
- [ ] Login with invalid password
- [ ] Login with both fields empty
- [ ] Login with empty username
- [ ] Login with empty password
- [ ] User remains on login page after failed login
- [ ] Error message is displayed after failed login
- [ ] User can retry login after failed attempt
- [ ] Successful login redirects to Products page

---

## Error Handling

- [ ] Error message is displayed for invalid credentials
- [ ] Error message is visible to the user
- [ ] Error message does not break the page layout
- [ ] Error message disappears or updates after a new login attempt
- [ ] User can correct invalid credentials and retry

---

## UI Checks

- [ ] Login page layout is displayed correctly
- [ ] Username field is visible
- [ ] Password field is visible
- [ ] Login button is visible
- [ ] Text is readable
- [ ] Fields are aligned correctly
- [ ] No overlapping elements are visible
- [ ] Password is not displayed as plain text

---

## Final Result

**Checklist Status:** PASS

**Tested User:** `standard_user`

**Defects Found:** None during initial Login testing.

---

## Notes

The Login module was checked using positive, negative, functional, validation, and UI scenarios.

All checked scenarios behaved as expected with the `standard_user` account.
