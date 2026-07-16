# SpaceX Falcon 9 First Stage Landing Prediction

This repository contains the final presentation and project assets for the IBM Applied Data Science Capstone. The project analyzes SpaceX Falcon 9 launch data to identify factors associated with successful first-stage landings and to build a classification model that predicts landing outcomes.

## Project objective

The business goal of the project is to estimate whether the Falcon 9 first stage will land successfully, because booster recovery is closely tied to launch cost and SpaceX's reusable launch advantage.

## Repository contents

The repository is organized in the same sequence used in the capstone workflow:

1. `01_SpaceX-Data-collection-api.ipynb` - collects and structures launch data from the SpaceX API.
2. `02_SpaceX-Webscraping.ipynb` - extracts complementary launch information from the web.
3. `03_SpaceX-Data-wrangling.ipynb` - cleans the data and creates the binary landing outcome target variable.
4. `04_EDA_SQL_sqllite.ipynb` - explores the dataset with SQL queries and business-oriented analysis.
5. `05_EDA_Data_Visualization.ipynb` - performs exploratory visual analysis of launch site, orbit, payload, and success relationships.
6. `06_SpaceX_VisualAnalytics_Folium.ipynb` - builds geospatial analysis using Folium maps.
7. `07_SpaceX_Visual_Analytics_Plotly_Dash.py` - creates an interactive Plotly Dash dashboard for visual analytics.
8. `08_SpaceX_PredictiveAnalytics.ipynb` - trains and evaluates classification models for landing prediction.
9. `SPACEX-IBM-Capstone-Project-Report.pdf` - final presentation deck summarizing the project story and findings.

## Workflow summary

### 1. Data collection

Launch records were collected from the SpaceX API and supplemented with launch-history details from web scraping to create a richer analytical dataset.

### 2. Data wrangling

The landing outcome column was transformed into a binary `Class` label, where 1 represents a successful landing and 0 represents an unsuccessful landing.

### 3. Exploratory analysis

The project used both SQL and Python visualizations to study how landing success varies by launch site, orbit, payload mass, booster version, and time.

### 4. Interactive analytics

Folium maps were used to examine launch-site geography and proximity to coastal and transport-related features, while Plotly Dash was used to create interactive dashboard views for landing outcomes and payload analysis.

### 5. Predictive modeling

Multiple classification models were trained and compared, including Logistic Regression, SVM, KNN, and Decision Tree, to predict whether the Falcon 9 first stage would land successfully.

## Key findings

- Landing success improved over time, suggesting that recovery performance increased as the Falcon 9 program matured.
- Launch-site location matters, and major launch sites are positioned near the coast to reduce public safety risk in the event of launch failure.
- Payload mass and orbit type are important explanatory variables in landing outcomes.
- All four evaluated classifiers achieved a test accuracy of about 83.3 percent in the notebook outputs.
- The confusion matrix shows that the model correctly classified 15 of 18 test launches, including all 12 actual successful landings, while incorrectly labeling 3 failed launches as successful.

## Model performance

| Model | Test Accuracy |
|------|---------------|
| Logistic Regression | 83.33% |
| SVM | 83.33% |
| Decision Tree | 83.33% |
| KNN | 83.33% |

Although all models achieved the same test accuracy, the Decision Tree model achieved the strongest cross-validation score during tuning in the notebook workflow.

## Presentation summary

The final presentation explains the project in a business-friendly sequence:

- Business problem and motivation
- Data collection and preparation
- SQL and visual exploratory analysis
- Folium and Dash interactive analytics
- Predictive modeling and evaluation
- Conclusions and business implications

## Business takeaway

Predicting first-stage landing success helps explain SpaceX's cost advantage and demonstrates how data science can support operational decision-making in reusable launch systems.

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
