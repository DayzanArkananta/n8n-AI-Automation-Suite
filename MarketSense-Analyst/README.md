# 📈 MarketSense Analyst
### Autonomous AI Agent for Market Monitoring and Insight Generation

**Workflow:** RSS Feed → AI Agent (Groq) → Gmail  

---

## 🧠 Overview
MarketSense Analyst is an **AI-driven market analysis agent** built on **n8n**, designed to interpret daily financial news and generate actionable insights automatically.  

Unlike simple summarizers, this system uses an **AI Agent** that reasons over multiple headlines, detects underlying sentiment, and formulates concise, human-readable investment takeaways — all without manual review.  

The workflow periodically fetches the latest updates from trusted financial sources (e.g., MarketWatch, Reuters, Investing.com), processes them through the AI Agent, and sends a polished daily briefing via Gmail.

---

## ⚙️ Core Process
1. **Fetch & Gather:** Pulls new financial news from selected RSS feeds.  
2. **Reasoning & Analysis:** The AI Agent analyzes trends, sentiment, and relevance, connecting data across articles.  
3. **Recommendation:** Based on its reasoning, it provides a brief strategic note (e.g., “Tech sector likely to recover; focus on semiconductors”).  
4. **Delivery:** Generates a clean email summary and delivers it via Gmail.  

---

## ⚙️ Key Components
| Node | Purpose |
|------|----------|
| **RSS Feed Trigger** | Collects real-time market news and updates. |
| **AI Agent (Groq Reasoning Engine)** | Performs multi-article analysis and generates structured insights. |
| **HTML Formatter** | Builds a clean, minimal market summary email layout. |
| **Gmail Node** | Sends the final report to the analyst or team. |

---

## 💡 Why It Matters
- 🧠 **Autonomous reasoning:** The agent understands context, not just keywords.  
- 📊 **Action-ready:** Converts market chatter into clear, actionable perspectives.  
- 🕒 **Low maintenance:** Operates quietly on schedule, no human supervision needed.  

**Ideal for:** analysts, fintech startups, investment teams, and business strategists who value daily context without manual curation.

---

🧩 [Example Output (Email)](./example_output_email.png)
