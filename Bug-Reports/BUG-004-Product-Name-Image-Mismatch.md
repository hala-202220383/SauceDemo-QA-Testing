# BUG-004 — Product name does not match its displayed image

**Linked Test Case:** TC-PROD-011
**Linked to:** Task "Prepare and Execute Product Display Test Cases" → Story "Verify Product Display and Information" → Epic "Product Testing"

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. Review each product on the Products page.
3. Compare the written name with the image shown next to it.

## Expected Result
The name should match the image.

## Actual Result
There are cases where one product's name appears with another product's image.

## Severity / Priority
High / Major

## Status
Open

## Note
Closely related to BUG-001 (same underlying image-mapping defect). Kept as a separate report since it originates from a different Test Case; may be merged during triage.
