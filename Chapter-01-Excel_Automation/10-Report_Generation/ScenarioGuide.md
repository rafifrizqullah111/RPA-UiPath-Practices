# 📘 Case 10 - Report Generation

## 🎯 Objective
Generate a summary report in Excel using UiPath.

---

## 📝 Sample Data
| ID  | Name    | Department | Score |
|-----|---------|-----------|-------|
| 1   | Alice   | HR        | 85    |
| 2   | Bob     | IT        | 70    |
| 3   | Charlie | HR        | 90    |
| 4   | David   | IT        | 60    |
| 5   | Eva     | Finance   | 95    |
| 6   | Frank   | HR        | 75    |
| 7   | Grace   | IT        | 80    |
| 8   | Helen   | Finance   | 88    |
| 9   | Ian     | HR        | 92    |
| 10  | Jane    | IT        | 78    |

---

## 🛠️ Steps
1. Read data into DataTable.
2. Use **Group By / Pivot** to summarize average Score per Department.
3. Write summary report to a new sheet.

---

## ✅ Expected Output
| Department | Average Score |
|------------|---------------|
| HR         | 85.5          |
| IT         | 72.0          |
| Finance    | 91.5          |

---

## 📦 Covered Activities
- `Read Range`  
- `Group By / Pivot Table`  
- `Write Range`
