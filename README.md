# FLASH IDS — Provenance Graph Based Intrusion Detection System

## Overview

This project is based on the research paper:

**FLASH: A Comprehensive Approach to Intrusion Detection via Provenance Graph Representation Learning**

FLASH IDS is a graph-based intrusion detection system designed to detect stealthy cyber attacks such as:
- Advanced Persistent Threats (APT)
- PowerShell Empire Attacks
- Data Exfiltration Attacks
- Zero-Day Attacks
- Mimicry Attacks

Unlike traditional IDS systems that rely on signatures and static rules, FLASH uses:
- Provenance Graphs
- Word2Vec Semantic Encoding
- Temporal Encoding
- Graph Neural Networks (GraphSAGE)
- Embedding Recycling
- XGBoost Classification

to perform scalable and real-time intrusion detection.

---

# Objective

The objective of this project was:
- To understand the working of FLASH IDS
- To execute and analyze the research implementation
- To study provenance graph based intrusion detection
- To reproduce experimental outputs and graphs
- To evaluate attack detection and scalability

---

# Novelty Work

The following additional work was performed during the project:

- Divided large datasets into smaller chunks for efficient streaming analysis
- Created custom evaluation graphs and comparison plots
- Performed threshold sensitivity analysis for anomaly detection
- Simulated real-time streaming detection using batch event processing

---

# Datasets Used

The following datasets were used:

| Dataset | Purpose |
|---|---|
| DARPA OpTC | Enterprise attack detection |
| DARPA E3 | Provenance graph evaluation |
| StreamSpot | Streaming graph anomaly detection |
| Unicorn | IDS comparison |

---

# Project Workflow

```text
System Logs
    ↓
Provenance Graph Construction
    ↓
Word2Vec Semantic Encoding
    ↓
Temporal Encoding
    ↓
Graph Neural Network (GraphSAGE)
    ↓
Embedding Recycling Database
    ↓
XGBoost Classifier
    ↓
Attack Detection & Alerts
```

---

# How FLASH IDS Works

## 1. Log Collection

FLASH collects:
- Windows Event Logs
- Linux Audit Logs
- File activities
- Process executions
- Network connections

---

## 2. Provenance Graph Construction

System activities are converted into provenance graphs.

### Nodes
- Processes
- Files
- Sockets
- Modules

### Edges
- Read
- Write
- Execute
- Send
- Receive

Example:

```text
Outlook.exe
    ↓
PowerShell.exe
    ↓
Sensitive Files
```

---

## 3. Semantic Encoding

FLASH uses Word2Vec to generate semantic embeddings from:
- process names,
- command line arguments,
- file paths,
- IP addresses.

This helps FLASH understand suspicious behavior patterns.

---

## 4. Temporal Encoding

FLASH preserves event order using positional encoding.

Example:

```text
download
→ execute
→ compress
→ exfiltrate
```

This sequence strongly indicates malicious behavior.

---

## 5. Graph Neural Network (GraphSAGE)

FLASH uses GraphSAGE to learn:
- node relationships,
- graph structures,
- neighborhood behavior.

This helps identify stealthy malicious nodes.

---

## 6. Embedding Recycling

Previously generated embeddings are stored and reused.

Benefits:
- reduced computation,
- faster inference,
- real-time scalability.

---

## 7. XGBoost Classification

FLASH combines:
- semantic embeddings,
- temporal information,
- graph embeddings.

XGBoost classifies nodes as:
- normal,
- malicious.

---

# Attack Detection Flow

Typical attack flow detected by FLASH:

```text
Phishing Email
    ↓
PowerShell Execution
    ↓
Sensitive File Access
    ↓
Data Compression
    ↓
Data Exfiltration
```

FLASH analyzes:
- relationships,
- execution order,
- semantic meaning,
- graph structure

to detect attacks effectively.

---

# Notebooks Executed

The following notebooks were executed and analyzed:

- `OpTC.ipynb`
- `streamspot.ipynb`
- `unicorn.ipynb`
- `Cadets.ipynb`
- `Theia.ipynb`
- `Trace.ipynb`
- `FiveDirections.ipynb`

---

# Graphs and Outputs Generated

Generated outputs include:
- Precision/Recall/F-score graphs
- Runtime comparison graphs
- FLASH vs Unicorn comparison tables
- Streaming detection analysis
- Scalability evaluation plots

---

# Technologies Used

- Python
- PyTorch
- Torch Geometric
- Gensim
- XGBoost
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

---

# Advantages of FLASH IDS

| Feature | FLASH IDS |
|---|---|
| Semantic Understanding | Yes |
| Temporal Encoding | Yes |
| Graph Learning | Yes |
| Real-Time Detection | Yes |
| Low False Positives | Yes |
| Scalable Architecture | Yes |

---

# Conclusion

FLASH IDS provides a scalable and intelligent intrusion detection framework using provenance graph representation learning.

By combining:
- semantic analysis,
- temporal encoding,
- graph neural networks,
- embedding recycling,

FLASH achieves:
- high detection accuracy,
- real-time scalability,
- effective detection of stealthy cyber attacks.
