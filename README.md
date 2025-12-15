# 🔋 AI Energy Prediction Models

Predicting energy consumption of AI workloads using machine learning models to support more sustainable and energy-aware AI systems.

---

## 📌 Project Overview

This project uses machine learning to predict **energy consumption and efficiency metrics** for AI workloads based on model architecture, hardware configuration, and runtime parameters. By estimating energy usage ahead of time, this work aims to support **responsible AI development** and **energy-efficient system design**.

---

## 👥 Team Members

| Name | GitHub | Contributions |
|------|--------|---------------|
| Your Name | @yourhandle | Data preprocessing, model training, evaluation |
| Teammate Name | @handle | EDA, visualization, feature engineering |
| Mentor / Advisor (optional) | — | Project guidance |

---

## ✨ Project Highlights

- Built regression models to predict AI energy consumption
- Implemented and compared **Decision Tree**, **Random Forest**, and **XGBoost**
- Performed extensive exploratory data analysis (EDA)
- Identified key features driving energy usage
- Evaluated models using standard regression metrics
- Visualized results for interpretability and insight

---

## 📊 Data Exploration (EDA)

### Dataset

The dataset contains information about AI workloads and system configurations, including:

- Model architecture and workload type
- Hardware configuration (e.g., GPU type)
- Runtime parameters (batch size, sequence length)
- Power and energy measurements

### Preprocessing

- Removed missing and invalid records
- Encoded categorical variables
- Scaled numerical features when appropriate
- Split data into training and testing sets

### Key Insights

- Energy usage increases non-linearly with batch size
- Hardware choice strongly impacts power consumption
- Certain model architectures consistently consume more energy

### Visualizations

- Energy consumption distributions  
- Correlation heatmaps  
- Energy vs. batch size plots  
- Energy usage by model architecture  

(See `figures/` for annotated plots.)

---

## 🧠 Model Development

### Models Used

- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**

### Training Process

- Hyperparameter tuning using cross-validation
- Trained on processed feature set
- Evaluated on held-out test data
- Compared models across performance metrics

---

## 📈 Results & Key Findings

### Performance Metrics

Models were evaluated using:

- **R² Score**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

| Model | R² | MAE | RMSE |
|------|----|-----|------|
| Decision Tree | XX | XX | XX |
| Random Forest | XX | XX | XX |
| XGBoost | **XX** | **XX** | **XX** |

### Key Findings

- XGBoost achieved the best overall predictive performance
- Random Forest reduced variance and handled non-linear features well
- Decision Tree provided interpretability but lower accuracy
- Feature importance highlighted hardware and batch size as dominant predictors

### Visualizations

- Predicted vs. actual energy consumption
- Feature importance plots
- Model comparison charts

---

## 🚀 Next Steps

- Incorporate deep learning models (LSTM, Transformer)
- Expand dataset to additional hardware platforms
- Add SHAP explainability for model interpretation
- Build an interactive energy prediction dashboard
- Extend predictions to carbon emissions and cost estimation
- Deploy the model as a web API

---

## 🛠️ Tech Stack

- Python
- scikit-learn
- XGBoost
- pandas, NumPy
- matplotlib, seaborn

---

## 📁 Repository Structure

