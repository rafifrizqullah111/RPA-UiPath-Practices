# 📂 Case 06 - Distinct & Deduplication

## 📄 Description
Remove duplicate entries and extract unique values from a dataset using LINQ.  
This helps ensure data integrity and simplifies further processing.

---

## 🎯 Objectives
- Learn to use `Distinct` to eliminate duplicates.  
- Apply deduplication based on a single column or multiple columns.  
- Export cleaned data to Excel or DataTable.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope`  
- `Assign` (for LINQ `Distinct` queries)  
- `CopyToDataTable` (convert IEnumerable to DataTable)  
- `Write Range` (export cleaned dataset)  
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
  | ORD011  | Alice Wong | 250    | OfficeSup |
  | ORD012  | John Doe   | 800    | ITEquip   |

---

## 🚀 Hands-On Steps
1. Read `Orders.xlsx` into a DataTable (`dtOrders`).  
2. Remove duplicates based on `OrderID` using LINQ:  
   ```vbnet
   dtDistinct = dtOrders.AsEnumerable().
       GroupBy(Function(r) r("OrderID")).
       Select(Function(g) g.First()).
       CopyToDataTable()
   ```
3. Optionally, remove duplicates based on multiple columns:
   ```vbnet
   dtDistinctMulti = dtOrders.AsEnumerable().
       GroupBy(Function(r) New With { Key .Customer = r("Customer"), Key .Amount = r("Amount") }).
       Select(Function(g) g.First()).
       CopyToDataTable()
   ```
4. Write dtDistinct or dtDistinctMulti to a new Excel sheet (Cleaned_Orders.xlsx).
5. Log the count of distinct rows.

---
 
## ✅ Expected Output
- Cleaned DataTable or Excel with unique orders.
- Example output (based on OrderID):

| OrderID | Customer   | Amount | Category  |
| ------- | ---------- | ------ | --------- |
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

