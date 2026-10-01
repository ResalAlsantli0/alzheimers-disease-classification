# Alzheimer's Disease Classification

A data mining project that explores demographic, lifestyle, clinical, and cognitive patient attributes to classify Alzheimer's disease diagnosis. The study covers data cleaning, exploratory analysis, visualization, model training, and comparative evaluation across six machine-learning classifiers.

> Educational portfolio project - not a medical diagnostic tool.

## Project highlights

- Cleaned duplicate records and handled missing values using mode, median, and mean imputation.
- Investigated continuous-feature outliers with box plots and the IQR method.
- Applied Min-Max scaling to continuous features while preserving binary variables.
- Performed exploratory data analysis with descriptive statistics and correlation analysis.
- Compared six classification algorithms using accuracy, F1-score, Jaccard score, log loss, confusion matrices, and classification reports.
- Evaluated model behavior with a 70/30 train-test split.

## Models evaluated

| Model | Test accuracy | F1-score | Jaccard score | Log loss |
| --- | ---: | ---: | ---: | ---: |
| Logistic Regression | 80.47% | 0.7225 | 0.5655 | 0.4319 |
| K-Nearest Neighbors | 66.36% | 0.3599 | 0.2194 | N/A |
| Decision Tree | **93.33%** | **0.9095** | **0.8340** | N/A |
| Random Forest | 90.54% | 0.8635 | 0.7598 | 0.4319 |
| Naive Bayes | 80.62% | 0.7289 | 0.5734 | **0.4312** |
| Support Vector Machine | 80.62% | 0.7191 | 0.5614 | **0.4312** |

The Decision Tree produced the strongest reported overall result, leading on accuracy, F1-score, and Jaccard score. These results reflect this particular dataset and split and should not be interpreted as evidence of clinical readiness.

## Repository structure

```text
data/
  README.md                              Dataset download instructions
notebooks/
  alzheimers_classification.ipynb       Complete analysis notebook
  alzheimers_classification.html        Viewable notebook export
requirements.txt                        Python dependencies
```

## Dataset

The project uses the **Alzheimer's Disease Dataset** by Rabie El Kharoua, published on Kaggle. It contains 2,149 patient records and 35 attributes covering demographics, lifestyle factors, medical history, clinical measurements, cognitive assessments, symptoms, and diagnosis.

Download the dataset from [Kaggle](https://www.kaggle.com/dsv/8668279), rename the CSV to `alzheimer_disease_patient.csv`, and place it in the `data/` directory.

The dataset is not duplicated in this repository. Refer to Kaggle for the source license, documentation, and citation information.

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab notebooks/alzheimers_classification.ipynb
```

Before running the notebook, confirm that this file exists:

```text
data/alzheimer_disease_patient.csv
```

## Methodology

1. Data quality checks and duplicate removal.
2. Missing-value imputation based on feature type.
3. Outlier inspection and treatment.
4. Feature scaling and removal of non-informative attributes.
5. Exploratory data analysis and visualization.
6. Train-test split and classifier training.
7. Multi-metric model comparison.

## Tools

- Python
- pandas and NumPy
- Matplotlib and seaborn
- scikit-learn
- Jupyter Notebook

## Limitations and responsible use

- This is a course project based on a public dataset, not a validated clinical system.
- Reported scores come from a single train-test split and may vary with a different random seed or sample.
- Preprocessing and tuning should be placed inside cross-validation pipelines for a production-grade evaluation and to avoid data leakage.
- Clinical deployment would require external validation, bias analysis, calibration, explainability, privacy safeguards, and specialist review.

## Team

Developed collaboratively for the DS312 Data Mining course at Princess Nourah bint Abdulrahman University by:

- Alhanouf Alsaiary
- Haya Altmmami
- Summer Alhamail
- Resal Alsantli
- Lena Aldokhayel

Team attribution is retained without publishing student identification numbers.
