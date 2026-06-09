# SkillPath - Machine Learning Analysis

## Project Overview

SkillPath is a Machine Learning project developed using the LinkedIn Job Postings 2024 dataset.

The goal of the project is to analyze real-world job market data using both supervised and unsupervised machine learning techniques.

The project focuses on two main tasks:

1. Career Level Classification
   - Predicting whether a job posting belongs to Junior, Mid-Level, or Senior career levels.

2. Job Clustering
   - Grouping similar job postings based on textual information, skills, industries, and locations.

---

## Dataset

Dataset: LinkedIn Job Postings 2024

Files used:

- linkedin_job_postings.csv
- job_skills.csv

The dataset contains:

- Job titles
- Job descriptions
- Required skills
- Industries
- Locations

The same dataset is used for both classification and clustering tasks.

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Dataset loading and merging
- Data cleaning
- Missing value handling
- Career level label engineering
- Label encoding
- Feature engineering
- TF-IDF vectorization
- Feature selection/reduction
- Train/Test split
- Feature scaling

---

## Features Used

The classification models use:

- Job Title
- Job Description
- Industry
- Location
- Required Skills

TF-IDF vectorization was applied to transform textual information into numerical features.

Feature selection/reduction was performed using TF-IDF with max_features=300. This keeps the 300 most important textual features and reduces the dimensionality of the dataset.

---

# Classification Task

## Target Classes

- Junior
- Mid-Level
- Senior

## Algorithms Implemented

1. K-Nearest Neighbors (KNN)
2. Decision Tree
3. Random Forest
4. Neural Network (MLP)

---

## Hyperparameter Tuning

### KNN

Tested values:

- k = 3
- k = 5
- k = 7
- k = 11
- k = 15

### Decision Tree

Tested values:

- max_depth = 4
- max_depth = 8
- max_depth = 12
- max_depth = 16
- max_depth = None

### Random Forest

Tested values:

- n_estimators = 50
- n_estimators = 100
- n_estimators = 200

### Neural Network

Architecture 1:

- Hidden layers: (64, 32)

Architecture 2:

- Hidden layers: (128, 64, 32)

Activation Function:

- ReLU

The best-performing architecture was selected based on the weighted F1-score.

---

## Evaluation Metrics

The classifiers were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Generated outputs:

- comparison_table.csv
- classifier_comparison.png
- confusion_matrices.png

---

# Clustering Task

K-Means clustering was applied after removing the target labels.

## Clustering Workflow

- Removal of class labels
- TF-IDF feature extraction
- PCA dimensionality reduction
- K-Means clustering
- Silhouette Score evaluation
- Cluster composition analysis

## Tested Cluster Sizes

- K = 3
- K = 4
- K = 5
- K = 6
- K = 8

The optimal value was selected using the Silhouette Score.

---

## Clustering Outputs

Generated files:

- clustering_pca.png
- silhouette_curve.png
- cluster_composition.csv
- cluster_composition_heatmap.png

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-Learn
- Matplotlib
- Seaborn

---

## Installation

Install required libraries:

```bash
pip install -r requirements.txt
```

## Running the Project

Place the dataset files inside:

```text
C:\data\
```

Required files:

```text
linkedin_job_postings.csv
job_skills.csv
```

Run the project:

```bash
python main.py
```

---

## Output Files

The project automatically generates:

- comparison_table.csv
- classifier_comparison.png
- confusion_matrices.png
- clustering_pca.png
- silhouette_curve.png
- cluster_composition.csv
- cluster_composition_heatmap.png

Output files are saved in:

```text
backend/public/ml-outputs/
```

---

## Conclusion

This project demonstrates the application of both supervised and unsupervised machine learning techniques on real-world job market data.

Multiple classification models were trained, optimized, evaluated, and compared using standard evaluation metrics. In addition, clustering techniques were applied to discover hidden structures within job postings and compare them with real career-level labels.

The results provide insights into career-level prediction and job market segmentation using machine learning methods.