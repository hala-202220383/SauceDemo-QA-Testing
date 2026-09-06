# BUG-001 — Product image does not match product name

**Linked Test Case:** TC-PROD-008
**Linked to:** Task "Prepare and Execute Product Display Test Cases" → Story "Verify Product Display and Information" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. Open the Products page.
3. Review each product and compare its image with its name.

## Expected Result
Each product's image should correctly correspond to its name.

## Actual Result
The displayed image does not match the product's name.

## Severity / Priority
High / Major — misleading UI for the user

## Status
Open
