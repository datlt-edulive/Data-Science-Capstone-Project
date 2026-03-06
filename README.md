# SpaceX Falcon 9 First Stage Landing Prediction - Final Capstone

## Overview
This repository contains the Final Capstone project for the IBM Data Science Professional Certificate. The central goal of this project is to predict the success of the SpaceX Falcon 9 first-stage landing. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, largely because SpaceX can reuse the first stage. By accurately predicting whether the first stage will land successfully, we can estimate the cost of a launch, giving a competitive advantage to alternative companies bidding against SpaceX for flights. The project encompasses full lifecycle data science tasks, including data collection via API and web scraping, data wrangling, exploratory data analysis (EDA), interactive visual analytics, and machine learning classification modeling.

## Objectives
1. **Request to the SpaceX API and Data Wrangling**: Collect launch data using the SpaceX REST API and process the information to handle missing values, format the structure, and create a comprehensive initial dataset.
2. **Web Scraping Falcon 9 Launch Records**: Extract historical Falcon 9 launch records structured in HTML tables from Wikipedia using BeautifulSoup, and transform them into a usable Pandas DataFrame.
3. **Exploratory Data Analysis (EDA) and Training Labels**: Compute basic statistical metrics, determine the landing outcome for each launch, and prepare discrete class labels (1 for a successful landing, 0 for failure) to be used by machine learning models.
4. **Database Integration**: Load the structured datasets into a local SQLite database (`my_data1.db`) and write SQL queries to explore the data, answering specific business and operational questions.
5. **Feature Engineering and Visualization**: Perform in-depth EDA using Pandas and Data Visualization libraries (Matplotlib, Seaborn) to identify correlations between various launch variables and landing success. Apply feature engineering to convert categorical attributes into dummy variables (One-Hot Encoding).
6. **Interactive Visual Analytics with Plotly Dash**: Build a dynamic web dashboard (`spacex_dash_app.py`) using Plotly Dash to interactively explore launch success rates using reactive pie charts and payload dependencies through scatter plots. Additionally, use Folium in Jupyter notebooks to visualize launch site geography and compute proximities to geographic landmarks like coastlines, railways, and highways.
7. **Machine Learning Models and Hyperparameter Tuning**: Standardize the prepared dataset and construct multiple classification models including Logistic Regression, Support Vector Machine (SVM), Decision Tree, and K-Nearest Neighbors (KNN). Optimize hyperparameters via `GridSearchCV` and evaluate the models based on classification accuracy to determine the best performing algorithm.

## Results
- Assembled and comprehensively cleaned a robust dataset of SpaceX Falcon 9 past launches.
- Uncovered that landing success rates have significantly improved over the years.
- Identified that certain launch sites (e.g., KSC LC-39A) possess higher success probabilities and observed distinct patterns relating payload mass and orbit types to landing success.
- Geospatial mapping revealed that all launch sites are strategically placed near coastlines and railways for logistical reasons, yet intentionally isolated from densely populated cities for safety.
- Developed and tuned multiple machine learning classifiers. The models achieved high predictive accuracy on the test data, providing a reliable tool for forecasting future first-stage rocket landings.

## Repository Structure
```text
.
├── 1.jupyter-labs-spacex-data-collection-api.ipynb   # Data collection via SpaceX API
├── 2.jupyter-labs-webscraping.ipynb                  # Data collection via Web Scraping
├── 3.labs-jupyter-spacex-Data wrangling.ipynb        # Data Wrangling and Label Mapping
├── 4.jupyter-labs-eda-sql-coursera_sqllite.ipynb     # EDA and Data Querying using SQL
├── 5. jupyter-labs-eda-dataviz.ipynb                 # EDA using Pandas, Matplotlib, and Seaborn
├── 6. lab_jupyter_launch_site_location.ipynb         # Geospatial Analysis using Folium maps
├── 7. SpaceX_Machine_Learning_Prediction_Part_5.jupyterlite.ipynb # ML Modeling & Evaluation
├── spacex_dash_app.py                                # Plotly Dash interactive reporting app
├── spacex_dash_app_screenshot.png                    # Dashboard application screenshot
├── spacex_launch_geo.csv                             # Geospatial dataset for launch sites
├── my_data1.db                                       # SQLite database containing project tables
└── README.md                                         # Project documentation (this file)
```

## Acknowledgments
- IBM: For providing the course and learning materials.
- Coursera: For the platform to access and complete the course.