# 📘 Case 03 - Authentication & Token Management

## 🎯 Objective
Handle secure API access using API keys, Bearer tokens, or OAuth2 in UiPath workflows.

---

## 📝 Sample Data
- API Endpoints (dummy):
  - GET: `https://api.example.com/products`
  - POST: `https://api.example.com/products`
- Authentication types:
  - API Key: `X-API-KEY: ABC123XYZ`
  - Bearer Token: `Authorization: Bearer <token>`
  - OAuth2 (client credentials): ClientID = `CLIENT123`, ClientSecret = `SECRET456`
- Token endpoint (for OAuth2): `https://api.example.com/token`

---

## 🛠️ Steps
1. **API Key / Bearer Token**
   - Add authentication headers in **HTTP Request** activity.  
   - Assign token or API key to header variable if needed.  

2. **OAuth2 Token Retrieval**
   - Use **HTTP Request** activity to call token endpoint with client credentials.  
   - Deserialize JSON response to extract access token using **Deserialize JSON**.  
   - Store token in a variable for subsequent API calls.  

3. **Using Token in API Calls**
   - Pass token dynamically in header for GET, POST, PUT/PATCH, DELETE requests.  
   - Validate that request succeeds with correct authentication.  

4. Optional: Log token retrieval success and API response status.

---

## ✅ Expected Output
- API calls succeed using API key, Bearer token, or OAuth2 token.  
- Tokens retrieved correctly and stored for reuse.  
- Workflow demonstrates secure API access in all HTTP requests.

---

## 📦 Covered Activities
- `HTTP Request`  
- `Assign`  
- `Deserialize JSON`  
- `Write Line` / `Log Message`  
- Authentication headers (API Key / Bearer / OAuth2)
