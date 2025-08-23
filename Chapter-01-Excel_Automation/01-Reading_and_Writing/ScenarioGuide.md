# 📘 Case 01 - Reading and Writing

## 🎯 Objective
Learn how to read data from Excel and write data back into Excel using UiPath Excel activities.

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
1. Use **Excel Application Scope** to open the workbook.
2. Use **Read Range** to read the data into a DataTable.
3. Modify or add new data (e.g., add a new row: `ID=11, Name=Kevin, Score=82`).
4. Use **Write Range** to write the updated DataTable back into Excel.

---

## ✅ Expected Output
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
| 11  | Kevin   | 82    |

---

## 📦 Covered Activities
- `Excel Application Scope`  
- `Read Range`  
- `Write Range`
