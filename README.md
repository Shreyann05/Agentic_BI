# 🤖 Agentic BI Demo — Sales Intelligence Platform

> Inspired by **Polestar Analytics' Agenthood AI** — a proof-of-concept 
> showing how Agentic BI goes beyond dashboards to deliver automated 
> anomaly detection, plain-English explanations, and recommended actions.

---

## 💡 The Problem This Solves

Traditional dashboards answer **"What happened?"**

They don't tell you **why** it happened or **what to do next.**

This is the "last-mile problem" in enterprise analytics — the gap 
between data and decisions. This project closes that gap.

---

## 🔍 What This Project Does

**Step 1 — Detects anomalies automatically**
Uses Facebook Prophet to forecast expected weekly CPG sales and 
flags every week where actual sales deviate beyond the confidence 
interval — both drops and spikes.

**Step 2 — Explains them in plain English**
Each anomaly is sent to Llama 3.1 (via Groq API) with full business 
context. The LLM returns a one-sentence business reason — no charts, 
just a direct answer.

**Step 3 — Recommends one concrete action**
For every anomaly, the LLM generates a single, specific next step 
a business team can act on immediately.

**Step 4 — Interactive dashboard**
Click any anomaly dot on the chart — the AI insight panel updates 
instantly. No Python needed to view or share the output.

---

## 📊 Results on Superstore Dataset

| Metric | Value |
|--------|-------|
| Transactions analysed | 9,994 |
| Weekly periods covered | 209 weeks (2014–2017) |
| Anomalies detected | 38 (17 drops, 21 spikes) |
| Worst drop | -79.4% (May 2016) |
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

## 🚀 How to Run
```bash
# 1. Clone the repo
git clone https://github.com/Shreyann05/agentic-bi-demo

# 2. Install dependencies
pip install pandas prophet plotly groq python-dotenv

# 3. Add your Groq API key
# Create a .env file in the project root:
# GROQ_API_KEY=your_key_here
# Get a free key at: console.groq.com

# 4. Run the notebook
jupyter notebook agentic_bi_demo.ipynb

# 5. Or just open the dashboard directly
# Open agentic_bi_demo.html in any browser — no Python needed
```

---



## 📸 Dashboard Preview

> Chart shows actual vs forecast sales with anomaly dots.  
> Click any dot → AI insight panel reveals reason + action instantly.

*(Add a screenshot here after running — drag image into README on GitHub)*

---

## 🔗 Why I Built This

Polestar Analytics describes their Agenthood AI as moving enterprises 
from "500 dashboards that can't explain an 8% revenue drop" to 
"agents that detect, explain, and act."

This project is my attempt to understand and demonstrate that 
concept at a smaller scale — using open data, free tools, and 
the same underlying logic.

---

**Built by:** Shreyan Sharma  
**Institution:** MANIT Bhopal (B.Tech Mechanical Engineering)  
**LinkedIn:** [ShreyanSharma](https://www.linkedin.com/in/shreyan-sharma-566a0727b/)  
**GitHub:** [Shreyann05](https://github.com/Shreyann05)
```

---

## STEP 22 — requirements.txt

Create a new file called `requirements.txt` in your project folder:
```
pandas
prophet
plotly
groq
python-dotenv
openpyxl
kaleido
notebook
```

---

## STEP 23 — .gitignore

Create `.gitignore` file:
```
.env
venv/
__pycache__/
*.pyc
.ipynb_checkpoints/
*.egg-info/
dist/
