# 📘 Case 06 - Email-Based Approval / Notifications

## 🎯 Objective
Send approval requests or notifications via email and handle responses automatically.

---

## 📝 Sample Data
| No  | To                   | Subject           | Body                                | Attachment          |
|-----|--------------------|-----------------|----------------------------------|-------------------|
| 1   | alice@mail.com     | Budget Approval  | Please approve budget document     | budget.xlsx       |
| 2   | bob@mail.com       | Leave Approval   | Please approve leave request       | leave_request.docx|
| 3   | charlie@mail.com   | Invoice Approval | Please approve invoice #123        | invoice_123.pdf   |
| 4   | david@mail.com     | Project Approval | Approve project plan               | project_plan.docx |
| 5   | eva@mail.com       | Policy Update    | Review and acknowledge policy      | policy.pdf        |
| 6   | frank@mail.com     | Expense Approval | Approve expense report             | expense.pdf       |
| 7   | grace@mail.com     | Client Feedback  | Feedback review                    | feedback.docx     |
| 8   | helen@mail.com     | Meeting Approval | Approve meeting agenda             | agenda.docx       |
| 9   | ian@mail.com       | Report Approval  | Approve monthly report             | report.xlsx       |
| 10  | jane@mail.com      | Team Notification| Notify team about schedule         | schedule.pdf      |

---

## 🛠️ Steps
1. Loop through list of approvers/recipients using **For Each Row**.  
2. Send email using **Send Outlook Mail Message** or **Send SMTP Mail Message** with attachments.  
3. Optionally, monitor inbox for approval responses using **Get Outlook Mail Messages** or **Get IMAP Mail Messages**.  
4. Apply **If** to process responses (Approved / Rejected).  

---

## ✅ Expected Output
- All recipients receive approval/notification emails correctly.  
- Responses are tracked and logged if applicable.  

---

## 📦 Covered Activities
- `Send Outlook Mail Message`  
- `Send SMTP Mail Message`  
- `Get Outlook Mail Messages`  
- `Get IMAP Mail Messages`  
- `For Each Row`  
- `If`
