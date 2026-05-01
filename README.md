# 📊 AI Data Analysis Agent

🚀 A fast, offline-first data agent that lets you **analyze large datasets using natural language queries — no SQL or coding required**.

---

## 💡 Why This Matters

Data analysis usually requires:
- Writing SQL queries
- Understanding schemas
- Manual data exploration

👉 This tool eliminates that friction:

**Ask questions → Get answers → See insights instantly**

---

## ⚡ Key Features

- 📂 Supports CSV, Excel, and Parquet datasets  
- 💬 Natural language querying (no SQL needed)  
- ⚡ Fully offline (no API keys required)  
- 🧠 Deterministic execution using Pandas  
- 📊 Built-in analytics (aggregations, trends, anomalies)  
- 🔍 Evidence-first outputs (plan + method + preview)  
- 🤖 Optional LLM-powered “Insights (caveated)”  

---

## 🧠 Example Queries

```bash
Top 5 states by sales
Average revenue by year
Show anomalies in transactions
Correlation between price and demand
```

## 🏗️ How It Works

User Query → Planner → Execution Engine → Result + Explanation

## Components:

Planner → Converts natural language into structured operations
Execution Engine → Runs safe Pandas-based computations
Analysis Layer → Handles aggregates, trends, anomalies
Answer Formatter → Returns results with explanations

## 🛠️ Tech Stack

Python
Pandas
PyArrow
scikit-learn (optional)
OpenAI / Anthropic (optional insights)

## ⚙️ Setup

Windows (PowerShell)
```bash
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

macOS/Linux
```bash
python3 -m venv venv
source venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## ▶️ Running the Agent

Local File
```bash
python -m src.agent --data-path "C:\path\to\file.csv"
```
Excel
```bash
python -m src.agent --data-path "file.xlsx" --sheet "Sheet1"
```
Parquet (Recommended)
```bash
python -m src.agent --data-path "file.parquet"
```

## ⚡ Runtime Flags

| Flag | Description |
|------|------------|
| `--data-path` | Path to local dataset (CSV / XLSX / Parquet) |
| `--from-url` | Load dataset from a remote URL |
| `--sheet` | Specify Excel sheet name |
| `--sep` | Override CSV delimiter (e.g., `;` or `|`) |
| `--date-col` | Column used for time-based analysis (year extraction) |
| `--insights` | Enable optional LLM-generated insights |
python -m src.agent --from-url "https://example.com/data.csv"

## 🤖 Optional: LLM Insights

Enable AI-generated summaries:
```bash
pip install openai
$env:OPENAI_API_KEY="your-key"
python -m src.agent --data-path "file.parquet" --insights
```

## 📊 What You Get
Every query returns:

- ✅ Execution plan
- ✅ Method used
- ✅ Result preview
- ✅ Optional insights

## ⚠️ Assumptions & Limitations
- Correlation ≠ causation
- Outliers may be valid data
- Year trends depend on date column
- LLM insights are approximate

## 🏎️ Performance Tips
- Use Parquet for large datasets
- Avoid high-cardinality group-bys
- Keep previews small
- Drop null-heavy columns

## 📁 Project Structure
- src/
- ├─ agent.py
- ├─ dataset.py
- ├─ preprocess.py
- ├─ planner.py
- ├─ analysis.py
- ├─ answer.py
- ├─ utils.py
- └─ insights.py

## 🚀 Impact

- ⏱️ Reduces analysis time significantly
- 📊 Makes data accessible to non-technical users
- 🤖 Bridges gap between raw data and insights

## 👤 Author
Shreyas Mysore Narayana

AI & Data Engineer | Automation Builder
