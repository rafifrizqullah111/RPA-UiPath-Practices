# 📘 Case 02 - Filtering Data

## 🎯 Objective
Learn how to filter data in Excel using UiPath activities.

---

## 📝 Sample Data
| ID  | Name    | Score |
|-----|---------|-------|
| 1   | Alice   | 85    |
| 2   | Bob     | 70    |
| 3   | Charlie | 90    |
| 4   | David   | 60    |
| 5   | Eva     | 95    |
| 6   | Frank   | 75    |
| 7   | Grace   | 80    |
| 8   | Helen   | 88    |
| 9   | Ian     | 92    |
| 10  | Jane    | 78    |

---

## 🛠️ Steps
1. Read data into a DataTable using **Read Range**.
2. Use **Filter Data Table** to select rows where `Score >= 80`.
3. Output the filtered table to a new sheet or variable.

---

## ✅ Expected Output
| ID  | Name    | Score |
|-----|---------|-------|
| 1   | Alice   | 85    |
| 3   | Charlie | 90    |
| 5   | Eva     | 95    |
| 7   | Grace   | 80    |
| 8   | Helen   | 88    |
| 9   | Ian     | 92    |

---

## 📦 Covered Activities
- `Read Range`  
- `Filter Data Table`  
- `Write Range`
