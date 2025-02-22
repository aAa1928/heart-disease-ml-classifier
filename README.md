# heart-disease-ml-classifier

A PyTorch model designed to predict the risk of heart disease based on a combination of symptoms, lifestyle factors, and medical history from 70,000+ data samples.
The model achieves approximately 99.27% accuracy on test data.

[Download the dataset here](heart_disease_classifier_model.pth)

[Kaggle Dataset link](https://www.kaggle.com/datasets/mahatiratusher/heart-disease-risk-prediction-dataset)

## Overview

This project uses PyTorch to build a neural network classifier for heart disease risk prediction. The model analyzes several medical predictor variables to determine if a patient is at risk of heart disease.

## Dataset

The dataset contains medical predictor variables from the heart_disease_risk_dataset_earlymed.csv file.

It contains 18 medical predictors of heart disease:

1. Chest Pain: Presence of chest pain (Yes/No)
2. Shortness of Breath: Difficulty breathing (Yes/No)
3. Fatigue: Feeling of tiredness (Yes/No)
4. Palpitations: Irregular heartbeat sensations (Yes/No)
5. Dizziness: Feeling lightheaded (Yes/No)
6. Swelling: Edema in extremities (Yes/No)
7. Pain Arms Jaw Back: Pain radiating to arms/jaw/back (Yes/No)
8. Cold Sweats Nausea: Presence of cold sweats or nausea (Yes/No)
9. High BP: High blood pressure diagnosis (Yes/No)
10. High Cholesterol: High cholesterol diagnosis (Yes/No)
11. Diabetes: Presence of diabetes (Yes/No)
12. Smoking: Current smoking status (Yes/No)
13. Obesity: Obesity status (Yes/No)
14. Sedentary Lifestyle: Physical inactivity (Yes/No)
15. Family History: Family history of heart disease (Yes/No)
16. Chronic Stress: Ongoing stress condition (Yes/No)
17. Gender: Patient's gender (Male/Female)
18. Age: Age of patient in years

Output variable:

- Risk: Risk of Heart Disease (low/high)

## Requirements

- Python 3.8+
- PyTorch
- pandas
- scikit-learn
- matplotlib

## Usage

1. Clone the repository
2. Create a virtual environment `py -m venv .venv` and activate it `.venv/Scripts/activate`
3. Install dependencies: `pip install -r requirements.txt`
4. Run the model: `python main.py`

## Model Architecture

- Input layer: 18 features
- Hidden layer 1: 64 neurons with ReLU activation
- Hidden layer 2: 28 neurons with ReLU activation
- Output layer: 2 neurons (Binary classification)
- Optimization: Adam optimizer with learning rate 0.005
- Loss function: Cross Entropy Loss

## Results

The model is trained for 1000 epochs and the training progress is visualized through a loss plot that is automatically generated and saved as 'loss_plot.png'.
The model achieves approximately 99.27% accuracy on the test set, with results being reproducible using a fixed random seed (392).

## Model Persistence

The trained model is saved to 'heart_disease_classifier_model.pth' for later use.

## License

[MIT License](LICENSE)
