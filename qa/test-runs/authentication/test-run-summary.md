# Authentication — Initial Test Run

## Overview

- **Application:** OWASP Juice Shop
- **Test management tool:** Qase
- **Test type:** Manual functional testing
- **Test suite:** Authentication
- **Test cases executed:** 8
- **Execution status:** Completed
- **Overall result:** Failed — one test case did not meet its expected result

## Scope

The test run covered authentication functionality, including:

- Login with valid credentials
- Login with an invalid password
- Email format validation
- Login with empty credentials
- Logout
- Access after logout
- Login using an unregistered email address
- Login with a password containing special characters

## Results

| Metric | Result |
|---|---:|
| Test cases executed | 8 |
| Passed | 7 |
| Failed | 1 |
| Completion rate | 100% |

## Failed Test Case

### OJST-3 — Login with invalid email format

**Observed behavior:**

The login form was submitted with the invalid email value `besoj57936.pl`. The application displayed `Invalid email or password.` without a specific email format validation message.

**Expected behavior:**

The test case expected the application to prevent submission and display a specific validation message indicating that the email address format was invalid.

**Assessment:**

The observed behavior differs from the expected result defined in the test case. Confirmation against the application's requirements is needed before classifying this behavior as a confirmed defect.

**Evidence:**

- Screenshot: `../../evidence/screenshots/OJST-3-invalid-email-format.png`
- Detailed report: `../../bug-reports/OJST-3-invalid-email-format.md`

## Observations

- Login with valid credentials was successful.
- Login with an invalid password was rejected.
- The login button remained disabled when both credential fields were empty.
- Logout completed successfully.
- Login with an unregistered email address was rejected.
- Login with a valid password containing special characters was successful.
- The test case concerning access after logout passed. Further evidence could improve the documentation of the protected functionality checked.

## Limitations

The results reflect behavior observed during this manual test run. They do not establish complete authentication coverage or confirm compliance with requirements that have not been independently verified.

## Conclusion

Seven of the eight executed test cases passed. One test case failed because the observed email validation behavior differed from its expected result.

The results and supporting evidence are documented for further review.
