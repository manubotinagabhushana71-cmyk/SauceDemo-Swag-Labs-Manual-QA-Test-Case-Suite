# SauceDemo (Swag Labs) — Manual QA Test Case Suite

A complete manual testing project covering the end-to-end user journey on [SauceDemo](https://www.saucedemo.com), a demo e-commerce site commonly used for QA practice. This workbook documents test design, execution, and defect reporting across all major flows of the application.

## 📋 What's Inside

The workbook contains **89 test cases** across **7 functional areas**, each with full traceability (Requirement ID, test data, pre-conditions, steps, expected vs. actual results, severity, priority, and defect linkage):

| Sheet | Module | Test Cases |
|---|---|---|
| Sheet2 | Login Page | 19 |
| Sheet1 | Products Page | 17 |
| Sheet3 | Add to Cart | 17 |
| Sheet4 | Payments (Validation) | 6 |
| Sheet5 | Checkout: Your Information | 10 |
| Sheet6 | Checkout: Overview | 12 |
| Sheet7 | Order Confirmation | 8 |

## 🐞 Results Summary

- **70 Passed** / **19 Failed**
- **19 defects logged** (BUG-SL-001 through BUG-SL-019), covering issues such as:
  - Session not invalidated after logout (browser Back button access)
  - No rate-limiting on repeated failed logins (brute-force risk)
  - Cart data leaking between different user sessions
  - Stale price totals after mid-checkout cart changes
  - No input sanitization on Zip/Postal Code field (XSS risk)
  - Checkout steps bypassable via direct URL navigation
  - Duplicate order submission possible via browser Back button

## 🧪 Testing Approach

Each test case follows a structured format:
- **Test Objective/Scenario** — what is being verified
- **Test Data** — exact inputs used
- **Pre-Condition** — required state before execution
- **Test Steps** — numbered, reproducible steps
- **Expected vs. Actual Result** — for clear pass/fail evidence
- **Severity & Priority** — impact-based defect triage
- **Related Defects** — linked bug IDs for traceability

Testing combined **positive, negative, boundary, security (XSS/SQLi), and session-state** scenarios to reflect real-world QA coverage, not just happy-path testing.

## 🛠️ Tech/Tools Context

- Manual functional testing (no automation in this artifact)
- Application under test: [saucedemo.com](https://www.saucedemo.com)
- Test case design informed by standard QA techniques: boundary value analysis, equivalence partitioning, and exploratory testing

## 📁 Files

- `final_full_edited.xlsx` — Full test case suite (all 7 sheets)

---
*Tested by: Nagabhushanamma*
