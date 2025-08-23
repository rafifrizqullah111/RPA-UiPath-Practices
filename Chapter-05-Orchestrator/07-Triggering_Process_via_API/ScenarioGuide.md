# 📘 Case 07 - Triggering Processes via API / External Events

## 🎯 Objective
Start jobs or processes using Orchestrator API or webhook integration.

---

## 📝 Sample Data
- Processes: `InvoiceProcessing`, `ReportGeneration`  
- API endpoint: `https://orchestrator.example.com/odata/Jobs/UiPath.Server.Configuration.OData.StartJobs`  

---

## 🛠️ Steps
1. Use Orchestrator API or HTTP Request to trigger process execution.  
2. Send required parameters (process name, robot, input arguments).  
3. Monitor job status via API response or dashboard.  

---

## ✅ Expected Output
- Jobs triggered successfully via API.  
- Input parameters passed correctly.  
- Job execution status reflected in Orchestrator.  

---

## 📦 Covered Activities
- HTTP Request / Orchestrator API  
- Trigger Job  
- Monitor Job Status
