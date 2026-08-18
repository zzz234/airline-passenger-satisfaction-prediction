# airline-passenger-satisfaction-prediction
Predicting airline passenger satisfaction using machine learning classification models in Python.
# ✈️ Airline Passenger Satisfaction Prediction

A machine learning classification project that predicts airline passenger satisfaction using passenger characteristics, travel information, and service-related features.

##Overview

Customer satisfaction is an important indicator of service quality in the airline industry. This project explores whether passenger satisfaction can be predicted using demographic, travel, flight, and service-related attributes.

Multiple machine learning classification algorithms were developed and evaluated to compare their predictive performance and identify a suitable model for distinguishing between **satisfied** and **neutral or dissatisfied** passengers.

##Objective

The objective of this project is to build a classification model that predicts passenger satisfaction based on available passenger and flight-related features.

The target variable contains two classes:

* **Satisfied**
* **Neutral or Dissatisfied**

##Dataset

The dataset contains passenger and flight-related information, including:

* Passenger demographics
* Customer and travel type
* Travel class
* Flight distance
* Departure and arrival delays
* Online booking and boarding experience
* Inflight Wi-Fi service
* Seat comfort
* Inflight entertainment
* Leg room service
* Other airline service ratings

The dataset was divided into training and testing sets using a **70/30 stratified split** to preserve the distribution of the target classes.

> The original dataset is not included in this repository.

##Data Preprocessing

Several preprocessing steps were performed before model training:

* Removed the identifier column
* Investigated missing values
* Applied mean imputation to missing arrival-delay observations
* Checked for duplicate observations
* Encoded categorical variables for machine learning
* Applied feature scaling to numerical variables
* Investigated potential outliers
* Separated predictor variables from the target variable
* Created stratified training and testing datasets

##Machine Learning Models

Multiple classification algorithms were explored and compared:

* Decision Tree
* k-Nearest Neighbours (kNN)
* Multilayer Perceptron (MLP)
* Support Vector Machine (NuSVM)
* AdaBoost
* Random Forest

The models were evaluated to compare their ability to correctly classify passenger satisfaction.

##Model Evaluation

Model performance was assessed using several classification metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC-AUC

Using multiple evaluation metrics provides a more comprehensive understanding of model performance than relying on accuracy alone.

##Results

The models achieved different levels of predictive performance on the test dataset.

| Model                                    | Approx. Test Accuracy |
| ---------------------------------------- | --------------------: |
| Decision Tree                            |                  ~93% |
| k-Nearest Neighbours                     |                  ~91% |
| Multilayer Perceptron                    |                  ~94% |
| NuSVM                                    |                  ~86% |
| AdaBoost                                 |                ~90.5% |
| Random Forest                            |                ~94.8% |
| **Random Forest with Feature Selection** |            **~95.0%** |

**Random Forest** achieved the strongest overall classification performance and was selected for further analysis.

Feature importance was subsequently used to identify influential predictors and refine the feature set. The resulting Random Forest model achieved approximately **95% test accuracy**.

##Key Insights

Random Forest feature importance indicated that several service-related factors were particularly influential in predicting passenger satisfaction.

Important features included:

* Online boarding
* Inflight Wi-Fi service
* Travel class
* Inflight entertainment
* Seat comfort
* Leg room service
* Ease of online booking

These results suggest that both the digital travel experience and onboard service quality are important indicators of overall passenger satisfaction.

##Technologies

* **Python**
* **Pandas** — data manipulation and preprocessing
* **NumPy** — numerical operations
* **Scikit-learn** — machine learning and model evaluation
* **Matplotlib** — data visualisation
* **Seaborn** — statistical visualisation
* **Jupyter Notebook / Google Colab** — development environment

##Repository Structure

```text
airline-passenger-satisfaction-prediction/
│
├── README.md
├── airline_satisfaction_prediction.ipynb
└── .gitignore
```

The Jupyter Notebook contains the complete workflow, including data preprocessing, exploratory analysis, model development, model comparison, evaluation, feature importance analysis, and final prediction.

##Skills Demonstrated

This project demonstrates practical experience in:

* Data cleaning and preprocessing
* Exploratory data analysis
* Feature encoding and transformation
* Supervised machine learning
* Classification model development
* Model comparison and evaluation
* Feature importance analysis
* Feature selection
* Data visualisation
* Python-based data analytics

##Future Improvements

Potential improvements to the project include:

* More systematic hyperparameter optimisation
* Cross-validation for more robust model comparison
* Further review and refinement of categorical feature encoding
* Additional feature engineering
* Model explainability using techniques such as SHAP
* Deployment of the selected model through an interactive web application
