# BUG-005 — Sorting "Name (Z to A)" does not work correctly

**Linked Test Case:** TC-SORT-006
**Linked to:** Task "Prepare and Execute Product Sorting Test Cases" → Story "Verify Product Sorting" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. On the Products page, select the sort option **Name (Z to A)**.
3. Review the resulting product order.

## Expected Result
Products should be sorted alphabetically from Z to A.

## Actual Result
The sort order is incorrect.

## Severity / Priority
Medium

## Status
Open
