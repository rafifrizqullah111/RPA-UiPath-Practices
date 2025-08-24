# 📂 Case 04 - End-to-End REFramework Capstone

## 📄 Description
Build a complete REFramework automation that integrates multiple data sources (Excel, Queues, and Web forms).  
This project simulates a real-world business process from **data ingestion → validation → multi-stage approval → reporting**, using full REFramework best practices.

---

## 🎯 Objectives
- Apply all REFramework concepts in a single end-to-end project.  
- Combine multiple input sources (Excel, Orchestrator Queue, Web scraping/API).  
- Implement Dispatcher & Performer pattern.  
- Apply retry logic, logging, and config-driven design.  
- Produce final reporting and exception handling output.  

---

## 🛠️ Activities / Components
- `Config.xlsx` (stores queue names, paths, system URLs)  
- `Dispatcher Robot` (loads data from multiple sources into queues)  
- `Performer Robot` (processes each transaction, applies rules)  
- `Excel Application Scope` (read input data / write reports)  
- `HTTP Request` or `Data Scraping` (fetch external data)  
- `Business Rule Exception` & `System Exception` handling  
- `Orchestrator Queues` (to manage transactions)  
- `Send Outlook Mail Message` (notify stakeholders)  

---

## 📂 Sample Dataset
1. **Excel Input** – `CustomerOrders.xlsx`  
   | OrderID | Customer   | Amount | Category  | Status   |
   |---------|------------|--------|-----------|----------|
   | ORD001  | Alice Wong | 250    | OfficeSup | Pending  |
   | ORD002  | Mark Chan  | 1200   | ITEquip   | Pending  |
   | ORD003  | Lina Kim   | 450    | Travel    | Pending  |

2. **External Data Source** – Web/API with currency rates (e.g., USD to IDR).  

3. **Output File** – `Orders_Processed.xlsx`.  

---

## 🚀 Hands-On Steps
### Dispatcher
1. Read `CustomerOrders.xlsx`.  
2. Fetch currency exchange rates via API (optional).  
3. Add each order as QueueItem into Orchestrator Queue (`Order_Processing_Queue`).  

### Performer
1. Retrieve transaction from `Order_Processing_Queue`.  
2. Validate fields (OrderID, Amount, Category).  
   - If invalid → throw `BusinessRuleException`.  
3. Apply rules:  
   - If Amount ≤ 500 → auto-approve.  
   - If Amount > 500 and ≤ 1000 → requires Manager approval.  
   - If Amount > 1000 → requires Director approval.  
4. For approvals → simulate email notification or Action Center validation.  
5. Update final order status (Approved / Rejected / Pending Review).  
6. Log all results in `Orders_Processed.xlsx`.  

### Reporting
1. Generate summary: total processed, approved, rejected, pending.  
2. Send summary report via email.  

---

## ✅ Expected Output
- All orders processed according to rules.  
- Queue items retried automatically if failed due to System Exception.  
- **Output file example:**  

`Orders_Processed.xlsx`  

| OrderID | Customer   | Amount | Category  | FinalStatus      |
|---------|------------|--------|-----------|------------------|
| ORD001  | Alice Wong | 250    | OfficeSup | Approved         |
| ORD002  | Mark Chan  | 1200   | ITEquip   | Pending Director |
| ORD003  | Lina Kim   | 450    | Travel    | Approved         |

- Email sent: **“Daily Order Pro**
