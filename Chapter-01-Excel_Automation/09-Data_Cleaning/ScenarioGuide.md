# 📘 Case 09 - Data Cleaning

## 🎯 Objective
Clean messy data in Excel using UiPath.

---

## 📝 Sample Data
| ID  | Name      | Email               | Score |
|-----|-----------|-------------------|-------|
| 1   | Alice     | alice@gmail.com    | 85    |
| 2   | Bob       | bob@gmail          | 70    |
| 3   | Charlie   | charlie@gmail.com  | 90    |
| 4   | David     |                   | 60    |
| 5   | Eva       | eva@gmail.com      | 95    |
| 6   | Frank     | frank@domain.com   | 75    |
| 7   | Grace     | grace@gmail.com    | 80    |
| 8   | Helen     | helen@gmail        | 88    |
| 9   | Ian       | ian@gmail.com      | 92    |
| 10  | Jane      | jane@domain.com    | 78    |

---

## 🛠️ Steps
1. Read data into DataTable.
2. Use **Remove Duplicate Rows**.
3. Use **Replace/Regex** to fix invalid emails.
4. Handle missing `Email` by filling `N/A`.

---

## ✅ Expected Output
| ID  | Name    | Email              | Score |
|-----|---------|------------------|-------|
| 1   | Alice   | alice@gmail.com   | 85    |
| 2   | Bob     | N/A               | 70    |
| 3   | Charlie | charlie@gmail.com | 90    |
| 4   | David   | N/A               | 60    |
| 5   | Eva     | eva@gmail.com     | 95    |
| 6   | Frank   | frank@domain.com  | 75    |
| 7   | Grace   | grace@gmail.com   | 80    |
| 8   | Helen   | N/A               | 88    |
| 9   | Ian     | ian@gmail.com     | 92    |
| 10  | Jane    | jane@domain.com   | 78    |

---

## 📦 Covered Activities
- `Read Range`  
- `Remove Duplicate Rows`  
- `Replace/Regex`  
- `Write Range`
