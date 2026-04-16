# 📉 Recession Prediction using Temporal Graph Neural Networks (TGNN)

---

## 🚀 Overview

This project predicts **economic recessions** using a **Temporal Graph Neural Network (TGNN)** by modeling macroeconomic indicators as a **dynamic graph**.

Instead of treating variables independently, this approach captures:

* Relationships between economic indicators
* How these relationships evolve over time

---

## 🧠 Approach

* **Nodes:** Economic indicators (GDP, CPI, Unemployment, etc.)
* **Edges:** Correlation-based relationships
* **Model:** TGNN (Graph Convolution + Temporal Learning)

```text
Input Data → Graph Construction → GCN Layers → GRU → Prediction
```

---

## 📊 Dataset

* 20+ macroeconomic indicators
* Time range: **1985 – 2023**
* Data sources:

  * Federal Reserve (FRED)
  * BLS
  * World Bank
  * IMF

⚠️ Raw datasets are not included due to size.

---

## ⚙️ Pipeline

1. Data preprocessing & normalization
2. Temporal alignment of multi-frequency data
3. Graph construction (Pearson correlation)
4. Model training (GCN, TGNN)
5. Class imbalance handling (SMOTE, Focal Loss)
6. Evaluation (Accuracy, F1, AUC)
7. Local deployment using Gradio

---

## 📈 Results

| Model | Accuracy  | F1 Score | AUC      |
| ----- | --------- | -------- | -------- |
| GCN   | ~0.87     | 0.87     | 0.95     |
| TGNN  | **~0.97** | **0.95** | **0.99** |

**Insight:**
Temporal modeling significantly improves recession prediction performance.

---

## 🖥️ Run the Project

```bash
python Interface.py
```

Then open:

```
http://127.0.0.1:7860
```

---

## 📂 Project Structure

```text
├── gnn_pipeline.ipynb      # Training pipeline
├── Interface.py           # Prediction interface
├── DataMining_report.pdf  # Detailed report
├── artifacts/             # scaler, features, graph edges
├── models/                # trained models
```

---

## ⚠️ Limitations

* Linear relationships only (Pearson correlation)
* No explainability module
* Potential time-series leakage if not handled carefully

---

## 🔮 Future Improvements

* Graph Attention Networks (GAT / TGAT)
* Explainable AI (SHAP, GNNExplainer)
* Real-time data integration (FRED API)
* API deployment (FastAPI + Docker)

---

## 👨‍💻 Author

**Anirudh Koganti**
M.S. Computer Science — Missouri S&T

---

⭐ If you found this project interesting, consider starring the repository!
