# 🧠 AI-Network-Threat-Detection

🚨 **Goal**  
Build an intelligent, end-to-end network intrusion detection pipeline using **Suricata logs** and **machine learning models** (Random Forest, LSTM, and LLM-based classifiers). This project aims to bridge traditional IDS systems with modern AI-driven threat detection and context-aware flow analysis.

---

## 🎯 Background & Motivation

This project stems from real-world work conducted at the **Security Intelligence and Operations Center (SIOC)** at **Kansas State University**, where I assisted in deploying network-based detection tools, managing log pipelines, and building Microsoft Sentinel dashboards for alert visibility.

Here, I replicate and extend that work using **public datasets (e.g., CIC-IDS2017)** and a modern ML toolchain — transforming raw Suricata logs into actionable threat classifications and intelligent summaries.

---

## 🔍 Project Roadmap

### ✅ Phase 1: Baseline ML Detection
- [x] Parse `eve.json` (Suricata logs) into structured session-level features
- [x] Engineer features: byte counts, packet size, protocol, timestamp deltas, IP pairs
- [x] Train classical ML classifiers (Random Forest, XGBoost) on CICIDS2017
- [x] Evaluate precision, recall, F1-score on test set

### 🚧 Phase 2: Temporal & Sequential Modeling
- [ ] Prepare time-windowed session sequences for LSTM
- [ ] Train and evaluate LSTM model on malicious vs benign behavior patterns
- [ ] Compare with baseline ML models

### 🌟 Phase 3 (Stretch Goal): LLM + Threat Summary
- [ ] Integrate a lightweight transformer model (e.g., MiniLM, DistilBERT)
- [ ] Convert log flow into tokenized sequence → pass through LLM → classify/summarize
- [ ] Evaluate performance + runtime on edge device (optional)

---

## 🧰 Tech Stack

| Tool          | Purpose                                  |
|---------------|-------------------------------------------|
| **Suricata**  | Open-source IDS for log generation        |
| **Python**    | Core language for all scripting & modeling |
| **Pandas**    | Log parsing, feature engineering          |
| **Scikit-learn** | Baseline ML models                    |
| **PyTorch**   | Deep learning models (LSTM, LLMs)         |
| **Jupyter**   | Interactive development + visualizations |
| **CICIDS2017**| Public dataset for model training         |

---

## 🧪 Data Source

- Dataset: [CIC-IDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)  
- Preprocessed to extract:
  - Source/Destination IPs
  - Protocol & port
  - Flow duration
  - Packet counts
  - Byte transfer
  - Timestamps
  - Label (Benign or specific attack type)

---

## 📊 Model Performance (Coming Soon)

| Model         | Accuracy | Precision | Recall | F1 Score |
|---------------|----------|-----------|--------|----------|
| Random Forest | TBD      | TBD       | TBD    | TBD      |
| LSTM          | TBD      | TBD       | TBD    | TBD      |
| MiniLM        | TBD      | TBD       | TBD    | TBD      |

---

## 📦 Folder Structure

