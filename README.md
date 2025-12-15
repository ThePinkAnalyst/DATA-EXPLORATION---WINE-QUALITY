# Exploratory Data Analysis for Product Quality Drivers: Red Wine Case Study

## Executive Summary

Understanding the drivers of product quality is essential for quality control, process optimization, and predictive modeling.

This project applies exploratory data analysis (EDA) techniques to a red wine quality dataset to identify how chemical properties influence perceived product quality. By examining distributions, correlations, and outliers, the analysis highlights key variables that can inform quality improvement strategies and downstream machine learning models.


## Business & Analytical Objective

Wine quality is influenced by multiple interacting chemical properties, making it difficult to isolate which factors most strongly affect consumer perception.

The objectives of this analysis are to:
- Identify chemical attributes most associated with high-quality ratings
- Detect patterns and anomalies that may indicate production issues
- Prepare the dataset for reliable downstream modeling


## Dataset Overview

The dataset contains physicochemical measurements of red wine samples alongside a quality score assigned by expert tasters.

Key features include:
- Acidity measures (fixed acidity, volatile acidity, citric acid, pH)
- Sulfur dioxide content
- Sugar, density, sulphates, and alcohol content
- Target variable: wine quality score (ordinal scale)



## Data Preparation & Quality Checks

- Dataset structure and distributions were examined using summary statistics
- No missing values were detected
- Duplicate records were identified and removed

### Outlier Handling
Outliers were detected using the Interquartile Range (IQR) method. Extreme values were removed to prevent distortion of correlation analysis and summary statistics.

This approach reflects a quality-control perspective, where extreme measurements may indicate measurement errors or atypical production batches.


## Quality Distribution

The dataset contains four quality ratings (4–7), with most wines rated 5 or 6. This imbalance suggests that distinguishing between average and high-quality wines may be more challenging than detecting low-quality outliers.


## Correlation Analysis

Correlation analysis revealed several meaningful relationships:

- **Alcohol content** shows the strongest positive correlation with quality, indicating that higher alcohol levels are generally associated with better-rated wines.
- **Volatile acidity** exhibits a strong negative correlation, suggesting that excessive acidity negatively impacts perceived quality.
- **Residual sugar** and **free sulfur dioxide** show weak correlations, indicating limited direct influence on quality scores.


## Distributional Insights

Fixed acidity displays a right-skewed distribution across quality categories, particularly for wines rated 5 and 6. This suggests that while acidity contributes to quality, extreme values do not necessarily lead to higher ratings.


## Feature Relationships

Several notable relationships between chemical properties were identified:

- Fixed acidity and citric acid are positively correlated and jointly associated with higher quality
- Fixed acidity and pH exhibit a strong inverse relationship, reflecting known chemical behavior
- Volatile acidity and citric acid show a negative relationship, reinforcing their opposing roles in wine quality
- Free and total sulfur dioxide are strongly correlated, as expected from production practices


## Analytical Implications

The findings from this EDA have direct implications for downstream analysis:

- Alcohol content and volatile acidity should be prioritized features in predictive models
- Weakly correlated variables may contribute limited predictive power
- Outlier handling significantly improves stability for regression and classification tasks
- Feature interactions (e.g., acidity + density) suggest non-linear modeling approaches may be beneficial


## Limitations

- Quality ratings are subjective and based on human perception
- The dataset lacks contextual variables such as grape variety, region, and production method
- Cross-sectional data limits causal inference


## Future Work

- Develop regression or classification models to predict wine quality
- Explore interaction effects and non-linear relationships
- Incorporate additional features such as production conditions or sensory descriptors
- Use findings to inform feature engineering pipelines


## Conclusion

This exploratory analysis identified key chemical drivers of red wine quality and highlighted the importance of thoughtful data cleaning and feature evaluation.

Beyond descriptive insights, the analysis provides a strong foundation for predictive modeling and quality optimization, demonstrating how EDA supports data-driven decision-making in product-focused domains.
