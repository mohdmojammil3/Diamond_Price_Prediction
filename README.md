# Diamond Price Prediction

This project aims to predict diamond prices based on several features using various regression models such as Linear Regression, Lasso, Ridge, and ElasticNet. The model that provided the best results is Lasso.


# Table of Contents

* Installation
* Project Structure
* Usage
* Model Training
* Prediction
* References
* License

# Installation

Clone the repository:

git clone https://github.com/mohdmojammil3/Diamond-Price-Prediction.git
cd Diamond-Price-Prediction

Create a virtual environment and activate it:

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

Install the required packages:

pip install -r requirements.txt

# Project Structure

The project follows the following structure:

Diamond-Price-Prediction/
│
├── .ebextensions/
│   └── python.config        # Configuration file for Elastic Beanstalk deployment
│
├── data/
│   ├── train_data.csv        # Raw training data
│   └── test_data.csv         # Raw test data
│
├── artifacts/
│   ├── preprocessor.pkl      # Serialized data preprocessor
│   └── model.pkl             # Serialized best performing model (Lasso)
│
├── notebooks/
│   ├── EDA.ipynb             # Exploratory Data Analysis notebook
│   ├── Model.ipynb           # Model training and evaluation notebook
│   └── research.ipynb        # Research and experimentation notebook
│
├── src/
│   ├── data_preprocessing.py # Data preprocessing scripts
│   ├── model_trainer.py      # Model training script
│   └── data_ingestion.py     # Data ingestion script
│
├── .gitignore                # Git ignore file
├── app.py                    # Flask application script
├── requirements.txt          # List of Python dependencies
└── README.md                 # This file

# Explanation of .ebextensions/python.config

.ebextensions/python.config: This file contains configuration settings for Elastic Beanstalk to deploy a Python application. It specifies details such as environment variables, packages to install, or commands to run during deployment.

# Usage

To run the application:
python app.py

Open your web browser and go to http://127.0.0.1:5000/predict
or
link: 

# Model Training 

The model is trained using various regression algorithms including Linear Regression, Lasso, Ridge, and ElasticNet. The Lasso artifact showed the best performance in predicting diamond prices.

# Model Training Process:

Data Ingestion: Load and preprocess the training data.
Data Preprocessing: Handle missing values, encode categorical features, and scale numerical features.
Model Training: Train the Lasso artifact using the preprocessed training data.

# Prediction

To make predictions using the trained Lasso artifact:

* Load the preprocessor (preprocessor.pkl) and artifact (model.pkl) from their respective files.
* Preprocess the input data using the preprocessor.
* Use the artifact to predict diamond prices based on the preprocessed data.

# References

Pandas Documentation
Scikit-Learn Documentation
Flask Documentation
Elastic Beanstalk Documentation

# License

This project is licensed under the MIT License. See the LICENSE file for details.