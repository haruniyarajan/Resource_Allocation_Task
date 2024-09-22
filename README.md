# Technical Assessment: Analyst, Data Science – 167

## Overview
This notebook is part of a technical assessment for resource allocation in the insurance domain. The goal is to analyze firm-level data and provide insights to help a supervisory manager allocate scarce resources by identifying firms that require more attention.

### Key Metrics for Analysis
The analysis focuses on the following firm characteristics:
1. **Firm Size**: Larger firms generally have a bigger impact on the market and may carry more risk. Metrics like Gross Written Premium (GWP) and Net Written Premium (NWP) are used to assess size.
2. **Changing Business Profile**: Significant year-on-year changes in financial data, such as GWP or claims, may indicate instability or growth, requiring closer monitoring.
3. **Outliers**: Firms with unusual data points in a single reporting period might indicate potential issues, such as reporting errors or unique business conditions.

### Data Sources
- **Dataset 1 - General**: Contains financial metrics for firms, including GWP, NWP, total assets, and SCR (Solvency Capital Requirement). This dataset spans multiple years, allowing for year-on-year comparisons.
- **Dataset 2 - Underwriting**: Contains information about each firm's underwriting performance, including:
  - Gross BEL (Best Estimate Liabilities)
  - Gross Expense Ratio
  - Gross Combined Ratio

## How to Run the Notebook

### Step 1: Upload the Datasets

If you are running this in Google Colab or any other cloud platform:
1. Upload the datasets manually using the upload functionality.
2. Update the data loading step in the notebook as follows:

```python
# Uncomment if running in Google Colab or other platforms:
from google.colab import files
uploaded = files.upload()

# Then, replace the file paths with the uploaded file names
df_general = pd.read_excel("your_uploaded_file_name.xlsx", sheet_name='Dataset 1 - General')
df_underwriting = pd.read_excel("your_uploaded_file_name.xlsx", sheet_name='Dataset 2 - Underwriting')
```
### Step 2: Install Necessary Libraries

Make sure you have all the necessary Python libraries installed:
```sh
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

### Step 3: Run the Notebook

After uploading the datasets and installing the dependencies, run the cells in the notebook sequentially to complete the analysis.
### Step 4: Modify the Data Loading Path (if needed)

```python
If you are running this notebook in a local Jupyter environment, make sure the paths to the datasets are correct in the following step:
# Load 'Dataset 1 - General'
df_general = pd.read_excel("/path/to/your/Data for technical assessment.xlsx", sheet_name='Dataset 1 - General')

# Load 'Dataset 2 - Underwriting'
df_underwriting = pd.read_excel("/path/to/your/Data for technical assessment.xlsx", sheet_name='Dataset 2 - Underwriting')
```

###Conclusion

The notebook provides a detailed analysis of firm-level data to assist in resource allocation. The insights are derived from clustering, time series forecasting,
and outlier detection, focusing on identifying high-risk firms and significant changes in business profiles.
