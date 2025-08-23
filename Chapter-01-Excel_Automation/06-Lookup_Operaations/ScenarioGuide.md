# 📘 Case 06 - Lookup Operations

## 🎯 Objective
Learn how to perform lookup operations (VLOOKUP/INDEX-MATCH) in Excel using UiPath.

---

## 📝 Sample Data

**Students Table**

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

**Grades Table**

| MinScore | MaxScore | Grade |
|----------|----------|-------|
| 90       | 100      | A     |
| 80       | 89       | B     |
| 70       | 79       | C     |
| 60       | 69       | D     |
| 0        | 59       | F     |

---

## 🛠️ Steps
1. Read Students and Grades tables into DataTables.
2. Use **Lookup Data Table** or **VLOOKUP** formula to assign grade based on score.
3. Write the result back to Excel in a new column `Grade`.

---

## ✅ Expected Output
| ID  | Name    | Score | Grade |
|-----|---------|-------|-------|
| 1   | Alice   | 85    | B     |
| 2   | Bob     | 70    | C     |
| 3   | Charlie | 90    | A     |
| 4   | David   | 60    | D     |
| 5   | Eva     | 95    | A     |
| 6   | Frank   | 75    | C     |
| 7   | Grace   | 80    | B     |
| 8   | Helen   | 88    | B     |
| 9   | Ian     | 92    | A     |
| 10  | Jane    | 78    | C     |

---

## 📦 Covered Activities
- `Read Range`  
- `Lookup Data Table`  
- `Write Range`
