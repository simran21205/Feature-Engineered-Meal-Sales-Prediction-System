# Feature Engineered Meal Sales Prediction System

This project leverages Machine Learning to predict daily meal sales and foot traffic at IIIT Delhi’s dining facilities. By analyzing historical sales, coupon data, and menu offerings, the project provides actionable insights to optimize food supply and minimize wastage in an institutional setting.

**Project Overview**

The primary goal was to develop a predictive framework for three target variables:

  1. Paytm + Cash Sales: Direct daily transactions. 
  2. Coupon Usage: Meals redeemed via pre-paid student coupons.
  3. Total Attendance: The combined sum of all meal types.

**Tech Stack**
  1. Languages: Python
  2. Libraries: Scikit-Learn, TensorFlow/Keras, Pandas, NumPy, Matplotlib, Seaborn 
  3. Models: Linear Regression, Random Forest Regressor, Support Vector Regressor (SVR), and Neural Networks (MLP) 

**Feature Engineering**

A significant portion of this project focused on transforming raw data into high-utility features to capture student behavior:
  1. Temporal Features: Derived weekday and month data to account for weekly cycles and seasonal trends.
  2. Academic Context: Integrated "Semester Type" (Academic vs. Vacation) and a "Holiday" counter to model student departures during breaks.
  3. Menu Item Encoding: Implemented One-Hot Encoding for 122 unique menu items, allowing the model to weigh the popularity of specific dishes (e.g., Dal Makhni vs. Matar Kulcha).
  4. Coupon Dynamics: Tracked monthly cumulative coupon sales to predict the likelihood of use in a given meal.

**Key Results & Analysis**

Feature Impact: One-Hot Encoding the menu was a strategic refinement that significantly captured variations in mess attendance.

Model Performance:
  1. Random Forest: Performed best for simpler relationships like Paytm+Cash sales.
  2. SVR: Demonstrated superior performance for complex, non-linear patterns in coupon usage.
  3. Neural Networks: Successfully reduced overfitting using Dropout layers and L2 Regularization, maintaining a balance between training and testing error.
  4. Validation: Sales dips aligned perfectly with labeled holiday breaks (Winter/Summer breaks), validating the data's integrity.

**Learnings**
  1. Demonstrated the critical role of domain knowledge in feature engineering.
  2. Identified the "Curse of Dimensionality" when one-hot encoding high-cardinality features like menu items.
  3. Balanced model interpretability with predictive accuracy across different regression architectures
