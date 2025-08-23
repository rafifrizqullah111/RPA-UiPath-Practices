# 📘 Case 01 - Read Emails and Extract Data

## 🎯 Objective
Read emails from inbox and extract key information from subject or body for further processing.

---

## 📝 Sample Data
| No  | From                  | Subject                        | Body                              | Received Date       |
|-----|----------------------|--------------------------------|----------------------------------|------------------|
| 1   | alice@mail.com       | Meeting Request                | Please confirm meeting at 10 AM  | 2025-08-23 09:15 |
| 2   | bob@mail.com         | Invoice #123                   | Invoice attached                  | 2025-08-23 10:20 |
| 3   | charlie@mail.com     | Project Update                 | Project deadline extended         | 2025-08-23 11:05 |
| 4   | david@mail.com       | Leave Request                  | Request leave for 2 days          | 2025-08-23 12:30 |
| 5   | eva@mail.com         | Team Lunch                     | Lunch at 1 PM                     | 2025-08-23 13:10 |
| 6   | frank@mail.com       | Invoice #124                   | Invoice attached                  | 2025-08-23 14:00 |
| 7   | grace@mail.com       | Client Feedback                | Feedback received from client     | 2025-08-23 14:45 |
| 8   | helen@mail.com       | Server Maintenance             | Server down 2 hours               | 2025-08-23 15:20 |
| 9   | ian@mail.com         | Monthly Report                 | Report attached                   | 2025-08-23 16:00 |
| 10  | jane@mail.com        | Budget Approval                | Please approve the budget         | 2025-08-23 16:45 |

---

## 🛠️ Steps
1. Use **Get Outlook Mail Messages** or **Get IMAP Mail Messages** to read inbox emails.  
2. Loop through emails using **For Each**.  
3. Extract key information: `From`, `Subject`, `Body`, `Received Date`.  
4. Store extracted data in a DataTable or Excel sheet.  

---

## ✅ Expected Output
| No  | From                  | Subject              | Body                              | Received Date       |
|-----|----------------------|--------------------|----------------------------------|------------------|
| 1   | alice@mail.com       | Meeting Request    | Please confirm meeting at 10 AM  | 2025-08-23 09:15 |
| 2   | bob@mail.com         | Invoice #123       | Invoice attached                  | 2025-08-23 10:20 |
| ... | ...                  | ...                | ...                              | ...              |

---

## 📦 Covered Activities
- `Get Outlook Mail Messages`  
- `Get IMAP Mail Messages`  
- `For Each`  
- `Assign`  
- `Write Range` (optional)
