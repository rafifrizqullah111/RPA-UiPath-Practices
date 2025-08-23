# 📘 Case 02 - Extract PDF Data Table

## 🎯 Objective
Extract structured tabular data from PDF documents for analysis.

---

## 📝 Sample Data
- PDF file: `sample_invoice.pdf`
- Example table (anonymized):

| Item   | Quantity | Price | Total  |
|--------|---------|-------|--------|
| AAA    | XX      | $XX   | $XXX   |
| BBB    | XX      | $XX   | $XXX   |
| CCC    | XX      | $XX   | $XXX   |
| ...    | ...     | ...   | ...    |

---

## 🛠️ Steps
1. Use **Read PDF Text** to extract full text from PDF.  
2. Apply **Generate Data Table** or Regex / String manipulation to parse tabular data.  
3. Store results into a DataTable or write to Excel.  

---

## ✅ Expected Output
- DataTable or Excel file containing structured table from PDF.  

---

## 📦 Covered Activities
- `Read PDF Text`  
- `Generate Data Table`  
- `Write Range`  
- Regex / String manipulation
