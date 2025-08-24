# 📂 Case 05 - Join Two Tables

## 📄 Description
Combine data from two different DataTables by matching keys using LINQ.  
Useful for merging reference data, lookups, or combining multiple sources for processing.

---

## 🎯 Objectives
- Learn to perform inner and left joins with LINQ.  
- Merge data from multiple tables based on a common key.  
- Export joined data to Excel for further processing.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope` (for both tables)  
- `Assign` (for LINQ join query)  
- `CopyToDataTable` (convert IEnumerable to DataTable)  
- `Write Range` (export joined table)  
- `Log Message` (optional, for verification)

---

## 📂 Sample Dataset
**Orders.xlsx**  
| OrderID | Customer   | Amount | Category  |
|---------|------------|--------|-----------|
| ORD001  | Alice Wong | 250    | OfficeSup |
| ORD002  | Mark Chan  | 1200   | ITEquip   |
| ORD003  | Lina Kim   | 450    | Travel    |
| ORD004  | John Doe   | 800    | ITEquip   |
| ORD005  | Maria Lee  | 150    | OfficeSup |

**Customers.xlsx**  
| Customer   | Region    | VIP  |
|------------|-----------|------|
| Alice Wong | Asia      | Yes  |
| Mark Chan  | Europe    | No   |
| Lina Kim   | Asia      | No   |
| John Doe   | America   | Yes  |
| Maria Lee  | Europe    | No   |

---

## 🚀 Hands-On Steps
1. Read `Orders.xlsx` and `Customers.xlsx` into DataTables (`dtOrders` and `dtCustomers`).  
2. Perform an inner join on `Customer` using LINQ:  
   ```vbnet
   dtJoined = (From o In dtOrders.AsEnumerable()
               Join c In dtCustomers.AsEnumerable()
               On o("Customer") Equals c("Customer")
               Select dtOrders.NewRow(o("OrderID"), o("Customer"), o("Amount"), o("Category"), c("Region"), c("VIP"))
              ).CopyToDataTable()
   ```
3. Write dtJoined to a new Excel sheet (Joined_Orders.xlsx).
4. Optionally, log the count of joined rows.

---

## ✅ Expected Output
- Joined DataTable or Excel combining order and customer info.
- Example output:

| OrderID | Customer   | Amount | Category  | Region  | VIP |
| ------- | ---------- | ------ | --------- | ------- | --- |
| ORD001  | Alice Wong | 250    | OfficeSup | Asia    | Yes |
| ORD002  | Mark Chan  | 1200   | ITEquip   | Europe  | No  |
| ORD003  | Lina Kim   | 450    | Travel    | Asia    | No  |
| ORD004  | John Doe   | 800    | ITEquip   | America | Yes |
| ORD005  | Maria Lee  | 150    | OfficeSup | Europe  | No  |

---
