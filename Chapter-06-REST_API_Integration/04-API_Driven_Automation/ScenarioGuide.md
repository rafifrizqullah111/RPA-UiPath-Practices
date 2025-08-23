# 📘 Case 04 - API-Driven Automation Workflow

## 🎯 Objective
Integrate multiple API calls (GET, POST, PUT/PATCH, DELETE) into an end-to-end business automation workflow in UiPath, including error handling and retry logic.

---

## 📝 Sample Data
- API Endpoints (dummy):
  - GET: `https://api.example.com/products`
  - POST: `https://api.example.com/products`
  - PUT/PATCH: `https://api.example.com/products/{ProductID}`
  - DELETE: `https://api.example.com/products/{ProductID}`
- Authentication:
  - Bearer Token: `Authorization: Bearer <token>`
- Workflow scenario (anonymized):
  1. Retrieve list of products (GET)  
  2. Add a new product if not exist (POST)  
  3. Update product price if conditions met (PUT/PATCH)  
  4. Remove discontinued products (DELETE)

---

## 🛠️ Steps
1. **Retrieve Data (GET)**
   - Use **HTTP Request** with authentication header.  
   - Deserialize JSON response into **DataTable** or **JObjects**.  

2. **Conditional Create / Update / Delete**
   - Iterate through data using **For Each Row**.  
   - Check conditions: product existence, category, price.  
   - Call **POST** to add new product if missing.  
   - Call **PUT/PATCH** to update product info.  
   - Call **DELETE** to remove discontinued products.  

3. **Error Handling & Retry**
   - Wrap API calls in **Try Catch**.  
   - Use **Retry Scope** for intermittent failures.  
   - Log messages using **Write Line** or **Log Message**.  

4. **Optional Output**
   - Write final product list to Excel using **Write Range**.  
   - Send notification email if critical errors occur (optional).

---

## ✅ Expected Output
- Products retrieved from API correctly.  
- New products added, existing products updated, discontinued products removed as per rules.  
- Errors handled gracefully; retries attempted for temporary failures.  
- Logs contain detailed success/failure messages.  
- Optional: Excel contains updated product list.

---

## 📦 Covered Activities
- `HTTP Request`  
- `Deserialize JSON`  
- `Assign`  
- `For Each Row`  
- `Try Catch`  
- `Retry Scope`  
- `Write Range`  
- Authentication headers (Bearer Token / API Key)
