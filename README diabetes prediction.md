# README for diabetes prediction

**Summary**

I predicted whether a patient was diabetic or not using different machine learning classification algorithms in Python. The target was to succesfully predict the results with an 80% accuracy, which I thought would be strong given the samll size of the dataset. The models were trained on previous patient data which included information such as the number of pregnancies, their glucose concentration and blood pressure. 

**Business Problem**

The number of people living with diabetes is expected to double by 2050.  Using machine learning models can mean that extremely large datasets can be analysed to capture trends and make future predictions, especially as the demand for healthcare increases.

**Methodology**

The key steps to solve the problem were:

1) Importing the dataset and noting first impressions
2) Replacing all zero values with the median of each class. Zero values will have occured due the patient not being tested on that feature
3) Splitting the dataset into testing and training data
4) Calculate accuracy using Naive-Bayes classifer, Support Vector Machine, K Nearest Neighbors and Decision Tree classifier
5) Plot a decision tree and confusion matrix to analyse results

**Skills**

Data preprocessing, data manipulation/visualisation, mathematical/statistical analysis, pandas, matplotlib, sklearn, seaborn

**Results**

93 of 116 total predictions were predicted correctly

In conclusion, an accuracy of 80% is solid for a dataset of just 768 records. Because of this size, I decided to use a smaller portion of 15% training data compared to the standard 20%, and also had to cap the max depth of the decision tree to 3. A larger dataset can withstand being trained on a full decison tree with pure leaf nodes, though here, it is prone to overfitting. The decision tree was the best performing model due to its simplicity of analysing the dataset. As it is a small dataset, there aren't too many 'questions' that need to be asked of the data, especially as I have limited the depth.

**Further Improvements**

Use more complex machine learning models and produce more detailed visualisations
