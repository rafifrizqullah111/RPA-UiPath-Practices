# 📂 Case 01 - Simple & Parameterized Library

## 📄 Description
Create a reusable workflow performing a basic calculation, such as computing total sales from quantity and unit price.  
Parameterize it to accept inputs and return outputs, making it reusable across multiple projects.

---

## 🎯 Objectives
- Build a simple workflow and convert it into a library.  
- Parameterize workflows using In/Out arguments.  
- Invoke the library workflow in a sample project.

---

## 🛠️ Activities / Components
- `Sequence` / `Flowchart`  
- `Assign`  
- `Invoke Workflow`  
- `Arguments` (In/Out)  
- `Write Line` / `Log Message`  
- `Publish Library`

---

## 📂 Sample Dataset
- No external dataset required for this case.  
- Example input parameters:  
  - `quantity` = 5  
  - `unitPrice` = 120.5  

---

## 🚀 Hands-On Steps
1. Create a new workflow called `CalculateTotal.xaml`.  
2. Add In arguments: `quantity` (Int), `unitPrice` (Double).  
3. Add Out argument: `totalAmount` (Double).  
4. Inside the workflow, use `Assign` to calculate:  
   ```vbnet
   totalAmount = quantity * unitPrice
   ```
5. Log or output the totalAmount.
6. Publish the workflow as a library (SalesLibrary).
7. Create a new project and add the published library via Manage Packages.
8. Invoke CalculateTotal workflow with sample inputs and verify the output.

---

## ✅ Expected Output
- When quantity = 5 and unitPrice = 120.5, the output totalAmount should be: `602.5`
- Library workflow is reusable in other projects with different quantities and prices.

---

