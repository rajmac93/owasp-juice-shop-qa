# OWASP Juice Shop — Manual QA Testing Portfolio

## Project Overview

This repository contains a manual QA testing portfolio project based on [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/), an intentionally vulnerable web application designed for security training and testing.

The goal of this project is to practice and document software testing activities in a structured way, including test planning, test case design, manual test execution, defect reporting, and test documentation.

## Objectives

- Design and execute manual functional test cases.
- Test authentication workflows and input validation.
- Document actual and expected results.
- Record test evidence and observed application behavior.
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

## Initial Test Run Results

| Metric | Result |
|---|---:|
| Test cases executed | 8 |
| Passed | 7 |
| Failed | 1 |
| Completion rate | 100% |

One test case, **OJST-3 — Login with invalid email format**, did not meet its expected result.

The application accepted the invalid email format for submission and displayed `Invalid email or password.` rather than a specific email format validation message.

This behavior is documented for further investigation. Confirmation against the application's requirements is needed before classifying it as a confirmed defect.

Detailed results and the original Qase export are available in [`qa/test-runs/authentication/`](qa/test-runs/authentication/).

## Test Documentation

- [Test Plan](qa/documentation/test-plan.md)
- [Test Environment](qa/documentation/test-environment.md)
- [Bug Reports](qa/bug-reports/)
- [Test Cases](qa/test-cases/)
- [Test Runs](qa/test-runs/)
- [Screenshots and Evidence](qa/evidence/screenshots/)

## Approach

Testing activities are documented with a focus on traceability, reproducibility, and clear reporting of expected and actual results.

The repository represents a work in progress. Test coverage and documentation will be expanded as the project develops.

## Disclaimer

OWASP Juice Shop is used as a deliberately vulnerable application for educational and testing purposes. All testing is performed in a local environment controlled by the project owner..
