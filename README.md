# chicago-building-permits-analysis
"Building permits analysis for Chicago from 2006 to present using machine learning techniques."

# Overview
This project aims to analyze building permits data issued in Chicago from 2006 to the present. The goal is to explore patterns, trends, and insights regarding permits, including types, costs, fees, and work being done. Machine learning models were implemented to predict the permit status based on features in the dataset, including Gradient Boosting, Random Forest Classifier, and K-Nearest Neighbors (KNN).

# Dataset
Link: https://data.cityofchicago.org/Buildings/Building-Permits-Dashboard/2s3k-mec8

This dataset includes information about currently-valid building permits issued by the City of Chicago from 2006 to the present. Building permits are issued subject to payment of applicable fees. If building or zoning permit fees show as unpaid, the permit is not valid. (A permit is valid if only “other fees” are shown as unpaid.) This dataset does not include permits which have been issued and voided or revoked. This dataset also does not include permits for mechanical amusement riding devices and carnivals issued by the Department of Buildings. 

Permit Tracking Numbers: Unique identifiers for each permit.
Permit Types: Classifications such as new construction, renovations, etc.
Application Start Dates & Issue Dates: For analyzing permit processing times.
Fees and Costs of Work: Monetary information associated with permits.
Geographic Information: Including building addresses and geographic coordinates.
Data Exclusions
Voided or revoked permits were excluded.
Mechanical amusement ride permits and carnival permits were not included in the dataset.
Project Workflow

# 1. Data Cleaning
Removed invalid or null entries.
Handled missing values.
Converted categorical features into numerical format for modeling.
Scaled numeric values for use in machine learning algorithms.

# 2. Exploratory Data Analysis (EDA)
Performed descriptive analysis of key fields such as permit types, application dates, and costs.
Visualized the distribution of permits across different types and neighborhoods in Chicago.
Explored the relationship between cost and permit type, as well as processing time and issue date.

# 3. Principal Component Analysis (PCA)
PCA was applied to reduce the dimensionality of the dataset while maintaining as much variance as possible.
The first 5 principal components explained over 99% of the variance in the data.
PCA allowed for efficient training of machine learning models without loss of important information.

# 4. Modeling
Three machine learning models were built to predict the permit status (whether a permit was completed or still under review):

## Gradient Boosting:
Accuracy: 96.0%
Balanced Accuracy: 71.2%
F-1 Score: 73.0%
Recall: 71.2%
Precision: 75.5%
Specificity: 71.2%
Random Forest Classifier:

## Accuracy: 96.9%
Balanced Accuracy: 77.2%
F-1 Score: 80.2%
Recall: 77.2%
Precision: 86.7%
Specificity: 77.2%

## K-Nearest Neighbors (KNN):
Accuracy: 60.1%
Balanced Accuracy: 48.6%
F-1 Score: 47.3%
Recall: 48.6%
Precision: 46.7%
Specificity: 48.6%

# 5. Model Evaluation
Models were evaluated using metrics such as Accuracy, F-1 Score, Recall, Precision, and Specificity.
Random Forest was determined to be the best-performing model, with an accuracy of 96.9%, precision of 86.7%, and recall of 77.2%.
Results
Feature Importance: Random Forest highlighted the most important features for predicting permit status, including the cost of work and geographic location.
Performance: Random Forest outperformed Gradient Boosting and K-Nearest Neighbors on almost all metrics.
Business Insight: The analysis helped identify which areas and types of permits are most likely to have a smooth and timely approval process, and which ones face delays or denials.
Key Findings
High Success Rate: Most permits are approved or completed successfully with minimal delays.
Neighborhood Influence: Geographic location and project type were found to be significant factors influencing permit approval times.
Cost Analysis: Higher project costs were often associated with longer approval processes but not necessarily higher fees.
Files in the Repository
Final_DSC345FinalProject_Eddie.ipynb: Jupyter notebook containing the full analysis, from data preprocessing to model evaluation.
chicago_building_permits.csv: Dataset used in the analysis (optional; you may provide a link to where the dataset can be downloaded if it's too large to include).
requirements.txt: List of Python packages and dependencies used in the project.
