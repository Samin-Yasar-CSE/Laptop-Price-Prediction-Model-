Laptop Price Prediction Project (Beginner-Friendly)

This is a beginner-friendly machine learning project that predicts the approximate price of a laptop based on its specifications.


Dataset Source:

The dataset used in this project was taken from Kaggle and contains real-world laptop specifications and their prices. File name: laptop_price.csv.


🔍 What This Project Does:

Takes laptop specifications (like RAM, weight, CPU frequency, screen resolution, brand, etc.) as input

Predicts an estimated price in Euros

Displays a likely price range (±10%) to reflect market fluctuations

Finds and shows similar laptops from the dataset, including their prices and major features


🧰 Technologies and Libraries Used:

pandas – to read and clean the dataset

numpy – for numeric operations

seaborn and matplotlib – to visualize data (e.g., heatmaps)

scikit-learn:

StandardScaler – to scale/normalize features

train_test_split – to divide data into training/testing sets

RandomForestRegressor – to train a regression model

cosine_similarity – to find similar laptops from the dataset


⚙️ How the Code Works (Step-by-Step):

The dataset is loaded and cleaned.

Unnecessary columns are dropped.

Screen resolution is split into screen width and height.

CPU and GPU brand information is extracted.

Memory sizes (e.g., GB/TB) are converted to numerical MB values.

Categorical features (like brand, type, and OS) are converted into numeric format using one-hot encoding.

The top features most correlated with price are selected.

The dataset is split into training and testing sets.

A RandomForestRegressor model is trained on the data.

Input from the user is taken and scaled.

The model predicts the price and shows the result.

Cosine similarity is used to find 2–3 similar laptops from the dataset for reference.


💻 How to Use:

Upload the dataset file: laptop_price.csv

Run all the code cells in Google Colab (or your Python environment)

Enter the specifications of a laptop when prompted (like RAM, screen size, etc.)

The program will output:

Estimated price

Likely price range

A few similar laptops with their prices and key features


⚠️ Limitations:

The model is trained on old data (before 2020) — it may not reflect current 2023 or 2024 prices

Price predictions can be significantly off (sometimes by €500 or more)

Model performance is basic — not ready for real-world commercial use

Predictions work best for mid-range laptops — less accurate for very cheap or very premium devices


📊 Accuracy :

R² Score: around 0.75 to 0.8, depending on random split

Typical prediction error: €100 to €800

Best-case accuracy: reasonable estimates for average laptops with standard specs

Worst-case: overestimations for low-end laptops or unusual combinations


🎯 Purpose of the Project:

This project was built for learning purposes only. It’s a good introduction to:

Data preprocessing

Feature engineering

Regression modeling

Finding similar entries using cosine similarity


Even though parts of the code were adapted or copied from tutorials, the final project helps in understanding how end-to-end ML pipelines work in real life.
