# King County House Sales Analysis

## Project Overview

This project analyzes house sales data from King County, Washington. The goal is to explore the main factors that influence house prices and build regression models that can estimate housing prices based on property features.

The project includes data exploration, data cleaning, visualization, feature analysis, and machine learning model development using Python.

## Dataset

The dataset contains residential house sale records from King County, Washington.

Common fields analyzed in this project include:

- House price
- Number of bedrooms
- Number of bathrooms
- Square footage of living space
- Square footage of lot
- Number of floors
- Waterfront status
- View rating
- House condition
- House grade
- Basement size
- Year built
- Year renovated
- Location-related features such as latitude and longitude

The main target variable is:

```text
price
```

## Project Objectives

- Load and inspect the housing dataset
- Understand the structure and quality of the data
- Clean missing or unnecessary values
- Explore relationships between house features and sale price
- Create visualizations to identify trends and patterns
- Build regression models to predict house prices
- Evaluate model performance using R² score

## Tools and Libraries Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Analysis Workflow

### 1. Data Loading and Inspection

The dataset is loaded into a Pandas DataFrame and reviewed using basic exploration methods such as:

- Viewing the first few records
- Checking column data types
- Reviewing summary statistics
- Identifying missing values

### 2. Data Cleaning

The cleaning process includes:

- Removing unnecessary columns
- Checking for missing values
- Replacing missing numerical values where appropriate
- Preparing the dataset for analysis and modeling

### 3. Exploratory Data Analysis

Exploratory analysis is performed to better understand the housing data. This includes examining how different property features relate to sale price.

Examples of explored relationships include:

- Price compared with square footage
- Price compared with waterfront status
- Price compared with number of floors
- Price compared with house grade and condition

### 4. Data Visualization

The project uses visualizations to support the analysis and make patterns easier to understand.

Visualizations may include:

- Count plots
- Box plots
- Regression plots
- Correlation-based analysis

### 5. Model Development

Regression models are used to estimate house prices.

Models and techniques used include:

- Simple Linear Regression
- Multiple Linear Regression
- Polynomial Features
- Ridge Regression
- Machine learning pipelines

### 6. Model Evaluation

The models are evaluated using the R² score to measure how well the selected features explain changes in house prices.

## Key Skills Demonstrated

- Data cleaning and preparation
- Exploratory data analysis
- Data visualization
- Feature selection
- Regression modeling
- Model evaluation
- Machine learning workflow development
- Working with real-world housing data

## Project Structure

```text
king-county-house-sales-analysis/
│
├── README.md
├── king_county_house_sales_analysis.ipynb
└── data/
    └── housing.csv
```

## How to Run This Project

1. Clone or download this repository.

   ```bash
   git clone https://github.com/your-username/king-county-house-sales-analysis.git
   ```

2. Open the project folder.

   ```bash
   cd king-county-house-sales-analysis
   ```

3. Install the required libraries.

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

4. Open the notebook.

   ```bash
   jupyter notebook king_county_house_sales_analysis.ipynb
   ```

5. Run the notebook cells from top to bottom.

## Results Summary

The analysis shows that house prices are strongly influenced by features such as living area, grade, location, number of bathrooms, view quality, and waterfront status. Regression models were used to estimate prices and compare predictive performance.
![Project Preview](2.png)![Project Preview](1.png)![Project Preview](3.png)
## Possible Future Improvements

- Add more advanced machine learning models
- Tune hyperparameters for better prediction accuracy
- Add interactive visualizations
- Create a dashboard version of the analysis
- Deploy the model as a simple web application

## Author

**Saeeda Younus**

Data Analyst | Python | SQL | Excel | Power BI | Machine Learning
