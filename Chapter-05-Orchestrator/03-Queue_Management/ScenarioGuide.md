# 📘 Case 03 - Queue Management

## 🎯 Objective
Create, add, and process transaction items using Orchestrator queues.

---

## 📝 Sample Data
- Queue: `InvoiceQueue`  
- Transaction items (anonymized):
  
| InvoiceID | Amount | Status |
|-----------|--------|--------|
| INV001    | $XXX   | New    |
| INV002    | $XXX   | New    |
| ...       | ...    | ...    |

---

## 🛠️ Steps
1. Create a queue in Orchestrator.  
2. Add transaction items manually or via automation workflow.  
3. Retrieve transaction items using **Get Transaction Item** activity.  
4. Update transaction status (Successful / Failed / Retried) after processing.  

---

## ✅ Expected Output
- Queue created and populated with transaction items.  
- Transactions processed successfully with correct status updates.  

---

## 📦 Covered Activities
- Create Queue  
- Add Queue Item  
- Get Transaction Item  
- Set Transaction Status
