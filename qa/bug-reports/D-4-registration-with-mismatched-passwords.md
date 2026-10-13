# D-4 — Registration Succeeds After Password Confirmation Becomes Mismatched

## Summary

The registration form allows account creation after the Password field is changed without updating the previously entered Repeat Password value.

## Related Test Case

- OJST-17 — Change the password after filling in the confirmation

## Preconditions

- The OWASP Juice Shop application is running.
- The user is on the registration page.

## Steps to Reproduce

1. Open the registration page.
2. Enter a valid email address.
3. Enter a valid password.
4. Enter the same value in the Repeat Password field.
5. Change the Password field to a different valid password without updating Repeat Password.
6. Submit the registration form.

## Actual Result

The form allows registration to succeed even though the Password and Repeat Password values no longer match. The application displays the registration completion challenge.

## Expected Result

The form should detect the mismatch after the Password field changes, display a validation message, and prevent registration until both password values match.

## Severity

Major

## Status

Open

## Evidence

Screenshot: `../evidence/screenshots/D-4-password-confirmation-mismatch.png`

## Related Test Run

Registration — Initial Test Run
