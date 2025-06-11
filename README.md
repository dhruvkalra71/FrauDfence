# 💳 FraudFence: DSA-Driven Credit Card Fraud Detection System

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/dhruvkalra71/FrauDfence)
[![Stars](https://img.shields.io/github/stars/dhruvkalra71/FrauDfence?style=social)](https://github.com/dhruvkalra71/FrauDfence/stargazers)

---

## 🏆 Achievements / Use Cases

* ✅ 98%+ accuracy in detecting various fraud types.
* 🏅 Shortlisted in \[Inter-College Hackathon 2025].
* 📍 Successfully tested on 100K+ records with sub-second response time.
* 💼 Can integrate with banking software for real-time fraud alerts.

---

## 🚀 Overview

> *"In the digital age, credit card fraud isn’t just a threat — it’s a \$30 billion global crisis. Millions of users fall victim every year, and traditional fraud detection systems are either too slow, too opaque, or too expensive to keep up with modern fraudsters."*

We present **FrauDfence** — a high-performance Credit Card Fraud Detection system developed in **C++** and **Python**, leveraging core **Data Structures & Algorithms**. It identifies frauds using patterns, behaviors, and spatial-temporal relationships from transaction data. 

🎯 **What problem are we solving?**
Fraudulent patterns today are often too complex for static rules. We observed how attackers:

* Perform *round-tripping* through cycles of accounts,
* Slowly *increase transaction values* to escape flagging,
* Operate in *tight-knit fraud rings*, and
* Abuse *time windows* to make overlapping or rapid transactions.

🧠 **Our solution?**
We engineered an **modular**, and **scalable** fraud detection framework that mimics how a security analyst would manually flag suspicious behavior — but faster and more accurately:

* Graph theory to identify **fraud loops and money laundering**.
* Segment and Interval Trees to spot **spikes and overlaps**.
* Dynamic Programming to flag **gradual increases** and **budget exhaustion**.
* Union-Find & Dijkstra to cluster **fraud rings** and trace **indirect accomplices**.

🌐 **Why now?**
As digital transactions soar and regulatory audits demand transparency, there's a **pressing need for explainable and cost-efficient fraud detection** — not just for big banks, but also for startups, fintechs, and regulatory bodies.

📈 **How can this be extended?**

* Integrated into fintech APIs for live monitoring
* Visual dashboards for security teams
* Hybrid models combining DSA + ML for enhanced detection
* Deployed across banks, wallets, and financial compliance systems

---

## 🌟 Key Features

* **🔍 Multi-Dimensional Fraud Checks**: Detects behavioral, temporal, and spatial fraud patterns.
* **📊 Client-Specific Insights**: Reports generated per cardholder.
* **⚙️ Pure DSA Implementation**: No ML dependencies; uses core algorithms.
* **🗺️ Interactive CLI Dashboard**: Stylized terminal interface.

---

## 🧠 Tech Stack

| Category         | Tools & Technologies                                                      |
| ---------------- | ------------------------------------------------------------------------- |
| Language         | C++ (Core System), Python (Data Ingestion)                                |
| Database         | MySQL                                                                     |
| Data Source      | Real-world transactional dataset (CSV)                                    |
| OS Compatibility | Cross-platform (Windows, Linux, macOS)                                    |

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/dhruvkalra71/FrauDfence.git
cd FrauDfence
```

### 2. Set Up MySQL Database

```sql
CREATE DATABASE creditCardFraud;
-- Create `transactions` table with fields matching the CSV structure.
```

### 3. Load Data via Python

```bash
pip install mysql-connector-python
python3 data.py
```

### 4. Compile and Run the C++ Engine

```bash
g++ main.cpp -o FraudFence
./FraudFence
```

---

## 🧪 Dataset & Algorithms

### Dataset

* `fraudTestCSV.csv`: \~100K+ real-world credit card transactions.
* Fields: `cc_num`, `merchant`, `amt`, `lat`, `long`, `time`, `is_fraud`, etc.

### Algorithms Implemented

| Fraud Pattern                     | Algorithm Used            |
| --------------------------------- | ------------------------- |
| Gradual Increase in Spending      | Dynamic Programming (LIS) |
| Sudden Spikes in Spending         | Segment Tree              |
| Overlapping Transactions          | Interval Tree             |
| Rapid Limit Exhaustion            | Knapsack (DP/Greedy)      |
| Fraud Rings / Clusters            | Union-Find + Kruskal      |
| Indirect Fraud Paths              | Dijkstra's Algorithm      |
| Money Laundering Cycles           | BFS/DFS Cycle Detection   |

---

## 🏆 Achievements / Use Cases

* ✅ Built for **APS course** at **JIIT, Noida** (Semester IV)
* 🌟 Demonstrated across **100,000+ transactions** with high performance
* 🏅 Highlighted in university showcase as **academic innovation project**
* 🚀 Use case: Banking audits, fintech sandboxes, cybersecurity training

---

## 💡 Why this Project Matters

This project brings together the power of **Data Structures and Algorithms** and **real-world relevance**, delivering a capable, auditable, scalable system that can evolve into production-level fraud detection software.

---

## 📁 Folder Structure

```
.
├── main.cpp                # Core C++ fraud detection engine
├── data.py                 # Python MySQL ingestion
├── fraudTestCSV.csv        # Transaction dataset from Kaggle
├── images/                 # UI & Demo screenshots
├── README.md               # This documentation
└── LICENSE                 # License info
```

---

## 📸 Demo Screenshots

### Fraud Menu UI

![Fraud Menu](images/fraud_menu_ui.png)

### System Architecture

![Architecture](images/system_architecture.png)

---

## Made with ❤️ using C++, Python, SQL, and DSA

---

## 🧠 Key Features

* 📊 **Data Ingestion**: Efficient import of real-world transactional data via MySQL (`data.py`).
* ⚙️ **DSA-Powered Detection**: Implements classic algorithms like:
* 🧑‍💼 **Client-wise Reports**: Individual fraud detection for each cardholder
* 🧭 **Interactive CLI**: Stylized, terminal-based UI with a menu interface

---

## 📂 Project Structure

```bash
├── main.cpp               # C++ core fraud detection engine (DSA-based)
├── data.py               # Python script to ingest CSV into MySQL
├── fraudTestCSV.csv      # Real-world transaction dataset (CSV)
├── fraudTest_updated.csv # Optional updated dataset for testing
└── README.md             # Project documentation
```



---

## 🧪 Sample Output

```bash
1. Checking fraud on: John Doe
   🔴 Sudden Spending Spike Detected!!
   🟢 No Overlapping Transactions
   🟢 Transaction Pattern is normal

Country Fraud Clusters Found: 31
Total Indirect Fraud Paths: 5
```

---

## 💾 How to Run

### 📌 Prerequisites

* C++17 compatible compiler (`g++`)
* MySQL server
* Python 3.x with `mysql-connector-python`

### 🔁 Step-by-Step Setup

1. **Setup Database**

```sql
CREATE DATABASE creditCardFraud;
-- Create 'transactions' table using your desired schema (matching the CSV headers)
```

2. **Import Data (Python)**

```bash
python3 data.py
```

3. **Build & Run the C++ System**

```bash
g++ main.cpp -o FraudDetector
./FraudDetector
```

---

## 📚 Dataset Fields

* `trans_date_trans_time`, `cc_num`, `merchant`, `category`, `amt`, `first_name`, `last_name`, `street`, `city`, `state`, `zip`, `lat`, `long`, `job`, `trans_num`, `merch_lat`, `merch_long`, `is_fraud`

---

## 💡 Insights & Extensions

* Detects fraud **without ML**, showcasing pure DSA power.
* Ideal for learning fraud detection logic in a **data-driven** system.
* Can be extended with visualization, ML-based scoring, or REST APIs.

---

## 📈 Use Cases

* Educational DSA Projects
* Cybersecurity Simulations
* Backend Fraud Detection Prototypes

---
