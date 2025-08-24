# 📂 Case 02 - Exception-Handled Library

## 📄 Description
Create a reusable library workflow that calculates discounted total sales and handles potential exceptions, such as negative quantity or price values.  
This ensures the workflow is robust and reliable across projects.

---

## 🎯 Objectives
- Build a parameterized workflow to compute discounted total.  
- Implement exception handling for invalid inputs.  
- Log errors and provide default or fallback values.  
- Publish as a library and reuse in multiple projects.

---

## 🛠️ Activities / Components
- `Sequence` / `Flowchart`  
- `Assign`  
- `If`  
- `Try Catch`  
- `Log Message`  
- `Throw`  
- `Arguments` (In/Out)  
- `Invoke Workflow`  
- `Publish Library`

---

## 📂 Sample Dataset
- No external dataset required for this case.  
- Example input parameters:  
  - `quantity` = 10  
  - `unitPrice` = 50.0  
  - `discountPercent` = 10  

---

## 🚀 Hands-On Steps
1. Create a new workflow called `CalculateDiscountedTotal.xaml`.  
2. Add In arguments: `quantity` (Int), `unitPrice` (Double), `discountPercent` (Double).  
3. Add Out argument: `totalAmount` (Double).  
4. Inside the workflow, wrap calculation inside a `Try Catch` activity.  
5. Use `Assign` to compute:  
   ```vbnet
   If quantity < 0 Or unitPrice < 0 Then
       Throw New BusinessRuleException("Quantity or Unit Price cannot be negative")
   Else
       totalAmount = quantity * unitPrice * (1 - discountPercent/100)
   End If
   ```
6. Log any exceptions caught and set totalAmount = 0 in case of errors.
7. Publish the workflow as a library (SalesLibrary).
8. Create a new project, import the library, and invoke the workflow with different inputs to test exception handling.

---

## ✅ Expected Output
- For valid inputs:
  - `quantity = 10`, `unitPrice = 50`, `discountPercent = 10` → `totalAmount = 450.0`
- For invalid inputs (e.g., negative values):
  - Workflow logs the error: `"Quantity or Unit Price cannot be negative"`
  - `totalAmount = 0` as fallback.
- Library is reusable with robust exception handling across projects.
