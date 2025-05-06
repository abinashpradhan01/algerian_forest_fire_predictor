# 🌲 Algerian Forest Fire Predictor

A machine learning application to predict the Fire Weather Index (FWI) in Algerian forests based on environmental and meteorological data.

## 📌 Project Overview

The Algerian Forest Fire Predictor is a web-based system that uses machine learning to assess the likelihood of forest fires. By analyzing environmental and weather parameters, the model helps support early detection and mitigation strategies for forest fire management in Algeria.

**Live Demo:** [https://algerian-forest-fire-predictor.onrender.com](https://algerian-forest-fire-predictor.onrender.com)

## 🔍 Features

- Predicts the Fire Weather Index (FWI) using multiple environmental variables
- Uses ElasticNetCV model with high accuracy (R² Score: 0.98)
- Responsive web interface for easy access on multiple devices
- Input validation and data preprocessing
- Detailed results with prediction confidence

## 🛠️ Tech Stack

- **Machine Learning:** Python, scikit-learn, ElasticNetCV
- **Backend:** Flask
- **Frontend:** HTML, CSS, JavaScript
- **Deployment:** Render

## 📊 Model Details

The system predicts the Fire Weather Index (FWI) from the following parameters:

| Parameter | Description | Range |
|-----------|-------------|-------|
| RH | Relative Humidity | 21% to 90% |
| WS | Wind Speed | 6 to 29 km/h |
| Rain | Total day in mm | 0 to 16.8 mm |
| FFMC | Fine Fuel Moisture Code | 28.6 to 92.5 |
| DMC | Duff Moisture Code | 1.1 to 65.9 |
| ISI | Initial Spread Index | 0 to 18.5 |
| Classes | Fire (1) or Not Fire (0) | Binary |
| Region | Bejaia region (0) or Sidi Bel Abbes region (1) | Binary |

### Model Performance

- **Model Type:** ElasticNetCV (with L1 and L2 regularization)
- **Mean Absolute Error:** 0.658
- **R² Score:** 0.981

## 🚀 Installation & Local Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/abinashpradhan01/algerian_forest_fire_predictor.git
   cd algerian_forest_fire_predictor
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application locally:
   ```bash
   python app.py
   ```

5. Access the application at `http://localhost:5000`

## 📂 Project Structure

```
algerian_forest_fire_predictor/
├── app.py                           # Flask application
├── models/                          # Trained ML models
│   └── elasticnetcv_model.pkl       # ElasticNetCV model
├── static/                          # Static assets
│   ├── css/                         # Stylesheets
├── templates/                       # HTML templates
│   ├── index.html                   # Homepage
│   └── home.html                 # Prediction form page
├── notebooks/                       # Jupyter notebooks
│   ├── Algerian_Forest_Fire_EDA.ipynb        # Exploratory Data Analysis
│   └── 05_Algerian_forest_fire_Model_training.ipynb  # Model training
└── README.md                        # Project documentation
```

## 📊 Exploratory Data Analysis

The data exploration phase included analysis of:
- Feature distributions and correlations
- Seasonal patterns in fire occurrences
- Regional differences between Bejaia and Sidi Bel Abbes
- Weather patterns associated with fire events

For detailed EDA, see the [Exploratory Data Analysis Notebook](https://github.com/abinashpradhan01/algerian_forest_fire_predictor/blob/c8e204e19e92fed67dc3a5d8caec8ffe6e1eccb0/notebooks/Algerian_Forest_Fire_EDA.ipynb).

## 🧪 Model Development

Multiple regression models were evaluated:
- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Decision Tree
- Random Forest
- XGBoost

ElasticNetCV was selected as the final model due to its superior performance and ability to handle multicollinearity in the dataset.

For model comparison details, see the [Model Training Notebook](https://github.com/abinashpradhan01/algerian_forest_fire_predictor/blob/c8e204e19e92fed67dc3a5d8caec8ffe6e1eccb0/notebooks/05_Algerian_forest_fire_Model_training.ipynb).

## 🧠 Usage Guidelines

For optimal predictions:
1. Ensure all input values are within the specified ranges
2. Select the appropriate region (Bejaia or Sidi Bel Abbes)
3. Input data from the same time of day when possible for consistency
4. Consider seasonal variations in your interpretation of results



## 👤 Author

**Abinash Pradhan**  
[Personal Website](https://abinashpradhan01.github.io)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---
