# DataAnalysis_Python
King County House Sales Analysis
Overview
This project analyzes house sales in King County, Washington, including the Seattle area. The goal is to explore the housing dataset, clean and prepare the data, identify relationships between housing features and sale price, and build regression models to estimate house prices.
The analysis uses Python-based data science tools including pandas, NumPy, seaborn, matplotlib, and scikit-learn.
Dataset
The dataset contains house sale records from King County, Washington for homes sold between May 2014 and May 2015.
The dataset includes features such as:
Sale price
Number of bedrooms
Number of bathrooms
Square footage of living space
Lot size
Number of floors
Waterfront status
View rating
House condition
Grade
Year built
Year renovated
Latitude and longitude
Zip code
The target variable for prediction is `price`.
Project Objectives
The main objectives of this project are to:
Import and inspect the housing dataset
Clean and prepare the data for analysis
Handle missing values
Explore relationships between house features and price
Visualize important trends and patterns
Build regression models to predict house prices
Compare model performance using R² scores
Tools and Libraries
This project uses:
Python
pandas
NumPy
matplotlib
seaborn
scikit-learn
Jupyter Notebook
Project Workflow
1. Importing and Inspecting the Data
The dataset is loaded into a pandas DataFrame and inspected using methods such as:
`head()`
`dtypes`
`describe()`
This step helps understand the structure of the data, data types, and summary statistics.
2. Data Wrangling
Unnecessary identifier columns such as `id` and `Unnamed: 0` are removed because they do not contribute meaningful predictive value.
Missing values are found in the following columns:
`bedrooms`
`bathrooms`
The missing values are replaced with the mean value of each respective column.
3. Exploratory Data Analysis
Exploratory analysis is performed to better understand the dataset and identify important relationships.
Key analysis steps include:
Counting houses by number of floors
Comparing prices for waterfront and non-waterfront homes using boxplots
Analyzing the relationship between above-ground square footage and price
Calculating feature correlations with house price
Some of the features most strongly correlated with price include:
`sqft_living`
`grade`
`sqft_above`
`sqft_living15`
`bathrooms`
Model Development
Several regression models are built and evaluated.
Simple Linear Regression
A simple linear regression model is trained using `sqft_living` to predict house price.
R² score: approximately `0.493`
Multiple Linear Regression
A multiple linear regression model is trained using selected housing features:
```python
features = [
    "floors",
    "waterfront",
    "lat",
    "bedrooms",
    "sqft_basement",
    "view",
    "bathrooms",
    "sqft_living15",
    "sqft_above",
    "grade",
    "sqft_living"
]
```
R² score: approximately `0.658`
Ridge Regression
A Ridge regression model is trained using the selected feature set and evaluated on a test set.
R² score: approximately `0.648`
Polynomial Ridge Regression
Polynomial features are generated using a second-degree polynomial transformation, then a Ridge regression model is trained.
R² score: approximately `0.700`
This was the best-performing model in the notebook.
Results Summary
Model	R² Score
Linear Regression using longitude	0.000
Simple Linear Regression using `sqft_living`	0.493
Multiple Linear Regression	0.658
Ridge Regression	0.648
Polynomial Ridge Regression	0.700
Key Findings
`sqft_living` has the strongest correlation with house price among the numeric features analyzed.
House grade, above-ground square footage, bathrooms, and nearby living space size are also strong predictors.
Waterfront homes show clear price differences and outliers compared with non-waterfront homes.
A polynomial Ridge regression model performed better than the simpler linear regression models.
Using multiple features significantly improved prediction performance compared with using a single feature.
How to Run the Project
Clone this repository:
```bash
git clone https://github.com/your-username/king-county-house-sales-analysis.git
```
Navigate into the project folder:
```bash
cd king-county-house-sales-analysis
```
Install the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn requests
```
Open the Jupyter Notebook:
```bash
jupyter notebook king_county_house_sales_analysis.ipynb
```
Run the notebook cells from top to bottom.
Repository Structure
```text
king-county-house-sales-analysis/
│
├── king_county_house_sales_analysis.ipynb
├── README.md

```
Note: The notebook downloads the dataset automatically from the provided source URL. If the dataset is not included in the repository, running the notebook will create `housing.csv`.
Skills Demonstrated
This project demonstrates:
Data loading and inspection
Data cleaning
Handling missing values
Exploratory data analysis
Data visualization
Correlation analysis
Feature selection
Linear regression modeling
Ridge regression
Polynomial feature transformation
Model evaluation using R² score
Future Improvements
Possible improvements include:
Add train/test evaluation for all regression models
Use cross-validation for more reliable performance comparison
Add residual analysis
Try additional models such as Random Forest or Gradient Boosting
Tune hyperparameters using GridSearchCV
Improve feature engineering with location-based and age-based features
Save final model predictions and evaluation charts
Author
Created by Saeeda as part of a data analysis and machine learning portfolio project.
