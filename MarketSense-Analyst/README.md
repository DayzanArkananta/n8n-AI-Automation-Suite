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

## 🧩 Example Output (Email)
```text
<!doctype html>\n<html>\n<head>\n<meta charset="utf-8" />\n<meta name="viewport" content="width=device-width,initial-scale=1" />\n<title>Daily Stock Insight</title>\n<style>\n  body { font-family: "Segoe UI", Arial, sans-serif; background:#f9fafb; margin:0; padding:30px; color:#333; }\n  .container { max-width:700px; margin:0 auto; background:#fff; border-radius:12px; box-shadow:0 4px 20px rgba(0,0,0,0.05); padding:28px; }\n  h1 { font-size:20px; color:#0ea5e9; margin-bottom:8px; }\n  a { color:#2563eb; text-decoration:none; }\n  p { line-height:1.6; margin:8px 0; }\n  .section { margin-top:18px; padding-top:14px; border-top:1px solid #e5e7eb; }\n  .tag { display:inline-block; padding:4px 10px; border-radius:6px; background:#f0f9ff; color:#0369a1; font-size:12px; margin-top:4px; }\n  .recommendation { font-weight:600; font-size:15px; color:#111827; margin-top:6px; }\n  .footer { margin-top:24px; font-size:13px; color:#6b7280; border-top:1px solid #e5e7eb; padding-top:14px; text-align:center; }\n  .amount { background:#f0f9ff; padding:10px 14px; border-radius:8px; display:inline-block; font-weight:600; color:#0c4a6e; }\n</style>\n</head>\n<body>\n  <div class="container">\n    <h1>📈 Stock futures rise over optimism for U.S.-China trade deal ahead of Trump-Xi meeting</h1>\n    <p><a href="https://www.marketwatch.com/story/u-s-china-say-trade-deal-groundwork-has-been-laid-ahead-of-trump-xi-meeting-9f1fbe34?mod=mw_rss_topstories">https://www.marketwatch.com/story/u-s-china-say-trade-deal-groundwork-has-been-laid-ahead-of-trump-xi-meeting-9f1fbe34?mod=mw_rss_topstories</a></p>\n\n    <div class="section">\n      <h3>📰 Summary</h3>\n      <p>U.S. stock futures rose on Sunday after senior negotiators from the United States and China said they have laid groundwork for a new trade agreement ahead of the upcoming Trump‑Xi summit. The optimism reflects progress on tariffs and market access, easing concerns of a prolonged trade war. Futures on the S&P 500 and Dow Jones ticked higher, while the Nasdaq also edged up. Investors see the potential deal as a catalyst for lower volatility and improved corporate earnings outlook, especially for export‑heavy sectors. The market is awaiting confirmation from the leaders’ meeting later this week.</p>\n    </div>\n\n    <div class="section">\n      <h3>💡 Analysis & Insight</h3>\n      <p>The prospect of a U.S.–China trade pact is likely to lift risk‑on assets across the board. Industrials, consumer discretionary and agriculture firms that rely on cross‑border supply chains could see earnings upgrades, while technology names may benefit from reduced geopolitical risk premiums. However, the market remains sensitive to any derailment; a stalled deal could trigger a rapid swing back to defensive positioning. Short‑term traders may capitalize on volatility around the summit, but long‑term investors should weigh sector exposure rather than single‑stock bets until concrete details emerge.</p>\n    </div>\n\n    <div class="section">\n      <h3>💬 Investment Recommendation</h3>\n      <p class="recommendation">Wait and Observe</p>\n      <p>While the optimism is encouraging, the actual terms of the agreement remain uncertain until the Trump‑Xi meeting. Maintaining a flexible stance allows investors to capture upside if the deal is confirmed, yet protects against downside if negotiations falter.</p>\n    </div>\n\n      <p>Date: <strong>Today</strong></p>\n      <p>Total: <span class="amount">USD 0.00</span></p>\n    </div>\n\n    <div class="footer">\n      Sent automatically by <strong>Stock Insight AI</strong> • 2025  \n      <br>Stay informed, stay profitable 🚀\n    </div>\n  </div>\n</body>\n</html>
