# 📂 Case 01 - Queue-Based Invoice Processing

## 📄 Description
Automate the processing of invoices by leveraging Orchestrator Queues in REFramework.  
Invoices are uploaded (via Excel or PDF metadata) and processed one by one, applying validation and business rules.  

---

## 🎯 Objectives
- Understand Queue-based transaction processing with REFramework.  
- Differentiate between **Dispatcher** and **Performer** roles.  
- Implement business rule and system exception handling.  
- Generate logs and reporting for invoice validation.  

---

## 🛠️ Activities / Components
- `Excel Application Scope` / `Read Range` (Dispatcher)  
- `Add Queue Item` (Dispatcher)  
- `Get Transaction Item` (Performer)  
- `If` / `Switch` (Business rule checks)  
- `Throw BusinessRuleException`  
- `Retry Mechanism` (built-in in REFramework)  
- `Write Line` / `Log Message`  
- `Write Range` (Export results)  

---

## 📂 Sample Dataset
- `Invoices.xlsx`  
  | InvoiceID | Vendor   | Amount | Currency | DueDate    |
  |-----------|----------|--------|----------|------------|
  | INV001    | ABC Ltd  | 1000   | USD      | 2025-08-01 |
  | INV002    | XYZ Inc  | 750    | EUR      | 2025-08-05 |
  | INV003    | DEF Co   | 5000   | USD      | 2025-08-10 |

---

## 🚀 Hands-On Steps
### Dispatcher
1. Read `Invoices.xlsx`.  
2. For each row, add a queue item to `InvoicesQueue` in Orchestrator.  
3. Log how many items were pushed.  

### Performer
1. Get transaction item from `InvoicesQueue`.  
2. Apply business rule checks (e.g., Amount > 3000 = Flag for approval).  
3. If validation fails → throw `BusinessRuleException`.  
4. If system error (e.g., cannot connect to Orchestrator) → retry transaction.  
5. Log transaction status (Success, Business Exception, System Exception).  
6. Export results to Excel `Invoices_Processed.xlsx`.  

---

## ✅ Expected Output
- Invoices are processed one by one from Orchestrator Queue.  
- Logs show success/error status for each transaction.  
- Business exceptions (e.g., invalid amount) are marked but do not stop the process.  
- **Output file example:**  

`Invoices_Processed.xlsx`  

| InvoiceID | Vendor   | Amount | Status             |
|-----------|----------|--------|--------------------|
| INV001    | ABC Ltd  | 1000   | Success            |
| INV002    | XYZ Inc  | 750    | Success            |
| INV003    | DEF Co   | 5000   | Business Exception |
