SPEND ANALYTICS
Problem Statement:-
 To analyse the amount spend to procure new assets and goods by 	  company.
Data Overview:-
The file has the data related to the amount spent by the companies on different items, materials, and short description about the items.
Data Columns :- Purch.Doc., Item, Changed On, Short Text, Material, CoCd, Plnt....

We are using columns from 0 to 19 because the rest of the columns are not very significant to append analysis compared to these.

Procedure:- 
•	Import the required libraries like PANDAS, NUMPY…..
•	Read the data using pandas.
•	Check for NAN values in the data.
•	Handle NAN values.
•	Visualize the Data.
•	Applying 80-20 rule find the 80% cost influencing data.
•	Select the features based on which you need to cluster.
•	Build a sample model.
•	Using Elbow Method find the best number of clusters.
•	Analyze the  clusters.
•	Explore the data clustered together. 



Observations:-
•	There are NaN values in the columns of Material,  SLoc, TrackingNo….
•	The amount spent in the Year 2019 (25836725216.86011)  is much higher than the amount spent on other year’s.
•	The year 2014(6305.9) has the least amount spent compared to other year’s.
•	The Material Group “2003” has spent the highest amount(670626233.3900012)  among all the other material groups.
•	The SLoc “9101” has the highest amount spent among all the Storage Locations.
Exploratory Data Analysis:- 
Handling NaN values:-
•	The “Material” column has “3091” missing values. As that is less than the 2% of the total data we can delete the rows which has “NaN” in “Material” column.
•	The column “Tracking Number” has “139146” missing values.
As the column has very less effect on the “Net Value” we can drop the column.
•	The column “SLoc” has “ 30104“ missing values. As the SLoc is required to analyse in which region is the amount spent. And to handle the NaN in “SLoc” we can see that the data is missing at random there is no particular pattern for the missing data so we will select a random sample and replace the NaN with the sample values.


Plotting the Data relationships:-
•	From the plot between the year and SLoc we can say that the spend is low at the beginning and for the year 2018, 2019 it increased gradually. 
 
•	The month’s 5,6,7,8 has least number of orders and net value compared to other months.
 
 
•	There are SLoc which have higher Net Value compared to other locations.
 


•	The year 2018, 2019 are having more number of orders and more Net Value than any other years.
 
•	The Month 1, 2, 3, 4, 10, 11, 12 are having higher Net Value that other month.
 
Selecting the Features suitable for building Model:
•	For building the model we are selecting “Net Value”, “PO Quantity”, “Changed on”, “Material” because as we are doing analysis on amount spend it is required to know the total value, total quantity, frequency of orders, and the product ordered.
Build a Sample Model:
•	Here we are choosing K-Prototype clustering algorithm as we are having both Numerical and Categorical data.
Finding the best suitable number of clusters:
•	We use ”Elbow” method to find the best possible number of clusters.
 
These are the cost values from different clusters  5.24356103280875e+17, 8.287356538281248e+16,
 6.645483217782765e+16,  6.192710366828393e+16,
 3.7315769900769496e+16,  3.5203416967313536e+16.
  Analyse the clusters:
•	The clusters are formed around the following centroids.
 
•	Cluster – 0:
Net Value : 19Lakhs – 63Lakhs
 
Material v/s Net Value :
 
The materials 7101334, 920450, 920000, 7101335, 7101336 are the costly materials
Major Producers :
 
The producers 9402, 9500, 9230, 9250, 9230 are the major producers.
Companies that are placing major orders:
 
The companies 9000, 7860 are placing most of the orders.
SLoc v/s PO Quantity: 
 
The locations F001, F002, F003, F007, CGEN, RMG2 are placing most of the orders.

•	Cluster – 1:
Net Value : 64Lakhs to 1.72crore
 
Material v/s Net Value:
 
The material 920000, 7101335, 7101336, 7101334, 7100109 are the costly materials
Major Producers:
 
The major producers are 1118, 1115, 1111, 13322, 1331, 1223, 1119, 1222, 1132
Companies that place most of the orders:
 
The companies 7860 and 9000 are placing most of the orders.
SLoc v/s PO Quatity:
 
The SLoc CGEN, 9101, 9102, 9502, 9106 are placing most orders.
Material v/s Quantity:
 
The material 7100109, 7100110, 7100111, 7101336, 7101335, 7101334…are the materials that are mostly bought.
•	Cluster – 2:
Net Value : 3Lakhs to 19Lakhs
 


Material v/s Net Value:
 
The materials 910017, 910000, 7101329, 7101328, 7101327 are costly
Plnt v/s PO Quantity:
 
The producers 9401, 1110… are the major producers.
CoCd v/s PO Quantity:
 
The company 7860, 9000 are placing the most of the orders.
SLoc v/s PO Quantity:
 
The SLoc 9502, 9404, F002, F001, T001  most of the orders are from these locations.
Material v/s PO Quantity:
 
The material 910017, 7101329, 7101328, 7101914, 910868 are the most bought items
•	Cluster – 3:
Net Value : 1.75Crores to 21.20Crores

Material v/s Net Value:
 
The materials 910017, 910000, 7101329, 7101328, 7101327….are costly
Major Producers:
 
1128, 1222, 1331, 1332, 1336…..are the major producers.
CoCd v/s PO Quantity:
 
The companies 7860, 9000 are placing the most of the orders.
SLoc v/s PO Quantity:;
 
The SLoc 9102, 9502, 9101, 9106, CGEN… are the locations that are placing most of the orders.
Material v/s PO Quantity:
 
The material 7100110, 7100109, 7100107, 7101336, 7100111….. are the most bought materials.


CONCLUSION: 
	From the above analysis we can see that most of the companies that are placing the order  and the major producers that are able to meet the demand. From that relationship we can form strategies to reduce the cost like placing most of the orders from small producers for low cost.
