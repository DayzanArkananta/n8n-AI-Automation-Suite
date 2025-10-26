# 📈 MarketSense Analyst
### Intelligent Market Monitoring & AI Insights via n8n

**Workflow:** RSS Feed → AI Summarizer (Groq / Llama) → Gmail  

---

## 🧠 Overview
MarketSense Analyst automates the process of monitoring market updates and generating concise investment insights — powered by **n8n** and **AI-driven analysis**.  

The workflow periodically checks trusted financial RSS feeds (e.g., MarketWatch, Reuters, or Investing.com), then uses **Groq AI** to:
1. Summarize key financial events and market movements.  
2. Identify sentiment (positive / negative / neutral).  
3. Craft a short, natural-language insight for quick decision-making.  
4. Deliver the summary directly via **Gmail**, formatted in a clear daily briefing style.

This system works quietly in the background, giving investors, analysts, or consultants quick context before market hours.

---

## ⚙️ Key Components
| Node | Purpose |
|------|----------|
| **RSS Feed Trigger** | Fetches new financial headlines or articles periodically. |
| **HTTP Request + Groq AI** | Summarizes and analyzes the market sentiment using natural language understanding. |
| **HTML Formatter** | Builds a clean, responsive email layout. |
| **Gmail Node** | Sends the final market summary email to the analyst or team. |

---

## 💡 Why It Matters
- 📊 **Time-efficient:** Get a curated, human-like market summary without scrolling endless feeds.  
- 🧠 **Contextual:** AI extracts not just facts, but *implications* behind the news.  
- 🧩 **Adaptive:** Easily reconfigured for crypto, forex, or stock niches.  

**Ideal for:** analysts, investment advisors, fintech product teams, or content strategists who rely on up-to-date market awareness.

---

## 🧩 Example Output (Email)
```text
📰 MarketSense Daily Brief — Oct 24, 2025

• S&P 500 gains 0.7% on renewed optimism around tech earnings.  
• Oil prices stabilize after OPEC supply update.  
• AI stocks show steady recovery amid increased investment flows.

🧠 Summary: Sentiment remains cautiously positive. Analysts highlight resilience in core sectors despite inflation pressure.
