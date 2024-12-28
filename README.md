# Power Consumption Prediction using LSTM

This project focuses on predicting power consumption using **Long Short-Term Memory (LSTM)**, a type of Recurrent Neural Network (RNN) model. By analyzing historical power consumption data, the project aims to predict future energy usage trends, which can assist in resource planning and optimization.

---

## 📊 **Overview**

### **Objective**
- Predict hourly power consumption from historical data.
- Use LSTM for sequence modeling and prediction due to its ability to capture long-term dependencies in time-series data.

### **Data**
- Dataset: Historical power consumption data from **2002 to 2018** and validation data from **2022 to 2023**.
- Features extracted include:
  - **Temporal Information**: Hour, day, month, year, weekday.
  - **Consumption Patterns**: Trends in daily, weekly, and yearly power usage.

---

## 🛠️ **Technologies Used**
- **Languages**: Python
- **Libraries**:
  - `numpy`, `pandas` - Data processing and manipulation
  - `matplotlib`, `seaborn` - Visualization
  - `tensorflow`, `keras` - Deep learning model development
  - `scikit-learn` - Data preprocessing and evaluation
- **Model**: Long Short-Term Memory (LSTM)

---

## ⚙️ **Project Workflow**

1. **Data Exploration**:
   - Loaded and visualized hourly power consumption data.
   - Inspected data distribution and trends across time (yearly, monthly, weekly).
   - Extracted features such as `hour`, `day`, `month`, `year`, `day of week`, and `week of year`.

2. **Data Preprocessing**:
   - Scaled power consumption data using **Min-Max Scaling**.
   - Generated sequences for time-series input to the LSTM model.

3. **Model Building**:
   - Built an LSTM model with the following architecture:
     - Three LSTM layers with `tanh` activation.
     - Dropout layers to prevent overfitting.
     - Dense output layer for regression.
   - Optimized the model using **Adam Optimizer** with **Mean Squared Error (MSE)** as the loss function.

4. **Training and Evaluation**:
   - Trained the model on data from 2002 to 2018 for 10 epochs.
   - Achieved an **R² score of 0.94** on the test set, indicating excellent prediction accuracy.
   - Validated the model on 2022–2023 data with similar performance.

5. **Visualization**:
   - Compared **actual vs. predicted power consumption** trends.
   - Plotted power consumption patterns across different time frames.

---

## 🧪 **Results**

- **Model Performance**:
  - **R² Score**:
    - Test Set (2018): **0.94**
    - Validation Set (2022–2023): **0.94**
- Predicted power consumption aligns closely with actual data, demonstrating the model's effectiveness.

- **Visualization**:
  - Time-series plot of **actual vs. predicted** power consumption.
  - Trends analyzed by year, month, and week to showcase seasonal and temporal effects on energy consumption.

---

## 📂 **Folder Structure**

```plaintext
├── data/
│   ├── DOM_hourly.csv          # Training data (2002–2018)
│   ├── powervalidate.csv       # Validation data (2022–2023)
├── notebooks/
│   ├── power_consumption.ipynb # Jupyter notebook for analysis and modeling
├── models/
│   ├── lstm_model.h5           # Saved LSTM model
├── README.md                   # Project documentation


## Key Visualizations
Power Consumption Distribution:
Distribution plots to explore the range of power consumption values.
Daily Trends:
Pivot tables showing daily consumption patterns by weekday and hour.
Actual vs. Predicted Consumption:
Side-by-side comparison of actual and predicted power consumption over time.


🚀 How to Run
Clone the repository:
bash

git clone https://github.com/yourusername/power-consumption-lstm.git
Navigate to the project directory:
bash

cd power-consumption-lstm
Install dependencies:

bash

pip install -r requirements.txt
Run the Jupyter notebook:

bash

jupyter notebook notebooks/power_consumption.ipynb
🎯 Future Scope
Explore other machine learning models for comparison (e.g., Random Forest, XGBoost).
Use ensemble techniques to improve accuracy.
Extend the dataset to include additional features like weather and economic data.
🙌 Acknowledgments
Special thanks to the creators of the dataset and the open-source community for providing tools to make this project possible.

Author: Sai Manikanta kasireddy
Contact: saikasireddy1999@gmail.com



This `README.md` provides a clear, structured overview of your project and makes it appealing to vie
