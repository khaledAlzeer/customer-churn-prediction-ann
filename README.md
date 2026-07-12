# Bank Customer Churn Prediction using Artificial Neural Network (ANN)

A deep learning project that predicts whether a bank customer will leave (churn) using an Artificial Neural Network built with TensorFlow/Keras, complete with exploratory data analysis and performance visualizations.

## 📌 Overview

This project uses a Bank's customer dataset (`Churn_Modelling.csv`) containing **10,000 customer records** to train an Artificial Neural Network that predicts customer churn (whether a customer will exit the bank or stay).

The model achieves an accuracy of **~86%** on the test set, along with a strong **AUC score** on the ROC Curve, and is evaluated using a full suite of visualizations and metrics beyond raw accuracy.

## 📊 Dataset

The dataset (`Churn_Modelling.csv`) contains the following features:

| Column | Description |
|---|---|
| RowNumber | Row index |
| CustomerId | Unique customer ID |
| Surname | Customer's last name |
| CreditScore | Customer's credit score |
| Geography | Customer's country (France, Spain, Germany) |
| Gender | Customer's gender |
| Age | Customer's age |
| Tenure | Number of years as a bank customer |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Whether the customer has a credit card (1 = Yes, 0 = No) |
| IsActiveMember | Whether the customer is an active member (1 = Yes, 0 = No) |
| EstimatedSalary | Customer's estimated salary |
| Exited | Target variable (1 = customer left the bank, 0 = customer stayed) |

## ⚙️ Tech Stack

- **Python 3**
- **NumPy** & **Pandas** – Data manipulation
- **Matplotlib** & **Seaborn** – Data exploration and result visualizations
- **Scikit-learn** – Preprocessing (Label Encoding, One-Hot Encoding, Feature Scaling, Train/Test split), evaluation metrics
- **TensorFlow / Keras** – Building and training the ANN

## 🧭 Workflow

1. Import the required libraries.
2. Explore the dataset (correlation heatmap).
3. Preprocess the dataset (encoding, splitting, scaling).
4. Build the ANN model.
5. Train the model.
6. Evaluate the model (accuracy, confusion matrix, classification report, ROC/AUC).
7. Visualize the results.
8. Make predictions on new data.

## 🧠 Model Architecture

- **Input layer** + **1st Hidden Layer**: 6 units, ReLU activation
- **2nd Hidden Layer**: 6 units, ReLU activation
- **Output Layer**: 1 unit, Sigmoid activation (binary classification)

**Compilation:**
- Optimizer: `adam`
- Loss: `binary_crossentropy`
- Metrics: `accuracy`

**Training:**
- Batch size: 32
- Epochs: 100
- Validation split: 20% (to monitor overfitting during training)

## 📈 Results & Evaluation

- **Test Accuracy:** ~86%
- **Confusion Matrix:**
  ```
  [[1514   81]
   [ 191  214]]
  ```
- **Classification Report:** Precision, Recall, and F1-score reported per class (Stayed / Exited), since the dataset is imbalanced.
- **ROC Curve & AUC Score:** Evaluates model performance across all classification thresholds, providing a more robust metric than accuracy alone for imbalanced data.

## 📊 Visualizations Included

This project goes beyond basic metrics and includes the following visualizations:

1. **Correlation Heatmap** – Explores relationships between numerical features and the target variable (`Exited`) before preprocessing.
2. **Training & Validation Loss/Accuracy Curves** – Plots how the model's loss and accuracy evolved over 100 epochs, helping detect overfitting.
3. **Confusion Matrix Heatmap** – A clearer, color-coded visualization of prediction results using `seaborn`.
4. **ROC Curve** – Visualizes the trade-off between the True Positive Rate and False Positive Rate across thresholds, along with the AUC score.

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/customer-churn-prediction-ann/bank-churn-ann.git
   cd bank-churn-ann
   ```

2. Install the required dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn tensorflow scikit-learn
   ```

3. Make sure `Churn_Modelling.csv` is in the project directory.

4. Run the notebook:
   ```bash
   jupyter notebook artificial_neural_network.ipynb
   ```

## 📁 Project Structure

```
bank-churn-ann/
│
├── artificial_neural_network.ipynb   # Main notebook with full ANN pipeline, EDA, and visualizations
├── Churn_Modelling.csv                # Dataset
└── README.md                          # Project documentation
```

## 📓 Notebook Structure

```
Artificial Neural Network
├── Importing the libraries
│
├── Part 1 - Data Preprocessing
│   ├── Importing the dataset
│   ├── Exploring Feature Correlations (Correlation Heatmap)
│   ├── Encoding categorical data
│   │   ├── Label Encoding the "Gender" column
│   │   └── One Hot Encoding the "Geography" column
│   ├── Splitting the dataset into the Training set and Test set
│   └── Feature Scaling
│
├── Part 2 - Building the ANN
│   ├── Initializing the ANN
│   ├── Adding the input layer and the first hidden layer
│   ├── Adding the second hidden layer
│   └── Adding the output layer
│
├── Part 3 - Training the ANN
│   ├── Compiling the ANN
│   └── Training the ANN on the Training set (with validation split)
│
├── Part 4 - Making the predictions and evaluating the model
│   ├── Predicting the result of a single observation
│   ├── Predicting the Test set results
│   └── Making the Confusion Matrix
│
└── Part 5 - Visualizing the Model's Performance
    ├── Plotting the Training and Validation Loss/Accuracy
    ├── Visualizing the Confusion Matrix as a Heatmap
    ├── Classification Report
    └── Plotting the ROC Curve and AUC Score
```

## 🔮 Example Prediction

Predicting whether a customer with the following details will leave the bank:

- Geography: France
- Credit Score: 600
- Gender: Male
- Age: 40
- Tenure: 3 years
- Balance: $60,000
- Number of Products: 2
- Has Credit Card: Yes
- Active Member: Yes
- Estimated Salary: $50,000

**Result:** The model predicts this customer will **stay** with the bank.

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).

## 🙋‍♂️ Author

Feel free to reach out or open an issue if you have any questions or suggestions.
