This is a beginner-friendly machine learning project that predicts the approximate price of a laptop based on its specifications.


Dataset Source:
The dataset was taken from Kaggle (laptop_price.csv).


What this project does:
Takes laptop specifications (RAM, weight, CPU frequency, screen resolution, brand, etc.) as input.
Predicts the estimated price of the laptop in Euros.
Shows a possible price range (±10%) to cover fluctuation.
Displays a few similar laptops from the dataset with their price and main features.


Technologies and libraries used:
pandas: for reading and cleaning the dataset
numpy: for numerical operations
seaborn and matplotlib: for data visualization
scikit-learn:
StandardScaler: for scaling features
train_test_split: to divide data into training and testing sets
RandomForestRegressor: to train the model for price prediction
cosine_similarity: to find similar laptops


How the code works (step-by-step):
Load the dataset from Kaggle.
Drop unnecessary columns and extract important info like screen width, height, CPU brand, frequency, etc.
Convert categorical features (like brand, type, OS) into numeric format using one-hot encoding.
Clean and convert RAM, memory size, and other fields into usable numeric values.
Choose the top features that affect price based on correlation.
Split the data and train a Random Forest model.
Use StandardScaler to normalize input features.


Create a function that:
Takes user input (RAM, weight, screen size, GPU, etc.)
Predicts price based on the model
Shows an estimated range
Finds and prints a few similar laptops


How to use:
Upload the dataset file (laptop_price.csv).
Run all code cells in order (preferably in Google Colab or VS Code with Python).
Enter laptop specs when asked.
The program will show you:
Estimated price
Price range
A few similar laptops from the dataset


Limitations:
The model is trained on an old dataset and may not reflect real 2023 or 2024 market prices.
Sometimes the prediction might be very off (more than €500-€800 difference).
Model performance is average — it’s not a commercial-level estimator.
Accuracy depends a lot on how well the features match real-world models.
Accuracy (honest estimate):
R² score: around 0.75 to 0.8 depending on random data split
Works better for mid-range laptops than extreme budget or premium ones
Price error can range from €100 to €800 in some cases


Purpose:
This is a learning project to practice data preprocessing, feature engineering, regression, and similarity matching.
Even though some parts were copied or inspired by tutorials, this still helps you understand how machine learning pipelines work in real scenarios
