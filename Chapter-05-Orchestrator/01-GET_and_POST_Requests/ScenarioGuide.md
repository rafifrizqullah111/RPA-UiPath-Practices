# 📘 Case 01 - GET & POST Requests

## 🎯 Objective
Retrieve data from an API using GET requests and create new records using POST requests in UiPath.

---

## 📝 Sample Data
- API Endpoints (dummy):
  - GET: `https://api.example.com/products`
  - POST: `https://api.example.com/products`
- Sample GET Response (JSON, anonymized):
```json
[
  { "ProductID": "P001", "ProductName": "Product A", "Category": "Cat X", "Price": 100 },
  { "ProductID": "P002", "ProductName": "Product B", "Category": "Cat Y", "Price": 150 },
  { "ProductID": "P003", "ProductName": "Product C", "Category": "Cat X", "Price": 200 }
]
```
- Sample GET Response (JSON, anonymized):
```json
{
  "ProductID": "P010",
  "ProductName": "Product J",
  "Category": "Cat Z",
  "Price": 120
}
```

---

## 🛠️ Steps
1. GET Request
   - Use HTTP Request activity to call the GET endpoint.
   - Store response in a string variable.
   - Deserialize JSON into a DataTable using Deserialize JSON Array.
   - Iterate through rows with For Each Row to log or process data.
2. POST Request
   - Prepare payload as JSON string (use Assign activity).
   - Use HTTP Request activity to call the POST endpoint.
   - Include headers for authentication if required (Bearer token or API key).
   - Validate response for success (HTTP 200 / 201).
3. Optional: Write retrieved data from GET request into Excel using Write Range.

---

## ✅ Expected Output
- GET Request: DataTable contains all products returned by the API.
- POST Request: New product created successfully on the server.
- Excel (optional): Sheet contains product list from GET request.

---

## 📦 Covered Activities
- `HTTP Request`
- `Assign`
- `Deserialize JSON Array`
- `For Each Row`
- `Write Range`
- Authentication headers (Bearer token / API key)
