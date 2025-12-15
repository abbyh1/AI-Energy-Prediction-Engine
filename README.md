# AI Energy Prediction Engine - Team KPMG 1F



---

### 👥 **Team Members**

**Example:**

| Name             | GitHub Handle | Contribution                                                             |
|------------------|---------------|--------------------------------------------------------------------------|
| Abigail Huang   | @abbyh1 | Data exploration, model developing, overall project coordination            |
| Jordan Ramirez   | @jramirez     | Data collection, exploratory data analysis (EDA), dataset documentation  |
| Amina Hassan     | @aminahassan  | Data preprocessing, feature engineering, data validation                 |
| Alou Kone        | @pmehta       | Model selection, hyperparameter tuning, model training and optimization  |
| Chris Park       | @chrispark    | Model evaluation, performance analysis, results interpretation           |

---

## 🎯 **Project Highlights**

- Developed three machine learning models to help KPMG use AI models more sustainably.
- Achieved **R² > 0.99**, demonstrating strong predictive performance and business value for KPMG.
- Generated actionable insights to inform business decisions at KPMG.


---

## 👩🏽‍💻 **Setup and Installation**
Follow these steps to run the project in **Google Colab** and reproduce the results.

* Open the Colab notebook [KPMG_1F_AI_ENERGY_Analsysis.ipynb](https://colab.research.google.com/github/abbyh1/AI-Energy-Prediction-Engine/blob/main/KPMG_1F_AI_ENERGY_Analsysis.ipynb)

2. Click **“File → Save a copy in Drive”** to make your own editable copy.

3. Follow the notebook instructions and run the cells **top to bottom**.

The notebook installs all required dependencies, loads the dataset, performs EDA, trains the models, and evaluates results automatically.


---

## 🏗️ **Project Overview**

*Help KPMG use AI models more strategically 
*Predict and reduce the dollar cost, energy consumption (kWh), and carbon emissions associated with specific AI workloads 
*Enable "what-if" scenario analysis to help KPMG and its clients select the most cost-effective configuration that meets their performance targets 


---

## 📊 Data Exploration

### Dataset

This project uses the **ML.Energy Dataset**, which contains detailed measurements of energy consumption and performance for AI workloads across different model architectures, hardware configurations, and runtime settings. Key variables include batch size, GPU type, token throughput, latency, parallelism settings, and total energy usage (in joules).

---

### Data Exploration & Preprocessing

Exploratory Data Analysis (EDA) was performed to understand feature distributions, relationships, and potential sources of noise. Preprocessing steps included:

- Filtering out invalid or missing energy measurements
- Handling missing values in categorical fields (e.g., GPU type)
- Normalizing and scaling numerical features where appropriate
- Encoding categorical variables such as GPU type and engineered GPU tiers

To better capture system-level behavior, several **task-level engineered features** were introduced:

- **Energy per batch unit**:  
  Total energy consumption normalized by batch size  
  → captures energy efficiency across workloads

- **Tokens per joule**:  
  Token throughput divided by total energy  
  → measures energy efficiency for LLM-style tasks

- **Latency per batch**:  
  Batch latency normalized by batch size  
  → helps compare latency across different workload scales

- **GPU tier classification**:  
  GPUs were grouped into tiers (flagship, enterprise, mid-range, entry) based on model name  
  → improves generalization and reduces hardware sparsity

- **Parallelism indicator**:  
  Binary feature indicating whether tensor or pipeline parallelism was used  
  → captures scaling effects in distributed workloads

---

### Challenges & Assumptions

- **Heterogeneous workloads**: The dataset includes a wide variety of models and configurations, which introduces variance that cannot be fully controlled.
- **Incomplete hardware metadata**: Some GPU entries were missing or inconsistent, requiring assumptions during tier classification.
- **Task-specific features**: Metrics such as token throughput are only meaningful for certain workloads (e.g., LLMs), so assumptions were made when engineering efficiency features.
- **Measurement noise**: Energy readings may vary due to background system processes and benchmarking conditions.

Despite these challenges, feature engineering and normalization enabled the models to learn meaningful relationships between system configuration and energy usage.


---

## 🧠 **Model Development**

* Model(s) used: Random Forest, XGBoost Regressor, Decision Tree
* Feature selection and Hyperparameter tuning strategies
* Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)


---

## 📈 **Results & Key Findings**

* Random Forest Results: Train_R2: 0.9964  Test_R2: 0.9926  MAE: 0.0918   RMSE: 0.1432
* XGBoost Regressor Results: Train_R2: 0.9882  Test_R2: 0.9744  MAE: 0.1864  RMSE: 0.2656
* Decision Tree Results: Train_R2: 0.9882  Test_R2: 0.9744  MAE: 0.1864  RMSE: 0.2656

**Potential visualizations to include:**



---

## 🚀 **Next Steps**


* Generate and train a new model (LSTM)
* Decide GPU/model configs using a simple efficiency score and rank by ROI.
* Develop the FastAPI service


---




---

