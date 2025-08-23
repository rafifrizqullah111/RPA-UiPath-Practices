# 📘 Case 03 - Save Email Attachments

## 🎯 Objective
Save attachments from emails to local or network folder automatically.

---

## 📝 Sample Data
| No  | From                | Subject          | Attachment Name       | Received Date       |
|-----|-------------------|----------------|--------------------|------------------|
| 1   | alice@mail.com    | Project Files   | project_files.zip   | 2025-08-23 09:15 |
| 2   | bob@mail.com      | Invoice #123    | invoice_123.pdf     | 2025-08-23 10:20 |
| 3   | charlie@mail.com  | Monthly Report  | report_august.xlsx  | 2025-08-23 11:05 |
| 4   | david@mail.com    | Meeting Agenda  | agenda.docx         | 2025-08-23 12:30 |
| 5   | eva@mail.com      | Team Lunch      | lunch_invite.pdf    | 2025-08-23 13:10 |
| 6   | frank@mail.com    | Invoice #124    | invoice_124.pdf     | 2025-08-23 14:00 |
| 7   | grace@mail.com    | Client Feedback | feedback.docx       | 2025-08-23 14:45 |
| 8   | helen@mail.com    | Server Update   | server_notes.pdf    | 2025-08-23 15:20 |
| 9   | ian@mail.com      | Monthly Budget  | budget.xlsx         | 2025-08-23 16:00 |
| 10  | jane@mail.com     | Approval Request| approval_form.docx  | 2025-08-23 16:45 |

---

## 🛠️ Steps
1. Read emails using **Get Outlook Mail Messages** or **Get IMAP Mail Messages**.  
2. Loop through emails with **For Each**.  
3. Use **Save Mail Attachments** to save files to a predefined folder.  
4. Optionally, move processed emails to another folder using **Move Outlook Mail Message**.  

---

## ✅ Expected Output
- All attachments are saved in the specified folder with correct filenames.  
- Processed emails moved to “Processed” folder (optional).  

---

## 📦 Covered Activities
- `Get Outlook Mail Messages`  
- `Get IMAP Mail Messages`  
- `Save Mail Attachments`  
- `Move Outlook Mail Message`  
- `For Each`
