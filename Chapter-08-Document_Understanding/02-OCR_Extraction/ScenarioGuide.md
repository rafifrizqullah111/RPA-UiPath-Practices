# 📂 Case 02 - OCR Extraction

## 📄 Description
Extract text from scanned or image-based documents using **OCR (Optical Character Recognition)**.  
This is useful for invoices, receipts, or contracts that are not machine-readable.

---

## 🎯 Objectives
- Convert image-based or scanned PDFs into text.  
- Use UiPath OCR engines (e.g., Tesseract, Microsoft, or Document OCR).  
- Handle multi-page documents.  
- Store OCR results for downstream processing.

---

## 🛠️ Activities / Components
- `Digitize Document`  
- `OCR Engine (Tesseract / Microsoft / UiPath Document OCR)`  
- `Read PDF with OCR`  
- `Write Text File` / `Write Range`

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_Scanned_01.pdf`  
- `Receipt_Scanned_01.pdf`  
- `Contract_Scanned_01.pdf`

(*Use your own dummy files later*)

---

## 🚀 Hands-On Steps
1. Input scanned PDF into workflow.  
2. Apply `Digitize Document` activity with preferred OCR engine.  
3. Extract full text or structured data.  
4. Write extracted results into `.txt` or `.xlsx` file for review.  
5. Validate if text accuracy is sufficient (>80%).  

---

## ✅ Expected Output
- Text content extracted from scanned documents.  

- Example (saved as `.txt` or Excel):

| FileName               | ExtractedText (sample)             | Confidence |
|-------------------------|------------------------------------|------------|
| Invoice_Scanned_01.pdf  | "Invoice No: XXXX, Amount: XXXX"  | 0.85       |
| Receipt_Scanned_01.pdf  | "Store: XXXX, Date: XXXX"         | 0.83       |
| Contract_Scanned_01.pdf | "Agreement between XXXX and XXXX" | 0.90       |
