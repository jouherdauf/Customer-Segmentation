# Customer-Segmentation
<p>In a world where companies are expanding rapidly and regularly serving a big consumer base. Businesses must now classify their clientele in order to provide better customer service and to better understand the various ways that varied clientele might affect their operations. The purpose of this project is to categorize customers and determine how they affect the company.</p>
<h1><b>Problem Description</b></h1>
<p></p>In this project, your task is to identify major customer segments on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.</p>
<h1>Data Description</h1>
<ul>
<li>InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.</li>
<li></li>StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
Description: Product (item) name. Nominal.</li>
<li>Quantity: The quantities of each product (item) per transaction. Numeric.</li>
<li>InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.</li>
<li>UnitPrice: Unit price. Numeric, Product price per unit in sterling.</li>
<li>CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.</li>
<li>Country: Country name. Nominal, the name of the country where each customer resides.</li>
</ul>

<p> This project has been completed in 5 steps :-</p>
<ol>
<li>Data Cleaning</li>
<li>Exploratory Data Analysis (EDA)</li>
<li>Data Transformation</li>
<li>Clustering</li>
<li>Cluster Profiling</li>
<li>Model Performance</li>
</ol>

<p>From the EDA section some assumptions can be made</p>
<ol>
<li>Small to medium quantities of each item are purchased more.</li>
<li>Unit price for most products is low.</li>
<li>Last quarter of the year has more orders maybe due to the holiday season.</li>
<li>As customers buy in large quantites, it is a volume based business.</li>
</ol>

<h1>Model Performance</h1>
<h2>Kmeans</h2>
![kmeans](https://github.com/jouherdauf/Customer-Segmentation/assets/64728749/a43595a3-0a1b-49d3-a499-243b59933a95)

<h2>Heirachical</h2>
![heirachical](https://github.com/jouherdauf/Customer-Segmentation/assets/64728749/27bdc89e-93f8-404e-b30b-588e30a9eae8)

<h2>Model Evaluation Table</h2>
<table>
  <tr>
    <th>Sl.no</th>
    <th>Model Name</th>
    <th>Data</th>
    <th>Optimal_Number_of_cluster</th>
  </tr>
  <tr>
    <td>1</td>
    <td>K-Means with silhouette_score </td>
    <td>RFM</td>
    <td>3</td>
  </tr>
  <tr>
    <td>2</td>
    <td>K-Means with Elbow methos </td>
    <td>RFM</td>
    <td>3</td>
  </tr>
    <tr>
    <td>3</td>
    <td> K-Means with distortion methos</td>
    <td>RFM</td>
    <td>3</td>
  </tr>
    <tr>
    <td>4</td>
    <td>K-Means with calinski_harabasz </td>
    <td>RFM</td>
    <td>3</td>
  </tr>
    <tr>
    <td>5</td>
    <td>Hierarchical clustering(ward) with silhoutte_score</td>
    <td>RFM</td>
    <td>3</td>
  </tr>
    <tr>
    <td>6</td>
    <td>Hierarchical clustering(ward) with dendograms and eulidean distance 40</td>
    <td>RFM</td>
    <td>3</td>
  </tr>
</table>

## **Conclusion**


###1. Data Cleaning: Here, outliers, null values, and canceled orders were eliminated.
###2. Exploratory Data Analysis (EDA): In this section, univariate and bivariate analyses were performed to gain a deeper understanding of the data. The company offers medium-to-low quantities of single items at a cheaper unit cost. More orders of various items were placed in the previous quarter, with the UK placing the highest orders overall. The "pack of 72 retrospot cake cases" was the best-selling item in terms of amount sold.

###3. Data Transformation: For each customer ID in this section,Monetary , frequency, and recency analysis was produced. These three elements are essential part of customer segmentation.

###4 Outliers detection & Feture Transformation: Frequency  and Monetary contains high number's of outliers but by any customer id it means we may be ignoring potential client so we have remove very outliers.Recency,Frequency and Monetary is higly positive so we have applied logarithm transformation to it.

###5. Clustering Kmeans: In this step, the optimal number of clusters was ascertained by using silhouette analysis and the elbow technique. The optimal clusters were found to be three. The KMeans model contained three clusters. Every customer ID was allocated to one of the three clusters.

###6 Clustering Silhoutte - Using the silhoutte analysis and dendograms distance, the ideal number of clusters is three.

###7. Cluster Profiling: The frequency, monetary values, and recency of each client segment were averaged in this section. As a result, three groups were identified: high value and loyal customers, average value and frequent customers, and low value and infrequent customers.

###8. Model Performance: From the above table we can say that 3 clusters are optimum for clustering.The best performance is given by kmeans with 3 clusters and in Hierarchical clustering best model is given by ward method with 3 clusters


###Based on the results of this analysis, the company may provide its average and low-value clients with enticing offers, and it can also provide specific business services to its high-value clients, such loyalty points.



