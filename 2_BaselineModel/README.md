# Baseline Model

**[Notebook](baseline_model.ipynb)**

As baseline models, we chose a Multionomal Logistic Regression as well as a Support Vector Machine (SVM) due to their simplicity and effectiveness. We decide to use class weights to account for the identified class imbalances.

### Logistic Regression: 
A model that provides interpretability through feature coefficients. It serves as a benchmark for evaluating more complex models.

### Support Vector Machine (SVM):
SVM complements Logistic Regression by capturing non-linear relationships, offering a comparison between linear and non-linear approaches.

### Metrics to Evaluate the Model
Initially, we investigate a multitude of metrics to better understand the underlying data dynamics:

#### Primary Metrics
F1-Score: Balances Precision and Recall for each class.
Recall: Ensure no pathological cases are missed (focus on sensitivity).
#### Secondary Metrics
Confusion Matrix: Analyze detailed classification errors.
Accuracy: Provides an overall performance snapshot but is less reliable for imbalanced datasets.
Precision: Evaluate the proportion of correct positive predictions to avoid excessive false alarms.

### Main results for the baseline models:
- The overall accuracy for these rather simple models is already quite satisfactory (LR: 0.85, SVM: 0.88).
- However, having a closer look at other metrics, the results show that, e.g., precision for the less frequent classes "Suspect" and "Pathologic" is significantly lower than for the dominiating class "Normal" (0.55 and 0.60 vs. 0.99 in the LR). This indicates that even using class weights is not sufficient to account for the clear class imbalances in these simple models.
  

