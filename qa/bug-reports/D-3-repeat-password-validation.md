# D-3 — Repeat Password Field Accepts 41 Characters Without Validation

## Summary

The Repeat Password field accepts a 41-character value without displaying a corresponding validation error, although the password length limit is 40 characters.

## Related Test Case

- OJST-15 — Register with a password exceeding the field length limit

## Preconditions

- The OWASP Juice Shop application is running.
- The user is on the registration page.

## Steps to Reproduce

1. Open the registration page.
2. Enter a 41-character password in the Password field.
3. Enter the same 41-character value in the Repeat Password field.
4. Observe the validation messages and character counters.

## Actual Result

The Password field displays a validation message indicating that the password must be between 5 and 40 characters long. The Repeat Password field accepts the 41-character value and displays a counter of `41/40` without a corresponding validation error.

## Expected Result

The Repeat Password field should consistently validate the password length limit and clearly indicate when the entered value exceeds the allowed maximum.

## Severity

Minor

## Status

Open

## Evidence

Screenshot: `../evidence/screenshots/D-3-repeat-password-validation.png`

## Related Test Run

Registration — Initial Test Run
