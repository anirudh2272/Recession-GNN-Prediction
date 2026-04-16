📉 **Recession Prediction using Temporal Graph Neural Networks (TGNN)**

---

**Overview**

This project predicts economic recessions using a Temporal Graph Neural Network (TGNN) by modeling macroeconomic indicators as a dynamic graph.

Instead of treating variables independently, it captures:

* Relationships between economic indicators
* How these relationships evolve over time

---

**Approach**

* Nodes → Economic indicators (GDP, CPI, Unemployment, etc.)
* Edges → Correlation-based relationships
* Model → TGNN (Graph Convolution + Temporal Learning)

```
Input Data → Graph Construction → GCN Layers → GRU → Prediction
```

---

**Dataset**

* 20+ macroeconomic indicators
* Time range: 1985 – 2023
* Sources:

  * Federal Reserve (FRED)
  * BLS
  * World Bank
  * IMF

Note: Raw datasets are not included due to size.

---

**Pipeline**

* Data preprocessing and normalization
* Temporal alignment of multi-frequency data
* Graph construction (Pearson correlation)
* Model training (GCN, TGNN)
* Class imbalance handling (SMOTE, Focal Loss)
* Evaluation (Accuracy, F1, AUC)
* Local deployment using Gradio

---

**Results**

Model Performance:

* GCN → Accuracy ~0.87 | F1 ~0.87 | AUC ~0.95
* TGNN → Accuracy ~0.97 | F1 ~0.95 | AUC ~0.99

Insight: Temporal modeling significantly improves prediction performance.

---

**Run the Project**

```
python Interface.py
```

Open in browser:

```
http://127.0.0.1:7860
```

---

**Project Structure**

```
gnn_pipeline.ipynb      → Training pipeline  
Interface.py           → Prediction interface  
DataMining_report.pdf  → Detailed report  
artifacts/             → scaler, features, graph data  
models/                → trained models  
```

---

**Limitations**

* Uses linear correlation (no nonlinear relationships)
* No explainability module
* Requires careful time-series validation

---

**Future Improvements**

* Graph Attention Networks (GAT / TGAT)
* Explainable AI (SHAP, GNNExplainer)
* Real-time data integration
* API deployment (FastAPI + Docker)

---

**Author**

Anirudh Koganti
M.S. Computer Science — Missouri S&T

---

⭐ If you found this useful, consider starring the repository
