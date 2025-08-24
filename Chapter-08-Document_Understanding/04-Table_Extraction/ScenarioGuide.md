# 📂 Case 04 - Table Extraction

## 📄 Description
Extract tabular data from documents such as invoices, purchase orders, or bank statements.  
This is useful when documents contain line-item details that need to be processed and exported into structured formats.

---

## 🎯 Objectives
- Digitize and detect tables from PDF or scanned documents.  
- Extract multiple rows and columns of structured data.  
- Export the extracted table into Excel or database.  

---

## 🛠️ Activities / Components
- `Digitize Document`  
- `Table Extraction Scope`  
- `Form Extractor` / `ML Extractor` (optional for complex layouts)  
- `Export Extraction Results`  

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_WithLineItems.pdf`  
- `PurchaseOrder_Table.pdf`  
- `BankStatement_Sample.pdf`

(*Replace with your own dummy files later*)

---

## 🚀 Hands-On Steps
1. Import PDF documents containing tables.  
2. Digitize documents using `Digitize Document`.  
3. Configure `Table Extraction Scope` to detect table regions.  
4. Map extracted data fields (e.g., Item, Qty, Price, Total).  
5. Export the extracted tables into Excel format.  
6. Validate accuracy by comparing Excel results with original PDFs.  

---

## ✅ Expected Output
- Excel file containing extracted tables with rows and columns aligned.  
- Example:  

| Item        | Qty | Unit Price | Total |
|-------------|-----|------------|-------|
| Product A   |  10 |     5.00   | 50.00 |
| Product B   |   2 |    12.00   | 24.00 |
| Product C   |   5 |     8.00   | 40.00 |

---
