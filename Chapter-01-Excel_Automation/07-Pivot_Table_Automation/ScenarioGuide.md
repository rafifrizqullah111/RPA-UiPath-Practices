# 📘 Case 07 - Pivot Table Automation

## 🎯 Objective
Learn to create Pivot Tables in Excel using UiPath.

---

## 📝 Sample Data
| ID  | Name    | Subject  | Score |
|-----|---------|---------|-------|
| 1   | Alice   | Math    | 85    |
| 2   | Bob     | Math    | 70    |
| 3   | Charlie | Math    | 90    |
| 4   | David   | Science | 60    |
| 5   | Eva     | Science | 95    |
| 6   | Frank   | Math    | 75    |
| 7   | Grace   | Science | 80    |
| 8   | Helen   | Math    | 88    |
| 9   | Ian     | Science | 92    |
| 10  | Jane    | Science | 78    |

---

## 🛠️ Steps
1. Read data into DataTable.
2. Use **Create Pivot Table** activity.
   - Row: `Subject`
   - Values: `Score` (Average)
3. Output the Pivot Table to a new sheet.

---

## ✅ Expected Output

| Subject  | Average of Score |
|----------|----------------|
| Math     | 82             |
| Science  | 81             |

---

## 📦 Covered Activities
- `Read Range`  
- `Create Pivot Table`  
- `Write Range`
