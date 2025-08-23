# 📘 Case 05 - Monitor Email Inbox

## 🎯 Objective
Continuously monitor inbox for new emails and trigger workflows automatically.

---

## 📝 Sample Data
| No  | From                | Subject           | Body                          | Received Date       |
|-----|-------------------|-----------------|------------------------------|------------------|
| 1   | alice@mail.com    | Meeting Request  | Please confirm meeting at 10 AM  | 2025-08-23 09:15 |
| 2   | bob@mail.com      | Invoice #123     | Invoice attached                  | 2025-08-23 10:20 |
| 3   | charlie@mail.com  | Project Update   | Project deadline extended         | 2025-08-23 11:05 |
| 4   | david@mail.com    | Leave Request    | Request leave for 2 days          | 2025-08-23 12:30 |
| 5   | eva@mail.com      | Team Lunch       | Lunch at 1 PM                     | 2025-08-23 13:10 |
| 6   | frank@mail.com    | Invoice #124     | Invoice attached                  | 2025-08-23 14:00 |
| 7   | grace@mail.com    | Client Feedback  | Feedback received from client     | 2025-08-23 14:45 |
| 8   | helen@mail.com    | Server Maintenance | Server down 2 hours            | 2025-08-23 15:20 |
| 9   | ian@mail.com      | Monthly Report   | Report attached                   | 2025-08-23 16:00 |
| 10  | jane@mail.com     | Budget Approval  | Please approve the budget         | 2025-08-23 16:45 |

---

## 🛠️ Steps
1. Use **Get Outlook Mail Messages** or **Get IMAP Mail Messages** periodically (e.g., every 5 minutes).  
2. Apply **If** to check for new emails.  
3. Trigger automated workflow actions (e.g., save attachments, send reply, forward).  
4. Optionally, log processed emails or move to another folder.  

---

## ✅ Expected Output
- New emails trigger automatic actions as defined in workflow.  
- Inbox monitored continuously without manual intervention.  

---

## 📦 Covered Activities
- `Get Outlook Mail Messages`  
- `Get IMAP Mail Messages`  
- `Delay`  
- `If`  
- `For Each`
