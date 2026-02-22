# Industrial Human Resource Geo-Visualization

## Project Overview
This project analyzes the industrial classification of the workforce 
in India. It visualizes the distribution of main and marginal workers 
across various industries, states, and genders using an interactive 
Streamlit dashboard.

## Domain
Resource Management

## Technologies Used
- Python
- Pandas
- Scikit-learn
- Plotly
- Streamlit
- Google Colab

## Dataset
- 23 CSV files merged into a single dataset
- Total Records: 195,145
- Total Columns: 25
- No missing values found

## Project Structure
```
├── CCT.ipynb                        # Main project notebook
├── app.py                           # Streamlit dashboard
├── merged_dataset.csv               # Merged dataset
├── cleaned_dataset.csv              # Cleaned dataset
├── feature_engineered_dataset.csv   # Feature engineered dataset
└── README.md                        # Project documentation
```

## Workflow

### Step 1 - Data Merging
- Unzipped and merged 23 CSV files into a single dataframe
- Final shape: 195,145 rows and 25 columns

### Step 2 - Data Exploration
- Analyzed shape, data types, missing values
- Performed statistical summary and data quality checks
- No missing values, duplicates, or negative values found

### Step 3 - Data Cleaning
- Removed backtick prefix from code columns
- Standardized all column names to snake_case
- Created industry_text column for NLP

### Step 4 - Feature Engineering
- Created 7 new features:
  - total_workers
  - total_male_workers
  - total_female_workers
  - total_rural_workers
  - total_urban_workers
  - dominant_worker_type
  - industry_word_count

### Step 5 - NLP and Model Building
- Used rule-based NLP to group industries into categories:
  - Retail, Agriculture, Manufacturing, Construction, Poultry
- Built TF-IDF + Logistic Regression model
- Achieved 100% accuracy on test data

### Step 6 - Streamlit Dashboard
- Built interactive dashboard with 5 Plotly charts:
  - Total Workers by Business Category
  - Top 10 States by Worker Population
  - Rural vs Urban Worker Distribution
  - Gender-wise Worker Distribution
  - Female Workforce by Industry
- Key Facts and Figures section

## How to Run

### Install dependencies
```
pip install streamlit plotly pandas scikit-learn
```

### Run the dashboard
```
streamlit run app.py
```

## Key Insights
- Manufacturing is the dominant industry category
- West Bengal has the highest worker population
- Urban workers slightly outnumber rural workers
- Male workers significantly outnumber female workers
- Total workforce across all Indian states is over 181 million

## Coding Standards
- Modular code written in functional blocks
- Follows PEP 8 coding standards
- All functions have proper docstrings
- Portable and maintainable code structure

