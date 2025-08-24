# 📂 Case 02 - Group & Aggregate

## 📄 Description
Summarize and aggregate data by a specific column or category using LINQ.  
This allows you to generate totals, counts, or averages without manual loops.

---

## 🎯 Objectives
- Learn to group data by a column (e.g., Category).  
- Perform aggregate operations like `Sum`, `Count`, or `Average`.  
- Export aggregated results to Excel for reporting purposes.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope`  
- `Assign` (for LINQ group and aggregate queries)  
- `CopyToDataTable` (if converting grouped data to DataTable)  
- `Write Range` (export aggregated result)  
- `Log Message` (optional, for verification)

---

## 📂 Sample Dataset
`Orders.xlsx`  
  | OrderID | Customer   | Amount | Category  |
  |---------|------------|--------|-----------|
  | ORD001  | Alice Wong | 250    | OfficeSup |
  | ORD002  | Mark Chan  | 1200   | ITEquip   |
  | ORD003  | Lina Kim   | 450    | Travel    |
  | ORD004  | John Doe   | 800    | ITEquip   |
  | ORD005  | Maria Lee  | 150    | OfficeSup |
  | ORD006  | Peter Pan  | 300    | Travel    |
  | ORD007  | Jane Doe   | 950    | ITEquip   |
  | ORD008  | Sam Smith  | 100    | OfficeSup |
  | ORD009  | Amy Wong   | 700    | Travel    |
  | ORD010  | Tom Lee    | 500    | OfficeSup |

---

## 🚀 Hands-On Steps
1. Read `Orders.xlsx` into a DataTable (`dtOrders`).  
2. Assign grouped and aggregated data to a new variable using LINQ:  
   ```vbnet
   dtGrouped = dtOrders.AsEnumerable().
       Group By cat = Function(r) r("Category") 
       Into TotalAmount = Sum(Function(r) r("Amount")), Count = Count()
       Select Category = cat, TotalAmount, Count
       CopyToDataTable()
   ```
3. Write `dtGrouped` to a new Excel sheet (`Aggregated_Orders.xlsx`).
4. Optionally log the total amount per category.

---

## ✅ Expected Output
- Aggregated DataTable or Excel with totals and counts per category.
- Example output:

| Category  | TotalAmount | Count |
| --------- | ----------- | ----- |
| OfficeSup | 1000        | 4     |
| ITEquip   | 2950        | 3     |
| Travel    | 1450        | 3     |

---
