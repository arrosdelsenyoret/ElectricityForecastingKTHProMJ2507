# Electricity Market Forecasting - Spain (2023–2025) ⚡

This repository contains the data pipeline, preprocessing, and machine learning models for analyzing and forecasting the Spanish electricity market (Project for course **MJ2507**).

## 📂 Repository Structure

* **`01_data_extraction_and_cleaning.ipynb`**: Extracts raw historical data from the ENTSO-E API (Load, Day-ahead prices, Nuclear generation, Hydro reservoirs, and Wind/Solar forecasts), handles missing values/DST transitions, and generates the engineered master dataset.
* **`02_Logistic_regression.ipynb`**: Implementation and evaluation of the Logistic Regression model using the engineered dataset.
* **Reference & Project Documentation (`.pdf`)**:
  * `Project explanation_General.pdf` & `MJ2507_P1_Spain (1).pdf`: Project guidelines and context.
  * `Supervision session notes.pdf`: Notes from project supervision meetings.
  * `JagrutiPaper.pdf` & `Mix Eléctrico Futuro de España (1).pdf`: Literature and background research.
* **`requirements.txt`**: List of required Python dependencies.

*(Note: Data folders `raw/`, `processed/`, and `model_input/` are ignored by Git to keep the repository lightweight. They are automatically generated when running the first notebook).*

---

## 🚀 Getting Started

### 1. Install Dependencies
Make sure you have Python installed, then install the required packages in your virtual environment:
```bash
pip install -r requirements.txt
```

### 2. Configure the ENTSO-E API Key
To extract the data yourself, you need an API token from the [ENTSO-E Transparency Platform](https://transparency.entsoe.eu/).
1. Create a file named **`.env`** in the root directory of this project.
2. Add your token inside the file using the following format:
```env
ENTSOE_API_KEY=your_secret_api_key_here
```

### 3. Run the Pipeline
1. Execute **`01_data_extraction_and_cleaning.ipynb`** to download the data and generate the `model_input/Master_Dataset_Engineered_2023_2025.csv` file.
2. Execute **`02_Logistic_regression.ipynb`** to train and evaluate the model.