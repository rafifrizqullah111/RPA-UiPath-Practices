# 📘 Case 02 - PUT & DELETE Requests

## 🎯 Objective
Update existing records using PUT/PATCH requests and remove records using DELETE requests via API in UiPath.

---

## 📝 Sample Data
- API Endpoints (dummy):
  - PUT/PATCH: `https://api.example.com/products/{ProductID}`
  - DELETE: `https://api.example.com/products/{ProductID}`
- Sample PUT/PATCH Payload (JSON, anonymized):
```json
{
  "ProductName": "Product A Updated",
  "Category": "Cat X",
  "Price": 110
}
```
- Sample DELETE Target:
  - ProductID = `P003`
 
---

## 🛠️ Steps
1. PUT Request
   - Prepare payload JSON string using Assign.
   - Use HTTP Request activity to call PUT/PATCH endpoint (replace {ProductID} dynamically).
   - Include headers for authentication if required.
   - Validate response for success (HTTP 200).
2. DELETE Request
   - Use HTTP Request activity to call DELETE endpoint (replace {ProductID} dynamically).
   - Include headers for authentication if required.
   - Validate response for success (HTTP 200 / 204).
3. Optional: Log success or failure messages using Write Line or Log Message.
4. Optional: Add Try Catch or Retry Scope for error handling.

---

## ✅ Expected Output
- PUT Request: Target product updated with new values.
- DELETE Request: Target product removed from the system.
- Logs indicate success or error messages correctly.

---

## 📦 Covered Activities
- `HTTP Request`
- `Assign`
- `Write Line` / `Log Message`
- `Try Catch` / `Retry Scope` (for error handling)
- Authentication headers (Bearer token / API key)
