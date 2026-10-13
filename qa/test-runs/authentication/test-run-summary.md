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

### OJST-3 — Login form validation for invalid email format

**Execution history:**

The initial execution used the input `user@` and was marked as Passed under the original expected result, which allowed either appropriate validation feedback or login feedback. The test case was later revised to require a specific email format validation message and retested using `besoj57936.pl`.

The Passed and Failed statuses therefore reflect different expected results across the two executions.

**Latest observed behavior:**

The login form was submitted with `besoj57936.pl`. The application displayed `Invalid email or password.` without a specific email format validation message. The user remained unauthenticated.

**Assessment:**

The latest execution was marked as Failed because the observed behavior did not match the expected result defined for that execution. However, the requirement for a specific email format validation message has not been independently confirmed.

The result should therefore be treated as an observation requiring requirements clarification, rather than a confirmed application defect.

**Evidence:**

- Screenshot: `../../evidence/screenshots/D-1-invalid-email-format-on-login.png`
- Detailed report: `../../bug-reports/D-1-invalid-email-format-on-login.md`


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
