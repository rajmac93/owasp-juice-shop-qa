# Test Plan — OWASP Juice Shop

## 1. Project Overview

**Project:** OWASP Juice Shop — Manual QA Testing  
**Application Under Test:** OWASP Juice Shop  
**Testing Type:** Manual Web Application Testing  
**Project Status:** In Progress

This project demonstrates a structured QA workflow, including test
planning, test design, manual test execution, defect reporting, and
regression testing.

OWASP Juice Shop is an intentionally vulnerable application used in
this project as a local educational testing environment.

## 2. Test Objectives

The objectives of this project are to:

- Verify the selected user workflows.
- Check form validation and error handling.
- Identify unexpected application behaviour.
- Apply positive, negative, and boundary value testing.
- Record test results and supporting evidence.
- Prepare clear, reproducible defect reports.
- Explore selected security-related behaviours in the local environment.

## 3. Scope

### 3.1 In Scope

The planned functional testing scope includes:

- User authentication and registration.
- Product catalogue and product search.
- Shopping cart operations.
- Checkout workflow.
- Form validation and error messages.
- Navigation and selected user interface behaviours.

Additional activities may include:

- Exploratory testing.
- Regression testing.
- Selected API testing.
- Security testing of the local application within the controlled environment.

The scope is being addressed incrementally. The areas currently documented
as tested are authentication and registration. The remaining areas are
planned and must not be considered tested until execution results are recorded.

### 3.2 Out of Scope

The initial phase excludes:

- Load and performance testing.
- Testing production systems or unrelated third-party services.
- Automated test implementation.
- Formal compliance certification.
- Testing outside the approved local environment.

The scope may be revised as the project progresses.

## 4. Test Approach

Testing is performed manually, with attention to risk and the selected
test objectives.

The following techniques are used where appropriate:

- **Positive testing:** checking expected behaviour with valid inputs.
- **Negative testing:** checking behaviour with invalid or unexpected inputs.
- **Boundary value analysis:** checking values at and around relevant limits.
- **Equivalence partitioning:** grouping inputs expected to behave similarly.
- **Exploratory testing:** investigating application behaviour beyond
  predefined test steps.
- **Regression testing:** rechecking selected behaviours after changes.

Test cases should specify preconditions, test data, steps, and expected
results. Actual results and execution statuses are recorded after the
corresponding tests have been performed.

## 5. Test Environment

The test environment is documented in:

`qa/documentation/test-environment.md`

The application runs locally using Docker and is accessed at:

`http://localhost:3000`

The documented application version and Docker image digest provide a
baseline for identifying the tested environment.

## 6. Entry Criteria

Testing may begin when:

- The application is available.
- The target workflow can be accessed.
- Required test data is available or can be created.
- Relevant test cases have been reviewed.
- The test environment has been documented.

Additional entry criteria may apply to individual tests.

## 7. Exit Criteria

A test cycle may be considered complete when:

- Planned test cases have been executed or explicitly marked as blocked
  or not run.
- Actual results and execution statuses have been recorded.
- Failed tests have been reviewed.
- Relevant defects have been documented.
- Supporting evidence has been saved.
- Risks and limitations have been summarised.

Completion of a test cycle does not prove that the application is free
from defects.

## 8. Defect Reporting

A defect report should include, where applicable:

- Unique defect identifier.
- Clear, concise title.
- Environment and preconditions.
- Steps to reproduce.
- Expected result.
- Actual result.
- Severity and priority, where assessed.
- Supporting evidence.
- Current status.

Observed behaviour should be distinguished from a confirmed defect when
the expected behaviour or requirement has not been established.

Functional defects should also be distinguished from behaviours that are
intentionally vulnerable in this educational application.

## 9. Risks and Limitations

- The application intentionally contains security vulnerabilities.
- Application behaviour may vary between versions.
- The initial scope covers selected workflows rather than the entire application.
- Manual testing cannot guarantee detection of all defects.
- Evidence should be reviewed for sensitive information before publication.
- The Docker image tag `latest` is mutable; the recorded image digest
  provides a more precise reference to the image inspected.

## 10. Test Deliverables

Project deliverables include:

- Test plan.
- Test scenarios.
- Detailed test cases.
- Test data documentation, where needed.
- Test execution records and summaries.
- Defect reports.
- Supporting evidence.
- Public portfolio repository.

## 11. References

- OWASP Juice Shop Companion Guide:
  https://pwning.owasp-juice.shop/companion-guide/latest/
- Test environment documentation:
  `qa/documentation/test-environment.md`
