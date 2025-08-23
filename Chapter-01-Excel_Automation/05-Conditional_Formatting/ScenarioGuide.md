# 📘 Case 05 - Data Cleaning

## 🎯 Objective
Handle missing or invalid data in Excel.

---

## 📝 Sample Data (with some blanks)

| ID  | Name      | Score |
|-----|-----------|-------|
| 1   | Alice     | 85    |
| 2   | (blank)   | 70    |
| 3   | Charlie   |       |
| 4   | Diana     | 60    |
| 5   | Ethan     | 75    |
| 6   | Fiona     | 88    |
| 7   | George    |       |
| 8   | Hannah    | 92    |
| 9   | Ian       | 65    |
| 10  | Julia     | 80    |

---

## 🛠️ Steps
1. Read Excel into `dtStudents`
2. Loop rows:
   - If `Name` = blank → replace with `"Unknown"`
   - If `Score` = blank → replace with `0`
3. Write cleaned data into `Cleaned.xlsx`

---

## ✅ Expected Output
| ID  | Name      | Score |
|-----|-----------|-------|
| 1   | Alice     | 85    |
| 2   | Unknown   | 70    |
| 3   | Charlie   | 0     |
| 4   | Diana     | 60    |
| 5   | Ethan     | 75    |
| 6   | Fiona     | 88    |
| 7   | George    | 0     |
| 8   | Hannah    | 92    |
| 9   | Ian       | 65    |
| 10  | Julia     | 80    |

---

## 📦 Covered Activities
- `If`
- `Assign`
- `For Each Row`
