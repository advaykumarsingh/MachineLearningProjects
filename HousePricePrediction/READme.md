# Machine Learning Models for House Price Prediction

## Project overview
This project demonstrates the implementation of eleven popular machine learning models using a single dataset. The models include both regression and neural network approaches. Each model is built, trained, and evaluated to showcase its performance in solving a regression task.

### Models implementated:
1. Lasso Regression

2. Ridge Regression

3. Bayesian Ridge Regression

4. Decision Tree Regression

5. Support Vector Regression (SVR)

6. K-Nearest Neighbors (KNN)

7. Neural Networks (MLPRegressor)

8. Random Forest Regression

9. Gradient Boosting Regression (GBR)

10. XGBoost Regressor

10. Elastic Net Regression

11. Custom Neural Network (Keras)


## Dataset Description
The dataset used in this project is sourced from Kaggle. It contains both numerical and categorical features and is suited for regression tasks. All preprocessing steps are applied to handle missing values, scale numerical features, and encode categorical variables.

### Source
- Source: Kaggle https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data
  


### Key Features of the Dataset:
* Contains a mix of numerical and categorical columns.

* Includes missing values handled through imputation.

* Target variable (Sale Price) is continuous, making it suitable for regression.


## Preprocessing steps
1. Handling Missing Values:
    * Numerical columns: Imputed using the mean.
    * Categorical columns: Imputed using the most frequent value.

2. Encoding Categorical Variables:

   * Converted all categorical columns to category codes using .cat.codes.

3. Feature Scaling:

   * Applied standard scaling to numerical columns for models sensitive to feature scaling (e.g., SVR, Neural Networks).

4. Train-Test Split:

   * Split the dataset into training (80%) and testing (20%) sets.


## Model Implementation
Each model is implemented with the following steps:

1. Model Initialization:
   * Specifying key hyperparameters for each algorithm.
2. Training:
   * Fitting the model on the training dataset.
3. Evaluation:
   * Evaluating the model's performance using Mean Squared Error (MSE) and R-squared metrics.

### Model-Specific details:
1.  Lasso Regression:
    * Regularized linear regression with L1 penalty.
    * Hyperparameter: alpha (regularization strength). 
2. Ridge Regression:
    * Regularized linear regression with L2 penalty.
    * Hyperparameter: alpha (regularization strength).
3. Bayesian Ridge Regression:
    * Probabilistic regression model.
    * No significant hyperparameter tuning required.
4. Decision Tree Regression:
    * Tree-based model that splits data based on feature thresholds.
    * Hyperparameters: max_depth, min_samples_split, min_samples_leaf.
5. Support Vector Regression (SVR):
    * Regression using a margin-based approach.
    * Hyperparameters: C, epsilon, and kernel type (e.g., RBF).
6. K-Nearest Neighbors (KNN):
    * Instance-based learning algorithm.
    * Hyperparameter: n_neighbors (number of nearest neighbors).
7.  Neural Networks (MLPRegressor):
    * Multi-layer perceptron for regression tasks.
    * Hyperparameters: Number of hidden layers, number of neurons, activation function, and learning rate.
8. Random Forest Regression:
    * Ensemble method using multiple decision trees to improve performance and reduce overfitting.
    * Hyperparameters: n_estimators (number of trees), max_depth (maximum depth of trees), and random_state (reproducibility).
9. Gradient Boosting Regression (GBR):
    * Sequential ensemble method that builds trees incrementally to minimize errors.
    * Hyperparameters: n_estimators (number of boosting iterations), learning_rate (step size), and max_depth (maximum depth of trees).

10. XGBoost Regressor:
    * A powerful and efficient implementation of gradient boosting optimized for speed and performance, widely used in machine learning competitions
    * Hyperparameters: n_estimators (number of boosting iterations), learning rate (step size), booster: Specifies the type of booster to use. Options include:
'gbtree' (default): Tree-based models.
'gblinear': Linear models.
'dart': Tree-based models with dropout.
nthread: Number of parallel threads to use. Set to the number of cores for faster training.
verbosity: Controls the amount of information printed during training (0 = silent, 1 = warnings, 2 = info).
11. Elastic net regression:
    * Linear regression model that combines L1 (Lasso) and L2 (Ridge) penalties.
    * Hyperparameters: alpha (regularization strength), l1_ratio (balance between L1 and L2 regularization).
12. Custom Neural Network (Keras):
    * Built using the Keras API in TensorFlow.
    * Architecture:
      * Input Layer: Matches the number of features in the dataset.
      * Hidden Layers: Multiple layers with relu activation and Dropout to reduce overfitting.
      * Output Layer: Single neuron with a linear activation function for regression.
    * Hyperparameters:
      * Number of hidden layers
      * Learning rate
      * Batch size
      * Epochs
    * Metrics:
      * Loss: Mean Squared Error (MSE)
      * Metric: Mean Absolute Error(MAE)

## Results
Each model's performance is evaluated on the test set using:
* Mean Squared Error (MSE): Measures the average squared difference between predicted and actual values.
* R-squared (R²): Indicates how well the model explains the variance in the target variable.

### Summary of results
|Model          |Mean Squared Error |R-squared
|----------------------------------|-----------------|-----------------|
Lasso Regression| 1184759412.055152| 0.8455398923001439|
Ridge Regression| 1173204459.4975164| 0.8470463409498518|
Bayesian Ridge Regression| 1173204459.4975164| 0.8470463409498518|
Decision Tree| 1490390601.0547945| 0.8056939743112499|
Support Vector Machine| 1890996181.4483337| 0.7534660025702085|
K-Nearest Neighbor| 1659180792.139452| 0.7836883663976647|
Multi-layered Perceptron| 893186017.4328521| 0.8835530597647941|
Random Forest|809359173.8650926 |0.8944817792616538|
Gradient Boosting| 805875826.1040913| 0.894935912197713|
XGBoost| 626428791.0319506| 0.9183309078216553|
Elastic Net| 1173621121.6675448| 0.8469920196395484|


### Neural network statistics
validation loss vs training loss
<img src="Train/Val Loss.jpg">


## Future Work

* Extend the project to include classification tasks.

* Experiment with more complex neural network architectures using TensorFlow or PyTorch.

* Perform hyperparameter tuning for all models using GridSearchCV.









