# 📘 Case 02 - Send Emails with Attachments

## 🎯 Objective
Send automated emails with attachments to recipients.

---

## 📝 Sample Data
| No  | To                   | Subject            | Body                          | Attachment             |
|-----|---------------------|------------------|------------------------------|-----------------------|
| 1   | alice@mail.com      | Project Files     | Attached are the files       | project_files.zip     |
| 2   | bob@mail.com        | Invoice           | Please find invoice attached | invoice_123.pdf       |
| 3   | charlie@mail.com    | Monthly Report    | Report attached              | report_august.xlsx    |
| 4   | david@mail.com      | Meeting Agenda    | Agenda for tomorrow          | agenda.docx           |
| 5   | eva@mail.com        | Team Lunch Invite | Lunch details attached       | lunch_invite.pdf      |
| 6   | frank@mail.com      | Invoice           | Please find invoice attached | invoice_124.pdf       |
| 7   | grace@mail.com      | Client Feedback   | Feedback document attached   | feedback.docx         |
| 8   | helen@mail.com      | Server Update     | Update notes attached        | server_notes.pdf      |
| 9   | ian@mail.com        | Monthly Budget    | Budget document attached     | budget.xlsx           |
| 10  | jane@mail.com       | Approval Request  | Please approve attached file | approval_form.docx    |

---

## 🛠️ Steps
1. Loop through recipient list using **For Each Row** in DataTable.  
2. Use **Send Outlook Mail Message** or **Send SMTP Mail Message**.  
3. Include `To`, `Subject`, `Body`, and `Attachments`.  
4. Send email automatically.  

---

## ✅ Expected Output
- Each recipient receives an email with the correct subject, body, and attachment.  

---

## 📦 Covered Activities
- `Send Outlook Mail Message`  
- `Send SMTP Mail Message`  
- `Add Attachment`  
- `For Each Row`
