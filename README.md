# 🌫️ Air Quality Index (AQI) Prediction using Decision Trees

A machine learning-based project that predicts the **Air Quality Index (AQI)** value and its **associated health category** using real-world pollutant data. The project includes a Decision Tree Classifier for categorizing AQI and a Decision Tree Regressor for precise AQI value prediction, with visual explanations and overfitting checks.

---

## ✅ Key Features

- **Decision Tree Classifier** to predict AQI category (e.g., Good, Moderate, Unhealthy, etc.)
- **Decision Tree Regressor** to predict numerical AQI value
- Supports pollutants: `PM2.5`, `PM10`, `OZONE`, `SO2`, `NO2`, and `CO`
- Custom AQI calculation formulas based on pollutant-specific thresholds
- Data preprocessing and encoding
- Overfitting detection for both classification and regression
- Decision tree visualization (`plot_tree`) for model interpretability
- **User input** interface for live AQI prediction

---

## 📊 Dataset

- Dataset contains:
  - Pollutant measurements (`min`, `max`, `avg`)
  - Location details (`country`, `state`, `city`, `station`)
  - Pollutant type and timestamp
- AQI is calculated using **EPA-based pollutant-specific ranges** and converted to categorical and numeric labels.

---

## 🛠️ Technologies Used

- **Python 3**
- **Google Colab / Jupyter Notebook**
- **Libraries**:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `scikit-learn` (Decision Trees, metrics, model evaluation)

---

## 🚀 Getting Started

1. **Open in Google Colab**  

2. **Upload your dataset**
   - Ensure the CSV file is uploaded to `/content/datasheet.csv`
   - you can download from here also : https://www.data.gov.in/resource/real-time-air-quality-index-various-locations

3. **Run the notebook**
   - All sections are labeled and ready to execute step-by-step

---

## 🧠 Model Performance

### ✅ Classifier (Decision Tree)
- **Accuracy:** 100%
- **Precision/Recall/F1-score:** 1.0 across all AQI categories

### ✅ Regressor (Decision Tree)
- **R² Score:** 0.998 (Testing)
- **Mean Squared Error:** 6.29 (Testing)

Both models show **excellent performance** with no overfitting observed.

---

## 🩺 Health Risk Labels

Based on AQI, the following health advisories are provided:

| AQI Category | Health Risk |
|--------------|-------------|
| Good         | Satisfactory air quality |
| Moderate     | Acceptable; minor health concerns |
| Unhealthy for Sensitive Groups | Risk to sensitive individuals |
| Unhealthy    | Health effects for everyone |
| Very Unhealthy | Health alert for all |
| Hazardous    | Emergency conditions |

---

## 🧪 Example: User Input Prediction

Enter pollutant details to predict AQI:
Pollutant Minimum: 85
Pollutant Maximum: 160
Pollutant Average: 98
Pollutant ID (PM2.5, PM10, OZONE, SO2, NO2, CO): NO2

## output
Predicted AQI Category: Good
Predicted AQI Value: 49.68
Health Risk: Good: Air quality is satisfactory.

📚 Project Structure
aqi-prediction-decision-tree/
├── datasheet.csv                   # Dataset (not shared publicly)
├── aqi_prediction_notebook.ipynb  # Main Colab notebook
├── README.md                      # Project documentation

🔮 Future Enhancements
Add support for more ML models (e.g., Random Forest, XGBoost)

Deploy via Flask or Streamlit as a web app

Real-time AQI data via APIs (OpenAQ, CPCB)

