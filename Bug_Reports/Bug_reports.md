# 📌 Bug Report: Web Application Issues

---

## 🐞 Bug: Contact Form Allows Submission with Invalid or Missing Input
**Priority & Severity:** P3 - Medium

### Description:
The contact form allows submission with empty or invalid fields, including an incorrect email format.

### Steps to Reproduce:
1. Go to (https://www.demoblaze.com/)
2. Click on the "Contact" option in the header
3. In the contact form, enter any random characters in the "Contact Email" field (e.g., 123abc!@#) or leave it empty
4. Leave the "Contact Name" and "Message" fields empty
5. Click on the "Send message" button

### Expected Result:
- The form should validate the input:
  - The "Contact Email" field should only accept a valid email format (e.g., example@mail.com)
  - The "Contact Name" and "Message" fields should be required
  - The "Send Message" button should be disabled until all required fields are correctly filled

### Actual Result:
- The form allows submission even when:
  - The "Contact Email" field contains invalid characters or is empty
  - The "Contact Name" and "Message" fields are not filled
- After submission, the user receives the message: "Thanks for the message", even though the input is invalid.

---

## 🐞 Bug: Misaligned Play Button in About Us Video
**Priority & Severity:** P4 - Low

### Description:
The "About Us" section opens a small overlay with a video, but the Play button is not centered as expected. Instead, it appears misaligned in the upper-left corner of the video.

### Steps to Reproduce:
1. Go to (https://www.demoblaze.com/)
2. Click on "About Us" in the header
3. Observe the video that appears in the overlay
4. Check the position of the Play button

### Expected Result:
- The Play button should be centered in the middle of the video, following standard UI design for video playback.

### Actual Result:
- The Play button is positioned in the upper-left corner of the video instead of being centered.

---

## 🐞 Bug: "Welcome (Profile Name)" Button Not Redirecting
**Priority & Severity:** P2 - High

### Description:
The "Welcome (profile name)" button in the header does not redirect the user to the profile page when clicked, as expected.

### Steps to Reproduce:
1. Go to (https://www.demoblaze.com/)
2. Click on the "Welcome (profile name)" button in the header
3. Observe that nothing happens and the user is not redirected to the profile page

### Expected Result:
- The "Welcome (profile name)" button should redirect the user to their profile page when clicked.

### Actual Result:
- Clicking the "Welcome (profile name)" button does not redirect the user to the profile page.

---

## 🐞 Bug: No Validation Message for Negative Values in Withdrawal Field
**Priority & Severity:** P3 - Medium

### Description:
The withdrawal field allows users to enter negative values, but when clicking the "Withdraw" button, nothing happens—no transaction is processed, and no validation message is displayed.

### Steps to Reproduce:
1. Go to the Banking App login page (https://www.globalsqa.com/angularJs-protractor/BankingProject/#/login)
2. Click on "Customer Login"
3. Select any available user and log in
4. Navigate to the "Withdrawal" section
5. Enter a negative amount (e.g., -500)
6. Click the "Withdraw" button

### Expected Result:
- The system should either:
  - Display an error message (e.g., "Invalid amount. Please enter a positive value.")
  - Disable the "Withdraw" button when an invalid value is entered

### Actual Result:
- Nothing happens when clicking the "Withdraw" button after entering a negative value. There is no error message or validation feedback.

---

## 🐞 Bug: No Validation Message for Negative Values in Deposit Field
**Priority & Severity:** P3 - Medium

### Description:
The deposit field allows users to enter negative values, but when clicking the "Deposit" button, nothing happens—no transaction is processed, and no validation message is displayed.

### Steps to Reproduce:
1. Go to the Banking App login page (https://www.globalsqa.com/angularJs-protractor/BankingProject/#/login)
2. Click on "Customer Login"
3. Select any available user and log in
4. Navigate to the "Deposit" section
5. Enter a negative amount (e.g., -500)
6. Click the "Deposit" button

### Expected Result:
- The system should either:
  - Display an error message (e.g., "Invalid amount. Please enter a positive value.")
  - Disable the "Deposit" button when an invalid value is entered

### Actual Result:
- Nothing happens when clicking the "Deposit" button after entering a negative value. There is no error message or validation feedback.

---

## 🐞 Bug: Intermittent Incorrect Tar Calculation in Cigarette Consumption
**Priority & Severity:** P3 - Medium

### Description:
The total tar calculation for cigarettes sometimes displays incorrect values. When entering 4 cigarettes × 7 mg tar, the result was incorrectly calculated as 30 mg, but this does not happen consistently.

### Steps to Reproduce:
1. Go to Consumption Calculator (https://www.globalsqa.com/angularJs-protractor/ConsumptionCalculator/)
2. In the Cigarette Consumption section, enter:
  - 4 in the "Number of cigarettes" field
  - 7 mg in the "Tar per cigarette" field
3. Observe the displayed result
4. Repeat the process multiple times to check for inconsistencies

### Expected Result:
- The total tar should always be 4 × 7 mg = 28 mg

### Actual Result:
- Occasionally, the system displays an incorrect value (e.g., 30 mg).

---

## 🐞 Bug: Coffee Calculation Not Triggered When Typing Caffeine Amount
**Priority & Severity:** P3 - Medium

### Description:
When manually typing the caffeine amount in the input field, the system does not update the calculation. However, when using the up/down arrows (spinner control), the calculation works correctly.

### Steps to Reproduce:
1. Go to Consumption Calculator (https://www.globalsqa.com/angularJs-protractor/ConsumptionCalculator/)
2. In the Coffee Consumption section, enter:
  - Any valid number (e.g., 100 mg) manually in the "Caffeine per coffee" field
3. Observe that the calculation does not update
4. Use the up/down arrows (spinner control) to adjust the caffeine amount
5. Observe that the calculation updates correctly

### Expected Result:
- The total caffeine intake should be calculated immediately, whether the value is typed manually or changed using the spinner control.

### Actual Result:
- The system only updates the calculation when using the spinner control, but not when manually entering a value.

---

## 🐞 Bug: Missing Add to Cart/Buy Buttons
**Priority & Severity:** P2 - High

### Description:
The product listing page does not display any "Buy" or "Add to Cart" buttons, making it impossible for users to purchase products directly from the page.

### Steps to Reproduce:
1. Go to (https://juice-shop.herokuapp.com/#/search)
2. Observe the listed products
3. Notice that there are no options to add items to the cart or buy them

### Expected Result:
- Each product should have a "Buy" or "Add to Cart" button to allow purchases.

### Actual Result:
- There are no purchasing options visible on the product listing page.

---

## 🐞 Bug: Language Switcher Does Not Fully Update Page
**Priority & Severity:** P3 - Medium

### Description:
When changing the language using the language switcher, only a few text elements update. The product names and most interface elements remain in the original language until the page is refreshed.

### Steps to Reproduce:
1. Go to (https://juice-shop.herokuapp.com/#/search)
2. In the top-right corner, click the language switcher
3. Select English (or any other language)
4. Observe that only some text updates (e.g., labels like "Only 2 left!")
5. Refresh the page
6. Notice that now all text updates correctly

### Expected Result:
- When switching the language, all text should update immediately, without needing a page refresh.

### Actual Result:
- Only some UI elements change language immediately, while others stay in the original language until the page is refreshed.

---

