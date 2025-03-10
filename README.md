# Bias-Detection-in-LLMs-for-Job-Application-Portals

## Table of Contents

1. [Introduction](#Introduction)  
2. [Contributions](#Contributions)
3. [Key Features](#Key-Features)  
4. [Technologies Used](#Technologies-Used)  
5. [Notebook Structure](#notebook-structure)
6. [Installation & Setup](#Installation&Setup)
7. [References](#References)

---

## Introduction

This project aims to create a classification model that aims to classify the resumes that are generated with ChatGpt with sample names that are generated from the firstnames and surnames datasets . In this project we utilized the multiple models that are available and one custom built three layered model that we built and BERT transformer model for better complex classification.

---

## Contributions

1. **Uday Kocherla**   - Creating the models that are used for classification like Bert, XGBoost, MLP classifier and Random Forest.
2. **Tharun Kumar Gadige**  - Sample name generation and preprocessing the data for the models that used for classifying the data.
3. **Satishkumar Mannam**   - Generating resumes from the generated sample names dataset and labeling them as biased and unbaised.

---

## Key Features
- BERT Transformer that is used for text based classification
- Encoding the categorical data using the one hot encoding and vectorization using Tf-Idf Vectorization
- used multiple classifiers using the Random Forest, MLP classifier and XGBoost
- Custom built three-layered classification model that uses Relu activation

## Technologies Used

- ML classifiers : Random Forest, MLP classifier, XGBoost and Custom Built Three layered model
- NLP Classifiers : BERT transformer
- Encoding: One Hot Encoding and Tf-Idf Vectorization.
- Datasets: Harvard Dataverse (First name demographic distributions) ,FiveThirtyEight (Most common surname data),US Labor Force Statistics.
- Performance Evaluation: Accuracy, F1-score, precision, recall, support.
- Training Environment: Google Colab

  ## **Project Structure**
```
/Bias-Classification
├── Bias Classification Models.ipynb   #  Notebook with bias code implementation
├── requirements.txt           # Dependencies for running the project
├── README.md                  # Project documentation
└── Datasets                    # All the datasets that are used in the project
└── SampleNamesGeneration.ipynb         # Notebook with sample name generation code implementation


```
## **Installation & Setup**
1. Clone the repository:

```
https://github.com/uday-kocherla/Bias-Detection-in-LLMs-for-Job-Application-Portals.git
cd Bias-Detection-in-LLMs-for-Job-Application-Portals
```

2. Install dependencies:

```
pip install -r requirements.txt
```

3. Run the Jupyter Notebook:

```
jupyter notebook Bias Classification Models.ipynb
jupyter notebook  SampleNamesGeneration.ipynb
```
---
## **References**
- Derous E, Ryan AM. (2019) When your resume is (not) turning you down: Modelling ethnic bias in resume screening. Hum Resour Manag J. 
- Nadeem et al.. (2021). StereoSet: Measuring stereotypical bias in pretrained language models.
- Chatterjee, Madhura & Ahmed, Md & Dadure, Pankaj & Pakray, Dr. Partha. (2022). Inclination of NLP Applications Towards Stereotypical and Gender Biased Results. 


---
