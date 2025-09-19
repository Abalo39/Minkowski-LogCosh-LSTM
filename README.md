# Hybrid-Minkowski-LogCosh-Loss-LSTM

A robust LSTM forecasting framework leveraging the **Hybrid Minkowski-LogCosh (MLC) loss function** for **time series prediction** under both clean and noisy conditions.  
This repository includes code, datasets, and results from our **malaria forecasting study in the Oti Region (Ghana)**.  

The proposed loss introduces a tunable **Minkowski exponent `p`** that improves flexibility, generalization, and robustness to outliers.  

---

## 📂 Project Files

### 1. `Confirmed_notebook.ipynb`
Trains an **LSTM model on the confirmed malaria case variable** from the **original climate-malaria dataset**.  
- Evaluates performance under clean conditions.  
- Employs **GridSearch** to tune the **Minkowski-LogCosh loss** hyperparameters.  

### 2. `Confirmed_outliers_notebook.ipynb`
Trains an **LSTM model on a modified dataset** where artificial outliers were injected into the confirmed malaria case variable.  
- Designed to test the robustness of the model under noisy data conditions.  
- Also uses **GridSearch** to optimize the MLC loss across different values of the Minkowski exponent.  

### 3. `merged_climate_malaria_data.csv`
The full **climate-malaria dataset**, including:  
- The **confirmed malaria case variable** (used as the target in this study).  
- Additional climate-related variables, which were not included in this particular analysis but remain available in the dataset for future experimentation.  

---

## 🔬 Summary of Experiments

Both notebooks implement LSTM forecasting with the **Hybrid MLC loss function**:  

- **`Confirmed_notebook.ipynb`** → LSTM trained on **cleaned data**.  
- **`Confirmed_outliers_notebook.ipynb`** → LSTM trained on **noisy, outlier-rich data**.  
