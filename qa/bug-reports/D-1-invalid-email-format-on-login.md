# D-1 — No Specific Validation Message for Invalid Email Format on Login

## Summary

When an invalid email address is submitted on the login form, the application displays a generic authentication error instead of a specific email format validation message.

## Test Environment

- Application: OWASP Juice Shop
- Test type: Manual functional testing
- Related test case: OJST-3 — Login form validation for invalid email format

## Steps to Reproduce

1. Open the Login page.
2. Enter `besoj57936.pl` in the email field.
3. Enter any password.
4. Submit the form.

## Expected Result

If specific email format validation is required, the application should display a clear validation message indicating that the email address format is invalid.

## Actual Result

The form was submitted with the invalid email format `besoj57936.pl`. The application displayed `Invalid email or password.` without a specific email format validation message.

## Evidence

Screenshot: `../evidence/screenshots/D-1-invalid-email-format-on-login.png`

## Status

Observed behavior documented. Further confirmation against the application's requirements is needed to determine whether this is a defect.

## Related Test Run

Authentication — Initial Test Run

## Qase Export

The defect export is available at `exports/OJST-2026-10-13.csv`.
