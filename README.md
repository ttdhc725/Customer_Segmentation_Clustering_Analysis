# Customer Segmentation & Clustering Analysis

## Project Overview

This project analyzes mall customer data to identify different customer groups for marketing strategy. The main goal is to help the marketing team understand customer behavior and decide which customer segments should be targeted first.

The analysis uses Python and K-Means clustering to group customers based on their annual income and spending score.

## Business Problem

The marketing team wants to answer three key questions:

1. What types of customers does the mall have?
2. Which customer group has the highest marketing value?
3. How can marketing campaigns be designed for different customer groups?

Instead of using the same marketing campaign for every customer, customer segmentation helps the business create more targeted strategies.

## Dataset

The dataset contains 200 mall customers.

Key variables include:

- **CustomerID**: Unique customer ID
- **Gender**: Customer gender
- **Age**: Customer age
- **Annual Income (k$)**: Customer annual income in thousands
- **Spending Score (1-100)**: Customer spending behavior score

In this project, **Annual Income** represents customer spending ability, while **Spending Score** represents customer spending behavior.

## Tools Used

- Python
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Analysis Process

### 1. Exploratory Data Analysis

I first explored the dataset to understand customer demographics and behavior.

The analysis included:

- Gender distribution
- Age distribution
- Annual income distribution
- Spending score distribution
- Correlation between numerical variables
- Pairplot and scatterplot analysis

Key findings:

- Female and male customers have similar average age and income.
- Female customers have a slightly higher average spending score.
- Age and spending score have a weak negative relationship.
- Annual income alone does not directly explain spending score.

This means income by itself is not enough to identify the best customers. A customer can have high income but low spending behavior, or lower income but high spending behavior.

### 2. K-Means Clustering

I used K-Means clustering to group customers based on similarity.

First, I tested income-only clustering. This created three income groups:

- Low income customers
- Middle income customers
- High income customers

However, income-only clustering is not enough for marketing because high income does not always mean high spending.

Then I used both:

- Annual Income
- Spending Score

This created a clearer customer segmentation result.

### 3. Elbow Method

I used the elbow method to choose a reasonable number of clusters.

The elbow method compares different numbers of clusters and checks the inertia score. Inertia measures how close customers are to the center of their assigned cluster.

A lower inertia score means customers are closer to their cluster center. However, adding too many clusters can make the result harder to explain. The goal is to find a reasonable balance.

Based on the elbow method and business interpretation, I selected 5 customer segments.

## Main Result: 5 Customer Segments

The final K-Means model grouped customers into five segments:

| Segment | Business Meaning |
|---|---|
| High income + high spending | Best target customers |
| High income + low spending | Potential customers |
| Low income + high spending | Promotion-sensitive customers |
| Middle income + average spending | Regular customers |
| Low income + low spending | Low priority customers |

## Business Insights

### Best Target Customers

Customers with high income and high spending score are the most valuable group. They have both strong spending ability and strong spending behavior.

Recommended strategy:

- VIP programs
- Premium campaigns
- Personalized offers
- High-end product promotions

### Potential Customers

Customers with high income but low spending score have strong purchasing power, but they are not currently spending much.

Recommended strategy:

- Personalized marketing campaigns
- Exclusive offers
- Brand engagement campaigns
- Customer preference analysis

### Promotion-Sensitive Customers

Customers with low income but high spending score show strong spending behavior, even though their income is lower.

Recommended strategy:

- Coupons
- Discounts
- Seasonal promotions
- Loyalty rewards

### Regular Customers

Customers with middle income and average spending score represent stable customers.

Recommended strategy:

- General marketing campaigns
- Membership programs
- Regular product recommendations

### Low Priority Customers

Customers with low income and low spending score are not the best short-term marketing target.

Recommended strategy:

- Low-cost engagement campaigns
- Basic awareness campaigns

## Business Recommendation

The marketing team should prioritize the high-income, high-spending customer segment because this group has the highest marketing value.

The business should also create different strategies for different customer groups instead of using one general campaign for all customers.

Customer segmentation allows the marketing team to:

- Identify high-value customers
- Improve campaign targeting
- Reduce wasted marketing spend
- Design more personalized promotions
- Better understand customer behavior

## Conclusion

This project shows how customer segmentation can support marketing decision-making. By using K-Means clustering, the mall can group customers based on income and spending behavior, then design targeted marketing strategies for each customer segment.

The most important business insight is that annual income alone does not define customer value. The best marketing target is the group with both high income and high spending score.
