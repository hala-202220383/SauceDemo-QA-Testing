# BUG-008 — Last Name field does not accept keyboard input (problem_user)

**Linked Test Case:** TC-CHECKOUT-011
**Linked to:** Task "Prepare and Execute Checkout Test Cases" → Story "Verify Checkout Process" → Epic "Checkout Testing"

**Blocks:** TC-CHECKOUT-012, TC-CHECKOUT-013, TC-CHECKOUT-014, TC-CHECKOUT-015

## Environment
- Browser: Google Chrome
- OS: Windows 11 Pro
- Application: SauceDemo

## Preconditions
Logged in as `problem_user` / `secret_sauce`

## Steps to Reproduce
1. Log in as `problem_user`.
2. Add a product to the Cart and proceed to Checkout.
3. Click the Last Name field and try typing any text.

## Expected Result
The Last Name field should accept text input normally.

## Actual Result
No characters appear when typing in the Last Name field — the field is completely unresponsive to keyboard input, preventing checkout completion.

## Severity / Priority
**Critical / Blocker** — prevents the user from completing the purchase flow entirely

## Impact
Because checkout cannot be completed, four downstream test cases (TC-CHECKOUT-012 to TC-CHECKOUT-015) could not be executed and are marked **Blocked** in Jira, linked to this bug via "blocks".

## Status
Open
