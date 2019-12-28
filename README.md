# identifyCustomerSegments
Unsupervised Learning: Identify Customer Segments  - Principal Component Analysis and Clustering

# Project Overview
(as provided by Udacity)</br>
In this project, you will work with real-life data provided to us by our Bertelsmann partners AZ Direct and Arvato Finance 
Solution. The data here concerns a company that performs mail-order sales in Germany. Their main question of interest is to
identify facets of the population that are most likely to be purchasers of their products for a mailout campaign. Your job as
a data scientist will be to use unsupervised learning techniques to organize the general population into clusters, then use
those clusters to see which of them comprise the main user base for the company. Prior to applying the machine learning 
methods, you will also need to assess and clean the data in order to convert the data into a usable form.

N.B.: Data cannot be disclosed due to the abiding the terms and conditions from the data provider.

# Project Details
## The Data
- Udacity_AZDIAS_Subset.csv: Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
- Udacity_CUSTOMERS_Subset.csv: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
- Data_Dictionary.md: Information file about the features in the provided datasets.
- AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographic data.

### Preprocessing
The following steps were followed for data preprocessing:</br>
Each step is discussed in detail in the `Identify_Customer_Segments.ipynb` notebook.
- Converted data that matches a 'missing' or 'unknown' value code into a numpy NaN value.
- Performed an assessment of how much missing data there is in each _column_ of the dataset.
- Investigated patterns in the amount of missing data in each column.
- Remove the outlier columns from the dataset.(If the columns contained more than 20% of missing values, then those columns 
were considered to outliers. The threshold of 20% was decided arbitrarily by visualizing missing values per column)
- Assessed missing data in each _row_
- Re-Encoded Categorical Features
- Engineered Mixed-Type Features

### Feature Transformation
The following steps were followed for feature transformation:</br>
Each step is discussed in detail in the `Identify_Customer_Segments.ipynb` notebook.
- Applied Feature Scaling (used an `Imputer` and a `StandardScaler` for feature scaling)
- Performed Dimensionality Reduction using Principal Component Analysis
- Interpreted the Principal Components

### Clustering
The following steps were followed for clustering:</br>
Each step is discussed in detail in the `Identify_Customer_Segments.ipynb` notebook.
- Applied Clustering to General Population(KMeans clustering)- Value of K was decided using elbow method.
- Applied the preprocessing, feature transformation and clustering steps to the Customer data.
- Compared Customer Data to Demographics Data

### Conclusion:
Conclusions were provided for personalized/direct marketing based on the principal components and clusters. Please check end 
of the notebook `Identify_Customer_Segments.ipynb`
