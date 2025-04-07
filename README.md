<p align="center">
  <img src="https://github.com/Heihei0421/mirna-ml-project/blob/main/banner.png" alt="miRNA ML Banner" width="600"/>
</p>

#  miRNA-Disease Association Prediction using Machine Learning

This project aims to predict whether a microRNA (miRNA) is associated with cancer using basic sequence features and machine learning techniques. It combines biological knowledge from HMDD and sequence data from miRBase, extracts biologically meaningful features, and builds a classifier to distinguish between cancer-related and non-cancer miRNAs.

---

##  Project Structure

```
mirna-ml-project/
├── notebooks/
│   ├── 01_data_eda.ipynb           # Data cleaning & feature engineering
│   └── 02_model_training.ipynb     # Model training, evaluation & visualization
├── data/
│   └── processed/
│       └── mirna_features.csv      # Final feature dataset used for modeling
├── README.md
└── requirement.txt                 # Python dependencies
```


---

##  Data Sources

| Source | Description |
|--------|-------------|
| [HMDD v3.2](http://www.cuilab.cn/hmdd) | Curated list of experimentally supported miRNA-disease associations |
| [miRBase](https://www.mirbase.org/) | Mature miRNA sequences in FASTA format |

---

##  Feature Extraction

We extracted basic sequence-level features from each miRNA:

| Feature       | Description                              |
|---------------|------------------------------------------|
| `length`      | Total number of nucleotides              |
| `gc_content`  | Proportion of G and C nucleotides        |
| `au_content`  | Proportion of A and U nucleotides        |

> Feature extraction is done in `01_data_eda.ipynb`, and the resulting dataset is stored in `mirna_features.csv`.

---

##  Model Training & Evaluation

A `RandomForestClassifier` was trained to classify miRNAs as either cancer-associated (`label = 1`) or not (`label = 0`).

### Model Specs

- Classifier: `RandomForestClassifier(n_estimators=100, random_state=42)`
- Data Split: 80% training / 20% testing
- Input features: `length`, `gc_content`, `au_content`

### Evaluation Metrics

| Metric              | Description |
|---------------------|-------------|
| ✅ Classification Report | Precision, Recall, F1-score |
| ✅ Confusion Matrix      | Heatmap of prediction vs actual labels |
| ✅ Feature Importance     | Visual ranking of each input feature |
| ✅ ROC-AUC Score          | Classifier effectiveness over thresholds |

All evaluations and plots are available in `02_model_training.ipynb`.

---

##  Sample Output

<img width="535" alt="截屏2025-04-07 22 48 47" src="https://github.com/user-attachments/assets/e2e0e965-7442-40cc-a656-20a1d37f8ebb" />

<img width="541" alt="截屏2025-04-07 22 49 35" src="https://github.com/user-attachments/assets/8511e9ee-7061-442b-b1a2-fd77fcb0bfbd" />

```python
ROC-AUC Score: 0.87
Top Feature: GC Content

## Contact
Email: 2977811Y@student.gla.ac.uk  

