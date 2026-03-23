# 🏦 End-to-End Banking Flow Case Study (T24 QA)

## 🎯 Scenario Objective

Validate an end-to-end Temenos T24 core banking workflow from **customer onboarding to transaction posting**, ensuring:

* Data integrity
* Correct authorization flow (Maker → Checker)
* Accurate financial accounting (Debit = Credit)

---

## 🔁 Business Flow

Customer → Account → Funds Transfer → Statement / Accounting Entries

---

## ⚙️ Preconditions

* Maker and checker users are configured (segregation of duties)
* Required product/category setup exists (ACCOUNT, FT)
* Accounts are active and transaction-enabled
* Sufficient balance available for debit account
* Test data approved for environment
* API routines configured:

  * VALIDATION.RTN
  * INPUT.ROUTINE
  * AUTH.ROUTINE

---

## 🧪 Scenario Steps with QA Validation

### 👤 1. Create Customer

**Steps:**

* Create new CUSTOMER record
* Populate mandatory fields (Name, KYC, Address)
* Validate → Commit → Authorize

**QA Validation:**

* Mandatory fields enforced (VALIDATION.RTN)
* Default values applied correctly
* Record lifecycle: NAU → LIVE
* Duplicate customer detection

---

### 💳 2. Open Account

**Steps:**

* Open ACCOUNT for customer
* Enter Category, Currency, Account Title
* Validate → Commit → Authorize

**QA Validation:**

* Customer linkage is correct
* Currency and category valid
* Unique account number generated
* INPUT.ROUTINE executed (if configured)
* Record lifecycle: NAU → LIVE

---

### 💰 3. Fund Account

**Steps:**

* Ensure debit account has sufficient balance
* Confirm account status = ACTIVE

**QA Validation:**

* Available balance ≥ transfer amount
* No posting restrictions or blocked funds
* Account eligible for transaction

---

### 💸 4. Perform Funds Transfer

**Steps:**

* Create new FT transaction
* Enter debit account, credit account, amount, and narrative
* Commit → Authorize

**QA Validation:**

* VALIDATION.RTN:

  * Reject invalid accounts
  * Validate currency consistency
* INPUT.ROUTINE:

  * Prevent duplicate or invalid entries
* AUTH.ROUTINE:

  * Ensure post-authorization updates

---

### 📊 5. Verify Outcomes

#### Functional Validation

* Debit account balance decreases correctly
* Credit account balance increases correctly
* Transaction appears in enquiry

#### Accounting Validation

* Total Debit = Total Credit
* Correct entries in:

  * ACCOUNT
  * STMT.ENTRY
  * Accounting tables

#### Audit Validation

* Transaction recorded in history (HIS)
* Audit trail available
* Maker/Checker properly recorded

---

## ⚠️ Risks Validated

* Incorrect authorization flow (NAU → LIVE bypass)
* Invalid balance updates
* Duplicate transactions
* Missing accounting entries
* Data inconsistency across modules
* Weak segregation of duties

---

## 🔍 API Validation Coverage

| API            | Validation Focus                                |
| -------------- | ----------------------------------------------- |
| VALIDATION.RTN | Field validation, defaulting, cross-field rules |
| INPUT.ROUTINE  | Pre-save checks, duplicate prevention           |
| AUTH.ROUTINE   | Post-authorization updates                      |
| EB.API         | Correct program invocation                      |
| BATCH.CONTROL  | Batch execution and downstream processing       |

---

## 🧠 QA Techniques Applied

* Functional Testing
* Data Validation (UI vs Backend)
* Integration Testing (Customer → Account → FT)
* Authorization Flow Testing
* Negative Testing (invalid input, insufficient balance)

---

## 💼 Portfolio Talking Points

* Demonstrates strong core banking domain knowledge (T24)
* Covers full end-to-end transaction lifecycle
* Validates financial accuracy and accounting integrity
* Shows understanding of Maker/Checker controls
* Includes API-level validation (VALIDATION.RTN, AUTH.ROUTINE)
* Can be expanded into smoke, regression, and release test packs

---

## 🚀 Summary

This case study demonstrates a **real-world banking QA scenario**, combining:

* Functional validation
* Financial data verification
* API-driven process validation

It highlights the ability to test **complex, integrated financial systems**, beyond standard UI-based testing.
