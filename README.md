# **HEALTH CARE PREMIUM AMOUNT PREDICTION**

This project is a machine learning-based web application designed to predict healthcare insurance premium amounts. It uses a streamlined end-to-end workflow, including data preparation, model building, evaluation, and deployment with Streamlit.

## **FEATURES**

### ->**Data Preparation**

Cleaned and transformed raw data for model training.

Engineered relevant features for accurate premium predictions.

### ->**Model Development**

Developed and trained machine learning models for different age groups:

model_young: Predicts premiums for younger individuals (18-25 age group).

model_rest: Predicts premiums for all other age groups.

Applied scaling for numerical features for better model performance.

### ->**Web Application**

Deployed a user-friendly interface using Streamlit for real-time predictions.

## **Why Two Models?**

In our analysis, we observed a high error margin when trying to predict healthcare premium amounts for all age groups using a single model. To improve accuracy, we decided to segment the data into two groups:

18-25 Age Group: A separate model (model_young) was trained for this group to address unique factors affecting premium predictions for younger individuals.

Rest of the Age Groups: A second model (model_rest) was trained for all other age groups to account for their different patterns and influences on premium amounts.

This segmentation allowed us to:

Reduce the overall error margin by tailoring predictions to distinct age-based characteristics.

Ensure better performance and accuracy for each group.

## **Project Workflow**

->Data Processing

Data cleaning, handling missing values, and scaling features using Scaler_young and Scaler_rest.

->Model Training

Trained separate models for different user segments (model_young and model_rest).

Exported models as artifacts for deployment.

->Deployment

Built and deployed the Streamlit app for users to input data and receive predictions.

## **Project Structure**

.venv/: Virtual environment containing all dependencies.

artifacts/: Folder containing the trained models and scalers:

model_young: Model for predicting premiums for younger users.

Scaler_young: Scaler for normalizing features for young user data.

model_rest: Model for predicting premiums for other users.

Scaler_rest: Scaler for normalizing features for other user data.

main.py: Streamlit application file for the web interface.

prediction_helper.py: Helper functions to load models and make predictions.

requirements.txt: File listing all dependencies for the project.

## **Prerequisites**

Before running the project, ensure you have the following installed:

Python 3.x

Required libraries: streamlit, pandas, numpy, scikit-learn, joblib, and others listed in requirements.txt.

## **Installing Dependencies**

Clone the repository:

git clone https://github.com/PRAMEELA-REDDDY/ML_Health_Premium_Prediction.git
cd ML_Health_Premium_Prediction

Install dependencies:

pip install -r requirements.txt

Activate the virtual environment (if used):

source .venv/bin/activate  # For Linux/Mac
.venv\Scripts\activate     # For Windows

## **Running the Project**

Start the Streamlit App:Navigate to the project folder and run:

streamlit run main.py

Access the Application:Open the browser and visit the URL displayed (e.g., http://localhost:8501).

## **Future Enhancements**

Improve the accuracy of the prediction models by experimenting with advanced algorithms.

Add features to the web app, such as:

Storing user predictions for analytics.

Generating premium cost reports for different demographic groups.
