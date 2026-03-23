# 🏦 T24 QA Portfolio (Temenos Transact)

A domain-focused QA portfolio showcasing testing practices for **Temenos Transact (T24) Core Banking System**, covering end-to-end workflows, API validation, TAP (AAA) controls, and financial data integrity.

---

## 🎯 Repository Purpose

This repository demonstrates how I structure **real-world QA assets for core banking systems**, including:

* Reusable Excel-based test cases with execution tracking
* End-to-end banking flow scenarios
* API-level validation (T24 internal subroutines)
* TAP (AAA) security and accounting validation
* Sample defect reports
* Portfolio-ready documentation for interviews and case studies

---

## 📁 Repository Structure

```text
T24-QA-Portfolio/
├── Test-Cases/
│   ├── T24_QA_Test_Cases_with_Execution_Report.xlsx
│   ├── T24_API_Test_Cases_with_Execution_Report.xlsx
│   ├── T24_AAA_Test_Cases_with_Execution_Report.xlsx
├── Test-Scenarios/
│   └── End-to-End-Banking-Flow.md
├── Defect-Reports/
│   └── Sample_Defects.md
└── README.md
```

---

## 🧪 Scope Covered

* Customer module (onboarding & validation)
* Account module (creation, configuration)
* Funds Transfer (FT) transactions
* End-to-end Maker/Checker flow
* Authorization lifecycle (NAU → LIVE)
* Enquiry, history, and audit traceability
* API-driven processing (validation, input, authorization)
* TAP (AAA) model:

  * Authentication (login/session control)
  * Authorization (role-based access, maker/checker)
  * Accounting (ledger validation, debit = credit)

---

## 🔍 API Coverage (T24 Internal APIs)

This portfolio includes testing of key T24 internal APIs:

* `VALIDATION.RTN` → Field validation & business rules
* `INPUT.ROUTINE` → Pre-save processing
* `AUTH.ROUTINE` → Post-authorization updates
* `EB.API` → Program invocation
* `BATCH.CONTROL` → Batch and EOD processing

---

## 📊 Execution & Reporting

Enhanced Excel workbooks include an **Execution Report** sheet with:

* Pass/Fail tracking
* Summary by **AAA Area (Authentication / Authorization / Accounting)**
* Summary by **Module**
* Total cases, Passed, Failed, Blocked, Not Run
* Pass rate (%)
* Linked execution detail view from test cases

👉 This simulates **real QA reporting used in enterprise projects**

---

## ⚙️ How to Use This Portfolio

1. Open Excel files under `Test-Cases/`
2. Execute test cases and update the **Status** column (Pass/Fail/Blocked/Not Run)
3. Review the **Execution Report** sheet for metrics and progress
4. Explore `Test-Scenarios/` for end-to-end validation flows
5. Extend with:

   * Screenshots (evidence)
   * Defect logs
   * Automation scripts (future enhancement)

---

## 🧠 Testing Approach

This portfolio demonstrates:

* Functional Testing
* Negative Testing
* Integration Testing (Customer → Account → FT)
* Authorization Flow Validation (Maker/Checker)
* Financial Data Validation (Debit = Credit)
* API Testing (T24 internal subroutines)
* TAP (AAA) Validation (Authentication, Authorization, Accounting)
* Regression Testing

---

## 💡 Key Highlights

* Focus on **financial accuracy and accounting integrity**
* Validates **core banking workflows end-to-end**
* Demonstrates **domain expertise in banking + payments systems**
* Includes **API-level validation (rare skill in QA portfolios)**
* Covers **TAP (AAA) security model (high-value in banking QA)**
* Structured for **real project usage and interview discussions**

---

## 🚀 Future Enhancements

* Automation scripts (Playwright / API simulation)
* CI/CD integration (test execution pipelines)
* Defect tracking dashboard (linked to execution results)
* Performance and batch testing scenarios
* REST API testing (Postman integration for external services)

---

## 👨‍💻 Author

**Ramon Tan Jr**
Senior QA Engineer | Core Banking | Payments | End-to-End Systems Validation
