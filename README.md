# st2195_assignment_3
## Practice Assignment 03

Download the Data Expo 2009 data from the [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7) and construct an
 SQLite Database called airline2.db with the following tables:
 
1. ontime (with the data from 2000 to 2005 – including 2000 and 2005)
2. airports (with the data in airports.csv)
3. carriers (with the data in carriers.csv)
4. planes (with the data in plane-data.csv)

Create a GitHub repository called “st2195_assignment_3” that includes:

1. a README.md file with a short markdown description of this assignment and a
reference to the Data Expo 2009 data, and the [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7) [1 point]
2. a folder called “r_sql” with a R code for constructing the database (from the csv inputs) and replicating the queries in the practice quiz (see Additional Notes section for list of queries Q1 to Q4). The latter should be done both using DBI and dplyr notation [1.75 points each]
3. a folder called “python_sql” with a Python version of the code in point 2, based on sqlite3 [1.75 points]
4. A simplified solution for the query in Q4 in either R or Python (placed either in the R or Python *_sql folder) [1.75 points]

Note that the database file should not be placed in the GitHub repository (it is quite large). Also, the R and Python scripts should save the output of the queries in csv within their respective folders [1 point each].

Additional Notes:
• Select and download the required data files via Harvard Dataverse link given. These are large data files, so processing them may take a while.

 ![ass3ss](https://user-images.githubusercontent.com/91592407/138642194-4e0cf3df-8ed5-4dc2-80e7-338212ba253e.png)


• Queries

o Q1 – Which plane model has the lowest associated average departure delay
(excluding cancelled and diverted flights)?

o Q2 – Which city has the highest number of inbound flights (excluding
cancelled flights)?

o Q3 – Which carrier has the highest number of cancelled flights?

o Q4 – Which carrier has the highest number of cancelled flights, relative to
their number of total flights?

• Hints

o Read about and understand the variables in each data file. This will help
determine which attributes/variables you can use to join the tables.

o Q1 – You may filter to those with departure delay > 0

o Q4 – One way is to create 2 sub-queries (the first to count cancelled flights,
and the second to count total flights), then join them to compute cancelled flights to total flights ratio. Here, you may also need to use CAST function to force counts to be in real numbers.

o Q4 – Another way is simpler, and due to how cancelled flights are represented in the data.
 2
