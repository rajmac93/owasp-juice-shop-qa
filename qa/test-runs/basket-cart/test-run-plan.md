# Basket / Cart — Test Run Plan

## Purpose

Document the scope and preparation for the initial manual test run of the Basket / Cart functionality in OWASP Juice Shop.

**Execution status:** Planned / in progress in Qase. Test results have not yet been recorded in this repository.

## Test suite

- **Qase project:** OWASP Juice Shop Testing (`OJST`)
- **Suite:** Basket / Cart
- **Qase suite ID:** `3`
- **Test run:** Basket / Cart – Initial Test Run
- **Test cases:** `OJST-27`–`OJST-37` (11 cases)

## Scope

The run covers the following scenarios:

| Qase ID | Test case | Focus |
|---|---|---|
| OJST-27 | Add a product to the basket | Adding one product |
| OJST-28 | Add multiple products to the basket | Adding two different products |
| OJST-29 | Increase the quantity of a product in the basket | Quantity and recalculated amounts |
| OJST-30 | Decrease the quantity of a product in the basket | Quantity and recalculated amounts |
| OJST-31 | Remove a product from the basket | Removing an item and recalculating the total |
| OJST-32 | Verify the basket total for multiple products | Independent calculation of the total |
| OJST-33 | Basket contents persist after logout and re-login | Basket state across authentication |
| OJST-34 | Verify basket contents after refreshing the page | Basket state after refresh |
| OJST-35 | Add the same product twice | Repeated addition of one product |
| OJST-36 | Decrease the quantity of a product with quantity 1 | Behaviour at the minimum quantity |
| OJST-37 | Access the basket without logging in | Basket behaviour for a logged-out user |

Known intentional Juice Shop challenges, such as viewing or manipulating another user's basket and negative quantities, are out of scope for this functional run and must not automatically be reported as functional defects.

## Test environment and data

- Application: OWASP Juice Shop, running locally.
- Base URL: `http://localhost:3000`
- Test approach: manual UI testing.
- Browser: Firefox (record the actual version if relevant).
- Test account: use a dedicated account created for this suite; do not record its password in this document or in screenshots.
- Product A: Apple Juice (1000ml).
- Product B: Orange Juice (1000ml).
- Record the catalogue prices of Product A and Product B before execution.
- Compare displayed monetary amounts to two decimal places, as shown by the application.

## Execution notes

1. Start from the precondition stated in each Qase test case. Clear or prepare the basket when necessary so that previous cases do not affect the result.
2. Record the actual outcome in the Qase test run. Do not mark a case as Passed or Failed before executing it.
3. Capture screenshots for unexpected results and defects. Avoid including passwords, session tokens, or other secrets in evidence.
4. For OJST-29, confirm whether the basket's `Price` column shows a unit price or a line amount before finalising the expected result.
5. For OJST-35, observe whether adding the same product twice produces one row with quantity 2 or separate rows, and record the basket indicator behaviour.
6. For OJST-36, observe what happens when decreasing an item at quantity 1. Do not assume whether the item is removed or the control is disabled until verified.
7. For OJST-37, observe the actual behaviour when adding a product and opening the basket while logged out.
8. For OJST-33 and OJST-34, treat persistence as the expectation under test; record what the application actually does before deciding whether the result is a defect.

## Results and reporting

Execution results and defect reports will be added after the manual run is completed. This plan does not assert that any of the test cases have passed or failed.

Suggested supporting artefacts after execution:

- Qase test-run export for **Basket / Cart – Initial Test Run**.
- Screenshots for failed or otherwise noteworthy results.
- Defect reports for reproducible behaviour that conflicts with a confirmed expected result.

## Current status

- [x] Basket / Cart suite prepared in Qase.
- [x] Initial test run created in Qase.
- [ ] Execute the 11 test cases.
- [ ] Export the completed test run.
- [ ] Add the results summary and evidence references.
- [ ] Document any confirmed defects.
