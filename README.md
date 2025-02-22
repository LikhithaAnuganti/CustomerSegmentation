Here’s a README for your project on Customer Segmentation using RFM Analysis:

---

# Customer Segmentation using RFM Analysis

This project uses **Recency, Frequency, and Monetary (RFM)** analysis to segment customers based on their behavior in an eCommerce environment. By applying clustering techniques, it identifies groups of customers that exhibit similar patterns, which can help businesses better understand their customer base and optimize marketing strategies.

## Project Overview

### Purpose:
To perform customer segmentation based on RFM metrics and gain insights into customer behaviors, which can be leveraged for targeted marketing, product recommendations, and customer retention strategies.

### Key Concepts:
- **Recency (R)**: How recently a customer has made a purchase.
- **Frequency (F)**: How often a customer makes a purchase.
- **Monetary (M)**: How much money a customer has spent.

### Tools & Libraries:
- **Python**: Used for data analysis and visualization.
- **Libraries**: `pandas`, `matplotlib`, `seaborn`, `sklearn`, and `warnings`.

### Data:
The dataset used in this analysis is a CSV file containing transactional data from an eCommerce platform. The dataset includes columns such as:
- `InvoiceNo`: Invoice number identifying each transaction.
- `StockCode`: Product code.
- `Description`: Product name.
- `Quantity`: Quantity of products purchased.
- `InvoiceDate`: Date and time of the transaction.
- `UnitPrice`: Price per unit of the product.
- `CustomerID`: Unique identifier for each customer.
- `Country`: Country of the customer.

## Steps Involved:

### 1. **Data Preprocessing:**
- Loading the dataset and cleaning missing values.
- Converting `InvoiceDate` to datetime format.
- Handling missing values for `Description` and `CustomerID`.

### 2. **RFM Calculation:**
- **Recency**: The number of days since the customer’s most recent purchase.
- **Frequency**: The number of unique invoices for each customer.
- **Monetary**: The total spending of each customer.

### 3. **RFM Segmentation:**
- Quartiles are used to assign scores (1 to 4) for each RFM metric.
- Customers are assigned a unique `RFM_Score` based on the combination of their Recency, Frequency, and Monetary scores.

### 4. **Customer Segmentation with K-Means Clustering:**
- Using K-Means clustering, customers are grouped into clusters based on their RFM metrics.
- The optimal number of clusters is determined using the elbow method.

### 5. **Visualizations:**
- Average Recency, Frequency, and Monetary values across customer segments.
- Scatter plots to visualize the relationships between RFM metrics across clusters.
- Time analysis to visualize the distribution of orders by day of the week and hour of the day.

### 6. **Product Analysis:**
- Identifying the top 10 most frequently purchased products across all RFM segments.
- Analyzing average prices of products across RFM segments.
- Determining the product category generating the highest revenue.

### 7. **Time Analysis:**
- Analyzing the number of orders by day of the week and hour of the day to identify peak times for orders.

### 8. **Exporting Results:**
- Exporting the final RFM segmented data into a CSV file for further analysis.

## Outputs:
- **Customer Segmentation CSV**: A file containing customer IDs and their corresponding RFM scores and clusters.
- **Visualizations**: Graphs showing average RFM metrics by customer segment, as well as order patterns over time.
- **Insights**: Information about the most frequent purchasing behaviors, product preferences, and peak order times.

## Getting Started

### Prerequisites:
Ensure the following libraries are installed:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

### Running the Code:
1. Load the dataset using `pd.read_csv('ecommerce_data.csv')`.
2. Preprocess and clean the data.
3. Calculate the RFM metrics for each customer.
4. Perform K-Means clustering to segment the customers.
5. Visualize the results and interpret the segments.
6. Analyze product sales and order times.
7. Export the segmented customer data to a CSV file.

## Insights & Next Steps:
- Based on the customer segmentation, businesses can target high-value customers with personalized offers and promotions.
- Segmenting customers helps in identifying dormant customers, loyal customers, and new customers for focused marketing efforts.
- Further improvements can include integrating additional features (e.g., customer demographics, browsing history) to refine the segmentation model.
