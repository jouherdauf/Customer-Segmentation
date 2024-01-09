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


