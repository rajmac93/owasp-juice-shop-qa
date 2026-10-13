# D-5 — Registration Accepts an Email Address Differing Only by Letter Case

## Summary

The registration form accepts an email address that differs from an existing address only in letter case.

## Related Test Case

- OJST-19 — Register with an existing email address in different letter case

## Preconditions

- The OWASP Juice Shop application is running.
- An account using `admin@juice-sh.op` is assumed to exist.

## Steps to Reproduce

1. Open the registration page.
2. Enter `ADMIN@juice-sh.op` as the email address.
3. Complete the remaining required fields with valid values.
4. Submit the registration form.
5. Observe the registration result.

## Actual Result

Registration using `ADMIN@juice-sh.op` succeeds, and the application displays the registration completion challenge.

## Expected Result

If email addresses are intended to be unique regardless of letter case, registration should reject an address that differs from an existing account's email address only by letter case.

## Severity

Major

## Status

Open

## Notes

The expected behavior regarding email address case sensitivity should be confirmed against the application's requirements. The existence and accessibility of the account using the lowercase address were not independently verified during this test.

## Evidence

Screenshots:
- Registration: `../evidence/screenshots/D-5-registration-uppercase-email.png`
- Login attempt: `../evidence/screenshots/D-5-login-lowercase-email.png`

## Related Test Run

Registration — Initial Test Run
