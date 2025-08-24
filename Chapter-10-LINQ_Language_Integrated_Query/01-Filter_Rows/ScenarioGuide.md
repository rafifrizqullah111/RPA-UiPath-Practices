# 📂 Case 01 - Filter Rows

## 📄 Description
Extract a subset of data from a DataTable, List, or Array based on specified conditions using LINQ.  
This is the fundamental scenario for filtering datasets without loops.

---

## 🎯 Objectives
- Learn to apply LINQ `Where` clause to filter data.  
- Reduce usage of nested `For Each` loops.  
- Export filtered results to Excel or new DataTable.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope`  
- `Assign` (for LINQ queries)  
- `CopyToDataTable` (convert filtered IEnumerable to DataTable)  
- `Write Range` (export result)  
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
2. Assign filtered data to a new DataTable using LINQ:  
   ```vbnet
   dtFiltered = dtOrders.AsEnumerable().
       Where(Function(r) r("Amount") > 500).
       CopyToDataTable()
   ```
3. Write dtFiltered to a new Excel sheet (Filtered_Orders.xlsx).
4. Log the count of filtered rows (optional).

---

## ✅ Expected Output
- Filtered DataTable or Excel file with orders where Amount > 500.
- Example output:

| OrderID	| Customer	| Amount | Category |
|---------|-----------|--------|----------|
| ORD002  |	Mark Chan |	1200	 | ITEquip  |
| ORD004  |	John Doe  |	800	   | ITEquip  |
| ORD007  |	Jane Doe  |	950	   | ITEquip  |
| ORD009  |	Amy Wong  |	700	   | Travel   |

---
