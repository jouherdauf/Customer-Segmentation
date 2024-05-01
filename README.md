# Customer Segmentation

In a world where companies are expanding rapidly and regularly serving a large consumer base, businesses must classify their clientele to provide better customer service and understand how different customer segments might affect their operations. The purpose of this project is to categorize customers and determine how they affect the company.

## Problem Description

In this project, your task is to identify major customer segments in a transnational dataset. The dataset contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts, and many of its customers are wholesalers.

## Data Description

- **InvoiceNo**: Invoice number. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
- **StockCode**: Product (item) code. A 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name.
- **Quantity**: The quantities of each product (item) per transaction.
- **InvoiceDate**: Invoice Date and time, the day and time when each transaction was generated.
- **UnitPrice**: Unit price. Product price per unit in sterling.
- **CustomerID**: Customer number, a 5-digit integral number uniquely assigned to each customer.
- **Country**: Country name, the name of the country where each customer resides.

## Project Steps

1. **Data Cleaning**
2. **Exploratory Data Analysis (EDA)**
3. **Data Transformation**
4. **Clustering**
5. **Cluster Profiling**
6. **Model Performance**

### Assumptions from EDA

1. Small to medium quantities of each item are purchased more.
2. Unit price for most products is low.
3. The last quarter of the year has more orders, maybe due to the holiday season.
4. As customers buy in large quantities, it is a volume-based business.

## Model Performance

### Kmeans

![Kmeans](https://github.com/jouherdauf/Customer-Segmentation/blob/main/images/capstoneimage1.png)

### Hierarchical

![Hierarchical](https://github.com/jouherdauf/Customer-Segmentation/assets/64728749/27bdc89e-93f8-404e-b30b-588e30a9eae8)

### Model Evaluation Table

| Sl.no | Model Name                                 | Data    | Optimal Number of Clusters |
|-------|--------------------------------------------|---------|----------------------------|
| 1     | K-Means with silhouette score              | RFM     | 3                          |
| 2     | K-Means with Elbow method                  | RFM     | 3                          |
| 3     | K-Means with distortion method             | RFM     | 3                          |
| 4     | K-Means with calinski_harabasz             | RFM     | 3                          |
| 5     | Hierarchical clustering (ward) with silhouette score | RFM | 3                   |
| 6     | Hierarchical clustering (ward) with dendograms and Euclidean distance 40 | RFM | 3 |

## Conclusion

1. **Data Cleaning:** Outliers, null values, and canceled orders were eliminated.
2. **Exploratory Data Analysis (EDA):** Medium-to-low quantities of single items are sold at a cheaper unit cost. More orders of various items were placed in the previous quarter, with the UK placing the highest orders overall. The "pack of 72 retrospot cake cases" was the best-selling item in terms of the amount sold.
3. **Data Transformation:** Monetary, frequency, and recency analysis was performed for each customer ID.
4. **Outliers Detection & Feature Transformation:** Frequency and Monetary contain a high number of outliers, but removing them may result in ignoring potential clients. Recency, Frequency, and Monetary are highly positively skewed, so logarithm transformation was applied.
5. **Clustering (Kmeans):** The optimal number of clusters was found to be three. Every customer ID was allocated to one of the three clusters.
6. **Clustering (Hierarchical):** Using silhouette analysis and dendrogram distance, the ideal number of clusters was found to be three.
7. **Cluster Profiling:** The frequency, monetary values, and recency of each client segment were averaged, resulting in three groups: high-value and loyal customers, average value and frequent customers, and low-value and infrequent customers.
8. **Model Performance:** The best performance is given by Kmeans with 3 clusters, and in hierarchical clustering, the best model is given by the ward method with 3 clusters.

Based on the results of this analysis, the company may provide average and low-value clients with enticing offers, and it can also provide specific business services to high-value clients, such as loyalty points.
