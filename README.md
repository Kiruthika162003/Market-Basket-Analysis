# Bread Basket Analysis

## Overview

This project analyzes the sales data from a bakery to understand customer purchasing patterns. The analysis includes data pre-processing, exploration, visualization, and the application of the Apriori algorithm for market basket analysis.

## Algorithms Used

- **Apriori Algorithm**
 This algorithm is used to find frequent itemsets and generate association rules. It helps in identifying items that are often bought together.

## Dataset

The dataset contains sales transactions from a bakery. It includes the following columns:
- **Transaction**
- Unique identifier for each transaction.
- **Item**
-  The item purchased.
- **date_time**
-  The date and time of the transaction.
- **period_day**
-  The period of the day (morning, afternoon, etc.).
- **weekday_weekend**
-  Whether the transaction occurred on a weekday or weekend.

## Data Pre-processing

1. **Loading Data**: The data is loaded from a CSV file.
2. **Overview**: An initial overview of the data is obtained to check for missing values and data types.
3. **Date and Time Conversion**: The `date_time` column is converted to a datetime format for easier extraction of date, hour, month, and weekday.
4. **Cleaning Item Names**: Item names are converted to lowercase and stripped of any spaces.

## Data Exploration and Visualizations

### Best Selling Items

- The top 20 best-selling items are identified and visualized using a bar plot.

### Number of Items per Transaction

- The distribution of transactions by the number of items is analyzed and visualized using a histogram.

### Quantity Sold by Month

- The quantity of items sold each month is counted and visualized using a bar plot.

### Quantity Sold by Days of Week

- The number of transactions by day of the week is analyzed and visualized using a bar plot.

### Quantity Sold by Hours

- The number of items sold in different hours of the day is analyzed and visualized using a bar plot.

## Market Basket Analysis

### Data Preparation

- The data is transformed into a one-hot encoded format suitable for the Apriori algorithm.

### Frequent Itemsets

- Frequent itemsets are identified using the Apriori algorithm with a minimum support threshold of 1%.

### Association Rules

- Association rules are generated from the frequent itemsets with a minimum lift threshold of 1.2. Lift measures the strength of the association between items.

### Visualization

- **Parallel Coordinates Plot**: Visualizes the association rules.
- **Lift Heatmap**: Shows how often antecedents and consequents occur together more often than random.
- **Confidence Heatmap**: Shows how often the consequent is purchased given that the antecedent was purchased.

## Result Interpretation

- The analysis helps in understanding customer purchasing patterns, such as which items are frequently bought together.
- The visualizations provide insights into the best-selling items, the distribution of transactions, and the quantity sold by different time periods.
- The association rules can be used to make informed decisions about product placement, promotions, and inventory management.
