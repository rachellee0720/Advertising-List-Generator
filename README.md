# Advertising List Generator: KMeans

1. **Goal:** to find out customers who are interested in the products that are expected to be advertised.

2. **Process:**

	1. **Construct dataset**
		
		1. Collect the browsing behavior data of all customers in previous month before the expected advertising time point.
		2. Divide customers into key customers and potential customers. Key customers are those who have ever entered the order payment page of the products that are expected to be advertised.
		3. Created fields: customers' website browsing frequency, number of purchases and product preference, etc.	
	
	2. **Clustering:**
		1. cluster the key customers.
		2. Used model is KMeans, and select the number of clusters through elbow method.
		3. Find the most loyal key customers cluster through the average value of each column in dataset of each cluster.
		
	3. **Produce the advertising list:**
		1. Use cosine similarity to find potential customers who have similar browsing behaviors to the selected most loyal key customers cluster. These customers are considered to have purchase intentions but have not yet placed an order, so they are the target audiences of advertisement.

3. **Results:**

	1. Return on AD Spending (ROAS) increased from -0.72 % to 4.59 %.
	
	2. Compared with the performance of manually setting the advertising conditions, this model had a higher click through rate (CTR) and a lower cost per click (CPC).
