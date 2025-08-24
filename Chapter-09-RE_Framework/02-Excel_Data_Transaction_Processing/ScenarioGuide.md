# 📂 Case 02 - Excel Data Transaction Processing

## 📄 Description
Automate the processing of data stored in Excel where each row represents a transaction.  
Unlike queue-based processing, here transactions are handled **directly from Excel rows** within the REFramework.

---

## 🎯 Objectives
- Learn how to process Excel rows as transactions in REFramework.  
- Implement Init state (load Config, read data).  
- Use Transaction state to process one row at a time.  
- Handle Business Rule vs System exceptions.  
- Export processed results back to Excel.  

---

## 🛠️ Activities / Components
- `Excel Application Scope` / `Read Range`  
- `For Each Row` → transaction dispatcher logic  
- `TransactionItem = DataRow` (customized REFramework argument)  
- `If` / `Switch` (Validation rules)  
- `Throw BusinessRuleException`  
- `Log Message`  
- `Write Range` (output log to Excel)  

---

## 📂 Sample Dataset
`Orders.xlsx`  
  | OrderID | Customer   | Product      | Quantity | Price | Status   |
  |---------|------------|--------------|----------|-------|----------|
  | ORD001  | John Doe   | Laptop       | 1        | 800   | Pending  |
  | ORD002  | Jane Smith | Mouse        | 5        | 20    | Pending  |
  | ORD003  | Bob Lee    | Monitor      | 2        | 150   | Pending  |

---

## 🚀 Hands-On Steps
1. Load Config file (with input/output path).  
2. Read `Orders.xlsx` into a DataTable.  
3. Assign `TransactionItem = DataRow` (custom argument in REFramework).  
4. For each row (transaction):  
   - Validate data (e.g., Quantity > 0, Price > 0).  
   - If invalid → throw `BusinessRuleException`.  
   - If system error (e.g., Excel not accessible) → retry transaction.  
   - Update `Status` column to “Processed” or “Failed”.  
5. Write results to `Orders_Processed.xlsx`.  

---

## ✅ Expected Output
- Each row is treated as a transaction.  
- Errors do not stop the whole file, only mark failed rows.  
- **Output file example:**  

`Orders_Processed.xlsx`  

| OrderID | Customer   | Product  | Quantity | Price | Status   |
|---------|------------|----------|----------|-------|----------|
| ORD001  | John Doe   | Laptop   | 1        | 800   | Success  |
| ORD002  | Jane Smith | Mouse    | 5        | 20    | Success  |
| ORD003  | Bob Lee    | Monitor  | 2        | 150   | Success  |
