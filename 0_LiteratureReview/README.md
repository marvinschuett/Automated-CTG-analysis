# Description of the dataset
"This dataset consists of measurements of fetal heart rate (FHR) and uterine contraction (UC) features on cardiotocograms classified by expert obstetricians.
2126 fetal cardiotocograms (CTGs) were automatically processed and the respective diagnostic features measured. The CTGs were also classified by three expert obstetricians and a consensus classification label assigned to each of them. Classification was both with respect to a morphologic pattern (A, B, C. ...) and to a fetal state (N, S, P). Therefore the dataset can be used either for 10-class or 3-class experiments." [Source: UCI archive](https://archive.ics.uci.edu/dataset/193/cardiotocography).

# Additional information
The dataset is freely availabe from the [UCI archive](https://archive.ics.uci.edu/dataset/193/cardiotocography) and has been used quite extensively for learning purposes within the ML field (several Kaggle-competitions, e.g. [here](https://www.kaggle.com/datasets/propanon/uci-cardiotocography) and [here](https://www.kaggle.com/datasets/akshat0007/fetalhr/discussion)). It is also subject of an article on ["medium"](https://phuongdelrosario.medium.com/uci-cardiotocography-data-set-fetal-states-classification-part-1-data-summary-and-eda-e0cec8a61eff) as well as of several publications.

Below we summarize the main findings of three of the most recent publications.



# Literature Review

Approaches or solutions that have been tried before on similar projects.


**Summary of Each Work**:

- **Source 1**: [Cardiotocography Data Analysis for Fetal Health Classification Using Machine Learning Models]

  - **[Link](https://ieeexplore.ieee.org/abstract/document/10431783)**
  - **Objective**: From the abstract: "Development of efficient fetal health classification models [...] for optimizing medical resources and saving time. [...] application of machine learning (ML) techniques [...] to explore, develop, and analyze ML models capable of accurately classifying fetal health based on CTG data.
  - **Methods**: From the abstract: "Various ML models, including Random Forests, Logistic Regression, Decision Trees, Support Vector Classifiers, Voting Classes, and K-Nearest Neighbors, are deployed on the data set. The analysis involves rigorous training and testing of these models to assess their efficacy in classifying fetal health." .
  - **Outcomes**: From the abstract" The study yields promising outcomes, with the implemented ML models achieving a notable accuracy level of 93%, surpassing previous methods."
  - **Relation to the Project**: The findings hint towards promising ML models that can be used as baseline model for this analysis. This project seeks to find improvements in accuracy levels by alternating the ML model specification.

- **Source 2**: [Artificial intelligence-driven predictive framework for early detection of still birth]

  - **[Link](https://www.sciencedirect.com/science/article/pii/S2472630324000852#sec3)**
  - **Objective**: The study aims to develop a predictive framework using the TabPFN model to classify stillbirth and live birth outcomes efficiently and accurately based on CTG data, improving early detection and resource optimization in prenatal care. Unlike Study 1, which clearly uses the three CTG classes (normal, suspicious, pathological) for fetal health classification, this study focuses on predicting stillbirth.
  - **Methods**: Using the same CTG dataset as Study 1, which includes 2126 records categorized as normal, suspicious, or pathological, various machine learning models were trained and tested. The TabPFN model was evaluated alongside methods like Random Forest and Gradient Boosting using metrics such as accuracy, precision, recall, F1-score, MCC, and AUC. K-fold cross-validation ensured robustness and reliability. Additionally, the study provides a literature review, summarizing previous methods and models, which can serve as a useful resource for further research.
  - **Outcomes**: The TabPFN model outperformed all other approaches, achieving an accuracy of 97.91% and high scores across all evaluation metrics. Its computational efficiency allows for rapid predictions, making it suitable for real-time applications.
  - **Relation to the Project**: This work provides a baseline model for fetal health classification, combining accuracy and efficiency. The included literature overview offers references to more studies in this field.

- **Source 3**: [Cardiotocography Data Set - Fetal state classification — Part 1: Data Summary and EDA]

  - **[Link](https://phuongdelrosario.medium.com/uci-cardiotocography-data-set-fetal-states-classification-part-1-data-summary-and-eda-e0cec8a61eff)**
  - **Objective**: The article provides a comprehensive summary and exploratory data analysis (EDA) of the UCI Cardiotocography (CTG) dataset. It aims to prepare the data for subsequent machine learning applications.
  - **Methods**: The CTG dataset comprises 2,126 observations with 40 attributes, including fetal heart rate and uterine contraction features. The author performs data cleaning by removing 18 irrelevant columns and standardizing the remaining 21 numerical features. An analysis of class distribution reveals an imbalance among the three classes: normal (N), suspect (S), and pathological (P). Correlation analysis identifies strong relationships between certain features. Histograms and Kolmogorov-Smirnov tests are utilized to assess the discriminative power of selected features across different classes.
  - **Outcomes**: The EDA uncovers significant class imbalance, with the normal class comprising the majority of observations. High correlations between specific features suggest potential multicollinearity, which may influence model performance. The analysis also identifies features with strong discriminative power, providing a foundation for feature selection in future modeling efforts.
  - **Relation to the Project**: This article offers valuable insights into the CTG dataset's structure and characteristics, serving as a crucial step in developing predictive models for fetal state classification. The findings from the EDA inform feature selection and address challenges such as class imbalance, which are essential considerations for building robust machine learning models.
 


### More Studies (extracted from Study 2)

#### [Rayhana T, et al. (2021)](https://www.researchgate.net/profile/Sabbir-Chowdhury/publication/358157030_Automatic_detection_of_fetal_health_status_from_cardiotocography_data_using_machine_learning_algorithms/links/61fbd33911a1090a79ce70e5/Automatic-detection-of-fetal-health-status-from-cardiotocography-data-using-machine-learning-algorithms.pdf)

- Models: LR, RF, SVM, k-NN, XGBoost
- Performance: 96.7% XGB

#### [Abiyev R, et al. (2023)](http://dx.doi.org/10.3390/diagnostics13101690)

- Models: T2-FNN, LR, GNB, SVC, RBF SVC, ANN, CART, RF, CatBoost, RNN
- Performance: 96.6% T2-FNN (63 rules)

#### [Li J & Liu X (2021)](https://ieeexplore.ieee.org/abstract/document/9389902)

- Models: GBC, ADA, CatBoost, Light GBM, Extreme GBC, Cascade Forest, ETC, DT, LR, k-NN, LDA, ADA, Stacker Model, Blender Model
- Performance: 95.9% Blender Model

#### [Rahmayanti N, et al. (2022)](https://www.sciencedirect.com/science/article/pii/S1877050921023541)

- Models: XGB, SVM, KNN, LGBM, RF, ANN, LSTM
- Performance: 99% LGBM (after removing outliers)

#### [Shruthi K & Poornima AS (2023)](https://ijisae.org/index.php/IJISAE/article/view/2849)

- Models: RF, GA
- Performance: 96.62% RF

#### [Muhammad Hussain N, et al. (2022)](https://doi.org/10.3390/s22145103)

- Models: RNN, RF, GoogleNet, DenseNet, NiftyNet, AlexNet, SVM-AlexNet
- Performance: 99.72% SVM-AlexNet

#### [Islam MM, et al. (2022)](https://www.researchgate.net/publication/371481096_Diagnosis_and_Classification_of_Fetal_Health_Based_on_CTG_Data_Using_Machine_Learning_Techniques)

- Models: SVM, GBC, RF, ADA, LR, k-NN, DTC
- Performance: 95% GBC

#### [Alam MT, et al. (2022)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9050321/)

- Models: RF, LR, DT, SVC, VC, k-NN
- Performance: 97.51% RF

#### [Kuzu A & Santur Y (2023)](https://doi.org/10.3390/diagnostics13152471)

- Models: RF, LR, GB, XGB
- Performance: 99.5%

#### [Piri J, et al. (2021)](https://www.researchgate.net/publication/355029967_Multi-objective_Ant_Lion_Optimization_Based_Feature_Retrieval_Methodology_for_Investigation_of_Fetal_Wellbeing)

- Models: RF, SVM, DT, k-NN
- Performance: 95% RF with smote

#### [Bhowmik P, et al. (2021)](https://www.researchgate.net/publication/355022211_Cardiotocography_Data_Analysis_to_Predict_Fetal_Health_Risks_with_Tree-Based_Ensemble_Learning)

- Models: Stacking EL, RF, DT, ETC, Deep forest
- Performance: 96.05% Stacking EL
