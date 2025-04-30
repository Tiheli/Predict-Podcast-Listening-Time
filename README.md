Podcast Listening Time Prediction

Project Description

This repository contains a machine learning pipeline for predicting podcast listening times (Listening_Time_minutes) as part of the Kaggle Playground Series S5E4 competition. The project is implemented in a Jupyter Notebook, featuring data preprocessing, advanced feature engineering, multiple model training, ensemble predictions, and comprehensive visualizations. The goal is to create an accurate and interpretable model while providing insights into the data and model behavior.
Features

Data Preprocessing: Clips numerical features and encodes categorical variables.
Data Cleaning: Removes outliers using IQR and normalizes numerical features with StandardScaler.
Feature Engineering: Includes interaction features (e.g., Length_Host_Interaction), time-based features (e.g., Is_Weekend), and group-based statistics (e.g., Genre_Mean_Length).
Model Training: Trains Linear Regression, Random Forest, XGBoost, and CatBoost models.
Hyperparameter Tuning: Optimizes XGBoost parameters using GridSearchCV.
Ensemble Predictions: Combines model outputs with a weighted average for improved accuracy.
Visualizations: Generates plots for target distribution, feature importance, predicted vs. actual values, correlation heatmap, and residuals.
Evaluation Metrics: Reports RMSE, MAE, and R² for model assessment.
Output: Produces a submission file (submission.csv) and visualization files.

Repository Structure
podcast-prediction/
│
├── notebook/
│   └── podcast_prediction_final.ipynb  # Main Jupyter Notebook
├── data/
│   ├── train.csv                       # Training dataset (not included, download from Kaggle)
│   └── test.csv                        # Test dataset (not included, download from Kaggle)
├── outputs/
│   ├── submission.csv                  # Predicted listening times
│   ├── target_distribution.png         # Target variable distribution
│   ├── feature_importance.png          # Feature importance plot
│   ├── predicted_vs_actual.png         # Predicted vs actual scatter plot
│   ├── correlation_heatmap.png         # Correlation heatmap
│   └── residuals_distribution.png      # Residuals distribution
├── README.md                           # This file
└── requirements.txt                    # Python dependencies

Installation

Clone the Repository:
git clone https://github.com/your-username/podcast-prediction.git
cd podcast-prediction


Install Dependencies:Create a virtual environment and install required packages:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

The requirements.txt includes:
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
catboost
scipy


Download Data:

Obtain train.csv and test.csv from the Kaggle Playground Series S5E4 competition.
Place them in the data/ directory.



Usage

Set Up Jupyter Notebook:Launch Jupyter Notebook:
jupyter notebook

Open notebook/podcast_prediction_final.ipynb.

Update File Paths:Modify the load_data function to point to your data files:
train = pd.read_csv("data/train.csv")
test = pd.read_csv("data/test.csv")


Run the Notebook:Execute all cells sequentially. The notebook will:

Load and preprocess data.
Clean data and engineer features.
Generate visualizations (saved in outputs/).
Tune hyperparameters and train models.
Evaluate models with RMSE, MAE, and R².
Create ensemble predictions and save submission.csv.


Check Outputs:

Visualizations: Stored in outputs/ (e.g., correlation_heatmap.png).
Submission: outputs/submission.csv for Kaggle submission.



Project Workflow

Data Loading: Loads and prepares train.csv and test.csv.
Preprocessing: Clips numerical ranges and encodes categorical features.
Data Cleaning: Removes outliers and normalizes numerical features.
Feature Engineering: Adds advanced features to capture data patterns.
Visualization: Plots data distributions, correlations, and model performance.
Hyperparameter Tuning: Optimizes XGBoost using GridSearchCV.
Model Training: Trains multiple models and compares their performance.
Ensemble: Combines predictions for better accuracy.
Evaluation: Reports multiple metrics for model assessment.
Submission: Saves predictions for competition submission.

Results

The ensemble model typically achieves a lower RMSE compared to individual models.
Visualizations reveal key features (e.g., Episode_Length_minutes) and model errors.
MAE and R² provide additional insights into prediction quality.

Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make changes and commit (git commit -m "Add your feature").
Push to your branch (git push origin feature/your-feature).
Open a Pull Request.

Please ensure your code follows PEP 8 style guidelines and includes relevant tests or documentation.
Issues
If you encounter bugs or have suggestions:

Open an issue on the GitHub Issues page.
Provide a detailed description, including error messages and steps to reproduce.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Built for the Kaggle Playground Series S5E4 competition.
Inspired by Kaggle community notebooks and machine learning best practices.
Thanks to the open-source community for libraries like xgboost and catboost.


Feel free to star this repository if you find it useful!
