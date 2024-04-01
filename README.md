Home_Sales
Module 22 Challenge

This challenge will require to use your understanding of the SparkSQL knowledge to determine the metrics about homes sales data. Once the dependencies of pyspark are imported, We can import the data from s3 bucket as read_csv and create as Data frame.Then we use sparksql to query the Data tables. Spark can be used to create temporary views, partition the data, cache and uncache temporary tables, and also to verify that the table has been uncached. The difference in the reading is seen due to the ability to use cached and uncached data.

Some of the questions addressed during the assignment using Spark were as follows:

What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places 
Answer: 

+----+---------+
|sale|avg_price|
+----+---------+
|2019| 300263.7|
|2020|298353.78|
|2021|301819.44|
|2022|296363.88|
+----+---------+

What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
 Answer:
 
+----------+---------+
|date_built|    price|
+----------+---------+
|      2010|292859.62|
|      2011|291117.47|
|      2012|293683.19|
|      2013|295962.27|
|      2014|290852.27|
|      2015| 288770.3|
|      2016|290555.07|
|      2017|292676.79|
+----------+---------+
  
  What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
  
   Answer: 
   +----------+---------+
|date_built|    price|
+----------+---------+
|      2010|285010.22|
|      2011|276553.81|
|      2012|307539.97|
|      2013|303676.79|
|      2014|298264.72|
|      2015|297609.97|
|      2016| 293965.1|
|      2017|280317.58|
+----------+---------+

What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places. 
Answer: --- 1.10978102684021 seconds ---

Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime. 

Answer: --- 0.8811173439025879 seconds ---

Run the query that filters the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

Answer--- 1.8267714977264404 seconds ---