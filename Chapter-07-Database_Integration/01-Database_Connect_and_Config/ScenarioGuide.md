# 📘 Case 01 - Database Connection & Configuration

## 🎯 Objective
Connect to a database (SQL/Oracle/MySQL) in UiPath and configure the connection securely for automation workflows.

---

## 📝 Sample Data
- Database: `SampleDB`  
- Tables: `Products`, `Orders`  
- Connection parameters (dummy):
  - Server: `db.example.com`
  - Database: `SampleDB`
  - User: `db_user`
  - Password: `********`
  - Provider: `System.Data.SqlClient` (for SQL Server)

---

## 🛠️ Steps
1. **Configure Connection**
   - Use **Connect** activity to set up the database connection.  
   - Provide server, database, username, password, and provider.  
   - Optionally, store credentials securely in **Windows Credential Manager** or Orchestrator assets.  

2. **Test Connection**
   - Use **Execute Query** or **Execute Non Query** to validate that the connection works.  
   - Catch errors with **Try Catch** if connection fails.  

3. **Disconnect**
   - Use **Disconnect** activity at the end of workflow to close the connection.

---

## ✅ Expected Output
- Connection established successfully to the target database.  
- Test query executes without errors.  
- Connection closed properly after workflow completes.  
- Logs indicate success or failure of connection attempt.

---

## 📦 Covered Activities
- `Connect`  
- `Disconnect`  
- `Execute Query` (for testing)  
- `Try Catch` (for error handling)  
- Secure credential handling (optional)
