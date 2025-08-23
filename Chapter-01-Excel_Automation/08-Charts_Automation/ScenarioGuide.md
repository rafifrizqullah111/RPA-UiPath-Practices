# 📘 Case 08 - Charts Automation

## 🎯 Objective
Automate chart creation in Excel using UiPath.

---

## 📝 Sample Data
| Month | Sales |
|-------|-------|
| Jan   | 5000  |
| Feb   | 7000  |
| Mar   | 6000  |
| Apr   | 8000  |
| May   | 7500  |
| Jun   | 9000  |
| Jul   | 8500  |
| Aug   | 9500  |
| Sep   | 8700  |
| Oct   | 9200  |

---

## 🛠️ Steps
1. Read data into DataTable.
2. Use **Add Chart** activity to create a Line Chart.
   - X-axis: `Month`
   - Y-axis: `Sales`
3. Place chart in a new sheet.

---

## ✅ Expected Output
- A line chart showing monthly sales trends for Jan–Oct.

---

## 📦 Covered Activities
- `Read Range`  
- `Add Chart`  
- `Write Range`
