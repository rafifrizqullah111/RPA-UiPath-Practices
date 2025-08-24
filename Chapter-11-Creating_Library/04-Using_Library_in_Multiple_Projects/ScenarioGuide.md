# 📂 Case 04 - Using Library in Multiple Projects

## 📄 Description
Import the previously created library into multiple UiPath projects and invoke its workflows to test reusability.  
This demonstrates how libraries simplify development and maintain consistency across automation projects.

---

## 🎯 Objectives
- Import a published library into different projects.  
- Map input/output arguments correctly when invoking library workflows.  
- Verify that the library functions consistently across projects.  
- Reinforce modular and reusable workflow design.

---

## 🛠️ Activities / Components
- `Manage Packages`  
- `Invoke Workflow`  
- `Arguments Mapping`  
- `Log Message` / `Write Line`  

---

## 📂 Sample Dataset
Inputs for testing library workflows:  
- Project 1: `quantity = 5`, `unitPrice = 100`, `discountPercent = 10`  
- Project 2: `quantity = 12`, `unitPrice = 50`, `discountPercent = 5`  

---

## 🚀 Hands-On Steps
1. Create two separate projects: `SalesProject1` and `SalesProject2`.  
2. In each project, go to `Manage Packages` and import the published library (`SalesLibrary`).  
3. Use `Invoke Workflow` to call the workflows from the library, e.g., `CalculateTotal` or `CalculateDiscountedTotal`.  
4. Map the input/output arguments correctly.  
5. Run the workflows in each project and log the outputs to verify correctness.  
6. Optionally, make changes to the library, update the version, and observe the updates in the projects.

---

## ✅ Expected Output
- **Project 1** → Inputs: `quantity = 5`, `unitPrice = 100`, `discountPercent = 10` → Output `totalAmount = 450`  
- **Project 2** → Inputs: `quantity = 12`, `unitPrice = 50`, `discountPercent = 5` → Output `totalAmount = 570`  
- Library functions correctly in multiple projects with consistent results.  
- Demonstrates modularity, reusability, and maintainability of workflows.
