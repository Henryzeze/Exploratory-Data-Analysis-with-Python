# Exploratory-Data-Analysis-with-Python


**Note:** ***This is a followup on my github repository "Data Wrangling with Python"***

## Introduction

The objective of this project is to perform Exploratory Data Analysis (EDA) on car-related data. By analyzing various characteristics and features, the aim is to determine the factors that significantly impact the pricing of cars.

## Steps

### Choosing the Appropriate Visualization Method

When analyzing individual variables, it's crucial to identify the variable type to select the most suitable visualization technique.

For instance, you can calculate the correlation between variables classified as "int64" or "float64" by using the "corr" method:

![](cor.JPG)

### Continuous Numerical Variables

The process involves analyzing continuous numerical variables using scatterplots with fitted regression lines. It aims to understand the linear relationship between individual variables and price, using "regplot" in Python's visualization libraries.

It showcases examples of different linear relationships:

**1. Positive Linear Relationship:**

Examining the correlation between 'engine-size' and 'price' reveals a direct positive correlation (approximately 0.87). As engine size increases, the price also increases, indicating a strong positive relationship.

![](eng.JPG)

**2. Negative Linear Relationship:**

Evaluating the correlation between 'highway-mpg' and 'price' shows an inverse/negative correlation (approximately -0.704). As highway mpg increases, the price decreases, suggesting a negative relationship.

![](high.JPG)

**3. Weak Linear Relationship:**

Assessing 'peak-rpm' as a predictor of 'price' demonstrates a weak and unreliable relationship (correlation approximately -0.101616). The regression line is nearly horizontal, indicating a lack of predictability in price based on peak rpm due to scattered and variable data points.

![](peak.JPG)

#### Categorical Variables

This process focuses on exploring categorical variables, which represent characteristics selected from specific groups or categories within the dataset. Categorical variables can be of type "object" or "int64", and boxplots are a useful visualization tool for these variables.

**Analyzing "body-style" vs. "price":**

The boxplot indicates an overlap in price distributions among different body-style categories, suggesting that body-style might not be a reliable predictor of price.

![](body.png)

**Investigating "engine-location" vs. "price":**

The boxplot reveals distinct price distributions between front and rear engine-location categories. This distinct difference suggests that engine-location could potentially be a good predictor of price.

![](eng.png)

**Evaluating "drive-wheels" vs. "price":**

The boxplot illustrates varying price distributions among different drive-wheels categories. This variation indicates that drive-wheels might serve as a possible predictor of price due to the differences observed in price distribution.

![](drive.png)

### Descriptive Statistical Analysis

This process focuses on conducting a descriptive statistical analysis of the dataset's continuous variables using the "describe" function. The function automatically calculates basic statistical measures for each continuous variable, excluding any NaN (missing) values. The statistics provided include:

- Count: The number of non-null entries for the variable.
- Mean: The average value of the variable.
- Standard deviation (std): A measure of the dispersion or spread of the data from the mean.
- Minimum value: The smallest value in the dataset.
- IQR (Interquartile Range): Represented by the 25th percentile (Q1), median (50th percentile or Q2), and 75th percentile (Q3). It signifies the range between the first and third quartiles of the data distribution.
- Maximum value: The largest value in the dataset.

![](describe.JPG)

### Value Counts

This process involves utilizing the "value_counts" method to analyze the distribution of different units within a specific characteristic or variable, such as 'drive-wheels.' It is a useful technique for understanding the frequency or count of each unique value in a categorical column.

1[](counts.JPG)
