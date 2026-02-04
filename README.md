# Unsupervised Discovery of Immunotherapy Resistance Biomarkers in Melanoma

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Tech](https://img.shields.io/badge/Bioinformatics-PCA%20%2F%20Transcriptomics-green)

## Abstract
In this project I have simulated and analyzed **bulk RNA-seq data** from a cohort of 100 melanoma patients treated with immunotherapy. They are NOT real. The only purpose was to work through a process of dimensionality reduction. What decisions do we make? Why do we make theem? What's the math behind the results? And what can EXACTLY be said mathematically about the results we got? Using unsupervised machine learning techniques (**Principal Component Analysis**), the study identifies distinct molecular subtypes driving treatment resistance.

The analysis demonstrates a robust workflow for high-dimensional biological data, moving from quality control and normalization strategies to biological interpretation of latent variables.

## Key findings
The unsupervised analysis revealed three distinct patient clusters:
1.  **Responders ("Hot Tumors"):** Characterized by high expression of immune markers (T-cells) and low proliferation.
2.  **Non-Responders ("Cold Tumors"):** Characterized by high proliferative signatures and immune desertification.
3.  **Noisy/Technical Cluster:** Defined by aberrant housekeeping gene expression.

> **Clinical implication:** Patients with a negative PC1 score are predicted to respond favorably to checkpoint inhibitors.

## Computational workflow
The project follows a standard bioinformatics pipeline:
1.  **Data Simulation:** Generation of synthetic counts modeling negative binomial distribution with technical outliers.
2.  **Quality Control (QC):** Detection of "leverage points" using raw PCA projections.
3.  **Normalization:** Application of `log1p` transformation and Z-score scaling to handle exponential gene expression distributions.
4.  **Dimensionality Reduction:** PCA to compress 50 genes into interpretable biological axes.
5.  **Feature Extraction:** Analysis of Loadings to decode the biological meaning of PC1 and PC2.

## Requirements
To reproduce this analysis, you will need the following libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

## How to run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Open the Jupyter Notebook in the `notebooks/` directory.

---
*Author: [Tu Nombre]* *Targeting precision medicine applications in oncology.*
