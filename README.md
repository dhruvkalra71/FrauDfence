# 💳 Credit Card Fraud Detection System (DSA-Driven)

A high-performance Credit Card Fraud Detection system developed in **C++** and **Python**, leveraging core **Data Structures & Algorithms**. It identifies frauds using patterns, behaviors, and spatial-temporal relationships from transaction data.

---

## 🧠 Key Features

* 📊 **Data Ingestion**: Efficient import of real-world transactional data via MySQL (`data.py`).
* ⚙️ **DSA-Powered Detection**: Implements classic algorithms like:

  * **LIS** (Dynamic Programming) → Gradual Increase Detection
  * **Segment Tree** → Sudden Spending Spike
  * **Interval Tree** → Overlapping Transactions
  * **Knapsack** → Unusual Spending Patterns
  * **Union-Find** → Fraud Clustering
  * **Dijkstra's Algorithm** → Indirect Fraud Paths
  * **BFS (Cycle Detection)** → Transaction Loops (Money Laundering)
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

## 🛠️ Algorithms & Techniques

| Fraud Type                        | Algorithm/DSA Used         | Function                                         |
| --------------------------------- | -------------------------- | ------------------------------------------------ |
| Gradual Increase in Spending      | Longest Increasing Subseq. | `graduallyIncreasingFraudelentTransactionAmount` |
| Sudden Spike in Spending          | Segment Tree               | `suddenSpikeInSpending`                          |
| Overlapping Transactions (Time)   | Interval Tree              | `detectOverlappingTransactions`                  |
| Unusual Spending Patterns         | Knapsack (DP & Greedy)     | `unusualSpendingPatterns`                        |
| Clustered Fraudulent Transactions | Union-Find (Kruskal)       | `clusterFraudlentTransactionsTogether`           |
| Indirect Fraud Paths              | Dijkstra’s Algorithm       | `shortestFraudPathBetweenTransactions`           |
| Fraud Loops (Money Laundering)    | BFS with Cycle Detection   | `fraudLoopInTransactionHistory`                  |

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
