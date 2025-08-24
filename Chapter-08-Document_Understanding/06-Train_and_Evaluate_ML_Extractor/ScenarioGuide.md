# 📂 Case 06 - Train & Evaluate ML Extractor

## 📄 Description
Train a custom **Machine Learning Extractor** to improve accuracy when extracting data from documents.  
This case focuses on building a training dataset, uploading it to AI Center, and evaluating the extractor’s performance.

---

## 🎯 Objectives
- Understand how to create training datasets for ML Extractor.  
- Upload and manage datasets in UiPath AI Center.  
- Train, evaluate, and deploy a custom ML Extractor.  
- Compare performance vs Regex/Keyword-based methods.  

---

## 🛠️ Activities / Components
- `Data Labeling Session`  
- `ML Extractor`  
- `Export Extraction Results`  
- **UiPath AI Center** (for training & evaluation)  
- `Evaluate Extraction Results`  

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_TrainSet_01.pdf`  
- `Invoice_TrainSet_02.pdf`  
- `Receipt_TrainSet_01.pdf`  
- `Contract_TrainSet_01.pdf`  

(*Replace with your own labeled training documents later*)

---

## 🚀 Hands-On Steps
1. Collect and prepare a dataset of documents (invoices, receipts, contracts).  
2. Use **Data Labeling Station** to manually tag important fields (Invoice No, Date, Amount, Vendor).  
3. Upload labeled dataset to **AI Center**.  
4. Train a new **ML Extractor model** using the dataset.  
5. Deploy trained ML model and connect it to Document Understanding workflow.  
6. Run workflow with new documents to evaluate accuracy.  
7. Compare results with Regex Extractor baseline.  

---

## ✅ Expected Output
- A trained and deployed ML Extractor model.  
- Evaluation report showing precision/recall or accuracy score.  
- Example Excel output (predicted vs actual):

| FileName             | Extracted_Amount | Actual_Amount | Status    |
|-----------------------|------------------|---------------|-----------|
| Invoice_TrainSet_01.pdf | 1200             | 1200          | ✅ Correct |
| Invoice_TrainSet_02.pdf | 980              | 1000          | ❌ Wrong   |
| Receipt_TrainSet_01.pdf | 250              | 250           | ✅ Correct |

