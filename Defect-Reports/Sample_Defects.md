# Sample Defect Reports

## DEF-001 Incorrect balance after funds transfer
**Module:** Funds Transfer  
**Severity:** Critical  
**Priority:** High  

**Steps to reproduce**
1. Create a valid FT between two live accounts
2. Authorize the transaction
3. Review balances for both accounts

**Expected result**
- Debit account decreases by the transfer amount
- Credit account increases by the transfer amount

**Actual result**
- FT is authorized but one account balance does not update correctly

**Impact**
Financial inconsistency and reconciliation risk.

---

## DEF-002 Authorization bypass on live posting
**Module:** Customer / Account / FT  
**Severity:** High  
**Priority:** High  

**Steps to reproduce**
1. Create a new record as maker
2. Skip the intended checker action
3. Review the record state

**Expected result**
Record remains in NAU until authorized by a permitted user.

**Actual result**
Record appears in LIVE without valid checker authorization.

**Impact**
Serious control failure and audit risk.

---

## DEF-003 Duplicate transaction allowed
**Module:** Funds Transfer  
**Severity:** High  
**Priority:** High  

**Steps to reproduce**
1. Submit a valid FT
2. Repeat the same FT immediately with the same key details

**Expected result**
The system warns, blocks, or flags the duplicate based on configuration.

**Actual result**
Both transactions are processed without warning.

**Impact**
Potential financial loss, duplicate posting, and operational rework.
