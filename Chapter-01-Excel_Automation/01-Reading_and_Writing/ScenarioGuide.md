# 📘 Case 01 - Basic Data Reading & Writing

## 🎯 Objective
Learn how to use UiPath Excel Modern Activities to:
- Read data from Excel
- Write data into a new sheet/file
- Append data to existing sheet

---

## 📝 Sample Data (Input: `Students.xlsx`)

| ID  | Name      | Score |
|-----|-----------|-------|
| 1   | Alice     | 85    |
| 2   | Bob       | 70    |
| 3   | Charlie   | 90    |
| 4   | Diana     | 60    |
| 5   | Ethan     | 75    |
| 6   | Fiona     | 88    |
| 7   | George    | 55    |
| 8   | Hannah    | 92    |
| 9   | Ian       | 65    |
| 10  | Julia     | 80    |

---

## 🛠️ Steps

1. Use **Excel Process Scope** → point to `Students.xlsx`
2. Inside scope, add **Read Range (Workbook)** to read `Sheet1`
3. Store result into variable `dtStudents`
4. Add **Write Range** activity to write `dtStudents` into `Output.xlsx` → `Sheet1`
5. Add **Append Range** activity to add the same data into `Sheet2`

---

## ✅ Expected Output

- **Output.xlsx (Sheet1)** contains the exact table above (copied from input)  
- **Output.xlsx (Sheet2)** contains duplicated table (from append)  

---

## 📦 Covered Activities
- `Excel Process Scope`
- `Read Range`
- `Write Range`
- `Append Range`
