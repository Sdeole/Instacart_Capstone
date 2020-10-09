 Instacart Basket Analysis: Predicting what the buyer will buy next in his basket

INTRODUCTION: 
Instacart is an American company that operates a grocery delivery and pick-up service in the United States and Canada. The company offers its services via a website and mobile app. The service allows customers to order groceries from participating retailers with the shopping being done by a personal shopper. The way the company generates revenue is by adding markup on prices for specific stores, delivery and membership fee. Hence, the main business objective for the organization is to, not only increase the number of customer memberships but also improve the repeat visit and orders. Predicting consumer engagement and behavior with the products and grocery stores have a huge impact on Instacart’s success.
The focus of this analysis was to build a probability model to predict what the probability is that an Instacart customer will order. To do that we have to understand customers behavior patterns. We will use data from previous purchases to know when most purchases are made on Instacart and order product data to learn what is a best-selling product. This analysis will mostly be done by data visualization and market basket analysis. 

Data Source: 
Instacart released a public dataset, “The Instacart Online Grocery Shopping Dataset 2017”. The dataset contains over 3 million anonymized grocery orders from more than 200,000 Instacart users. This analysis will make use of this datasets.
Data source can be downloaded here:
https://www.kaggle.com/c/instacart-market-basket-analysis/data

DATA DESCRIPTION:
With data Sourced from Kaggle: There are six csv data files - Order, Products, Aisles, Department, Order Product Prior, Order Product Train,
Instacart Data description (Sample):
•	Order: Contains order information of each customer including product, time and day of purchase
•	Products: Contains product name
•	Aisles: Contains product name, aisle number
•	Departments: Contains product name, department number
•	Order Products Prior: Contains customer cart information - order number, product number and product reordered
•	Order Products Train: Contains training data information (~131k orders)

RESEARCH GOAL AND OBJECTIVE:
•	Main Goal: The objective of this analysis was to predict what will the user buy in the next order, given all data of prior orders.
•	Secondary Objective: Before suggesting which users would reorder the item again, user interaction with the items will be explored by asking the following questions.
What days customers usually order, i.e hours and days
How many days it would take the users to reorder the product
What are the best-selling products or the most reordered products?
When do people order?

EXPLORATORY DATA ANALYSIS
Exploratory data analysis was performed to understand the buying behavior by asking some interesting questions.
•	What usually do people buy, and which products they usually reorder
•	When do they buy (day and time)? Is there a buying trend and does it influence what they buy?

PREDICTIVE DATA ANALYSIS 
Predictive data analysis was perfomed to predict what product the customer will purchase in his next basket. The prediction was based on the probability estimation of previously purchased products. This was a classification problem as well as regression of probability of repurchases. 
Naive Prediction, Smarter Naive Prediction and Logistic Regression were used for analysis. 

KEY OBSERVATIONS: 
	Most users made few orders. The number of orders users made decrease significantly along the order numbers. Maximum orders any users had made is 99.
	It is very obvious that most users made their orders weekly (every 7 days) and monthly (every 30 days). 
	Based on the analysis bananas are the most popular products. 
	The number of orders varied greatly for different products. Certain departments were clearly more popular, like produce and dairy eggs. 
	If we look at the buying trend of product by aisles it is certain that aisles like vegetables and fruits contributes to almost 30% of total orders
	Morning to afternoon were the peak shopping hours for Instacart customers and the hour order made influences basket size.
	In the grocery, there are close to 50,000 products. When we zoom into hourly purchases, we noticed that top 10 products managed to score between 6% to 8% of hourly sales.
	Every hour has slightly different combination of top 10 products (combination out of 12 products). That means certain products are predictable for ordering regardless of the hour of order.

DEEP INSIGHTS 
•	Customers always order from 8:00 - 18:00 and the most common day that customers like to order are Sunday and Monday
•	Majority of customers reorder the last day of the month
•	The best-selling products are either fruit or organic products

We know that Instacart is an online Grocery store (web app), so Market Basket Analysis can be used to drive business decision-making by using the association results. There are a number of ways in which Market Based Analysis can be used:
•	It can help in aisles layout. Aisles should be placed together on the web application to help customer better find their products. This can boost the sales and reduce the time spent in finding that Aisle. For instance, Cereal, Lunch Meat, and Bread Aisles should be placed together, as they are highly associated.

CONCLUSION
What have we learned?
•	Most orders are placed on Sunday and Monday between 08:00 - 18:00.
•	There are two categories of customers - those who reorder weekly and those who reorder on the 30th day.
•	The majority of customers who reordered, reorder on the 30th day
•	Organic Products and Fruit are the most ordered products.
•	For the reordered products, we noticed that many of the items are liquids, i.e Milk and organic milk.
•	Around 60% of ordered products are reordered.
•	Customers are more likely to reorder organic than non-organic products.
•	For the MBA, if customers purchased organic products or fruits, they purchased bananas and organic bananas.

FUTHER EXPLORATION
Based on the analysis done on Instacart, I found out that:
•	Most of the reordered items are liquids, specifically Milk and Organic Milk.
•	Top ordered product was either Organic or fruit
•	Top ordered products which are organic and fruit have a high probability of being reordered
The question to explore is that why customers tend to reorder organic products than non-organic. Even if organic products are more costly than non-organic. One of my hypotheses is that customers who ordered organic products are consuming unhealthy options outside their homes. They want to eat healthy at home. I would like to add an additional dataset i.e. income, education and job, or conduct a survey asking i.e. What products do you prefer organic or non-organic when eating at home and why do you prefer it?

RECOMMENDATIONS/USE CASE FOR PREDICTIONS
Based on the analysis done on Instacart, I found out that:
•	Customers tend to reorder organic products than non-organic products, so Instacart should focus more on organic products rather than non-organic.
•	Create subscription-based model for products prone to reordering
•	Assist partner stores with inventory management
•	Send promotions for most reordered and complimentary products
•	Suggest high margin substitutes for frequently reordered products

ACKNOWLEDGEMENTS:
This was one of my capstone projects for the Data Science Career Track program at TEXAS A&M.
I would like to thank my Professor Jonathan Fowler for his guidance, support and feedback. 
In addition, I would like to thank my colleague Gina Choe for helping out in the time of need.  

CITATIONS
1.	The Instacart Online Grocery Shopping Dataset 2017“, Accessed from https://www.instacart.com/datasets/grocery-shopping-2017
2.	Data Dictionary: https://gist.github.com/jeremystan/c3b39d947d9b88b3ccff3147dbcf6c6b 
3.	https://rstudio-pubs-static.s3.amazonaws.com/446413_6ac206ffa826466bb3a33be2f338c61f.html#analysis-recommendations 
4. https://www.kaggle.com/philippsp/exploratory-analysis-instacart


