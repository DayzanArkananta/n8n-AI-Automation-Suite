# 🧾 SmartInvoice Auditor
### Automated Financial Review and Monthly Report System

**Workflow:** Schedule Trigger → Google Sheets → AI Audit (Groq) → Gmail (HTML Report)

---

## 🧠 Overview
SmartInvoice Auditor automates the repetitive and time-consuming process of reviewing financial records and tracking overdue invoices.  
Built with **n8n** and enhanced by **AI reasoning**, it turns raw spreadsheet data into a readable, executive-style audit summary.

The workflow runs on a defined schedule (e.g., every Friday or monthly) and performs the following steps:

1. Fetches invoice and transaction data from **Google Sheets**.  
2. Uses **Groq AI** to detect anomalies — overdue invoices, unusual amounts, or missing entries.  
3. Summarizes findings into clear audit insights.  
4. Generates a **formatted HTML report** that highlights key issues and sends it via **Gmail** to the finance or operations team.

The result: a quiet, consistent assistant that keeps your financial data accurate and your team informed — without the need for complex accounting software.

---

## ⚙️ Key Components
| Node | Purpose |
|------|----------|
| **Schedule Trigger** | Runs the audit automatically on a fixed schedule. |
| **Google Sheets Node** | Retrieves invoice records and payment data. |
| **Groq AI Node** | Reviews and interprets data for inconsistencies or overdue items. |
| **HTML Template Node** | Builds a styled financial summary email. |
| **Gmail Node** | Sends the completed report to designated recipients. |

---

## 💡 Why It Matters
- 🧮 **Consistent accuracy:** Removes human error from monthly checks.  
- 🕒 **Time-saving:** Routine audits happen automatically on schedule.  
- 💬 **Readable summaries:** Financial reports are clear and business-friendly.  

**Ideal for:** agencies, finance teams, and operations managers who need simple recurring invoice checks.

---

## 🧩 Example Output (Email Summary)
```html
📊 <strong>SmartInvoice Monthly Report — September 2025</strong>

• 3 invoices overdue (avg delay: 9 days)  
• 1 transaction flagged: “Unusual amount deviation”  
• 22 invoices verified and reconciled ✅  

🧠 Summary: Payment delays decreasing month-over-month. Recommend follow-up with client X and review billing cycle Y.
