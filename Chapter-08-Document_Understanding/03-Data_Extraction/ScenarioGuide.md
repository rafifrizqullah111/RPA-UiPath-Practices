# 📂 Case 03 - Data Extraction

## 📄 Description
Extract structured information (like invoice numbers, dates, totals, or names) from documents.  
Focus on identifying key-value pairs or tabular data inside semi-structured PDFs or images.

---

## 🎯 Objectives
- Extract structured fields (Invoice No, Date, Total Amount, Vendor, etc).  
- Extract tabular data (line items in invoice/receipt).  
- Map extracted data to Excel or structured format.  
- Validate and clean extracted data.

---

## 🛠️ Activities / Components
- `Digitize Document`  
- `Intelligent Form Extractor` / `Document Understanding Extractor`  
- `Form Extractor`  
- `Validation Station`  
- `Write Range` (Excel)

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_Sample_01.pdf`  
- `Invoice_Sample_02.pdf`  
- `Receipt_Sample_01.pdf`

(*Use your own dummy files later*)

---

## 🚀 Hands-On Steps
1. Load PDF (invoice/receipt) into workflow.  
2. Digitize the document.  
3. Apply `Form Extractor` or `Intelligent Form Extractor`.  
4. Define fields to extract (Invoice No, Date, Amount, Vendor).  
5. Export extracted data to Excel.  
6. Validate results using `Validation Station`.

---

## ✅ Expected Output
- Extracted structured data in Excel format.  

- Example:

| FileName             | InvoiceNo | Date       | Vendor    | TotalAmount |
|-----------------------|-----------|------------|-----------|-------------|
| Invoice_Sample_01.pdf | INV-001   | 2025-01-15 | Vendor A  | 2,500.00    |
| Invoice_Sample_02.pdf | INV-002   | 2025-02-01 | Vendor B  | 3,800.00    |
| Receipt_Sample_01.pdf | RCP-123   | 2025-02-05 | Store C   | 150.00      |
