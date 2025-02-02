# Model Definition and Evaluation

**[Notebook](model_definition_evaluation.ipynb)**

## Model Selection
After comparing baseline models, we determined that a model capable of handling non-linearity was necessary. Based on previous studies (Alzakari et al., 2024; Amin et al., 2019; Ogasawara et al., 2021), neural networks emerged as a promising approach for CTG data analysis.

## Feature Engineering
We applied **SelectKBest** for feature selection and identified the top **8** features, which were subsequently used in model training.

## Hyperparameter Tuning
We utilized **Random Search** with **Keras Tuner** to identify the optimal hyperparameters for our neural network model.

## Evaluation Metrics
### Primary Metrics
- **Recall:** Ensures no pathological cases are missed (focus on sensitivity).
- **F1-Score:** Balances precision and recall for each class.

### Secondary Metrics
- **Precision:** Evaluates the proportion of correct positive predictions to avoid excessive false alarms.
- **Confusion Matrix:** Analyzes detailed classification errors.
- **Accuracy:** Provides an overall performance snapshot but is less reliable for imbalanced datasets.

## Model Comparison Summary
### Without Oversampling 
| Class            | Precision | Recall   | F1-Score |
| ---------------- | --------- | -------- | -------- |
| **Normal**       | 0.978528  | 0.957958 | 0.968134 |
| **Suspect**      | 0.791667  | 0.890625 | 0.838235 |
| **Pathologic**   | 0.964286  | 0.931034 | 0.947368 |
| **Macro Avg**    | 0.911493  | 0.926539 | 0.917912 |
| **Weighted Avg** | 0.949485  | 0.946009 | 0.947205 |


## Detailed Comparison: Neural Network vs Baseline Models

| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| **Neural Network (Selected Features)** | 0.946    | 0.949     | 0.946  | 0.947    |
| **SMOTE Neural Network** | 0.934 | 0.944     | 0.934  | 0.937    |
| **Logistic Regression** | 0.845 | 0.896     | 0.845  | 0.859    |
| **SVM**             | 0.876    | 0.916     | 0.876  | 0.885    |


### With SMOTE (Oversampling)
| Class            | Precision | Recall   | F1-Score |
| ---------------- | --------- | -------- | -------- |
| **Normal**       | 0.990446  | 0.933934 | 0.961360 |
| **Suspect**      | 0.737500  | 0.921875 | 0.819444 |
| **Pathologic**   | 0.875000  | 0.965517 | 0.918033 |
| **Macro Avg**    | 0.867649  | 0.940442 | 0.899612 |
| **Weighted Avg** | 0.944586  | 0.934272 | 0.937090 |

### Key Observations
- The **F1-Score** of the Neural Network (0.947) outperforms both **Logistic Regression (0.859)** and **SVM (0.885)**, highlighting the benefit of a deep learning model.
- **SMOTE** significantly improved recall for the **Suspect** class (0.921 vs. 0.890), bringing it to the **same level as SVM**.  A major advantage of **SMOTE** was that it ensured **no normal cases were misclassified as pathological**.

## Conclusion
The **Neural Network** model achieved the best overall performance, particularly excelling in **Recall and F1-Score**, which are crucial for detecting pathological cases. Compared to the **baseline models** (Logistic Regression and SVM), the Neural Network provides significant improvements. 
Additionally, **SMOTE** proved to be beneficial in enhancing recall for the **Suspect** class, bringing it to the same level as **SVM**, while ensuring that no **normal cases** were misclassified as **pathological**. 

