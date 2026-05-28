# 🤖 Agentic BI Demo — Sales Intelligence Platform
> Inspired by **Polestar Analytics' Agenthood AI** — a proof-of-concept showing how Agentic BI goes beyond dashboards to deliver automated anomaly detection, plain-English explanations, and recommended actions.

---

## 💡 The Problem This Solves

Most dashboards are good at telling you *what* happened.  
They're not so good at telling you *why* — or what you should do about it.

That gap between data and decisions is something I kept running into while studying analytics. This project is my attempt to close it, even at a small scale.

---

## 🔍 What This Project Does

**Step 1 — Detects anomalies automatically**  
Uses Facebook Prophet to forecast expected weekly CPG sales and flags every week where actual sales deviate beyond the confidence interval — both drops and spikes.

**Step 2 — Explains them in plain English**  
Each anomaly is sent to Llama 3.1 (via Groq API) with full business context. The model returns a one-sentence business reason — no jargon, just a direct answer.

**Step 3 — Recommends one concrete action**  
For every anomaly, the model generates a single, specific next step a business team can act on immediately.

**Step 4 — Interactive dashboard**  
Click any anomaly dot on the chart — the AI insight panel updates instantly. No Python needed to view or share the output.

---

## 📊 Results on Superstore Dataset

| Metric | Value |
|--------|-------|
| Transactions analysed | 9,994 |
| Weekly periods covered | 209 weeks (2014–2017) |
| Anomalies detected | 38 (17 drops, 21 spikes) |
| Worst drop | −79.4% (May 2016) |
| Biggest spike | +88.2% (Jan 2014) |
| AI insights generated | 38 explanations + 38 actions |

---

## 🛠️ Tech Stack

| Layer | Tool |
|-------|------|
| Language | Python 3.x |
| Forecasting / Anomaly Detection | Facebook Prophet |
| Data Processing | Pandas |
| LLM / AI Layer | Llama 3.1 (8B) via Groq API |
| Visualisation | Plotly |
| Dashboard Export | HTML + JavaScript |
| Dataset | Superstore Sales — Kaggle |

---

