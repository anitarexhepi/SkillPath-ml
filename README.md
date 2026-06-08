# SkillPath - Machine Learning Analysis

## Project Overview

SkillPath is a Machine Learning project developed using the LinkedIn Job Postings 2024 dataset.

The project focuses on two main tasks:

1. Career Level Classification

   * Predicting whether a job posting belongs to Junior, Mid-Level, or Senior career levels.

2. Job Clustering

   * Grouping similar job postings based on skills, descriptions, industries, and locations using unsupervised learning techniques.

---

## Dataset

Dataset: LinkedIn Job Postings 2024

Files used:

* linkedin_job_postings.csv
* job_skills.csv

The dataset contains information about:

* Job titles
* Job descriptions
* Required skills
* Industries
* Locations

The dataset is used for both classification and clustering tasks.

---

## Machine Learning Methodology

### Data Preprocessing

The following preprocessing steps were performed:

* Dataset loading
* Data cleaning
* Handling missing values
* Career level label engineering
* Label encoding
* Feature engineering
* TF-IDF vectorization
* Train/Test split

### Features Used

The classification model uses:

* Job Title
* Job Description
* Industry
* Location
* Required Skills

---

## Classification Task

The goal is to classify job postings into:

* Junior
* Mid-Level
* Senior

### Algorithms Implemented

1. K-Nearest Neighbors (KNN)
2. Decision Tree
3. Random Forest
4. Neural Network (MLP)

### Hyperparameter Tuning

The following parameters were tested:

#### KNN

* k = 3
* k = 5
* k = 7
* k = 11
* k = 15

#### Decision Tree

* max_depth = 4
* max_depth = 8
* max_depth = 12
* max_depth = 16
* max_depth = None

#### Random Forest

* n_estimators = 50
* n_estimators = 100
* n_estimators = 200

#### Neural Network

Architecture 1:

* Hidden layers: (64, 32)

Architecture 2:

* Hidden layers: (128, 64, 32)

Activation function:

* ReLU

---

## Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Generated outputs:

* comparison_table.csv
* classifier_comparison.png
* confusion_matrices.png

---

## Clustering Task

The project also applies K-Means clustering on job postings.

### Clustering Steps

* Removal of target labels
* TF-IDF feature extraction
* PCA dimensionality reduction
* K-Means clustering
* Silhouette score evaluation
* Cluster composition analysis

### Generated Outputs

* clustering_pca.png
* silhouette_curve.png
* cluster_composition.csv
* cluster_composition_heatmap.png

---

## Technologies Used

* Python
* NumPy
* Pandas
* Scikit-Learn
* Matplotlib
* Seaborn

---

## Installation

Install required libraries:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Place the dataset files in:

```text
C:\data\
```

Required files:

```text
linkedin_job_postings.csv
job_skills.csv
```

Run:

```bash
python main.py
```

---

## Output Files

The project automatically generates:

* comparison_table.csv
* classifier_comparison.png
* confusion_matrices.png
* clustering_pca.png
* silhouette_curve.png
* cluster_composition.csv
* cluster_composition_heatmap.png

---

## Conclusion

The project demonstrates the application of supervised and unsupervised machine learning techniques on real-world job market data. Multiple classification models were compared, clustering techniques were applied, and the results were analyzed through evaluation metrics and visualizations.
