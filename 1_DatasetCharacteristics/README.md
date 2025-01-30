# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**


The dataset consists of 2126 CTG observations with 21 features. There are no missing values in the dataset.

The target variable classifies the observation into three distinct groups: There are 1655 normal, 295 suspect and 176 pathological entries.
This indicates a clear class imbalance.

We use two different feature selection techniques to identify the main features (SelectKBest and Random Forest Feature Importance). They results have a high degree of overlap lending support to our interpretion of theses features as the most important ones. The selection made by SelectKBest will be used in the following analysis.

The distribution of the selected features is highly skewed in several cases. Accordingly, outlier detection measures that build on the distribution to detect outliersd (IQR, Z-score) claim some observations to be outlying. Since in our case, the "outlying observations" mostly coincide with the "Pathologic" and "Suspect" cases we would like to discriminate on, we decide to keep these observations. 



