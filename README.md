Insurance Charges Prediction
This project aims to predict medical insurance charges based on various factors such as age, gender, BMI, smoking habits, and region using machine learning techniques. The models implemented include Linear Regression and Random Forest Regressor to evaluate and compare their predictive performance.

Table of Contents
Project Overview
Dataset Description
Installation
Usage
Models Used
Evaluation Metrics
Results
Visualization
Contributing
License
Project Overview
In this project, we leverage regression techniques to predict the charges billed by health insurance companies. By analyzing different factors such as age, gender, BMI, number of children, smoking status, and residential region, the goal is to build a model that can accurately forecast medical costs for new patients.

Dataset Description
The dataset used in this project is a publicly available Insurance dataset that includes the following features:

age: Age of the individual (integer)
sex: Gender of the individual (male, female)
bmi: Body mass index (float) - A measure of body fat based on height and weight
children: Number of children/dependents (integer)
smoker: Smoking status (yes, no)
region: Residential region (northeast, northwest, southeast, southwest)
charges: Medical charges billed by health insurance (float) - This is the target variable we aim to predict
Installation
Follow these steps to set up the project locally:

Clone the repository:

bash
Copy code
git clone https://github.com/amaanlakdawala/medical-cost-prediction.git

Install dependencies: Make sure you have Python installed. Use the following command to install the required Python packages:

bash
Copy code
pip install -r requirements.txt
Download the dataset: Place the insurance.csv dataset in your project directory. You can use your local file path or a URL to load the dataset in the script.

Usage
To run the prediction models, follow these steps:

Load the dataset by specifying the path in the script:

python
Copy code
url = r"path_to_your_dataset/insurance.csv"
Run the script:

bash
Copy code
python insurance_prediction.py
The script will output the evaluation metrics and display visualizations comparing the actual vs. predicted charges.

Models Used
We implemented two machine learning models to predict insurance charges:

Linear Regression:
A simple linear model that assumes a linear relationship between the features and the target variable.
Random Forest Regressor:
An ensemble model that uses multiple decision trees to capture complex patterns in the data.
Evaluation Metrics
The models are evaluated using the following metrics:

Mean Squared Error (MSE): Measures the average of the squares of the errors or deviations.
R² Score (Coefficient of Determination): Represents the proportion of the variance for the target variable that's explained by the features.
Example Evaluation Output:
yaml
Copy code
Linear Regression Model:
Mean Squared Error (MSE): 33,596,915.85
R² Score: 0.78

Random Forest Regressor Model:
Mean Squared Error (MSE): 20,864,569.51
R² Score: 0.87
Results
The Random Forest Regressor outperformed the Linear Regression model, achieving a lower MSE and a higher R² score, indicating better predictive accuracy:

Linear Regression:
MSE: 33,596,915.85
R² Score: 0.78
Random Forest Regressor:
MSE: 20,864,569.51
R² Score: 0.87
Visualization
The project includes scatter plots to compare actual vs. predicted charges for both models.

python
Copy code
# Visualize the model predictions
plt.figure(figsize=(12, 6))

# Plot for Linear Regression
plt.subplot(1, 2, 1)
sns.scatterplot(x=y_test, y=y_pred_lr, color='blue')
plt.title("Linear Regression - Actual vs Predicted Charges")
plt.xlabel("Actual Charges")
plt.ylabel("Predicted Charges")

# Plot for Random Forest Regressor
plt.subplot(1, 2, 2)
sns.scatterplot(x=y_test, y=y_pred_rf, color='green')
plt.title("Random Forest - Actual vs Predicted Charges")
plt.xlabel("Actual Charges")
plt.ylabel("Predicted Charges")

plt.tight_layout()
plt.show()
Contributing
Contributions are welcome! If you would like to contribute to this project, please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit them (git commit -m 'Add feature').
Push to the branch (git push origin feature-branch).
Open a pull request.