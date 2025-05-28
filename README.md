# ⚡ VoltSight: Intelligent Electricity Demand Forecasting Dashboard

VoltSight is a web-based interactive dashboard that predicts electricity demand using machine learning models. It provides visual analytics, model comparisons, and insights into seasonal and weather-related demand patterns, making it ideal for energy analysts, researchers, and smart grid operators.

---

## 🔍 Features

- 📈 **Forecasting Panel**  
  Forecast electricity demand for selected cities and dates using multiple ML models.

- 🧪 **Model Comparison**  
  Evaluate and compare model performance (MAE, RMSE, MAPE) with visual plots and metrics.

- 🧠 **Feature Importance**  
  Interpret key predictors using model-specific feature importance analysis.

- 📊 **Demand Analysis**  
  Analyze how demand changes with temperature, time of day, weather, and season.

- 🔬 **Cluster Analysis**  
  Use KMeans clustering and PCA to explore demand patterns across different dimensions.

- 💾 **Export Options**  
  Download predictions and analysis results in CSV format.

---

## 🧠 Models Used

- Linear Regression
- Ridge Regression
- Random Forest Regressor
- XGBoost Regressor
- Ensemble (mean of multiple models)

---

## 🧰 Tech Stack

| Layer         | Tools / Libraries                              |
|---------------|------------------------------------------------|
| Frontend      | Streamlit, Plotly, Matplotlib                  |
| Backend       | Python, Pandas, NumPy, Scikit-learn, XGBoost   |
| ML Pipelines  | StandardScaler, OneHotEncoder, ColumnTransformer |
| Clustering    | KMeans, PCA                                    |
| Evaluation    | MAE, RMSE, MAPE                                |

---

## 📂 Project Structure

```
├── models/                    # Trained ML models and preprocessors
├── preprocessed_data2.csv    # Cleaned input data
├── predictive_modeling.py    # Model training and saving
├── frontend.py       # Streamlit app for forecasting and analysis
├── README.md                 # Project documentation
```

---
## 📦 Dataset

This project uses electricity demand and weather data from the following Kaggle dataset:

🔗 [US Top 10 Cities - Electricity and Weather Data](https://www.kaggle.com/datasets/shubhamkulkarni01/us-top-10-cities-electricity-and-weather-data?select=EIA930_BALANCE_2018_Jul_Dec.csv)  
Provided by **Shubham Kulkarni** on Kaggle. The dataset includes hourly electricity demand and weather conditions for 10 major US cities.

> Ensure you download and preprocess the dataset using the `preprocessing.ipynb` notebook before training models.
---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Mxneeb/VoltSight-Electricity-Demand-Forecasting
cd VoltSight-Electricity-Demand-Forecasting
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

> To generate `requirements.txt` from your environment:
```bash
pip freeze > requirements.txt
```

### 3. Run Preprocessing

Open and run the Jupyter Notebook to clean and engineer the raw dataset:

```bash
jupyter notebook preprocessing.ipynb
```

This will generate a cleaned dataset named `preprocessed_data2.csv`, required for training.

### 4. Train Models

```bash
python predictive_modeling.py
```

This will:
- Load the cleaned dataset (`preprocessed_data2.csv`)
- Train global and city-specific machine learning models
- Save them to the `models/` directory

### 5. Launch the Dashboard

```bash
streamlit run frontend.py
```

This will start the **VoltSight** interactive dashboard in your browser.


## 📸 Screenshots 

![Screenshot 2025-05-28 051253](https://github.com/user-attachments/assets/2495b74c-d3e2-4490-bbab-259576e315b7)
![Screenshot 2025-05-28 050754](https://github.com/user-attachments/assets/d8958baa-0b2a-4cc8-bc12-d75a562f5f29)
![Screenshot 2025-05-28 050829](https://github.com/user-attachments/assets/35b35fca-0cf5-4ce7-ba73-74d68af551bd)
![Screenshot 2025-05-28 050839](https://github.com/user-attachments/assets/30ec981a-550f-4677-944e-8a2af0ae7c42)
![Screenshot 2025-05-28 050850](https://github.com/user-attachments/assets/91b77d18-328d-41f4-a061-aa84f4ab901b)
![Screenshot 2025-05-28 050859](https://github.com/user-attachments/assets/f13850ba-2c09-422c-b6d9-dafcec2f589f)



## 🤝 Contributions

Contributions are welcome! Please open an issue or submit a pull request for improvements or fixes.

---

## 📝 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
