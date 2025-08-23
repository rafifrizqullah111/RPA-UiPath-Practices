# 📘 Case 02 - CRUD Operations (Insert / Update / Delete)

## 🎯 Objective
Perform Create, Read, Update, and Delete operations on database tables in UiPath workflows.

---

## 📝 Sample Data
- Database: `SampleDB`  
- Table: `Products`
  
| ProductID | ProductName | Category | Price |
|-----------|------------|---------|-------|
| P001      | Product A  | Cat X   | 100   |
| P002      | Product B  | Cat Y   | 150   |
| P003      | Product C  | Cat X   | 200   |

---

## 🛠️ Steps
1. **INSERT Operation**
   - Use **Execute Non Query** activity with SQL INSERT statement.  
   - Example: Add new product `P010` to `Products` table.  

2. **UPDATE Operation**
   - Use **Execute Non Query** activity with SQL UPDATE statement.  
   - Example: Update `Price` of `P001` to 110.  

3. **DELETE Operation**
   - Use **Execute Non Query** activity with SQL DELETE statement.  
   - Example: Remove `P003` from `Products` table.  

4. **Optional: Transaction Management**
   - Use **Begin Transaction** and **Commit/Rollback** to ensure data integrity.  
   - Wrap operations in **Try Catch** to handle errors gracefully.

---

## ✅ Expected Output
- INSERT: New product added to the table.  
- UPDATE: Target product price updated correctly.  
- DELETE: Target product removed successfully.  
- Logs indicate success or failure of each operation.  
- Database integrity maintained with transaction management (if used).

---

## 📦 Covered Activities
- `Execute Non Query`  
- `Try Catch`  
- `Begin Transaction / Commit / Rollback` (optional)  
- Logging with `Write Line` or `Log Message`
