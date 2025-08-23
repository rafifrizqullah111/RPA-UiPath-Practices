# 📘 Case 03 - Data Retrieval & Query Execution

## 🎯 Objective
Retrieve and filter data from database tables using SELECT queries in UiPath workflows, including joins and conditional filtering.

---

## 📝 Sample Data
- Database: `SampleDB`  
- Tables:
  
1. `Products`
   
| ProductID | ProductName | Category | Price |
|-----------|------------|---------|-------|
| P001      | Product A  | Cat X   | 100   |
| P002      | Product B  | Cat Y   | 150   |
| P003      | Product C  | Cat X   | 200   |

2. `Orders`
   
| OrderID | ProductID | Quantity | OrderDate  |
|---------|-----------|---------|------------|
| O001    | P001      | 2       | 2025-01-01 |
| O002    | P003      | 1       | 2025-01-05 |
| O003    | P002      | 3       | 2025-01-10 |

- Example Query: Retrieve product names and total quantity sold (join `Products` & `Orders`).

---

## ## 🛠️ Steps
1. **Execute Query**
   - Use **Execute Query** activity with SELECT statement.  
   - Example: 
     ```sql
     SELECT p.ProductName, SUM(o.Quantity) AS TotalSold
     FROM Products p
     JOIN Orders o ON p.ProductID = o.ProductID
     GROUP BY p.ProductName
     ```
   - Store result in a **DataTable** variable.  

2. **Filter / Process Data**
   - Use **For Each Row** to iterate through DataTable.  
   - Apply conditions or filters using **If** or LINQ (optional).  

3. **Optional Output**
   - Write retrieved and processed data to Excel using **Write Range**.  
   - Log results using **Write Line** or **Log Message**.

---

## ✅ Expected Output
- DataTable contains expected results from the query.  
- Each product shows total quantity sold correctly.  
- Optional: Excel sheet contains query results.  
- Logs reflect iteration and any applied filters.

---

## 📦 Covered Activities
- `Execute Query`  
- `DataTable`  
- `For Each Row`  
- `If` / LINQ (optional)  
- `Write Range` (optional)  
- `Write Line` / `Log Message`
