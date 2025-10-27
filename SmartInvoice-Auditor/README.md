# 🧾 SmartInvoice Auditor
### Autonomous AI Agent for Financial Review and Monthly Audit Reports

**Workflow:** Schedule Trigger → Google Sheets → AI Agent (Groq) → Gmail (HTML Report)

---

## 🧠 Overview
SmartInvoice Auditor is an **AI-driven financial audit agent** built on **n8n**, designed to monitor and analyze invoice data automatically.  
Instead of simply listing overdue items, the AI Agent reviews transaction patterns, detects inconsistencies, and produces a contextual audit summary — the kind a finance analyst would normally write manually.  

The workflow runs on a predefined schedule (weekly or monthly), quietly reviewing your financial spreadsheet, identifying anomalies, and sending a clean HTML report via Gmail.

---

## ⚙️ Core Process
1. **Data Retrieval:** Pulls invoice and transaction data from **Google Sheets**.  
2. **Autonomous Analysis:** The **AI Agent** reviews the dataset, identifies overdue invoices, anomalies, and trend deviations.  
3. **Reasoning & Summary:** The agent interprets findings and drafts a natural-language financial summary.  
4. **Delivery:** The results are formatted into a professional audit email and sent to your finance or operations team.

---

## ⚙️ Key Components
| Node | Purpose |
|------|----------|
| **Schedule Trigger** | Automates the workflow (weekly or monthly). |
| **Google Sheets Node** | Retrieves invoice and payment data. |
| **AI Agent (Groq)** | Performs autonomous reasoning and generates audit insights. |
| **HTML Template Node** | Builds a structured, visual email report. |
| **Gmail Node** | Sends the report to selected recipients. |

---

## 💡 Why It Matters
- 🤖 **Agent reasoning:** Understands invoice behavior and context, not just numbers.  
- 🧩 **Financial clarity:** Turns spreadsheet data into readable business insights.  
- ⏱️ **Always-on:** Runs audits automatically with zero manual review.  

**Ideal for:** agencies, finance departments, consultants, or operations teams who handle recurring billing cycles and client invoicing.

---

## 🧩 Example Output (AI Agent Email)
```text
📊 SmartInvoice Auditor — Monthly Review (September 2025)

• 4 overdue invoices (average delay: 6 days)  
• 1 record flagged as inconsistent (amount mismatch)  
• 28 transactions verified and balanced ✅  

🧠 AI Agent Summary:
"Overall cash flow remains stable. Notable improvement in on-time payments compared to August. Follow up with Client Delta for reconciliation."
