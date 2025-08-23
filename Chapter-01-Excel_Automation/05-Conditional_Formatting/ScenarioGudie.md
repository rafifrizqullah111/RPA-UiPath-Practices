# 📘 Case 05 - Conditional Formatting

## 🎯 Objective
Apply conditional formatting in Excel using UiPath activities.

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
| 10  | Jane    | 73    |

---

## 🛠️ Steps
1. Read data into DataTable.
2. Use **Conditional Formatting** to highlight `Score < 75` in Fail value.
3. Save changes back to Excel.

---

## ✅ Expected Output
- Rows with Score 70, 60, 75, 78 highlighted as a Fail value.

| ID  | Name    | Score | Result |
|-----|---------|-------|--------|
| 1   | Alice   | 85    |        |
| 2   | Bob     | 70    | Fail   |
| 3   | Charlie | 90    |        |
| 4   | David   | 60    | Fail   |
| 5   | Eva     | 95    |        |
| 6   | Frank   | 75    | Fail   |
| 7   | Grace   | 80    |        |
| 8   | Helen   | 88    |        |
| 9   | Ian     | 92    |        |
| 10  | Jane    | 73    | Fail   |

---

## 📦 Covered Activities
- `Read Range`  
- `Conditional Formatting`  
- `Write Range`
