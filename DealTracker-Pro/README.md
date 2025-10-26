# 💼 DealTracker Pro
### AI-Assisted Deal Scoring and Lead Intelligence Automation

**Workflow:** Webhook / Form Submission → AI Evaluator (Groq) → Google Sheets → Gmail / Slack  

---

## 🧠 Overview
DealTracker Pro automates lead management and deal evaluation with a mix of structured logic and AI reasoning.  
Whenever a new potential deal or client submission is received — whether from a landing form, CRM webhook, or custom input — the workflow:

1. Parses and validates the incoming lead data.  
2. Uses **Groq AI** to evaluate the lead’s quality and potential value based on context (budget, category, description, urgency).  
3. Assigns a **confidence score** and categorization (e.g., “High Priority”, “Moderate”, “Low”).  
4. Logs all data into **Google Sheets**, creating a lightweight deal-tracking dashboard.  
5. Sends a concise summary or alert via **Gmail** or **Slack**, depending on the lead’s score.

The result is a clean, automated intelligence layer for prioritizing opportunities — without heavy CRM software.

---

## ⚙️ Key Components
| Node | Purpose |
|------|----------|
| **Webhook Trigger / HTTP Node** | Captures new lead or deal submissions. |
| **Groq AI Node** | Evaluates and ranks each lead by analyzing key parameters and tone. |
| **Google Sheets Node** | Logs results with dynamic score and timestamp. |
| **If / Switch Logic** | Routes “high priority” leads to alert channels. |
| **Gmail / Slack Node** | Sends contextual deal summary to relevant team members. |

---

## 💡 Why It Matters
- 🧩 **Smarter pipeline:** Automatically detects the most promising leads.  
- ⏱️ **Reduced manual review:** Teams focus on negotiation, not sorting.  
- 💬 **Instant visibility:** Priority alerts reach the right people in seconds.  

**Ideal for:** real estate agencies, investment firms, SaaS sales teams, or B2B consultancies managing inbound deals.

---

## 🧩 Example Output (Slack Notification)
