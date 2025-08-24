# 📂 Case 03 - Multi-Stage Approval Workflow

## 📄 Description
Simulate an approval process where each transaction (e.g., expense claims) must go through multiple approval stages.  
Each stage applies its own business rules, and transactions can be routed for human review if exceptions occur.

---

## 🎯 Objectives
- Understand how to design **multi-step transaction processing** in REFramework.  
- Learn to handle queue handoffs between different stages.  
- Implement human-in-the-loop approval using Orchestrator / Action Center.  
- Apply both **Business Rule** and **System Exception** handling across stages.  

---

## 🛠️ Activities / Components
- `Orchestrator Queues` (Stage 1, Stage 2)  
- `TransactionItem = QueueItem`  
- `If` / `Switch` (Business Rules per stage)  
- `BusinessRuleException` (e.g., reject invalid claims)  
- `Orchestrator Action Center` (optional: human validation)  
- `Add Queue Item` (handoff to next stage)  
- `Log Message` (approval / rejection reason)  

---

## 📂 Sample Dataset
`ExpenseClaims.xlsx`  
  | ClaimID | Employee   | Amount | Purpose         | Stage   |
  |---------|------------|--------|-----------------|---------|
  | CLM001  | John Doe   | 200    | Travel Expense  | Pending |
  | CLM002  | Jane Smith | 1200   | Laptop Purchase | Pending |
  | CLM003  | Bob Lee    | 80     | Office Supplies | Pending |

---

## 🚀 Hands-On Steps
1. Load Config file (Excel path, Queue names).  
2. Dispatcher:
   - Read `ExpenseClaims.xlsx`.  
   - Add each row into `Stage1_Queue` in Orchestrator.  
3. Performer Stage 1:
   - Retrieve item from `Stage1_Queue`.  
   - Apply rule: Amount ≤ 500 → auto-approve, else → route to Stage2.  
   - If auto-approved → mark as "Approved - Stage 1".  
   - If routed → add transaction to `Stage2_Queue`.  
4. Performer Stage 2:
   - Retrieve item from `Stage2_Queue`.  
   - Rule: Amount ≤ 1000 → approve, else → require manual review.  
   - If requires manual review → send to `Action Center`.  
   - If approved/rejected → update Excel / Orchestrator Queue with final status.  
5. Generate final approval report (`ExpenseClaims_Processed.xlsx`).  

---

## ✅ Expected Output
- Each claim goes through 1 or 2 approval stages.  
- Claims above threshold may require manual intervention.  
- **Output file example:**  

`ExpenseClaims_Processed.xlsx`  

| ClaimID | Employee   | Amount | Purpose         | FinalStatus |
|---------|------------|--------|-----------------|-------------|
| CLM001  | John Doe   | 200    | Travel Expense  | Approved    |
| CLM002  | Jane Smith | 1200   | Laptop Purchase | Pending Review |
| CLM003  | Bob Lee    | 80     | Office Supplies | Approved    |
