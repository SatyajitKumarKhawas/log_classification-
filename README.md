
# Hybrid Log Classification System
An intelligent, multi-tiered log analysis pipeline that combines the speed of **Regex**, the precision of **BERT**, and the reasoning power of **LLMs** to categorize system logs with maximum cost-efficiency.
## 🚀 The Hybrid Architecture
Unlike standard classifiers, this system uses a **cascading logic** to optimize performance and minimize API costs:
 1. **Tier 1: Regex (Fastest)** – Instantly catches high-frequency, fixed patterns.
 2. **Tier 2: BERT + Logistic Regression (Accurate)** – Uses Sentence Transformers to classify complex logs with sufficient training data.
 3. **Tier 3: LLM (Reasoning)** – Leverages **DeepSeek R1 / Llama 3** (via Groq) as a fallback for rare, "long-tail" log events.
## 🛠️ Tech Stack
 * **Languages:** Python 3.10+
 * **AI/ML:** Scikit-learn, Sentence Transformers (BERT), Groq API (DeepSeek R1/Llama 3)
 * **Unsupervised Learning:** DBScan (for pattern discovery)
 * **Backend:** FastAPI, Uvicorn
 * **Data Handling:** Pandas, NumPy, Joblib
## 📂 Project Structure
```text
├── training/
│   ├── training.ipynb       # Data exploration & model training
│   └── data/                # Synthetic log datasets
├── models/
│   └── log_classifier.jblb  # Saved BERT+Logistic Regression model
├── processors/
│   ├── regex_proc.py        # Tier 1 Logic
│   ├── bert_proc.py         # Tier 2 Logic
│   └── llm_proc.py          # Tier 3 Logic
├── server.py                # FastAPI Implementation
├── requirements.txt         # Project Dependencies
└── README.md

```
## ⚙️ Setup & Installation
 1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/log-classification-system.git
   cd log-classification-system
   
   ```
 2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   
   ```
 3. **Environment Setup:**
   Create a .env file in the root directory and add your Groq API Key:
   ```env
   GROQ_API_KEY=your_api_key_here
   
   ```
 4. **Run the Server:**
   ```bash
   uvicorn server:app --reload
   
   ```
## 📊 Key Features
 * **Automated Pattern Discovery:** Uses **DBScan Clustering** to group raw logs, allowing for the automatic generation of Regex rules.
 * **Cost Optimization:** By handling 80%+ of logs via Regex and BERT, the system minimizes expensive LLM token usage.
 * **REST API Support:** Ready-to-use endpoints to upload .csv files and receive classified results.
## 📝 License
Distributed under the MIT License. See LICENSE for more information.
**Developed by [Your Name]** *Passionate about building scalable AI Automation and LLM-powered applications.*
