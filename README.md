# Movie Success Prediction - ML & Deep Learning Project

## Project Overview

This project predicts whether a movie is financially successful or not using the TMDB 5000 Movies dataset.

The project is a binary classification problem. A movie is labelled as successful if its revenue is greater than 1.5 times its budget.

The goal of this project was to understand the full machine learning workflow and compare a traditional machine learning model with simple deep learning models.

## Dataset

Dataset used:

TMDB 5000 Movie Dataset from Kaggle

File used:

- `tmdb_5000_movies.csv`

The credits dataset was not used in this simplified version.

Note: The dataset file is not included in this repository. To run the notebook, download the dataset from Kaggle and place `tmdb_5000_movies.csv` in the `data/` folder or upload it directly in Google Colab.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- Google Colab / Jupyter Notebook

## Problem Type

Binary classification.

Target variable:

- `success`

Rule:

- `success = 1` if `revenue > 1.5 * budget`
- `success = 0` otherwise

## Features Used

Input features:

- `budget`
- `popularity`
- `runtime`
- `vote_average`
- `vote_count`

## Avoiding Data Leakage

Revenue was used to create the target variable `success`.

Because of this, revenue was not used as an input feature. Using revenue as an input would cause data leakage because the model would indirectly receive the answer.

## Models Used

Three models were trained and compared:

1. Decision Tree Classifier
2. Baseline MLP Neural Network
3. Deep MLP Neural Network

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report

## Results

The models achieved similar performance:

- Decision Tree Accuracy: 75.23%
- Baseline MLP Accuracy: 76.16%
- Deep MLP Accuracy: 76.01%

The Baseline MLP performed slightly best, but the difference between the models was small.

## Key Learning

The main learning from this project was understanding the full machine learning workflow:

- Loading data
- Cleaning data
- Creating a target variable
- Avoiding data leakage
- Train-test split
- Scaling features for neural networks
- Training machine learning and deep learning models
- Evaluating and comparing results

This project also showed that deep learning is not always automatically better for tabular data.

## Limitations

- The success rule is simplified.
- Real movie success depends on more factors such as marketing, genre, release date, cast, director, and competition.
- Only numerical features were used.
- The credits dataset was not used.
- The project is academic and not a production-ready prediction system.

## Future Improvements

Possible future improvements:

- Add genres, release date, cast, director, and production company features.
- Use the credits dataset.
- Try more feature engineering.
- Add cross-validation.
- Test more models.
- Deploy the model as a simple web app or API.

## How to Run

1. Clone this repository.

```bash
git clone https://github.com/syxd24/movie-success-ml-dl.git
