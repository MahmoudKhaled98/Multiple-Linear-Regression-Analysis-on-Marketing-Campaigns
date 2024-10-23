# Multiple Linear Regression Analysis on Marketing Campaigns

## Project Overview
In this project, I will utilize multiple linear regression to explore the relationship between various promotional strategies and sales performance. The analysis will involve creating and fitting a model, checking model assumptions, analyzing performance, interpreting coefficients, and communicating the results to stakeholders. This project is particularly relevant for marketing teams seeking to understand the impact of different promotional activities on revenue generation.

The dataset includes information on various promotional strategies, such as discounts and advertising spending across multiple channels, alongside the corresponding sales figures. Insights from this analysis will guide company leaders in optimizing future marketing strategies and investments.

## Table of Contents
- [Introduction](#introduction)
- [Step 1: Imports](#step-1-imports)
- [Step 2: Data Exploration](#step-2-data-exploration)
- [Step 3: Model Building](#step-3-model-building)
- [Step 4: Results and Evaluation](#step-4-results-and-evaluation)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [References](#references)

## Introduction
In this project, I will explore the relationship between promotional strategies and sales through multiple linear regression analysis. Understanding this relationship is crucial for company leaders as they make informed decisions on where to allocate future marketing resources effectively.

## Step 1: Imports
### Import Packages
Importing the necessary libraries for data manipulation, visualization, and modeling.

### Load the Dataset
Loading the marketing dataset that contains information on various promotional spending and the corresponding sales.

## Step 2: Data Exploration
### Familiarizing with the Data's Features
Starting with exploratory data analysis (EDA) to understand and prepare the data for modeling. The features in the dataset include:

- Discount amount (in dollars)
- Advertising spending on TV (in dollars)
- Advertising spending on social media (in dollars)
- Sales (in dollars)

Each row represents a distinct promotional activity. The goal is to identify which features most strongly predict sales to inform future marketing investments.

### Reasons for Conducting EDA
- Understand which variables are present in the data.
- Analyze the distribution of features (min, mean, max values).
- Visualize relationships between the dependent and independent variables to identify the best predictors for sales.
- Identify any data quality issues, including missing values.

### Exploring the Data Size
Reviewing the overall structure and size of the dataset.

### Exploring the Independent Variables
Using descriptive statistics to examine the continuous independent variables: Discounts, TV advertising, and Social Media advertising.

### Exploring the Dependent Variable
Checking for missing values in the Sales column to ensure data quality.

### Removing Missing Data
Implementing strategies to handle any missing values identified in the dataset.

### Visualizing the Sales Distribution
Creating a histogram to visualize the distribution of sales, noting any trends or patterns in the data.

## Step 3: Model Building
Creating a pairplot to visualize relationships between variable pairs, helping select the best independent variables for regression.

Based on analysis, Discounts, TV advertising, and Social Media advertising will be used as independent variables \(X\) given their relationships with sales.

### Build and Fit the Model
Construct the multiple linear regression model using the selected independent variables.

## Step 4: Results and Evaluation

### Interpreting the Model Results
- The coefficient for `TVLow is` **`-148.2727`**, which indicates that, holding the `Radio` value constant, sales for `TVLow` are **`$148.2727`** million less than sales for `TVHigh`.

- The coefficient for `TVMedium` is **`-70.3024`**, which indicates that, holding the `Radio` value constant, sales for `TVMedium` are **`$70.3024`** million less than sales for `TVHigh`.

- The coefficient for `Radio` is **`3.0084`**, which means that regardless of whether `TV` is Low, Medium, or High, when `Radio` increases by one million, sales increase by **`$3.0084`** million.

- The `p-value` for all coefficients is **`0.000`**, indicating that all coefficients are statistically significant at the  level. lies within this interval.

### Measuring the Uncertainty of the Coefficient Estimates
 **Confidence Intervals for TV Promotions**: The **`95%` confidence interval** for the coefficient of **TVLow** is **`$[-160.302, -136.243]`** and **TVMedium** is **`$[-79.147, -61.458]`**. This means we are **`95%` confident** that the true impact of choosing a Low TV promotion or Medium TV promotion instead of a High TV promotion falls within these ranges, further supporting the assertion that Low TV promotions and Medium TV promotions significantly lower sales compared to High promotions.

## Conclusion

### Key Insights 

- **Impact of TV Promotion Levels**: The coefficient for **TVLow** is **`-148.2727`**, indicating that, when holding Radio constant, sales with **Low TV promotion** are expected to be **`$148.2727` million less** than sales with **High TV promotion**. Similarly, **TVMedium** has a coefficient of **`-70.3024`**, meaning sales for **Medium TV promotion** are **`$70.3024` million less** than those for **High TV promotion**.

- **Effect of Radio Advertising**: The positive coefficient for **Radio** of **`3.0084`** indicates that for every **`$1` million increase** in Radio spending, sales increase by **`$3.0084` million**, regardless of the level of TV promotion. This highlights the importance of Radio advertising in driving sales.

- **Statistical Significance of Coefficients**: All coefficients have a **p-value of `0.000`**, indicating that they are statistically significant at the **`p=0.05`** level. This suggests strong evidence that the relationships observed in the model are not due to random chance.

- **Confidence Intervals for TV Promotions**: The **`95%` confidence interval** for the coefficient of **TVLow** is **`[-160.302, -136.243]`**. This means we are **`95%` confident** that the true impact of choosing a Low TV promotion instead of a High TV promotion falls within this range, further supporting the assertion that Low TV promotions significantly lower sales compared to High promotions.
### Recommendations to Leadership
Prioritize increasing investments in discounts and TV advertising, as they have the strongest predictive relationships with sales outcomes.

### Summary for Stakeholders
The analysis indicates that **high TV promotional budgets** significantly boost sales. Specifically:

- **Switching from High to Medium TV Budget**: This change is associated with a **`$70.3024` million decrease** in sales, with a **`95%` confidence interval (CI)** of **`$[-79.147, -61.458]`**.
  
- **Switching from High to Low TV Budget**: This transition leads to a **`$148.2727` million reduction** in sales, supported by a **`95%` CI of `$[-160.302, -136.243]`**.

- **Radio Promotion Impact**: Increasing the radio promotional budget by **`$1` million** is expected to generate an additional **`$3.0084` million in sales**, with a **`95%` CI of `$[2.510, 3.507]`**.



## How to Run

1. **Clone the repository**:

    ```bash
    git clone <https://github.com/MahmoudKhaled98/Multiple-Linear-Regression-Analysis-on-Marketing-Campaigns.git>
    ```

2. **Install the required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Jupyter notebook**:

    ```bash
    jupyter notebook
    ```

## References

- Saragih, H.S. (2020). [*Marketing and Sales Data*](https://www.kaggle.com/datasets/harrimansaragih/dummy-advertising-and-sales-data).

- [Pandas Documentation](https://pandas.pydata.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Statsmodels Documentation](https://www.statsmodels.org/stable/index.html)
