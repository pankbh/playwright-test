# Test Plan for Login Functionality

## Objective
To ensure the login functionality of the web application at https://practicetestautomation.com/practice-test-login/ works as expected under various conditions.

## Positive Test Cases

### Test Case 1: Valid Login
- **Steps:**
  1. Navigate to the login page.
  2. Enter a valid username.
  3. Enter a valid password.
  4. Click the submit button.
- **Expected Result:**
  - User is successfully logged in and redirected to the dashboard/home page.

### Test Case 2: Logout
- **Steps:**
  1. Log in with valid credentials.
  2. Click the logout button.
- **Expected Result:**
  - User is logged out and redirected to the login page.

## Negative Test Cases

### Test Case 3: Invalid Username
- **Steps:**
  1. Navigate to the login page.
  2. Enter an invalid username.
  3. Enter a valid password.
  4. Click the submit button.
- **Expected Result:**
  - An error message is displayed: "Invalid username or password."

### Test Case 4: Invalid Password
- **Steps:**
  1. Navigate to the login page.
  2. Enter a valid username.
  3. Enter an invalid password.
  4. Click the submit button.
- **Expected Result:**
  - An error message is displayed: "Invalid username or password."

### Test Case 5: Empty Fields
- **Steps:**
  1. Navigate to the login page.
  2. Leave the username and password fields empty.
  3. Click the submit button.
- **Expected Result:**
  - An error message is displayed: "Username and password are required."

## Edge Cases

### Test Case 6: SQL Injection Attempt
- **Steps:**
  1. Navigate to the login page.
  2. Enter a SQL injection string (e.g., `" OR "1"="1`) in the username or password field.
  3. Click the submit button.
- **Expected Result:**
  - The application does not log in and displays an error message: "Invalid username or password."

### Test Case 7: Long Username and Password
- **Steps:**
  1. Navigate to the login page.
  2. Enter a username and password exceeding the maximum allowed length (e.g., 256 characters).
  3. Click the submit button.
- **Expected Result:**
  - An error message is displayed: "Username or password is too long."

## Usability Considerations

### Test Case 8: Password Masking
- **Steps:**
  1. Navigate to the login page.
  2. Enter a password in the password field.
- **Expected Result:**
  - The password is masked (e.g., displayed as dots or asterisks).

### Test Case 9: Responsive Design
- **Steps:**
  1. Navigate to the login page on different devices (desktop, tablet, mobile).
- **Expected Result:**
  - The login page is displayed correctly and is fully functional on all devices.

### Test Case 10: Accessibility
- **Steps:**
  1. Navigate to the login page.
  2. Use a screen reader to interact with the page.
- **Expected Result:**
  - All elements are accessible and properly labeled for screen readers.
