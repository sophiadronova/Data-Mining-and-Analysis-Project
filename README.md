# Detecting Illicit Bitcoin Transactions

This project analyzes illicit financial activity using the Elliptic++ Bitcoin Transaction Dataset, a large transaction network, to understand how fraud can be detected in complex, real-world systems. It investigates three key approaches: structural graph analysis to uncover how illicit transactions behave within the network, anomaly detection to test whether fraud appears as unusual behavior, and supervised machine learning models to evaluate predictive performance. A central finding is that detecting fraud is inherently difficult—illicit transactions often closely resemble normal ones, and severe class imbalance means they are rare and easy to miss, causing anomaly detection methods to perform poorly. While graph structure reveals meaningful patterns, it is not sufficient on its own, and the strongest results come from combining rich features with supervised learning. This problem is important beyond cryptocurrency: in a world driven by massive volumes of digital transactions, improving fraud detection has real-world impact for financial security, preventing money laundering, and protecting individuals and institutions across all transaction-based systems.

### 👉 The main deliverable is main_notebook.ipynb

## Research Questions
- Do illicit transactions occupy distinct structural positions in the transaction graph, and how do these patterns evolve over time?
- Can anomaly detection methods identify illicit transactions based on transaction features and graph-derived features?
- Do Graph Neural Networks improve illicit transaction detection compared to classical approaches, and how does class imbalance handling affect their performance?
  
## Project Video
https://youtu.be/np0U2wd_VUs

## Dataset Source
This project uses the Elliptic++ Bitcoin transaction dataset

Github: https://github.com/git-disl/EllipticPlusPlus/tree/main/Transactions%20Dataset

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
