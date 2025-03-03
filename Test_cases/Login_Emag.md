# eMAG Login Test Cases

## 1. Log in with Correct Credentials
**Test Case ID:** TC-001  
**Title:** Log in with correct credentials  
**Description:** Check if the login works when a user enters the correct credentials.  

### Steps to Reproduce:
1. Open [eMAG Login Page](https://auth.emag.ro/user/login)
2. Enter a valid email address.
3. Click the **„Continuă”** button.
4. Enter the correct password.
5. Click the **„Continuă”** button again.

### Expected Result:
- The user should be able to log in successfully and be redirected to their profile page.

### Test Data:
| Email | Password |
|--------|----------|
| ionut@email.com | 123456 |

### Pre-conditions:
- The user must have a valid eMAG account.
- The user must be logged out before starting the test.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Functional
- **Status:** Actual
- **Automation:** Manual

---

## 2. Login with SMS Verification
**Test Case ID:** TC-002  
**Title:** Login with SMS Verification  
**Description:** This test verifies that when an additional security check is triggered, the user receives an SMS verification code and must enter it to complete the login process.  

### Steps to Reproduce:
1. Follow steps 1-5 from **TC-001**.
2. The system requests additional security verification via SMS.
3. The user receives a verification code on their registered phone number.
4. Enter the received code in the verification field.
5. Click **„Confirmă”**.
6. Verify that the user is successfully logged in.

### Expected Result:
- The user enters the correct verification code and logs in successfully.

### Pre-conditions:
- The user has not logged in for a long time **OR** is logging in from a new device.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Security
- **Status:** Actual
- **Automation:** Manual

---

## 3. Verify Login with Incorrect Credentials
**Test Case ID:** TC-003  
**Title:** Verify login functionality with incorrect credentials  
**Description:** This test verifies that the system correctly handles incorrect login attempts by either redirecting the user to the account creation page or displaying an error message.  

### Steps to Reproduce:
1. Open [eMAG Login Page](https://auth.emag.ro/user/login).
2. Enter an incorrect email address.
    - If the email does not exist, the user should be redirected to the account creation page.
    - If the email exists, the user proceeds to the password entry screen.
3. If prompted for a password, enter an incorrect one.
4. Click the **„Continuă”** button.

### Expected Result:
- For a non-existent email: Redirected to account creation page with the message:
    _"Welcome! It looks like you don't have an eMAG account. Let's create a new one!"_
- For an incorrect password: Error message appears:
    _"You have entered the password or email address incorrectly. Please try again."_
- The user is not logged in.

### Pre-conditions:
- A valid eMAG account is required for testing the incorrect password scenario.

### Additional Information:
- **Severity:** Normal
- **Priority:** Medium
- **Type:** Functional
- **Status:** Actual
- **Automation:** Manual

---

## 4. Login After Multiple Failed Attempts
**Test Case ID:** TC-004  
**Title:** Login after multiple failed attempts  
**Description:** Check if the account will be temporarily blocked when a user enters the incorrect password multiple times.  

### Steps to Reproduce:
1. Open [eMAG Login Page](https://auth.emag.ro/user/login).
2. Enter the correct email.
3. Click **„Continuă”**.
4. Enter an incorrect password multiple times (e.g., 10 times).
5. Observe the system behavior.
6. Try logging in again with the correct credentials.

### Expected Result:
- The system temporarily locks the account and displays a message:  
  _"Prea multe încercări nereușite. Contul tău este blocat temporar."_
- Even with correct credentials, login is not allowed for a specific period.

### Pre-conditions:
- The user has failed multiple login attempts (e.g., 10 times).

### Additional Information:
- **Severity:** High
- **Priority:** High
- **Type:** Security
- **Status:** Actual
- **Automation:** Manual

---

## Notes
- All test cases follow industry-standard best practices.
- Each test case includes clear steps, pre-conditions, and expected results to ensure reproducibility.
- This document is structured for clarity, making it easy to integrate into a professional QA portfolio.

---

