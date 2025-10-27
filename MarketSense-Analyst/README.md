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
<!doctype html>
<html>
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Daily Stock Insight</title>
<style>
  body { font-family: "Segoe UI", Arial, sans-serif; background:#f9fafb; margin:0; padding:30px; color:#333; }
  .container { max-width:700px; margin:0 auto; background:#fff; border-radius:12px; box-shadow:0 4px 20px rgba(0,0,0,0.05); padding:28px; }
  h1 { font-size:20px; color:#0ea5e9; margin-bottom:8px; }
  a { color:#2563eb; text-decoration:none; }
  p { line-height:1.6; margin:8px 0; }
  .section { margin-top:18px; padding-top:14px; border-top:1px solid #e5e7eb; }
  .tag { display:inline-block; padding:4px 10px; border-radius:6px; background:#f0f9ff; color:#0369a1; font-size:12px; margin-top:4px; }
  .recommendation { font-weight:600; font-size:15px; color:#111827; margin-top:6px; }
  .footer { margin-top:24px; font-size:13px; color:#6b7280; border-top:1px solid #e5e7eb; padding-top:14px; text-align:center; }
  .amount { background:#f0f9ff; padding:10px 14px; border-radius:8px; display:inline-block; font-weight:600; color:#0c4a6e; }
</style>
</head>
<body>
  <div class="container">
    <h1>📈 {{ $json.title }}</h1>
    <p><a href="{{ $json.link }}">{{ $json.link }}</a></p>

    <div class="section">
      <h3>📰 Summary</h3>
      <p>{{ $json.summary || "A brief overview of today's market update or company insight." }}</p>
    </div>

    <div class="section">
      <h3>💡 Analysis & Insight</h3>
      <p>{{ $json.analysis || "Professional insight and interpretation of the latest financial data or market movement." }}</p>
    </div>

    <div class="section">
      <h3>💬 Investment Recommendation</h3>
      <p class="recommendation">{{ $json.recommendation || "Buy / Sell / Hold / Wait and Observe" }}</p>
      <p>{{ $json.recommendation_reason || "Rationale behind this recommendation goes here." }}</p>
    </div>

    <div class="section" style="text-align:right;">
      <p>Invoice No: <strong>{{ $json.invoice_number || "INV-{{ $json.date }}" }}</strong></p>
      <p>Date: <strong>{{ $json.date || "Today" }}</strong></p>
      <p>Total: <span class="amount">{{ $json.amount || "USD 0.00" }}</span></p>
    </div>

    <div class="footer">
      Sent automatically by <strong>Stock Insight AI</strong> • {{ new Date().getFullYear() }}  
      <br>Stay informed, stay profitable 🚀
    </div>
  </div>
</body>
</html>
