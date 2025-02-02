# Automated CTG-analysis

## Repository Link

[https://github.com/marvinschuett/Automated-CTG-analysis](https://github.com/marvinschuett/Automated-CTG-analysis)

## Description

Cardiotocography (CTG) is a standard technique used to monitor the fetal heartbeat and uterine contractions during pregnancy and labour.

### Problem: 
CTG-analysis remains partly subjective and has to be done ad hoc.

### Aim:
Objectify the analysis of CTG-data through ML-techniques using data from [2126 CTGs](https://archive.ics.uci.edu/dataset/193/cardiotocography).

### Task Type

Classification of CTG datainto Normal, Suspect and Pathologic (N,S,P).

### Results Summary

- **Best Model:** Neural Network
- **Evaluation Metric:** F1-Score
- **Result:** F1-score of 0.947

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/exploratory_data_analysis.ipynb)**
3. **[Baseline Model](2_BaselineModel/baseline_model.ipynb)**
4. **[Model Definition and Evaluation](3_Model/model_definition_evaluation.ipynb)**
5. **[Presentation](4_Presentation/README.md)**

## Cover Image

![Project Cover Image](CoverImage/CTG_image.jpg)
