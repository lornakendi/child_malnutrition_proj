Child Malnutrition in Kenya: Data Analysis Project
📊 Project Overview
This Jupyter Notebook contains the complete data analysis for the research project "Drivers of Nutritional Transition in Kenyan Children: Examining the Relative Contribution of Women's Education, Economic Development, and Sanitation Infrastructure to Reductions in Childhood Stunting (1993–2022)".

The analysis examines trends and determinants of child malnutrition in Kenya using seven rounds of Demographic and Health Survey (DHS) data spanning three decades (1993–2022).

📁 Datasets Used
The following CSV files (provided in the project folder) are required:

File Name	Description
select-nutrition-indicators_national_ken.csv - Child malnutrition indicators (stunting, wasting, overweight)
select-education-indicators_national_ken.csv -	Women's education and literacy data
water_national_ken.csv - Improved water source access
toilet-facilities_national_ken.csv - Improved sanitation access
covid-19-additional-factors_national_ken.csv - Household assets (electricity, television, refrigerator)

🎯 Research Objectives
1. Analyze trends in stunting, wasting, and overweight among Kenyan children (1993–2022)

2. Assess changes in women's education, household electrification, television ownership, water access, and sanitation access

3. Determine correlations between stunting and each predictor variable

4. Compare the relative predictive power of different factors using regression analysis

5. Identify key drivers of stunting reduction for policy recommendations

🔧 Requirements
Python Environment
This notebook requires Python 3.x with the following libraries:

- text
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- statsmodels

Installation Instructions (Windows)
Open Command Prompt or PowerShell and run:

bash
# Create a virtual environment (optional but recommended)
python -m venv malnutrition_env
malnutrition_env\Scripts\activate

# Install required packages
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
Or install all at once using a requirements file:

bash
pip install -r requirements.txt
Create a requirements.txt file with:

text
pandas==1.5.3
numpy==1.24.3
matplotlib==3.7.1
seaborn==0.12.2
scikit-learn==1.2.2
statsmodels==0.13.5

📓 Notebook Structure
The notebook is organized into the following sections:

1. Setup and Data Loading
Import libraries

Load all CSV files

Clean column names (remove special characters, handle header rows)

2. Data Cleaning and Preparation
Extract relevant indicators

Create clean dataframes for each indicator type

Merge all data into a single dataset

3. Trend Analysis
Plot trends in stunting, wasting, and overweight over time

Plot trends in predictor variables (education, electricity, sanitation, etc.)

Calculate absolute changes between first and last survey years

4. Correlation Analysis
Calculate Pearson correlations between stunting and each predictor

Generate correlation matrix

5. Regression Analysis
Perform simple linear regression for each significant predictor

Extract coefficients, R² values, p-values

Compare predictive power across factors

6. Visualization
Create combined plots (stunting vs education, electricity, sanitation)

Generate publication-ready figures

7. Results Summary
Compile key findings in tables

Export final dataset for reporting

🚀 How to Run
Ensure all CSV files are in the same folder as the Jupyter notebook

Open the notebook in VS Code or Jupyter:

bash
jupyter notebook malnutrition_analysis.ipynb
Run all cells (Kernel → Restart & Run All) or execute step by step

📊 Expected Outputs
Running the notebook will generate:

Printed tables showing malnutrition rates by year

Printed tables showing predictor variables by year

Correlation coefficients between stunting and each predictor

Regression results with coefficients, R², and p-values

Line graphs showing trends over time

Combined plots (dual-axis) comparing stunting with key predictors

A final merged dataset saved as kenya_nutrition_analysis_final.csv

📈 Key Findings Summary
Finding	Result
Stunting reduction (1993–2022)	39.9% → 17.6% (-22.3 points)
Women's secondary education increase	24.5% → 58.2% (+33.7 points)
Electricity access increase	8.8% → 51.1% (+42.3 points)
Strongest correlation with stunting	Women's secondary education (r = -0.988)
Best predictor (R²)	Women's secondary education (0.965)
Non-significant predictor	Improved sanitation (p = 0.157)

📝 Notes and Limitations
- Literacy data available only from 2003 onward

- Analysis based on national aggregates; sub-national variation not examined

- Small number of time points (n=6) limits multivariate analysis

- Associations should not be interpreted as causal

📁 Output Files
The notebook creates:

kenya_nutrition_analysis_final.csv – Merged dataset with all indicators by year

👩‍💻 Author
Lorna Kendi
lornahkendy@gmail.com
19/02/2026

📚 References
See the accompanying research proposal for full reference list.

📄 License
This project is for academic purposes. Data source: Demographic and Health Surveys (DHS) Program.