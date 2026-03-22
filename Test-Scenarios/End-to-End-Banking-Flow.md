# End-to-End Banking Flow Case Study

## Scenario objective
Validate a standard T24 banking flow from customer onboarding through transaction posting.

## Business flow
Customer -> Account -> Funds Transfer -> Statement / Accounting Entries

## Preconditions
- Maker and checker users are available
- Required product/category setup exists
- Source and destination accounts are allowed for the transaction type
- Test data is approved for the environment

## Scenario steps
### 1. Create customer
- Create a new customer record
- Validate mandatory fields
- Commit record
- Authorize record

### 2. Open account
- Open a current account for the customer
- Validate category, currency, and title fields
- Commit record
- Authorize record

### 3. Fund account
- Ensure the source account has available funds
- Confirm the account is active and transaction-ready

### 4. Perform funds transfer
- Create a new FT transaction
- Enter debit account, credit account, amount, and narrative
- Commit record
- Authorize record

### 5. Verify outcomes
- Source account balance decreases correctly
- Destination account balance increases correctly
- Transaction appears in the relevant enquiry
- Accounting entries remain balanced
- Audit trail and history are available

## Risks validated
- Incorrect authorization flow
- Invalid balance updates
- Duplicate transactions
- Missing accounting entries
- Weak segregation of duties

## Portfolio talking points
- Demonstrates domain knowledge beyond generic QA
- Shows understanding of maker/checker controls
- Highlights financial data accuracy checks
- Can be expanded into smoke, regression, and release packs
