# OWASP Juice Shop — Manual QA Testing Portfolio

## Project Overview

This repository contains a manual QA testing portfolio project based on [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/), an intentionally vulnerable web application designed for security training and testing.

The goal of this project is to practice and document software testing activities in a structured way, including test planning, test case design, manual test execution, defect reporting, evidence collection, and test documentation.

## Objectives

- Design and execute manual functional test cases.
- Test authentication and registration workflows.
- Verify input validation and form behavior.
- Document actual and expected results.
- Collect screenshots and other test evidence.
- Report and investigate potential defects.
- Maintain organized QA documentation using Git and GitHub.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| OWASP Juice Shop | Application under test |
| Qase | Test case management and execution |
| Git | Version control |
| GitHub | Portfolio and documentation |
| Linux Mint | Local testing environment |
| Docker | Running the application locally |

## Project Structure

```text
.
├── application/
│   └── docker/
├── qa/
│   ├── api/
│   ├── bug-reports/
│   │   └── exports/
│   ├── documentation/
│   ├── evidence/
│   │   ├── console/
│   │   ├── logs/
│   │   ├── network/
│   │   ├── screenshots/
│   │   └── videos/
│   ├── notes/
│   ├── test-cases/
│   ├── test-runs/
│   │   ├── authentication/
│   │   │   └── exports/
│   │   └── registration/
│   │       └── exports/
│   └── test-scenarios/
└── README.md
```

## Current Testing Scope

### Authentication

The initial manual test run covers eight test cases:

- Login with valid credentials
- Login with an invalid password
- Login with an invalid email format
- Login with empty credentials
- Logout successfully
- Access account after logout
- Login with an unregistered email address
- Login with a password containing special characters

### Registration

The initial registration test run contains 18 test cases covering:

- Valid and invalid registration data
- Required fields and email format validation
- Password length and character counter behavior
- Password confirmation validation
- Duplicate email handling and email letter case
- Password advice and navigation between registration and login

## Initial Test Run Results

### Authentication

| Metric | Result |
|---|---:|
| Test cases executed | 8 |
| Passed | 7 |
| Failed | 1 |
| Completion rate | 100% |

**Observation — D-1:** When an invalid email format was submitted on the login form, the application displayed `Invalid email or password.` rather than a specific email format validation message.

This behavior is documented for further investigation. Confirmation against the application's requirements is needed before classifying it as a confirmed defect.

Detailed results and the original Qase export are available in [`qa/test-runs/authentication/`](qa/test-runs/authentication/).

### Registration

| Metric | Result |
|---|---:|
| Test cases in export | 18 |
| Passed | 14 |
| Failed | 4 |
| Pass rate | 77.8% |
| Fail rate | 22.2% |
| Execution status | In progress |

The exported results include failed cases related to password length validation, password confirmation after changing the password, email letter case, and the password character counter.

**Note:** These figures reflect the exported test run and may change as execution continues. OJST-26 contains steps that were not executed at the time of export.

Detailed results and the original Qase export are available in [`qa/test-runs/registration/`](qa/test-runs/registration/).

## Defect Reports and Evidence

The `qa/bug-reports/` directory contains individual Markdown reports and dated CSV exports from Qase.

The current reports are identified as D-1 through D-5. They document observed application behavior and potential defects; observations that depend on unconfirmed requirements are explicitly marked for further investigation.

Screenshots are stored in [`qa/evidence/screenshots/`](qa/evidence/screenshots/) and use matching defect identifiers where applicable.

## Test Documentation

- [Test Plan](qa/documentation/test-plan.md)
- [Test Environment](qa/documentation/test-environment.md)
- [Bug Reports](qa/bug-reports/)
- [Test Cases](qa/test-cases/)
- [Test Runs](qa/test-runs/)
- [Screenshots and Evidence](qa/evidence/screenshots/)

## Approach

Testing activities are documented with a focus on traceability, reproducibility, and clear reporting of expected and actual results. Test execution results, defect reports, and evidence are maintained as the portfolio develops.

The repository represents a work in progress. Test coverage and documentation will be expanded as testing continues.

## Disclaimer

OWASP Juice Shop is used as a deliberately vulnerable application for educational and testing purposes. All testing is performed in a local environment controlled by the project owner.
