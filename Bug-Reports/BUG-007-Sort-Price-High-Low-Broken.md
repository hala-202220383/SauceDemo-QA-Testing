# BUG-007 — Sorting "Price (High to Low)" does not work correctly

**Linked Test Case:** TC-SORT-008
**Linked to:** Task "Prepare and Execute Product Sorting Test Cases" → Story "Verify Product Sorting" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. On the Products page, select the sort option **Price (High to Low)**.
3. Review the resulting product order.

## Expected Result
Products should be sorted from highest to lowest price.

## Actual Result
The sort order is incorrect.

## Severity / Priority
Medium

## Status
Open
