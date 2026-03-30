# Forexa Pro Dashboard

The **Forexa Pro Dashboard** serves as a decision-support terminal that merges traditional technical analysis with modern alternative data. Below is a detailed breakdown of the definitions and the professional workflow for using the system via GitHub Pages.

---

## 1. Core Component Definitions

### RSI (Relative Strength Index) – The Momentum Oscillator
In the Forexa Pro context, the RSI is a technical momentum indicator that measures the speed and change of price movements.

- **Scale:** 0 to 100  
- **Overbought (>70):** Asset may be overvalued → downward correction or "Sell" signal approaching  
- **Oversold (<30):** Asset may be undervalued → upward "Buy" recovery likely  
- **Professional Use:** Look for **divergence** (e.g., price makes a new high, but RSI does not), which suggests the current trend is weakening.

---

### Sentiment Analysis – The Psychological Filter
Unlike RSI, which only looks at past price data, Sentiment Analysis uses Natural Language Processing (NLP) to scan news, social feeds, and reports.

- **Bullish Sentiment:** High positive frequency → "Greed" or "Confidence"  
- **Bearish Sentiment:** High negative frequency → "Fear" or "Panic"  
- **Professional Use:** Sentiment is a **confirmation tool**. Example: RSI shows "Oversold" (Buy) but sentiment is "Extreme Fear" → wait until sentiment neutralizes before entering, avoiding a "falling knife" scenario.

---

## 2. The Professional User Menu Workflow

### Step A: Handshake & Tunnel Verification (Backend Page)
Before trading, a professional user must ensure the "Engine" is alive.

- **Service Indicator:** Top right of `backend.html` must show ● SERVICE: ONLINE  
- **Tunnel Endpoint:** Ensure Ngrok or Gist URL is active (bridge between Python AI and browser)  
- **Live Console:** Look for "Handshake Successful" logs → confirms XGBoost and LSTM models are feeding live data  

### Step B: Signal Interpretation (Index/Terminal Page)
The main dashboard is where execution happens.

- **Pred-Status Pill:** Final Decision output combining RSI, MACD, and Sentiment → BUY or SELL  
- **Live Graphing:** Chart.js visualizer tracks price action vs. AI’s predicted target price  
- **Raw API Stream:** JSON output shows confidence_score (e.g., BUY with 0.55 = risky, 0.85 = high conviction)

---

## 3. Professional Strategy – *The Confluence Filter*

Never rely on a single indicator. Follow this **Rule of Three**:

| Step | Action              | Requirement                                   |
|------|---------------------|-----------------------------------------------|
| 1    | Technical           | RSI must be in recovery zone (e.g., rising from 30) |
| 2    | Sentiment           | AI Sentiment must be Positive or Neutral for a Buy |
| 3    | Validation          | Backend Console latency must be low (< 2 seconds) |

---

## 4. Navigating the GitHub Pages Menu

- **About:** Review Model Architecture → understand "Weights" (how much AI values RSI vs. news)  
- **Backend:** Keep open in a second tab → acts as "Engine Room" to verify data freshness  
- **Download Client:** Access Android/Desktop app → lower latency than web-based GitHub Pages  

**Pro Tip:** If the status-indicator turns **Red (OFFLINE)** → stop trading immediately. This means the tunnel collapsed or the Google Colab engine timed out, so data is no longer live market reality.

---

## Forexa Pro Resources

- 🚀 **Open Codes** | 📂 **Project Files**  
- 💻 **Google Colab Engine** | 📄 **Google Drive Assets**  
- 🔗 **Open Source GitHub Repository** | 📘 **Documentation**  

**● System Version 2.0.4 – Live Updates**
