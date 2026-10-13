# Registration — Initial Test Run

## Overview

- **Application:** OWASP Juice Shop
- **Test management tool:** Qase
- **Test suite:** Registration
- **Test run:** Registration – Initial Test Run
- **Test case range:** OJST-9–OJST-26
- **Total test cases:** 18
- **Passed:** 14 (77.8%)
- **Failed:** 4 (22.2%)
- **Execution status:** In progress
- **Source:** `exports/OJST-Registration-Initial-Test-Run.csv`

## Results Summary

The initial registration test run covered valid and invalid registration data, password validation, email validation, duplicate email handling, password advice, and navigation between registration and login.

| Metric | Result |
|---|---:|
| Total test cases | 18 |
| Passed | 14 |
| Failed | 4 |
| Pass rate | 77.8% |
| Fail rate | 22.2% |

## Failed Test Cases

| Test Case | Title | Related Defect |
|---|---|---|
| OJST-15 | Register with a password exceeding the field length limit | D-3 |
| OJST-17 | Change the password after filling in the confirmation | D-4 |
| OJST-19 | Register with an existing email address in different letter case | D-5 |
| OJST-26 | Password character counter matches the allowed limit | D-2 |

## Notes and Limitations

- OJST-26 contains steps that were not executed at the time of export. Its result should therefore be interpreted in the context of the recorded execution details.
- The reported pass and fail counts reflect the exported Qase test run and may change as execution continues.
- The behavior covered by OJST-19 requires careful interpretation: registration with an email address differing only in letter case was accepted, but duplicate-account behavior should be confirmed against the application's requirements.
- Defect references are tracked separately in the project's bug reports.

## Next Steps

- Complete the remaining test execution steps.
- Review and update test results in Qase.
- Verify defect details and evidence.
- Export the final test run and update this summary.
