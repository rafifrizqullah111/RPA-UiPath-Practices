# 📂 Case 05 - Extract Data from Unstructured Documents

## 📄 Description
Extract important information (e.g., names, dates, amounts, reference numbers) from unstructured or semi-structured documents such as contracts, agreements, or letters.  
Unlike invoices or receipts, these documents have no fixed template, so extraction requires intelligent parsing.

---

## 🎯 Objectives
- Learn to handle unstructured text documents.  
- Use regex and ML Extractors for dynamic data extraction.  
- Export extracted data to Excel or CSV.  

---

## 🛠️ Activities / Components
- `Digitize Document`  
- `Regex Based Extractor`  
- `ML Extractor`  
- `Export Extraction Results`  
- `Write Range`  

---

## 📂 Sample Dataset (dummy placeholders)
- `Contract_Sample_01.pdf`  
- `Agreement_Sample_01.pdf`  
- `Letter_Sample_01.pdf`  

(*Replace with your own dummy files later*)

---

## 🚀 Hands-On Steps
1. Import PDF or scanned documents (contracts, agreements, letters).  
2. Digitize text content using `Digitize Document`.  
3. Apply `Regex Based Extractor` to capture common fields (e.g., Date → `\d{2}/\d{2}/\d{4}`).  
4. Use `ML Extractor` to identify dynamic fields such as party names, contract terms, or amounts.  
5. Export extracted results into structured Excel/CSV format.  

---

## ✅ Expected Output
- Extracted structured data table from unstructured documents.  
- Example Excel output:

| FileName              | Date       | PartyA          | PartyB          | Amount   |
|------------------------|------------|-----------------|-----------------|----------|
| Contract_Sample_01.pdf | 01/02/2024 | [Company A]     | [Company B]     | 10,000   |
| Agreement_Sample_01.pdf| 05/03/2024 | [Person X]      | [Person Y]      | N/A      |
| Letter_Sample_01.pdf   | 10/04/2024 | [Sender Name]   | [Recipient Name]| N/A      |
