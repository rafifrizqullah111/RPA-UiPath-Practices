# 📘 Case 07 - Organize and Move Emails

## 🎯 Objective
Automatically move or categorize emails based on rules or keywords.

---

## 📝 Sample Data
| No  | From               | Subject             | Body                         | Folder      |
|-----|------------------|-------------------|-----------------------------|------------|
| 1   | alice@mail.com   | Meeting Request    | Confirm meeting at 10 AM    | Meetings   |
| 2   | bob@mail.com     | Invoice #123       | Invoice attached            | Finance    |
| 3   | charlie@mail.com | Project Update     | Project deadline extended   | Projects   |
| 4   | david@mail.com   | Leave Request      | Request leave               | HR         |
| 5   | eva@mail.com     | Team Lunch         | Lunch details               | Events     |
| 6   | frank@mail.com   | Invoice #124       | Invoice attached            | Finance    |
| 7   | grace@mail.com   | Client Feedback    | Feedback received           | Clients    |
| 8   | helen@mail.com   | Server Maintenance | Server down 2 hours         | IT         |
| 9   | ian@mail.com     | Monthly Report     | Report attached             | Reports    |
| 10  | jane@mail.com    | Budget Approval    | Approve budget document     | Finance    |

---

## 🛠️ Steps
1. Read emails using **Get Outlook Mail Messages** or **Get IMAP Mail Messages**.  
2. Loop through emails using **For Each**.  
3. Apply rules using **If** to categorize emails based on subject/body.  
4. Move emails to corresponding folders using **Move Outlook Mail Message**.  

---

## ✅ Expected Output
- Emails are automatically organized into appropriate folders based on rules.  

---

## 📦 Covered Activities
- `Get Outlook Mail Messages`  
- `Get IMAP Mail Messages`  
- `For Each`  
- `If`  
- `Move Outlook Mail Message`
