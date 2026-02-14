# Data-Mining-and-Analysis-Project

## Motivation
Financial fraud detection is a critical challenge due to the scale, anonymity, and evolving nature of cryptocurrency transactions. Understanding structural and temporal patterns of illicit activity in transaction networks can improve detection methods and support financial forensics.

## Problem Statement
The goal of this project is to analyze structural and temporal characteristics of illicit Bitcoin transactions and evaluate whether graph-based features can help distinguish illicit activity from licit behavior.

## Dataset Summary
The Elliptic++ dataset is a large-scale directed graph of Bitcoin transactions designed for studying illicit activity detection. The network contains approximately 203,769 transactions (nodes) connected by 234,355 directed edges representing money flows. Transactions are observed across 49 time steps, capturing the temporal evolution of the network. Each transaction includes numerical features describing transaction behavior, along with class labels indicating illicit, licit, or unknown status for a subset of nodes. The dataset exhibits severe class imbalance, with illicit transactions representing a small minority, and the graph structure is highly sparse and fragmented.

## Key Findings (so far)
- Severe class imbalance (illicit transactions are rare)
- Network is sparse and fragmented
- Degree distribution is highly skewed
- Illicit transactions tend to have lower connectivity
- Illicit activity varies across time steps

## Key Limitations
- Severe class imbalance
- Many unlabeled nodes
- Large graph size
- Sparse connectivity
  
## Dataset Source
This project uses the Elliptic++ Bitcoin transaction dataset introduced in:

Elmougy, Y., & Liu, L. (2023).
Demystifying Fraudulent Transactions and Illicit Nodes in the Bitcoin Network for Financial Forensics.
Proceedings of the 29th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD ’23).
https://doi.org/10.1145/3580305.3599803

```
@article{elmougy2023demystifying,
  title={Demystifying Fraudulent Transactions and Illicit Nodes in the Bitcoin Network for Financial Forensics},
  author={Elmougy, Youssef and Liu, Ling},
  journal={arXiv preprint arXiv:2306.06108},
  year={2023}
}
```
