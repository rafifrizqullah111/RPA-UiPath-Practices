# 📘 Case 07 - Error Handling & Exception

## 🎯 Objective
Handle UI automation failures with retry mechanisms and proper logging.

---

## 📝 Sample Data
- Tasks: Click button, extract data, submit form  

---

## 🛠️ Steps
1. Wrap automation actions in **Try Catch**.  
2. Use **Retry Scope** for elements that may fail intermittently.  
3. Log exceptions using **Log Message** or **Write Line**.  
4. Optionally, send email alert if critical error occurs.  

---

## ✅ Expected Output
- Errors are caught and handled gracefully.  
- Automation continues or stops safely based on exception rules.  

---

## 📦 Covered Activities
- `Try Catch`  
- `Retry Scope`  
- `Element Exists`  
- `Log Message`
