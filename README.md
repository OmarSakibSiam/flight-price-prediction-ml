# ✈️ Flight Price Prediction

## 📌 Project Overview

This project focuses on predicting airline ticket prices using Machine Learning techniques. It analyzes flight-related information such as airline, source, destination, departure time, arrival time, duration, and number of stops to estimate ticket prices.

A **Random Forest Regressor** is used to train the prediction model and estimate flight prices based on the available features.

## 🎯 Objectives

- Analyze flight-related data to understand the factors affecting ticket prices.
- Perform data preprocessing and feature engineering.
- Convert categorical variables into numerical representations.
- Train a machine learning regression model.
- Predict flight prices using the trained model.

## 📂 Dataset

The project uses two Excel files:

- `Data_Train.xlsx` – Contains flight information with actual ticket prices for model training.
- `Test_set.xlsx` – Contains flight information without ticket prices for price prediction.

The combined dataset initially contains **13,354 records and 11 columns**.

## 🛠️ Technologies & Libraries

- Python
- Pandas – Data manipulation and analysis
- NumPy – Numerical operations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- Scikit-learn – Machine learning and preprocessing

## ⚙️ Project Workflow

### 1. Data Loading
- Load the training and testing datasets using Pandas.
- Combine both datasets for preprocessing.

### 2. Feature Engineering
Transform the original date and time columns into numerical features:

- Extract Day, Month, and Year from `Date_of_Journey`.
- Extract Arrival Hours and Minutes.
- Extract Departure Hours and Minutes.
- Convert Flight Duration into Hours and Minutes.
- Convert the number of stops into numerical values.
- Remove unnecessary columns such as Route and the original date/time columns.

### 3. Data Preprocessing
- Apply Label Encoding to categorical features:
  - Airline
  - Source
  - Destination
  - Additional_Info
- Handle missing values.
- Separate the training and testing datasets.

### 4. Model Training

The project uses **Random Forest Regressor** with the following configuration:

| Parameter | Value |
|---|---|
| Model | Random Forest Regressor |
| Number of Estimators | 200 |
| Max Depth | None |
| Minimum Samples Leaf | 2 |
| Random State | 42 |

The training dataset is divided into:
- 70% Training Data
- 30% Testing Data

### 5. Model Evaluation

The model is evaluated using the R² (R-squared) score.

**Achieved R² Score: 0.862**

This indicates that the model explains approximately 86.2% of the variance in the held-out ticket price data.

### 6. Price Prediction

After training, the Random Forest model is used to predict prices for the separate test dataset. The predicted prices are stored in a Pandas DataFrame named `PP`.

## 📊 Model Performance

| Evaluation Metric | Score |
|---|---:|
| R² Score | 0.862 |

## 📁 Repository Structure

```text
Flight-Price-Prediction/
│
├── Flight_price_prediction.ipynb
├── Data_Train.xlsx
├── Test_set.xlsx
└── README.md
```

## 🚀 How to Run the Project

**1. Clone the repository**

```bash
git clone https://github.com/your-username/Flight-Price-Prediction.git
```

**2. Navigate to the project directory**

```bash
cd Flight-Price-Prediction
```

**3. Install the required libraries**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

**4. Launch Jupyter Notebook**

```bash
jupyter notebook
```

**5. Open and run**

Open `Flight_price_prediction.ipynb` and execute the cells sequentially.

Make sure both Excel dataset files are available in the project directory.

## 🔮 Future Improvements

- Experiment with additional regression algorithms.
- Perform hyperparameter tuning to improve model performance.
- Use more advanced feature encoding techniques.
- Build an interactive web application for real-time flight price prediction.

## 👨‍💻 Author

**Omar Sakib Siam**

- GitHub: [OmarSakibSiam](https://github.com/OmarSakibSiam)

---

⭐ If you find this project interesting, feel free to explore the notebook and provide feedback!
