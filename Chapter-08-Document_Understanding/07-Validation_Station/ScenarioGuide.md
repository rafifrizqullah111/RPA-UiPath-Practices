# 📂 Case 07 - Validation Station (Human-in-the-loop)

## 📄 Description
Integrate **Validation Station** into the Document Understanding workflow to allow a human user to review, correct, and confirm extracted data.  
This ensures higher accuracy for critical business documents before final processing.

---

## 🎯 Objectives
- Learn how to implement **human-in-the-loop validation**.  
- Configure **Validation Station** for reviewing extracted fields.  
- Store corrected results back into workflow.  
- Understand when and why human validation is necessary.  

---

## 🛠️ Activities / Components
- `Digitize Document`  
- `Data Extraction Scope`  
- `Validation Station`  
- `Export Extraction Results`  
- `Write Range`  

---

## 📂 Sample Dataset (dummy placeholders)
- `Invoice_With_NoisyData_01.pdf`  
- `Receipt_BlurryScan_01.pdf`  
- `PurchaseOrder_PartialText_01.pdf`  

(*Replace with your own scanned or error-prone documents later*)

---

## 🚀 Hands-On Steps
1. Import scanned documents with OCR/partial extraction issues.  
2. Digitize documents using **OCR Engine**.  
3. Run **Data Extraction Scope** with multiple extractors (Regex, ML, Keyword-based).  
4. Route extracted data into **Validation Station**.  
5. Manually validate or correct extracted fields (e.g., Invoice Date, Amount, Vendor Name).  
6. Confirm results and export corrected data into Excel or database.  

---

## ✅ Expected Output
- Human validation screen displayed with extracted fields.  
- Corrected data saved after user approval.  
- Example Excel output:

| FileName                    | Extracted_Vendor | Corrected_Vendor | Extracted_Amount | Corrected_Amount |
|------------------------------|------------------|------------------|------------------|------------------|
| Invoice_With_NoisyData_01.pdf | VndorX          | VendorX Ltd      | 100              | 100              |
| Receipt_BlurryScan_01.pdf     | ReciiptCo       | ReceiptCo        | 55               | 55               |

