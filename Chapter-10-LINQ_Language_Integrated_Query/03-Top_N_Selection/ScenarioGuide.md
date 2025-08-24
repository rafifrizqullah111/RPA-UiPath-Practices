# 📂 Case 03 - Top-N Selection

## 📄 Description
Select the top N records from a dataset based on a numeric or sortable column.  
This is useful for identifying highest sales, largest transactions, or top-performing customers.

---

## 🎯 Objectives
- Learn to sort data in ascending or descending order using LINQ.  
- Extract only the top N rows.  
- Export results to Excel for reporting purposes.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope`  
- `Assign` (for LINQ queries with OrderBy / Take)  
- `CopyToDataTable` (convert IEnumerable to DataTable)  
- `Write Range` (export top-N results)  
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
2. Assign top-N records using LINQ (e.g., top 3 by Amount):  
   ```vbnet
   dtTop3 = dtOrders.AsEnumerable().
       OrderByDescending(Function(r) r("Amount")).
       Take(3).
       CopyToDataTable()
   ```

3. Write dtTop3 to a new Excel sheet (Top3_Orders.xlsx).
4. Optionally log top-N order details.

## ✅ Expected Output
- DataTable or Excel containing top 3 transactions by Amount.
- Example output:

| OrderID | Customer  | Amount | Category |
| ------- | --------- | ------ | -------- |
| ORD002  | Mark Chan | 1200   | ITEquip  |
| ORD007  | Jane Doe  | 950    | ITEquip  |
| ORD004  | John Doe  | 800    | ITEquip  |

---
