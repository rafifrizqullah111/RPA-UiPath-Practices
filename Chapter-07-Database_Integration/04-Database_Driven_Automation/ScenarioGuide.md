# 📘 Case 04 - Database Driven Automation Workflow

## 🎯 Objective
Integrate database operations (CRUD and queries) into an end-to-end automation workflow in UiPath, including conditional logic, error handling, and logging.

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

- Workflow scenario (anonymized):
  1. Retrieve all products (SELECT)  
  2. Add missing products (INSERT)  
  3. Update prices if certain conditions are met (UPDATE)  
  4. Remove discontinued products (DELETE)

---

## 🛠️ Steps
1. **Retrieve Data**
   - Use **Execute Query** to fetch product list.  
   - Store results in a **DataTable**.  

2. **Conditional CRUD Operations**
   - Iterate through DataTable using **For Each Row**.  
   - Use **If** activities to decide:  
     - INSERT new product if missing  
     - UPDATE price if condition met  
     - DELETE discontinued product  

3. **Error Handling & Transaction**
   - Wrap operations in **Try Catch**.  
   - Use **Begin Transaction** / **Commit / Rollback** to maintain data integrity.  
   - Log messages with **Write Line** or **Log Message**.

4. **Optional Output**
   - Write final product table to Excel using **Write Range**.  
   - Notify via email if workflow encounters critical errors (optional).

---

## ✅ Expected Output
- Products table updated correctly with insertions, updates, and deletions.  
- Queries return correct results.  
- Errors are handled gracefully; transactions maintain integrity.  
- Logs reflect operation outcomes.  
- Optional: Excel contains final product data.

---

## 📦 Covered Activities
- `Execute Query`  
- `Execute Non Query`  
- `For Each Row`  
- `If`  
- `Try Catch`  
- `Begin Transaction / Commit / Rollback` (optional)  
- `Write Range` (optional)  
- `Write Line` / `Log Message`
