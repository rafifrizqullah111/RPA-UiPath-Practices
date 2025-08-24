# 📘 REFramework Practice (UiPath)

This section contains **hands-on practice cases** for learning the Robotic Enterprise (RE) Framework in UiPath.  
Each case is designed to strengthen your understanding of transaction-based processing, exception handling, and scalable automation design.

---

## 📂 Cases Overview

### 01. Queue-Based Invoice Processing
- Process invoices stored in Orchestrator Queue and apply business rules.  
- **Covers:** TransactionItem = invoice data, Business Rule Exception handling, Retry mechanism, Logging.  
- **Dispatcher:** Reads invoice metadata (from Excel/PDF) and pushes items into `InvoicesQueue`.  
- **Performer:** Pulls each invoice from Queue, applies validation, and logs result.  

---

### 02. Excel Data Transaction Processing
- Read multiple rows from Excel and process them as individual transaction items.  
- **Covers:** Init state (load config), Transaction state (process row), Business Rule Exceptions, Retry handling.  
- **Dispatcher:** Reads rows from Excel and pushes them to `EmployeeDataQueue`.  
- **Performer:** Processes each row as a transaction (salary validation, reporting).  
- *Note:* For small datasets, Dispatcher & Performer can be merged into one robot.  

---

### 03. Multi-Stage Approval Workflow
- Simulate a process with multiple decision/approval stages (e.g., expense claims).  
- **Covers:** Multiple Business Rules, queue handoffs between stages, human-in-the-loop interaction.  
- **Dispatcher:** Reads claim requests (Excel/API) and pushes them into `ExpenseClaimsQueue`.  
- **Performer:** Processes approvals (Manager, Finance) transaction by transaction. May involve queue-to-queue handoff.  

---

### 04. End-to-End REFramework Capstone
- Build a complete REFramework solution combining multiple input types (Excel, Queue, Web data).  
- **Covers:** Config-driven design, robust exception handling, retry logic, Orchestrator integration, reporting.  
- **Dispatcher:** Loads different input sources (Excel, PDF, Web scraping) and pushes structured items into queues.  
- **Performer:** Processes each item type (Excel row, invoice, scraped data) using conditional logic within REFramework.  

---

## 🎯 Goal
By completing these 4 cases, you will gain hands-on experience in:  
- Transaction-based processing using REFramework  
- Exception handling (System vs Business Rule)  
- Retry logic and logging  
- Using Queues and Config files effectively  
- Designing scalable, enterprise-grade automation projects  
- Understanding **Dispatcher–Performer pattern** for large-scale automation

This practice set is designed to mimic **real-world REFramework implementations** for business processes.
