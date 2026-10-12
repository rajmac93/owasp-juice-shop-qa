# OJST-3 — No Specific Validation Message for Invalid Email Format

## Summary
The login form accepts an email address with an invalid format and allows the form to be submitted.

## Test Environment
- Application: OWASP Juice Shop
- Test type: Manual functional testing
- Test case: OJST-3 — Login form validation for invalid email format

## Steps to Reproduce
1. Open the Login page.
2. Enter `besoj57936.pl` in the email field.
3. Enter any password.
4. Submit the form.

## Expected Result
The application prevents submission and displays a specific validation message indicating that the email address format is invalid.

## Actual Result
The form was submitted with the invalid email format `besoj57936.pl`. The application displayed `Invalid email or password.` without a specific email format validation message.

## Evidence
Screenshot: `../evidence/screenshots/OJST-3-invalid-email-format.png`

## Status
Observed behavior documented. Further confirmation against the application's requirements is needed to determine whether this is a defect.

## Qase Export
[Download defect export (CSV)](exports/OJST-2026-10-12.csv)
