# Bank Customer Churn Prediction using Artificial Neural Network (ANN)

A deep learning project that predicts whether a bank customer will leave (churn) using an Artificial Neural Network built with TensorFlow/Keras.

## 📌 Overview

This project uses a Bank's customer dataset (`Churn_Modelling.csv`) containing **10,000 customer records** to train an Artificial Neural Network that predicts customer churn (whether a customer will exit the bank or stay).

The model achieves an accuracy of **~86%** on the test set.

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
- **Scikit-learn** – Preprocessing (Label Encoding, One-Hot Encoding, Feature Scaling, Train/Test split), evaluation metrics
- **TensorFlow / Keras** – Building and training the ANN

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

## 📈 Results

- **Test Accuracy:** ~86%
- **Confusion Matrix:**
  ```
  [[1514   81]
   [ 191  214]]
  ```

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/customer-churn-prediction-ann/bank-churn-ann.git
   cd bank-churn-ann
   ```

2. Install the required dependencies:
   ```bash
   pip install numpy pandas tensorflow scikit-learn
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
├── artificial_neural_network.ipynb   # Main notebook with full ANN pipeline
├── Churn_Modelling.csv                # Dataset
└── README.md                          # Project documentation
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

Khaled Alzeer.
