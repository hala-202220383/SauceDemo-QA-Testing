# SauceDemo Web Application — QA Testing Project

## Project Overview
This project demonstrates a complete manual software testing process performed on the [SauceDemo](https://www.saucedemo.com) web application (Swag Labs). The project covers the full QA lifecycle: test planning, test case design, test execution, exploratory testing, defect (bug) reporting, and test management using Jira.

The workflow followed throughout the project was:

```
Requirement → Test Case → Test Execution → PASS/FAIL → Bug Report → Retesting
```

## Testing Objective
To verify that the main functionalities of the SauceDemo web application work correctly and meet the expected behavior from an end-user perspective — identifying functional defects, validating user interactions, and ensuring correct behavior under different user scenarios.

## Test Case ID Naming Convention
| Prefix | Area |
|---|---|
| `TC-LOGIN-XXX` | Authentication / Login |
| `TC-PROD-XXX` | Product Display & Information |
| `TC-SORT-XXX` | Product Sorting |
| `TC-CART-XXX` | Shopping Cart |
| `TC-CHECKOUT-XXX` | Checkout |
| `TC-LOGOUT-XXX` | Logout / Session |

## Entry Criteria
Testing begins when:
- The application is accessible.
- Required test accounts are available.
- The test environment is ready.
- Test cases have been prepared.
- Required test data is available.

## Exit Criteria
Testing is considered complete when:
- Planned test cases have been executed.
- PASS / FAIL / BLOCKED results have been recorded.
- Failed test cases have corresponding bug reports where applicable.
- Bugs have been documented and linked to their relevant test cases.
- Critical functionality has been verified.
- Final test execution results have been documented.

## Defect Management Process
```
Execute Test Case
       ↓
Actual Result ≠ Expected Result
       ↓
Test Case = FAIL
       ↓
Investigate the issue
       ↓
Create Bug Report in Jira
       ↓
Link Bug to related Test Case
       ↓
Retest after fix
       ↓
PASS / FAIL
```

## Test Execution Strategy
Testing was performed in stages:

| Phase | Focus |
|---|---|
| 1 — Authentication | Verify login and access behavior |
| 2 — Product Testing | Verify product display, information, details, and sorting |
| 3 — Shopping Cart | Verify adding, removing, and managing products in the cart |
| 4 — Problem Users | Re-run selected scenarios with `problem_user` to surface defects not visible with `standard_user` |
| 5 — Bug Reporting | Document failed scenarios in Jira and link them to their test cases |
| 6 — Checkout | Verify the complete checkout and order process |
| 7 — Logout | Verify logout and session behavior |
| 8 — Final Regression | Re-verify affected areas and finalize results |

## Testing Scope
- Login / Authentication
- Product Display & Information
- Product Sorting
- Shopping Cart
- Checkout
- Logout / Session

## Testing Types & Techniques
- Manual Testing
- Functional Testing
- Positive Testing
- Negative Testing
- Exploratory Testing
- Smoke Testing
- Black Box Testing

## Test Environment
| Item | Detail |
|---|---|
| Browser | Google Chrome |
| Operating System | Windows 11 Pro |
| Application Under Test | SauceDemo (https://www.saucedemo.com) |

## Test Users (Demo Data — Public)
SauceDemo provides several demo accounts, each designed to trigger different application behaviors. No personal data is used or stored — these are public demo credentials provided by the application itself.

| Username | Purpose |
|---|---|
| `standard_user` | Normal / expected behavior |
| `locked_out_user` | Testing a blocked account |
| `problem_user` | Surfaces functional/UI bugs |
| `performance_glitch_user` | Testing performance/response delays |
| `error_user` | Testing error-handling behavior |
| `visual_user` | Testing visual/UI defects |

Password for all demo accounts: `secret_sauce`

## Jira Structure
The project was managed in Jira using the following hierarchy:

```
Epic → Story → Task → Test Case → Bug
```

Five Epics were completed:
1. **Authentication Testing** — Login
2. **Product Testing** — Product Display & Information, Product Sorting
3. **Shopping Cart Testing** — Add to Cart
4. **Checkout Testing** — Checkout process
5. **Logout / Session Testing** — Logout functionality

## Results Summary

| Epic | Story | Test Cases | Passed | Failed | Blocked |
|---|---|---|---|---|---|
| Authentication | Login | 6 | 6 | 0 | 0 |
| Product | Display & Info | 11 | 7 | 4 | 0 |
| Product | Sorting | 8 | 5 | 3 | 0 |
| Cart | Add to Cart | 10 | 10 | 0 | 0 |
| Checkout | Checkout Process | 15 | 10 | 1 | 4 |
| Logout | Logout Functionality | 4 | 4 | 0 | 0 |
| **Total** | | **54** | **42** | **8** | **4** |

**Overall pass rate:** 42/54 (≈78%)
**Bugs found:** 8 (see `Bug-Reports/`)

Most bugs were discovered using the `problem_user` account, which is intentionally designed by SauceDemo to expose functional and UI defects. Testing followed a disciplined approach: exploratory findings were first converted into formal, repeatable Test Cases before any Bug was filed, ensuring every reported defect is tied to a reproducible, documented test.

## Repository Structure
```
SauceDemo-QA-Testing/
├── README.md
├── Bug-Reports/                  → One Markdown file per bug (BUG-001 to BUG-008)
├── Test-Execution/
│   └── Test-Execution-Report.xlsx → Full execution results per Epic + summary
├── Test-Cases/                   → (optional) detailed test case sheets
├── Screenshots/                  → (optional) Jira board, execution, and bug evidence
└── Jira/                         → (optional) Jira project overview export
```

## Key Findings
- **BUG-003 (Critical):** Product price shown on Product Details differs from the price on the Products listing page.
- **BUG-008 (Blocker):** With `problem_user`, the Last Name field on the Checkout Information page does not accept keyboard input at all, blocking checkout completion entirely — this blocked 4 downstream test cases (TC-CHECKOUT-012 to 015).
- Most `problem_user` sorting options are broken except Name A→Z.
- Product images and names are frequently mismatched under `problem_user`.

## Author
Hala — QA Testing Portfolio Project

