# 📂 Case 04 - Transform & Projection

## 📄 Description
Transform a dataset into a different structure using LINQ, such as creating a list, dictionary, or anonymous objects.  
Useful for reshaping data for reporting, APIs, or further processing.

---

## 🎯 Objectives
- Learn to map and project data from one structure to another.  
- Convert DataTable rows to List, Dictionary, or anonymous objects.  
- Enable further automation processing or reporting in the desired format.

---

## 🛠️ Activities / Components
- `Read Range` / `Excel Application Scope`  
- `Assign` (for LINQ Select queries)  
- `ToList` / `ToDictionary` (convert IEnumerable to List/Dictionary)  
- `Write Range` (optional, for exporting)  
- `Log Message` (optional, for verification)

---

## 📂 Sample Dataset
`Orders.xlsx`  
  | OrderID | Customer   | Amount | Category  |
  |---------|------------|--------|-----------|
  | ORD001  | Alice Wong | 250    | OfficeSup |
  | ORD002  | Mark Chan  | 1200   | ITEquip   |
  | ORD003  | Lina Kim   | 450    | Travel    |
  | ORD004  | John Doe   | 800    | ITEquip   |
  | ORD005  | Maria Lee  | 150    | OfficeSup |
  | ORD006  | Peter Pan  | 300    | Travel    |
  | ORD007  | Jane Doe   | 950    | ITEquip   |
  | ORD008  | Sam Smith  | 100    | OfficeSup |
  | ORD009  | Amy Wong   | 700    | Travel    |
  | ORD010  | Tom Lee    | 500    | OfficeSup |

---

## 🚀 Hands-On Steps
1. Read `Orders.xlsx` into a DataTable (`dtOrders`).  
2. Transform the data into a list of customer names using LINQ:  
   ```vbnet
   customerList = dtOrders.AsEnumerable().
       Select(Function(r) r("Customer").ToString()).
       ToList()
   ```
3. Optionally, create a dictionary of OrderID → Amount:
   ```vbnet
   orderDict = dtOrders.AsEnumerable().
       ToDictionary(Function(r) r("OrderID").ToString(), Function(r) CInt(r("Amount")))
   ```
4. Export or log results as needed.

---

## ✅ Expected Output
- List of all customer names (unique or all depending on requirement).
- Dictionary of OrderID → Amount.

**Example List output:**
<br>`[ "Alice Wong", "Mark Chan", "Lina Kim", "John Doe", "Maria Lee", "Peter Pan", "Jane Doe", "Sam Smith", "Amy Wong", "Tom Lee" ]`

**Example Dictionary output:**
<br>`{ "ORD001": 250, "ORD002": 1200, "ORD003": 450, ..., "ORD010": 500 }`

---

