# BUG-002 — Product image differs between Products page and Product Details page

**Linked Test Case:** TC-PROD-009
**Linked to:** Task "Prepare and Execute Product Display Test Cases" → Story "Verify Product Display and Information" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. Note a product's image on the Products page.
3. Open that same product's Product Details page.
4. Compare the two images.

## Expected Result
The image should be identical on both pages.

## Actual Result
The image on the Product Details page differs from the one shown on the Products page.

## Severity / Priority
High / Major

## Status
Open
