# E-commerce Furniture Dataset 2024 - Sales Prediction Project

## 📅 Project Title:
**E-commerce Furniture Dataset 2024 - Predictive Analysis of Furniture Sales**

## 📚 Overview
This project focuses on predicting the number of furniture items sold based on their features such as price, title, and tag information. The dataset, sourced from AliExpress, contains 2,000 product entries and provides a solid foundation for applying data preprocessing, exploratory data analysis (EDA), and machine learning techniques.

## 🧪 Objective
To analyze and predict the sales performance (`sold`) of e-commerce furniture products using machine learning models based on available features like `price`, `tagText`, and `productTitle`.

## 📃 Dataset Summary
- **Source:** AliExpress (Scraped using Apify)
- **Entries:** 2,000 rows
- **Columns:**
  - `productTitle`: Name of the item
  - `originalPrice`: Original price (contains missing values)
  - `price`: Current selling price
  - `sold`: Number of units sold
  - `tagText`: Tag/Shipping info (e.g., "Free shipping")

## 🔧 Tools & Technologies
- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (Linear Regression, Random Forest Regressor)

## 🔄 Project Pipeline

### 1. Data Collection
Dataset was loaded using `pandas.read_csv()`.

### 2. Data Preprocessing
- Removed missing values and dropped the `originalPrice` column due to >75% nulls
- Converted `price` to float
- Encoded `tagText` using Label Encoding
- Simplified `tagText` into categories: `Free shipping`, `+Shipping: $5.09`, and `others`

### 3. Exploratory Data Analysis (EDA)
- Visualized the distribution of `price` and `sold`
- Analyzed correlation using scatterplots and pairplots
- Identified concentration of sales around low-cost and free-shipping items

### 4. Feature Engineering
- Created TF-IDF features from `productTitle`
- Merged TF-IDF vectors with the main dataset
- Dropped `productTitle` after encoding

### 5. Model Building
- Train-Test Split: 80/20
- Models Used:
  - Linear Regression
  - Random Forest Regressor (n_estimators=100)

### 6. Model Evaluation
- Evaluation Metrics:
  - Mean Squared Error (MSE)
  - R-squared Score (R2)
- Random Forest outperformed Linear Regression due to better handling of nonlinear data

### 7. Conclusion
Random Forest Regressor showed superior performance. Feature engineering, especially TF-IDF and tag encoding, contributed positively. The model can guide e-commerce platforms in optimizing listings, pricing, and marketing strategies.

## 🎓 Learnings
- Hands-on experience with real-world e-commerce data
- Importance of preprocessing and feature engineering
- Comparison of regression models
- Practical EDA skills and visualization techniques

## 👁️ Future Enhancements
- Hyperparameter tuning for Random Forest
- Incorporate NLP sentiment features from product reviews (if available)
- Build a Flask-based dashboard to visualize predictions

## 📅 Reference
- Dataset Source: AliExpress via Apify
- Image Credit: [Spacejoy on Unsplash](https://unsplash.com/@spacejoy)
- Project Code Sample: Adapted from Kaggle Python Notebook Structure

---

**Note:** This project is built for learning and showcasing data analytics & machine learning skills. Customize, enhance, and explain it confidently during interviews or academic submissions.

---

Feel free to fork or star the project on GitHub for collaboration or improvement!

