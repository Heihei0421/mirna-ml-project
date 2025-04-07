# Bioinformatics & Machine Learning Project
# Predicting Cancer-Associated microRNAs using Machine Learning

This project explores the use of sequence-derived features from human microRNAs to predict their association with cancer using machine learning models.

**Supervisor**: Prof. Kevin Bryson  
**Student**: Hang Yin | MSc Data Science, University of Glasgow

---

## Objectives

- Integrate public bioinformatics data (HMDD, miRBase)
- Extract simple but effective features (e.g. GC content, sequence length)
- Train ML models to predict miRNA-disease associations
- Evaluate model performance and interpret biological relevance

---

## Dataset Sources

- **HMDD v3.2**: [http://www.cuilab.cn/hmdd](http://www.cuilab.cn/hmdd)  
- **miRBase**: [https://www.mirbase.org/download/](https://www.mirbase.org/download/)

The final processed dataset contains:
- 800+ labeled miRNAs
- Features: GC content, sequence length (k-mer to be added)
- Binary label: 1 = cancer-related, 0 = not cancer-related

---

## Methodology

| Step | Description |
|------|-------------|
| 1 | Load miRNA sequence & cancer association |
| 2 | Feature extraction (GC %, length) |
| 3 | Random Forest classifier |
| 4 | Performance evaluation (F1, ROC-AUC) |



## Next Steps

- Add k-mer based features
- Explore deep learning sequence models
- Expand to multi-class disease classification

---

## How to Run

```bash
# Set up environment
pip install -r requirements.txt

# Run Notebooks:
# 1. Data preparation
# 2. Model training and evaluation


## Contact
 
Email: 2977811Y@student.gla.ac.uk  

