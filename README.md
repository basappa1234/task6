
# K-Nearest Neighbors (KNN) Classification on the Iris Dataset

## Objective

The objective of this project is to implement the K-Nearest Neighbors (KNN) algorithm for a classic classification problem. The process covers essential machine learning steps including data normalization, model training, hyperparameter tuning, performance evaluation, and visualization of decision boundaries

## About the Dataset

This project uses the famous **Iris dataset**, a classic in the field of machine learning.

-   **Source:** `Iris.csv`
-   **Features (Independent Variables):**
    1.  `SepalLengthCm`
    2.  `SepalWidthCm`
    3.  `PetalLengthCm`
    4.  `PetalWidthCm`
-   **Target (Dependent Variable):**
    -   `Species`: The species of the Iris flower, which is one of three classes:
        -   *Iris-setosa*
        -   *Iris-versicolor*
        -   *Iris-virginica*

## Project Pipeline

The project follows a structured machine learning workflow:

1.  **Data Loading and Preparation**:
    -   The `Iris.csv` dataset is loaded using Pandas.
    -   The data is split into features (X) and the target variable (y).
    -   The dataset is divided into an 80% training set and a 20% test set.
    -   Features are normalized using `StandardScaler` from Scikit-learn. This is a critical step for distance-based algorithms like KNN to ensure all features contribute equally.

2.  **Finding the Optimal K (Hyperparameter Tuning)**:
    -   The **Elbow Method** is used to determine the most effective value for K (the number of neighbors).
    -   The model's inertia (within-cluster sum of squares) is calculated for K values ranging from 1 to 14.
    -   A plot of Inertia vs. K is generated to visually identify the "elbow point," which represents the optimal balance between model simplicity and low error.

3.  **Model Training and Evaluation**:
    -   A `KNeighborsClassifier` model is trained using the optimal K value found in the previous step.
    -   The model's performance is evaluated on the unseen test set using two key metrics:
        -   **Accuracy Score**: The proportion of correctly classified instances.
        -   **Confusion Matrix**: A table showing the detailed breakdown of correct and incorrect predictions for each class.

4.  **Decision Boundary Visualization**:
    -   To visualize how the model separates the classes, a 2D plot of the decision boundaries is created.
    -   For clear visualization, only the two most informative features (`PetalLengthCm` and `PetalWidthCm`) are used for this step.
    -   The plot shows the decision regions for each class, providing an intuitive understanding of the model's classification logic.
