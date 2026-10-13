# D-2 — Password Character Counter Displays an Incorrect Maximum

## Summary

The password character counter displays a maximum of 20 characters, although the password validation allows passwords up to 40 characters long.

## Related Test Cases

- OJST-14 — Register with a 20-character password
- OJST-26 — Password character counter matches the allowed limit

## Preconditions

- The OWASP Juice Shop application is running.
- The user is on the registration page.

## Steps to Reproduce

1. Open the registration page.
2. Enter a password containing 20 characters.
3. Observe the password character counter and the password validation message.

## Actual Result

The character counter displays `20/20`, while the password validation allows passwords between 5 and 40 characters long.

## Expected Result

The character counter should consistently reflect the maximum password length enforced by the application.

## Severity

Trivial

## Status

Open

## Evidence

Screenshot: `../evidence/screenshots/D-2-password-counter.png`

## Related Test Run

Registration — Initial Test Run
