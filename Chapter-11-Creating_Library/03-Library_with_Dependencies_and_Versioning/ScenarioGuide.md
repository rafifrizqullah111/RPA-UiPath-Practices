# 📂 Case 03 - Library with Dependencies & Versioning

## 📄 Description
Create a library workflow that depends on other internal workflows or NuGet packages, and publish it with proper versioning.  
This ensures modularity, maintainability, and version control across enterprise projects.

---

## 🎯 Objectives
- Build a workflow library that calls other internal workflows.  
- Manage external dependencies via NuGet packages.  
- Apply versioning to published libraries.  
- Ensure reusability and traceability in multiple projects.

---

## 🛠️ Activities / Components
- `Sequence` / `Flowchart`  
- `Invoke Workflow`  
- `Arguments` (In/Out)  
- `Manage Packages`  
- `Publish Library`  
- `Log Message`  

---

## 📂 Sample Dataset
- Internal workflows to invoke:  
  - `CalculateTotal.xaml` (from Case 01)  
  - `CalculateDiscountedTotal.xaml` (from Case 02)  
- Sample inputs:  
  - `quantity = 8`  
  - `unitPrice = 75.0`  
  - `discountPercent = 15`  

---

## 🚀 Hands-On Steps
1. Create a new workflow called `ProcessSalesLibrary.xaml`.  
2. Add In arguments: `quantity` (Int), `unitPrice` (Double), `discountPercent` (Double).  
3. Add Out argument: `finalAmount` (Double).  
4. Inside the workflow, invoke `CalculateTotal.xaml` and `CalculateDiscountedTotal.xaml` workflows using `Invoke Workflow`.  
5. Handle dependencies:  
   - Ensure the internal workflows are included in the library project.  
   - Add any required NuGet packages via `Manage Packages`.  
6. Publish the library with version number (e.g., `1.0.0`).  
7. Test library in a separate project by importing it and invoking `ProcessSalesLibrary`.  

---

## ✅ Expected Output
- For inputs `quantity = 8`, `unitPrice = 75.0`, `discountPercent = 15`:  
  - `finalAmount = 510.0`  
- Library references internal workflows correctly.  
- Dependencies are resolved automatically when library is imported in other projects.  
- Versioning allows tracking changes and updates.
