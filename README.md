# SpaceX Falcon 9 First Stage Landing Prediction

This repository contains the final presentation and project assets for the IBM Applied Data Science Capstone. The project analyzes SpaceX Falcon 9 launch data to identify factors associated with successful first-stage landings and to build a classification model that predicts landing outcomes.[file:521][file:525][file:528]

## Project objective

The business goal of the project is to estimate whether the Falcon 9 first stage will land successfully, because booster recovery is closely tied to launch cost and SpaceX's reusable launch advantage.[file:521][file:524]

## Repository contents

The repository is organized in the same sequence used in the capstone workflow:

1. `01_SpaceX-Data-collection-api.ipynb` — collects and structures launch data from the SpaceX API.[file:521]
2. `02_SpaceX-Webscraping.ipynb` — extracts complementary launch information from the web.[file:522]
3. `03_SpaceX-Data-wrangling.ipynb` — cleans the data and creates the binary landing outcome target variable.[file:525]
4. `04_EDA_SQL_sqllite.ipynb` — explores the dataset with SQL queries and business-oriented analysis.[file:524]
5. `05_EDA_Data_Visualization.ipynb` — performs exploratory visual analysis of launch site, orbit, payload, and success relationships.[file:526]
6. `06_SpaceX_VisualAnalytics_Folium.ipynb` — builds geospatial analysis using Folium maps.[file:523]
7. `07_SpaceX_Visual_Analytics_Plotly_Dash.py` — creates an interactive Plotly Dash dashboard for visual analytics.[file:527]
8. `08_SpaceX_PredictiveAnalytics.ipynb` — trains and evaluates classification models for landing prediction.[file:528]
9. `Data-Science-Capstone-Project-Report.pptx` — final presentation deck summarizing the project story and findings.[file:529]

## Workflow summary

### 1. Data collection

Launch records were collected from the SpaceX API and supplemented with launch-history details from web scraping to create a richer analytical dataset.[file:521][file:522]

### 2. Data wrangling

The landing outcome column was transformed into a binary `Class` label, where 1 represents a successful landing and 0 represents an unsuccessful landing.[file:525]

### 3. Exploratory analysis

The project used both SQL and Python visualizations to study how landing success varies by launch site, orbit, payload mass, booster version, and time.[file:524][file:526]

### 4. Interactive analytics

Folium maps were used to examine launch-site geography and proximity to coastal and transport-related features, while Plotly Dash was used to create interactive dashboard views for landing outcomes and payload analysis.[file:523][file:527]

### 5. Predictive modeling

Multiple classification models were trained and compared, including Logistic Regression, SVM, KNN, and Decision Tree, to predict whether the Falcon 9 first stage would land successfully.[file:528]

## Key findings

- Landing success improved over time, suggesting that recovery performance increased as the Falcon 9 program matured.[file:526]
- Launch-site location matters, and major launch sites are positioned near the coast to reduce public safety risk in the event of launch failure.[file:523]
- Payload mass and orbit type are important explanatory variables in landing outcomes.[file:526]
- All four evaluated classifiers achieved a test accuracy of about 83.3 percent in the notebook outputs.[file:528]
- The confusion matrix shows that the model correctly classified 15 of 18 test launches, including all 12 actual successful landings, while incorrectly labeling 3 failed launches as successful.[file:528]

## Model performance

| Model | Test Accuracy |
|------|---------------|
| Logistic Regression | 83.33% [file:528] |
| SVM | 83.33% [file:528] |
| Decision Tree | 83.33% [file:528] |
| KNN | 83.33% [file:528] |

Although all models achieved the same test accuracy, the Decision Tree model achieved the strongest cross-validation score during tuning in the notebook workflow.[file:528]

## Presentation summary

The final presentation explains the project in a business-friendly sequence:

- Business problem and motivation
- Data collection and preparation
- SQL and visual exploratory analysis
- Folium and Dash interactive analytics
- Predictive modeling and evaluation
- Conclusions and business implications

## Business takeaway

Predicting first-stage landing success helps explain SpaceX's cost advantage and demonstrates how data science can support operational decision-making in reusable launch systems.[file:521][file:528]

## Tools and technologies

- Python
- Pandas
- BeautifulSoup
- SQLite / SQL
- Plotly
- Dash
- Folium
- Scikit-learn
- Jupyter Notebook

## How to use this repository

1. Review the notebooks in numerical order.
2. Run the data preparation and EDA notebooks first.
3. Explore the Folium and Dash visual analytics components.
4. Review the predictive modeling notebook for feature engineering, model tuning, and evaluation.
5. Open the presentation file for a concise project summary.

## Author

Prepared as part of the IBM Applied Data Science Capstone project.
