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

This project aims to create a classification model that aims to classify the resumes that are generated with ChatGpt with sample names that are generated from the firstnames and surnames datasets . In this project we utilized the multiple models that are available and one custom built three layered model that we built and BERT transformer model for better complex classification. Then performed the trustworthiness of our system in the aspects of fairness (Bias) and Robustness for the models.

---

## Contributions

1. **Uday Kocherla**   - Creating the models that are used for classification like Bert, XGBoost, MLP classifier and Random Forest. Has done CAT test for the Fairness evaluation
2. **Tharun Kumar Gadige**  - Sample name generation and preprocessing the data for the models that used for classifying the data. Has performed the robustness test on the classification models
3. **Satishkumar Mannam**   - Generating resumes from the generated sample names dataset and labeling them as biased and unbaised. Has done the statistical test to measure the Bias of the resumes from the US Labor force statistics.

---

## Key Features
- BERT Transformer that is used for text based classification
- Encoding the categorical data using the one hot encoding and vectorization using Tf-Idf Vectorization
- used multiple classifiers using the Random Forest, MLP classifier and XGBoost
- Custom built three-layered classification model that uses Relu activation
- CAT Analysis of the AI generated resumes to measure the stereotypical bias of the dataset for the classification model
- Test the robustness of the classification models

## Technologies Used

- ML classifiers : Random Forest, MLP classifier, XGBoost and Custom Built Three layered model
- OpenAI GPT 3.5 Turbo
- NLP Classifiers : BERT transformer
- Encoding: One Hot Encoding and Tf-Idf Vectorization.
- Datasets: Harvard Dataverse (First name demographic distributions) ,FiveThirtyEight (Most common surname data),US Labor Force Statistics.
- Performance Evaluation: Accuracy, F1-score, precision, recall, support.
- Training Environment: Google Colab


  ## **Project Structure**
```
/Bias-Classification
├── Bias Classification Models.ipynb   #  Notebook with bias code implementation
├── Bias_Classification_Models_Robustness.ipynb #Notebook for Robutness Test
├── requirements.txt           # Dependencies for running the project
├── README.md                  # Project documentation
└── Datasets                    # All the datasets that are used in the project
└── SampleNamesGeneration.ipynb         # Notebook with sample name generation code implementation
└── CAT
    └── main.py                             # python main file for CAT
    └── cat_prompts.py                       # All the 16 prompts for CAT Test
    └── run_cat.py                          # CAT program to establish the connection to OpenAI 
    └── evaluate_cat.py                     # evalution metric file for CAT test
    └── debug.py                            # Debug file for CAT


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
jupyter notebook Bias_Classification_Models_Robustness.ipynb
jupyter notebook  SampleNamesGeneration.ipynb
```

## Results

### Classification Results
| Model | Accuracy | Precision | Recall | F1 Score |
|----------|----------|----------|----------|----------|
|  Random Forest  | 80%  | 80%  | 77% | 78%  |
| XGBoost | 76%  | 75%  | 74%  | 74%  |
|  MLP   | 78% | 77% | 76%  | 76% |
|  Custom Model   | 82% | 81% | 81%  | 81% |
|  BERT   | 94% | 94% | 92%  | 93% |


### CAT Results
| Model | TEMP | NSS | SS | ICAT |
|----------|----------|----------|----------|----------|
|    | 0  | 25  | 75 | 12.5  |
| GPT 3.5 Turbo  | 1  | 12.5  | 87.5  | 3.12  |
|   | 0.7 | 25 | 68.75  | 15.62 |

### Robustness Results
| Model | Accuracy | Precision | Recall | F1 Score |
|----------|----------|----------|----------|----------|
|  Random Forest  | 76%  | 76%  | 72% | 73%  |
| XGBoost | 67%  | 66%  | 65%  | 66%  |
|  MLP   | 71% | 71% | 69%  | 69% |
|  Custom Model   | 73% | 73% | 71%  | 72% |
|  BERT   | 81% | 83% | 78%  | 79% |


Note: you need API of Wandb.ai to use BERT
---
## **References**
- Derous E, Ryan AM. (2019) When your resume is (not) turning you down: Modelling ethnic bias in resume screening. Hum Resour Manag J. 
- Nadeem et al.. (2021). StereoSet: Measuring stereotypical bias in pretrained language models.
- Chatterjee, Madhura & Ahmed, Md & Dadure, Pankaj & Pakray, Dr. Partha. (2022). Inclination of NLP Applications Towards Stereotypical and Gender Biased Results. 


---
