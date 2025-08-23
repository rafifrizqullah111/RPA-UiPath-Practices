# 📘 Case 08 - Data Merging

## 🎯 Objective
Merge data from two Excel files.

---

## 📝 Sample Data

### Students.xlsx
| ID | Name   | Score |
|----|--------|-------|
| 1  | Alice  | 85    |
| 2  | Bob    | 70    |

### Extra.xlsx
| ID | Department |
|----|------------|
| 1  | Science    |
| 2  | Arts       |

---

## 🛠️ Steps
1. Read both Excels into `dt1` and `dt2`
2. Use **Join Data Table** → join on `ID`
3. Write result into `Merged.xlsx`

---

## ✅ Expected Output
| ID | Name  | Score | Department |
|----|-------|-------|------------|
| 1  | Alice | 85    | Science    |
| 2  | Bob   | 70    | Arts       |

---

## 📦 Covered Activities
- `Join Data Table`
