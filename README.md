# 🏠 Housing Price Analysis: Crime Rate Impact Study

This project analyzes the relationship between **crime rates** and **median home values** using linear regression. The analysis quantifies exactly how much housing prices change with incremental changes in neighborhood crime rates.

![Housing Price Analysis](https://sandbox.zenodo.org/records/200488/files/house_crime.jpg?download=1)

## 🔍 Key Question Addressed

**For every 0.01 increase in the crime rate, how much does the median house price change?**

## 📋 Table of Contents

- [Project Structure](#project-structure)
- [Installation](#installation)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Analysis Steps](#analysis-steps)
- [Conclusion](#conclusion)

## 📁 Project Structure

```
crime_rate_impact_on_home_values/
├── data/
│   └── houseprice.csv           # Raw housing price and crime rate data
├── notebooks/
│   └── crime_vs_housing.ipynb   # Main analysis notebook
├── images/
│   ├── scatter_plot.png         # Crime rate vs. housing price scatter plot
│   ├── zoomed_scatter.png       # Zoomed in version focusing on main data cluster
│   └── regression_line.png      # Linear regression with fitted line
├── README.md                    # This file
└── requirements.txt             # Required Python packages
```

## 🛠️ Installation

Clone this repository and install the required packages:

```bash
git clone https://github.com/gaursuniverse/crime_rate_impact_on_home_values.git
cd crime_rate_impact_on_home_values
pip install -r requirements.txt
```

## 📊 Dataset

![Houseprice Dataset](https://sandbox.zenodo.org/records/200480/files/houseprice.csv?download=1) contains two key variables:
- `crime rate`: Per capita crime rate by town
- `Median Home Value`: Median value of owner-occupied homes in $1000s

**Sample Data:**

| crime rate | Median Home Value |
|------------|-------------------|
| 0.00632    | 24.0              |
| 0.02731    | 21.6              |
| 0.02729    | 34.7              |
| ...        | ...               |

## 🧮 Methodology

The relationship between crime rate and housing prices was analyzed using:

1. **Exploratory Data Analysis (EDA)**
   - Statistical summaries
   - Distribution analysis
   - Outlier detection

2. **Correlation Analysis**
   - Pearson correlation coefficient
   - Scatter plot visualization

3. **Linear Regression**
   - Manual calculation using the formula: y = β₀ + β₁x
   - Verification using scikit-learn
   - R-squared evaluation

## 🔑 Key Findings

Our analysis revealed:

- **For every 0.01 increase in crime rate, median home value decreases by approximately $4.15**
- Crime rate explains about 15% of the variance in housing prices (R² ≈ 0.15)
- The complete regression equation is: Median Home Value = 24.0331 + (-0.4152 × Crime Rate)

## 📈 Visualizations

### Crime Rate vs. Median Home Value
![Scatter Plot](https://sandbox.zenodo.org/records/200484/files/scatter_plot.png?download=1)

### Zoomed Scatter Plot
![Zoomed Scatter Plot](https://sandbox.zenodo.org/records/200484/files/zoomed_scatter.png?download=1)

### Linear Regression Model Fit
![Regression Line](https://sandbox.zenodo.org/records/200484/files/regression_line.png?download=1)

## 📝 Analysis Steps

The analysis follows this step-by-step process:

1. **Data Preparation**
   - Import necessary libraries
   - Load and clean dataset
   - Check for missing values and anomalies

2. **Exploratory Analysis**
   - Generate descriptive statistics
   - Visualize distributions and relationships
   - Calculate correlation coefficients

3. **Manual Linear Regression Calculation**
   - Calculate means of both variables
   - Compute the slope (β₁) using: Σ[(x-x̄)(y-ȳ)] / Σ[(x-x̄)²]
   - Calculate the y-intercept (β₀) using: ȳ - β₁x̄
   - Formulate the regression equation

4. **Model Verification**
   - Compare manual calculations with scikit-learn results
   - Visualize the regression line
   - Calculate and interpret R-squared

5. **Impact Analysis**
   - Determine the effect of a 0.01 increase in crime rate
   - Calculate confidence intervals for the estimate
   - Interpret findings in practical terms

## 💡 Conclusion

This analysis confirms that crime rate has a statistically significant negative relationship with housing prices. Specifically, for every 0.01 unit increase in crime rate, median home values decrease by approximately $4.15. This finding has implications for urban planning, real estate investment, and community safety initiatives.

While crime rate is an important factor influencing housing prices, it explains only part of the variation, suggesting that other factors (not included in this analysis) also play significant roles in determining housing values.


---

*Created with ❤️ by @gaurs_universe*

*Last Updated: April 2025*