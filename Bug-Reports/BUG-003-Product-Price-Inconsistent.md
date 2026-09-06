# BUG-003 — Product price inconsistent between Products and Product Details

**Linked Test Case:** TC-PROD-010
**Linked to:** Task "Prepare and Execute Product Display Test Cases" → Story "Verify Product Display and Information" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. Note the product's price on the Products page.
3. Open that same product's Product Details page.
4. Compare the two prices.

## Expected Result
The price should be the same on both pages.

## Actual Result
The price differs between the Products page and the Product Details page.

## Severity / Priority
**Critical** — directly affects purchase decisions and pricing trust

## Status
Open
