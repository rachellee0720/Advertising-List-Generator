# Advertising List Generator: KMeans

### **:dart: Goal** 
1. to find out customers who are interested in the products that are expected to be advertised.

### **:cactus: Process**
1. Construct dataset

	> 1. Collect the browsing behavior data of all customers in previous month before the expected advertising time point.
	> 2. Divide customers into key customers and potential customers. Key customers are those who have ever entered the order payment page of the products that are expected to be advertised.
	> 3. Created fields: customers' website browsing frequency, number of purchases and product preference, etc.	
	
2. Clustering
	> 1. cluster the key customers.
	> 2. Used model is KMeans, and select the number of clusters through elbow method.
	> 3. Find the most loyal key customers cluster through the average value of each column in dataset of each cluster.
		
3. Produce the advertising list
	> 1. Use cosine similarity to find potential customers who have similar browsing behaviors to the selected most loyal key customers cluster. These customers are considered to have purchase intentions but have not yet placed an order, so they are the target audiences of advertisement.

### **:clap: Results**
1. Return on AD Spending (ROAS) increased from -0.72 % to 4.59 %.
2. Compared with the performance of manually setting the advertising conditions, this model had a higher click through rate (CTR) and a lower cost per click (CPC).



# 廣告名單產生器：KMeans
1. 目標：找出對該次預計投放廣告之商品有興趣的顧客
2. 流程：
	1. 建構資料集：
		1. 蒐集預計投放廣告時間點前一個月所有顧客之瀏覽行為資料
		2. 將顧客分成關鍵顧客和潛在顧客，關鍵顧客為曾經進入該次預計投放廣告之商品的訂單付款頁面者。
		3. 創建欄位：顧客的網站瀏覽頻率、消費次數 和 對產品之偏好
	2. 模型分群：
		1. 將關鍵顧客進行分群
		2. 使用模型：KMeans，且透過Elbow Method選擇分群數
		3. 透過每群的欄位平均值尋找忠誠度最高之關鍵顧客群
	3. 產出名單：
		1. 透過餘弦相似度(cosine similarity)尋找潛在顧客中與挑選出之關鍵顧客群擁有相似瀏覽行為者，這些顧客被視為具有購買意圖但尚未下單者，因此成為廣告投放名單
3. 結果：
	1. 廣告投資報酬率(Return on AD Spending, ROAS)從 -0.72 % 增長到 4.59 %
	2. 此模型與人工設定投放廣告條件之投放結果相比，此模型獲得較高之點擊率(click through rate, CTR)且單次點擊之成本(cost per click, CPC)較低
