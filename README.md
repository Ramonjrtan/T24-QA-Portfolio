# 🏦 T24 QA Portfolio (Temenos Transact)

A domain-focused QA portfolio showcasing testing practices for **Temenos Transact (T24) Core Banking System**, covering end-to-end workflows, API validation, and financial data integrity.

---

## 🎯 Repository Purpose

This repository demonstrates how I structure **real-world QA assets for core banking systems**, including:

* Reusable Excel-based test cases
* End-to-end banking flow scenarios
* API-level validation (T24 subroutines)
* Sample defect reports
* Portfolio-ready documentation for interviews and case studies

---

## 📁 Repository Structure

```text
T24-QA-Portfolio/
├── Test-Cases/
│   ├── T24_QA_Test_Cases.xlsx
│   ├── T24_API_Test_Cases.xlsx
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

---

## 🔍 API Coverage (T24 Internal APIs)

This portfolio includes testing of key T24 internal APIs:

* `VALIDATION.RTN` → Field validation & business rules
* `INPUT.ROUTINE` → Pre-save processing
* `AUTH.ROUTINE` → Post-authorization updates
* `EB.API` → Program invocation
* `BATCH.CONTROL` → Batch and EOD processing

---

## ⚙️ How to Use This Portfolio

1. Open Excel files under `Test-Cases/`
2. Execute test cases and update the **Status** column (Pass/Fail)
3. Use the **Execution Report** sheet to track progress and KPIs
4. Review `Test-Scenarios/` for end-to-end validation flows
5. Extend with:

   * Screenshots
   * Execution evidence
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
* Regression Testing

---

## 💡 Key Highlights

* Focus on **financial accuracy and accounting integrity**
* Validates **core banking workflows end-to-end**
* Demonstrates **domain expertise in banking + payments systems**
* Includes **API-level validation (rare skill in QA portfolios)**
* Structured for **real project usage and interview discussions**

---

## 🚀 Future Enhancements

* Automation scripts (Playwright / API simulation)
* CI/CD integration (test execution pipelines)
* Expanded defect tracking and reporting
* Performance and batch testing scenarios

---

## 👨‍💻 Author

**Ramon Tan Jr**
Senior QA Engineer | Core Banking | Payments | End-to-End Systems Validation
