📘 **Energy Waste Detection in Smart Homes**

🔍 **Background**

Smart homes use IoT devices and sensors to monitor appliance-level energy consumption. When combined with weather data, this enables better understanding of energy usage patterns and helps identify inefficiencies and energy waste.

❗**Problem Statement**

Most Home Energy Management Systems provide only aggregated energy data and lack real-time, appliance-level insights. They also underutilize weather data, leading to undetected energy waste, higher costs, and inefficient energy usage.

🎯 **Objective**

To develop a machine learning-based framework that integrates appliance-level energy data and weather variables to detect and predict energy waste while maintaining user comfort.

📊 **Exploratory Data Analysis (EDA)**
⚡ **Energy Consumption**
Furnace is the highest energy consumer (69%), driven by seasonal heating needs.
Refrigerator accounts for 18.6%, dishwasher 9.2%, microwave 3.2%.
Furnace peaks in winter up to 2.47 kWh.

🏠**Usage Patterns**
Home office shows highest room-level usage due to cooling demand.
Daily energy spikes reach up to 3.5 kWh, indicating anomalies or high demand periods.
Energy generation remains low and does not cover peak consumption.

🌦️ **Weather Impact**
Strong correlation between temperature & apparent temperature (0.99).
Temperature & dew point correlation (0.89).
Cloud cover and precipitation reduce solar generation and influence energy demand.

🚨 **Energy Waste Detection**
7.92% of data classified as energy waste
Waste is mainly caused by:
Furnace overuse
Seasonal extremes
Sudden energy spikes

📊 **Clustering Insights**
7 appliance behavior clusters identified.
Furnace and kitchen appliances are main contributors to inefficiency.
Energy usage often exceeds generation → grid dependency.

🤖 **Model Performance**
Dataset is imbalanced (92% non-waste / 8% waste).
Metrics used: Precision, Recall, F1-score, ROC AUC.

🏆 Best Model: Random Forest
F1 Score: ~0.89
ROC AUC: ~0.99
Best balance between precision and recall.

⚡ Other Models
XGBoost & LightGBM: strong recall, moderate precision.
Deep Learning models: high recall but lower precision.
Logistic Regression & SVM: weakest performance.

🧠 **SHAP Explainability**
Key Drivers of Energy Waste:
Total energy usage
Furnace consumption
Precipitation intensity
Temperature
Kitchen appliances

**Insight:**
Weather conditions strongly influence energy waste, especially through furnace usage and reduced solar efficiency.

🎯**Conclusion**
Furnace is the dominant energy consumer and main source of inefficiency.
Weather is a key factor in energy waste patterns.
Random Forest is the most reliable model.
SHAP confirms appliance + weather interaction as main drivers of waste.
