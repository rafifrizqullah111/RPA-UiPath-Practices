# 📘 Case 02 - Filtering Data

## 🎯 Objective
Learn how to filter Excel data using UiPath and save the result into a new sheet.

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
1. Use **Read Range** to load data into `dtStudents`
2. Apply **Filter Data Table** activity → Condition: `Score >= 80`
3. Save result into `dtPassed`
4. Use **Write Range** to save `dtPassed` into `Filtered.xlsx` → `Sheet1`

---

## ✅ Expected Output
| ID  | Name    | Score |
|-----|---------|-------|
| 1   | Alice   | 85    |
| 3   | Charlie | 90    |
| 6   | Fiona   | 88    |
| 8   | Hannah  | 92    |
| 10  | Julia   | 80    |

---

## 📦 Covered Activities
- `Filter Data Table`
- `Write Range`
