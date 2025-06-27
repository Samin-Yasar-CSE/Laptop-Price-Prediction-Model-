# Laptop Price Prediction

This is a beginner-friendly machine learning project that predicts the approximate price of a laptop based on its specifications.

---

## Dataset Source

The dataset was taken from Kaggle (`laptop_price.csv`).

---

## What This Project Does

- Takes laptop specifications such as RAM, weight, CPU frequency, screen resolution, brand, and more as input.
- Predicts the estimated price of the laptop in Euros.
- Shows a possible price range (±10%) to cover fluctuations.
- Displays a few similar laptops from the dataset with their price and main features.

---

## Technologies and Libraries Used

- **pandas**: For reading and cleaning the dataset.
- **numpy**: For numerical operations.
- **seaborn** and **matplotlib**: For data visualization.
- **scikit-learn**:  
  - `StandardScaler` for scaling features.  
  - `train_test_split` to divide data into training and testing sets.  
  - `RandomForestRegressor` to train the model for price prediction.  
  - `cosine_similarity` to find similar laptops.

---

## How The Code Works (Step-by-Step)

1. Loads the dataset from Kaggle.
2. Drops unnecessary columns and extracts important info like screen width, height, CPU brand, and frequency.
3. Converts categorical features (brand, type, OS) into numeric format using one-hot encoding.
4. Cleans and converts RAM, memory size, and other fields into usable numeric values.
5. Selects the top features that affect price based on correlation.
6. Splits the data and trains a Random Forest model.
7. Uses `StandardScaler` to normalize input features.
8. Creates a function that:  
   - Takes user input (RAM, weight, screen size, GPU, etc.)  
   - Predicts price based on the model  
   - Shows an estimated price range  
   - Finds and prints a few similar laptops from the dataset.

---

## How To Use

1. Upload the dataset file (`laptop_price.csv`).
2. Run all code cells in order (preferably in Google Colab or VS Code with Python).
3. Enter laptop specs when prompted.
4. The program will show:  
   - Estimated price  
   - Price range  
   - A few similar laptops from the dataset

---

## Limitations

- The model is trained on an older dataset and may not reflect current 2023 or 2024 market prices.
- Predictions can sometimes be off by €500 to €800 or more.
- Model performance is average — it’s not a commercial-level estimator.
- Accuracy depends on how well the input features match real-world laptop models.

---

## Accuracy (Honest Estimate)

- R² score: Around 0.75 to 0.8 depending on the random data split.
- Works better for mid-range laptops than for very budget or very premium models.
- Price error can range between €100 and €800 in some cases.

---

## Purpose

This project is primarily for learning purposes, helping to practice data preprocessing, feature engineering, regression modeling, and similarity matching. While some parts were inspired by tutorials, it helps understand how machine learning pipelines work in practical scenarios.

---

Feel free to explore, modify, and improve the model!
