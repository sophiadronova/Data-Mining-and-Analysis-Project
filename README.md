# Detecting Illicit Bitcoin Transactions
**Project Video:** https://youtu.be/np0U2wd_VUs

---

## Overview
This project analyzes illicit financial activity using the Elliptic++ Bitcoin Transaction Dataset, a large transaction network, to understand how fraud can be detected in complex, real-world systems. It investigates three key approaches: structural graph analysis to uncover how illicit transactions behave within the network, anomaly detection to test whether fraud appears as unusual behavior, and supervised machine learning models to evaluate predictive performance. A central finding is that detecting fraud is inherently difficult—illicit transactions often closely resemble normal ones, and severe class imbalance means they are rare and easy to miss, causing anomaly detection methods to perform poorly. While graph structure reveals meaningful patterns, it is not sufficient on its own, and the strongest results come from combining rich features with supervised learning. This problem is important beyond cryptocurrency: in a world driven by massive volumes of digital transactions, improving fraud detection has real-world impact for financial security, preventing money laundering, and protecting individuals and institutions across all transaction-based systems.

---

## 👉 Main Notebook
**Start here:**  `main_notebook.ipynb`

Run this notebook top-to-bottom to reproduce all results.

---

## Research Questions
- Do illicit transactions occupy distinct structural positions in the transaction graph, and how do these patterns evolve over time?
- Can anomaly detection methods identify illicit transactions based on transaction features and graph-derived features?
- Do Graph Neural Networks improve illicit transaction detection compared to classical approaches, and how does class imbalance handling affect their performance?

---

## Data

This project uses the data from the following github repo:

- GitHub: https://github.com/git-disl/EllipticPlusPlus/tree/main/Transactions%20Dataset  

The dataset contains Bitcoin transactions represented as a graph, where:
- Nodes = transactions  
- Edges = money flow between transactions  
- Labels = illicit, licit, or unknown  

We use only labeled transactions and create additional graph features such as degree and PageRank. A temporal train/test split is applied based on time steps.

---

## Reproducibility / How to Run

This project was developed in Google Colab, but can also be run locally.

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Download data
Download the dataset from the github link above

### 3. Run the notebook
Run:
`main_notebook.ipynb`
from top to bottom.


## Key Dependencies

- Python 3.10
- pandas 2.x
- numpy 1.x
- scikit-learn 1.x
- networkx 3.x
- matplotlib 3.x
- torch 2.x
- torch-geometric

(Full list available in `requirements.txt`)

## Repository Structure

```
.
├── main_notebook.ipynb
├── requirements.txt
├── checkpoints/
└── README.md
```

---

## Results Summary

- Anomaly detection performs poorly, often near random baseline  
- Illicit transactions are not strongly anomalous  
- Supervised models significantly outperform anomaly detection  
- Random Forest achieves the best performance (F1 ≈ 0.82)  
- Graph features provide some signal but do not improve top models substantially  
- GCN improves over anomaly detection but does not outperform simpler models  

**Key takeaway:** Fraud detection is difficult because illicit behavior closely resembles normal transactions, making supervised learning with strong features the most effective approach.

## Citation
Elmougy, Y., & Liu, L. (2023).
Demystifying Fraudulent Transactions and Illicit Nodes in the Bitcoin Network for Financial Forensics.
Proceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD ’23).
https://doi.org/10.1145/3580305.359980

```
@article{elmougy2023demystifying,
  title={Demystifying Fraudulent Transactions and Illicit Nodes in the Bitcoin Network for Financial Forensics},
  author={Elmougy, Youssef and Liu, Ling},
  journal={arXiv preprint arXiv:2306.06108},
  year={2023}
}
```




