# 📘 Case 03 - Sorting Data

## 🎯 Objective
Learn how to sort data in Excel using UiPath activities.

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
2. Use **Sort Data Table** to sort by `Score` descending.
3. Output the sorted table back to Excel.

---

## ✅ Expected Output
| ID  | Name    | Score |
|-----|---------|-------|
| 5   | Eva     | 95    |
| 9   | Ian     | 92    |
| 3   | Charlie | 90    |
| 8   | Helen   | 88    |
| 1   | Alice   | 85    |
| 7   | Grace   | 80    |
| 10  | Jane    | 78    |
| 6   | Frank   | 75    |
| 2   | Bob     | 70    |
| 4   | David   | 60    |

---

## 📦 Covered Activities
- `Read Range`  
- `Sort Data Table`  
- `Write Range`
