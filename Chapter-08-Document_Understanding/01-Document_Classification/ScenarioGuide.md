# 📂 Case 01 - Document Classification

## 📄 Description
Automatically classify incoming business documents into predefined categories (e.g., Invoices, Receipts, Forms).  
This is the first step in most **Document Understanding** workflows before extraction.

---

## 🎯 Objectives
- Learn how to use UiPath **Taxonomy Manager**.  
- Digitize scanned documents for processing.  
- Apply **classification models** to assign document type.  
- Use **Classification Station** for human validation when confidence is low.

---

## 🛠️ Activities / Components
- `Taxonomy Manager`  
- `Load Taxonomy`  
- `Digitize Document`  
- `Classify Document Scope`  
- `Present Classification Station`  
- `Export Extraction Results`

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_Sample_01.pdf`  
- `Receipt_Sample_01.pdf`  
- `HR_Form_Sample_01.pdf`

(*Use your own dummy files later*)

---

## 🚀 Hands-On Steps
1. Define document categories (Invoice, Receipt, Form) in **Taxonomy Manager**.  
2. Use `Load Taxonomy` to bring definitions into workflow.  
3. Add `Digitize Document` to convert input PDFs into machine-readable text.  
4. Use `Classify Document Scope` with chosen classifier (Keyword, ML, or Regex).  
5. If classifier confidence is below threshold → trigger `Present Classification Station` for manual check.  
6. Save classification results into output file (Excel/CSV).

---

## ✅ Expected Output
- Each document is tagged with a **document type**:  
  - `Invoice`  
  - `Receipt`  
  - `Form`  

- Output file example (Excel/CSV):

| FileName              | ClassifiedAs | Confidence |
|------------------------|--------------|------------|
| Invoice_Sample_01.pdf  | Invoice      | 0.92       |
| Receipt_Sample_01.pdf  | Receipt      | 0.87       |
| HR_Form_Sample_01.pdf  | Form         | 0.95       |
