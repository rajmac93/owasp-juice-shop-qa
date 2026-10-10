# Test Plan — OWASP Juice Shop

## 1. Project Overview

**Project:** OWASP Juice Shop — Manual QA Testing  
**Application Under Test:** OWASP Juice Shop  
**Testing Type:** Manual Web Application Testing  
**Project Status:** In Progress

This project aims to demonstrate a structured QA workflow through
test planning, test design, manual test execution, defect reporting,
and regression testing.

The application is intentionally vulnerable and is used here as a
local educational testing environment.

## 2. Test Objectives

The objectives of this project are to:

- Check the core user workflows that have been selected.
- Check form validation and how errors are handled.
- Find unexpected problems with how something works.
- Carry out positive, negative, and boundary testing.
- Record test results and the evidence that supports them.
- Make sure that defect reports are clear and can be reproduced.
Look at the security-related behaviours in the local environment.

## 3. Scope

### 3.1 In Scope

The initial functional testing scope includes:

- Registration of users and verification of their identities.
- The product catalog and the ability to search for products.
- Shopping cart operations.
- Checkout workflow.
Form checks and error messages.
- The navigation features and certain aspects of the user interface.

Additional activities may include:

- Exploratory testing.
- Regression testing.
- Selected API testing.
- Carrying out security testing on the local application under control.

### 3.2 Not included

The initial phase excludes:

- Conducting load and performance testing.
- Testing the production systems or those of unrelated third-party services.
- Automated test implementation.
- Formal compliance certification.
- Carrying out testing outside the approved local environment.

The scope could be changed as the project progresses.

## 4. Test Approach

The testing will be carried out manually on a risk-based basis.

The following techniques will be considered:

- When carrying out positive testing, you check that the expected behaviour occurs with valid inputs.
- Negative testing involves checking a system's behaviour using invalid or unexpected inputs.
- Boundary value analysis involves checking the values at and around the relevant limits.
- Equivalence partitioning involves dividing the inputs into groups consisting of those expected to behave in the same way.
- Exploratory testing involves looking into the behaviour of the application beyond the predefined steps.
- Regression testing involves rechecking certain behaviours after modifications have been made.

The test cases will specify the preconditions, the test data, the steps, and the expected results.

Actual results and execution statuses will be recorded only after
The appropriate tests have been carried out.

## 5. Test Environment

The initial test environment is documented in:

`qa/documentation/test-environment.md`

The application runs locally using Docker and is accessed at:

`http://localhost:3000`

The documented application version and Docker image digest will be
served as the starting point for the environment baseline.

## 6. Entry Criteria

Testing may begin when:

- The application for that area is available.
- It is possible to access the target workflow.
The data needed for the test is either already available or can be obtained.
The team has looked over the test cases that matter.
The test environment is written down.

There may be extra conditions attached to individual tests.

## 7. Exit Criteria

The initial test cycle may be considered complete when:

- Planned test cases have been executed or explicitly marked as blocked
  or not run.
The real results have been recorded.
We have looked over the failed tests.
- The defects in question have been recorded where suitable.
Relevant evidence has been saved.
The various risks and limitations have been summed up.

Just because the application has been completed doesn't mean that it is free from defects.

## 8. Defect Reporting

A defect report should include, where applicable:

- Unique defect identifier.
- A title that is clear and to the point.
- Environment and preconditions.
- Steps to reproduce.
- Expected result.
- Actual result.
- Severity and priority.
- Supporting evidence.
- Current status.

Functional defects will be distinguished from intentionally vulnerable
problems relating to behavior and educational security.

## 9. Risks and Limitations

- The application has deliberately included security vulnerabilities.
The behaviour of the application can vary from one version to another.
-The first scope includes only certain workflows.
It cannot be guaranteed that manual testing will find all the defects.
- Evidence may contain sensitive data and must be reviewed before
  being published.
- The Docker image tag `latest` is mutable; the recorded digest
  Gives a more exact reference to the image that was tested.

## 10. Test Deliverables

The planned project artifacts include:

- Test plan.
- Test scenarios.
- Detailed test cases.
- Include documentation of the test data when necessary.
- Test execution records.
- Defect reports.
- Supporting evidence.
- Test summary report.
- Public portfolio repository.

## 11. References

- OWASP Juice Shop Companion Guide:
  https://pwning.owasp-juice.shop/companion-guide/latest/

- Test environment documentation:
  `qa/documentation/test-environment.md`
