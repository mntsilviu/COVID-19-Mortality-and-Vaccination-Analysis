# COVID-19 Data Analysis, Mortality and Vaccination Prediction

## Introduction
This project performs an in-depth analysis of COVID-19 epidemiological data to understand trends in confirmed cases, mortality, and vaccination dynamics. The study focuses on both descriptive analysis and predictive modeling, with an emphasis on mortality prediction and vaccination evolution using regression-based machine learning models.

The analysis is based on real-world data retrieved from Google Cloud BigQuery and processed within the **Google Cloud Platform (GCP)** ecosystem, using a distributed environment built with PySpark. The main goal is to evaluate how different models perform in predicting COVID-19 mortality and vaccination trends, as well as to interpret these results in an epidemiological context.

---

## Objectives
The main objectives of this project are:
- **Data extraction** from Google Cloud Platform (GCP) using BigQuery
- **Data cleaning and transformation** to prepare the dataset for analysis
- **Exploratory Data Analysis (EDA)** to identify trends and patterns
- **Construction of derived epidemiological indicators**
- **Predictive modeling** for mortality and vaccination evolution
- **Model evaluation and comparison** using quantitative metrics
- **Interpretation of results** in the context of pandemic dynamics

---

## Data Procurement
The data used in this project was obtained using:
- **Google Cloud Platform (GCP)**
- **Google BigQuery Public Datasets** (COVID-19 Open Data)
- **BigQuery API** for structured querying and data retrieval
- **JSON authentication file / Google Colab authentication**
- **Google Colab integration** for executing queries and managing data processing

---

## Data Structure
The dataset contains temporal, geographical, epidemiological, and vaccination-related information, including:
- `date` – daily observation date
- `country_code` – country identifier
- `location_key` – geographic location identifier
- `new_confirmed` – daily new confirmed COVID-19 cases
- `new_deceased` – daily new COVID-19 related deaths
- `new_vaccine_doses_administered_pfizer`
- `new_vaccine_doses_administered_moderna`
- `new_vaccine_doses_administered_janssen`
- cumulative vaccination indicators
- derived variables such as total administered vaccine doses

---

## Key Features
The project workflow includes the following stages:
- **Data extraction and preprocessing**
  - Missing value handling
  - Type conversion
  - Removal of duplicates and invalid values
  - Temporal and geographic feature extraction
- **Exploratory Data Analysis (EDA)**
  - Analysis of confirmed cases and deaths
  - Regional and temporal comparisons
  - Vaccination trends by manufacturer
- **Derived indicators**
  - Mortality rate
  - Growth rate of confirmed cases
  - Moving averages
- **Predictive modeling**
  - Mortality prediction
  - Vaccination evolution prediction
- **Model evaluation**
  - Quantitative performance assessment

---

## Algorithms Used
The following regression models were used in this project:
- **Linear Regression**
- **Gradient Boosted Trees Regressor**
- **Random Forest Regressor**

Different feature configurations were tested, especially for vaccination prediction, in order to analyze the impact of feature selection on predictive performance.

---

## Implementation Steps
The main implementation steps are:
1. **Environment setup**
   - Google Colab configuration
   - Google Cloud Platform authentication
2. **Data extraction and cleaning**
   - Querying BigQuery datasets
   - Data transformation and aggregation
3. **Exploratory Data Analysis**
   - Statistical summaries
   - Visual trend analysis
4. **Model training and evaluation**
   - Train-test split
   - Model fitting and prediction
5. **Result interpretation**
   - Comparison between models
   - Analysis of performance metrics

---

## Model Performance Metrics
Model performance was evaluated using:
- **R² (Coefficient of Determination)**
  - Measures the proportion of variance explained by the model
- **RMSE (Root Mean Square Error)**
  - Measures the magnitude of prediction errors

These metrics were computed on a test dataset to assess model generalization and stability.

---

## Technologies and Frameworks Used
- **Google Cloud Platform (GCP)**
- **Google BigQuery**
- **Google Colab**
- **PySpark (Spark SQL, MLlib)**
- **Pandas**
- **Matplotlib**
- **Seaborn**

---

## Conclusion
This project demonstrates how Big Data technologies and regression-based machine learning models can be used to analyze and predict COVID-19 epidemiological indicators. The results show that non-linear models are better suited for capturing complex mortality patterns, while vaccination trends exhibit more regular and predictable behavior that is strongly influenced by feature selection.

The study highlights the importance of careful data preprocessing, appropriate model selection, and critical interpretation of evaluation metrics when working with real-world public health data.
