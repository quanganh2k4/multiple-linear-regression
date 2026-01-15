# E-commerce Sales Prediction: App vs. Website

**Project by: Group 15**

## 1. Project Overview
An e-commerce company that sells clothing online and offers in-store style consulting sessions is facing a strategic decision. They need to decide whether to focus their efforts on their **Mobile App experience** or their **Website**.

The goal of our team in this project is to use **Multiple Linear Regression** to predict the `Yearly Amount Spent` by customers and determine which platform (App or Web) contributes more to revenue.

## 2. Technologies Used
Our team performed the analysis using **R Language** with the following key libraries:
- **Tidyverse (dplyr, ggplot2):** Data manipulation and visualization.
- **Car & Leaps:** Regression diagnostics and variable selection.
- **ISLR2 & Boot:** Statistical learning datasets and bootstrapping methods.

## 3. Dataset Description
The dataset `Ecommerce_Customers.csv` contains information on **500 customers**.

| Feature | Description |
| :--- | :--- |
| **Email** | Customer's email address. |
| **Address** | Customer's home address. |
| **Avatar** | Color of the customer's avatar. |
| **Avg. Session Length** | Average duration of in-store style advice sessions. |
| **Time on App** | Average time spent on the App (minutes). |
| **Time on Website** | Average time spent on the Website (minutes). |
| **Length of Membership** | How many years the customer has been a member. |
| **Yearly Amount Spent** | **Target Variable:** Total amount spent by the customer in a year. |

## 4. Methodology & Results
We built a Multiple Linear Regression model to quantify the relationship between customer behavior and their spending.

### Model Performance
- **R-squared:** `0.9843` (Our model explains **98.43%** of the variance in spending, indicating an excellent fit).
- **F-statistic p-value:** `< 2.2e-16` (The model is statistically significant).

### Coefficients & Interpretation
Based on our regression summary:

| Predictor | Coefficient | P-value | Interpretation |
| :--- | :--- | :--- | :--- |
| **Length of Membership** | **+61.58** | `< 2e-16` | **Strongest Driver.** For every 1 year increase in membership, yearly spend increases by ~$61.58. |
| **Time on App** | **+38.71** | `< 2e-16` | **Significant.** For every 1 minute increase on the App, yearly spend increases by ~$38.71. |
| **Avg. Session Length** | **+25.73** | `< 2e-16` | **Significant.** In-store sessions also drive sales effectively. |
| **Time on Website** | **+0.44** | `0.326` | **Not Significant.** The p-value is > 0.05, meaning the website usage does not reliably predict spending. |

## 5. Business Recommendation
Based on the data analysis, our group proposes two strategic paths for the company:

1.  **Develop the App:** The Mobile App is currently performing significantly better than the website. Investing here guarantees a return on investment (coefficient of ~38.71).
2.  **Overhaul the Website:** The Website is currently performing poorly (statistically insignificant impact on sales). It likely needs a complete redesign to match the App's performance.

**Strategic Advice:**
> Since **Length of Membership** has the highest impact on revenue (**61.58**), the company should also focus on **Customer Retention Programs** to keep users engaged longer, regardless of the platform they use.
