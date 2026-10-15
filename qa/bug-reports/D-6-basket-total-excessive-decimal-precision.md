# D-6 — Basket Total Displays Excessive Decimal Precision

## Summary

The basket total displays a floating-point precision artifact instead of a monetary value formatted to two decimal places.

## Related Test Case

- OJST-32 — Verify the basket total for multiple products

## Preconditions

- The OWASP Juice Shop application is running.
- The user is logged in.
- The basket contains 2 × Apple Juice (1000ml) and 1 × Orange Juice (1000ml).

## Steps to Reproduce

1. Add Apple Juice to the basket twice.
2. Add Orange Juice to the basket once.
3. Open the basket.
4. Observe the displayed total price.

## Actual Result

The expected total was 6.97, but the application displayed `6.970000000000001`.

## Expected Result

The basket total should be displayed as `6.97`, formatted to two decimal places.

## Severity

Minor

## Status

Open

## Notes

The expected total is calculated as (2 × 1.99) + (1 × 2.99) = 6.97. The observed output is consistent with a floating-point precision artifact. This test confirms an issue with the displayed monetary value; it does not independently establish whether the underlying transaction amount is incorrect.

## Evidence

Screenshot:
- `../evidence/screenshots/D-6-basket-total-excessive-decimal-precision.png`

## Related Test Run

Basket / Cart — Initial Test Run
