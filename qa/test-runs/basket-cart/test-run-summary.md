# Basket / Cart — Initial Test Run

## Overview

- **Application:** OWASP Juice Shop
- **Test management tool:** Qase
- **Test suite:** Basket / Cart
- **Test run:** Basket / Cart – Initial Test Run
- **Test case range:** OJST-27–OJST-37
- **Total test cases:** 11
- **Passed:** 10 (90.9%)
- **Failed:** 1 (9.1%)
- **Execution status:** Completed
- **Source:** `exports/OJST-Basket-Cart-Initial-Test-Run.csv`

## Results Summary

The initial Basket / Cart test run covered adding products to the basket, updating quantities, removing products, calculating the basket total, preserving basket contents after logout and re-login, refreshing the page, adding the same product more than once, decreasing the quantity at its minimum value, and accessing the basket without logging in.

| Metric | Result |
|---|---:|
| Total test cases | 11 |
| Passed | 10 |
| Failed | 1 |
| Pass rate | 90.9% |
| Fail rate | 9.1% |

## Failed Test Cases

| Test Case | Title | Related Defect |
|---|---|---|
| OJST-32 | Verify the basket total for multiple products | D-6 |

## Notes and Limitations

- OJST-32 failed because the basket total was displayed as `6.970000000000001` instead of `6.97`.
- D-6 documents the excessive decimal precision observed in the displayed basket total. The test does not independently establish whether the underlying transaction amount is incorrect.
- OJST-36 recorded that the quantity remained at 1 after the decrease control was clicked. The test was marked as Passed in Qase; this behavior is retained as an observation and is not reported as a confirmed defect.
- OJST-37 confirmed that the product could be added to the basket and the basket opened without logging in. This behavior was recorded as observed and was not automatically treated as a defect.
- Results reflect the exported Qase test run.

## Evidence and Defects

- **Defect:** `D-6-basket-total-excessive-decimal-precision.md`
- **Screenshot:** `../../evidence/screenshots/D-6-basket-total-excessive-decimal-precision.png`
- **Defect export:** `../../bug-reports/exports/OJST-2026-10-15.csv`

## Next Steps

- Review the recorded results and defect in Qase.
- Investigate the basket total formatting issue.
- Keep the test run export and evidence synchronized with the repository.
