# README for Market Basket Analysis

**Summary**

I used the Apriori algorithm from mlxtend to determine the most popular combinations of items that customers would purchase together. The dataset showed each item in a customers order, which then needed to be converted into a True or False format for further processing. I produced a heatmap to further illustrate this.

**Key terminology**

Apriori algorithm- a divide and conquer style algorithm which finds patterns in datasets by identifying frequent itemsets to create rules

Support- ratio of the number of times an item occurs in the transactions to the total number of transactions

Confidence- probability of items/itemsets occurring in an itemset together

Antecedent- First item in itemset (IF rule)

Consequent- Corresponding second (or third etc.) item in itemset (THEN rule)

Lift- ratio of confidence to antecedent support

**Business case**

Modern day computing allows for large organizations to be able to collect and store more data than ever before. They can use their findings to target more customers and increase sales. This is more efficient and logical that having marketers using their prior knowledge and intuition when developing marketing strategies

**Methodology**

1) Import dataset and create temporary subset without Item(s) column to count frequency of each item
2) Plot top 20 most frequently purchased products
3) Sum the number of non-null values for each row and plot histogram
4) Drop Item(s) column as not needed anymore, then iterate through every row adding all non-null values to the transactions list
5) Convert transactions list into a data frame, which is now able to be transaction encoded
6) Create frequent items dataframe with min support of 0.03 to show the itemsets with the highest support
7) Create rules dataframe with antecedent-consequent pairs, showing the support, lift and confidence
8) Plot scatter plots, for showing the various relationships between support, lift and confidence
9) Further analyse scatter plots by plotting antecedent support vs consequent support
10) Identify the item with the highest support, and retriev every antecedent-consequent pair where milk is the antecedent
11) Sum the support, lift, confidence and zhang metric to find out the most significant matches
12) Make a copy of the rules dataframe and remove the brackets
13) Plot a heatmap of item support

**Skills demonstrated**

Data preprocessing, data manipulation/visualisation, mathematical/statistical analysis, pandas, matplotlib, seaborn, mlxtend, apriori algorithm

**Results**

0.03 support was used so that the visualisations were clearer to understand i.e. it excludes consequents with more than 1 item. The top 10 sold items are whole milk, other vegetables, rolls/buns, soda, yogurt, root vegetables, tropical fruit, bottled water, sausage, and citrus fruit. With whole milk having the highest support, the top consequent for it was other vegetables (0.07) support. Whole milk also has the most connections with other products. 

**Further improvements**

Use a dataset which includes information such as order numbers, customer data, geographical data etc. More preprocessing would be required here. Add more complex visualisations such as a line map connecting two products, and noting what the support is

