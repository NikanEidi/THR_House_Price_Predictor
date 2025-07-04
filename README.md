# 🏠 Tehran House Price Predictor

This project leverages real-world data from approximately 4,000 apartment listings in Tehran to predict housing prices in **Toman** using supervised machine learning techniques. The dataset contains critical property features such as size, number of rooms, amenities, and approximate address.

---

## 📁 Dataset Features

- `Area` — House area in square meters  
- `Room` — Number of bedrooms  
- `Parking` — Whether the unit has a parking spot (0/1)  
- `Warehouse` — Whether the unit has a storage room (0/1)  
- `Elevator` — Whether the building has an elevator (0/1)  
- `Address` — Approximate location in Tehran  
- `Price` — Property price in Toman  
- `Price(USD)` — Property price in USD (not used for training)

---

## 🧹 Data Preprocessing

- Removed missing or invalid records (e.g., null addresses, unrealistic area values)
- Grouped rare addresses into an `Other_Address` category
- Created new **classification features** by combining meaningful variables:
  - `Elevator_Area`
  - `Room_Parking`
  - `Room_Warehouse`
  - `Combined_Facilities`
  - `Facilities_Score`
  - `Is_Luxury` (flag for premium properties)

---

## 📊 Exploratory Data Analysis

- Visualized feature distributions using `histograms` and `boxplots`
- Analyzed feature correlation with price
- Identified and removed extreme outliers using quantiles and Isolation Forest

---

## 🤖 Model Training

- Split data into `train` and `test` sets
- Applied **Linear Regression**, **Ridge Regression**, and **Random Forest Regressor**
- Performed **feature scaling** with `StandardScaler`
- Achieved R² score up to **0.704** with selected features and tuning

---

## 📈 Evaluation Metrics

- `R² Score`  
- `Mean Absolute Error (MAE)`  
- `Root Mean Squared Error (RMSE)`  
- Final model selected based on performance and generalization (no overfitting observed)

---

## ✅ Tools & Libraries

- Python  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn  

---

## 💡 Future Work

- Improve address clustering using NLP or geo-based grouping  
- Add time-based price trends if data becomes available  
- Deploy as a web app using Streamlit or Flask  

---

## 👨‍💻 Author

Made with 🔥 and patience after testing multiple models over two weeks.
