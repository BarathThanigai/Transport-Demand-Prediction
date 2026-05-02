Project Overview

This project focuses on building a regression-based machine learning system to forecast the number of seats likely to be sold per ride. The goal is to assist transportation providers in making informed decisions related to capacity planning, pricing strategies, and scheduling by leveraging historical data and predictive modeling.

Objectives

The primary objective of this project is to optimize fleet and seat allocation while reducing overbooking and underutilization. It also aims to improve operational efficiency, enable data-driven transport planning, and provide meaningful visualizations that reveal demand patterns and trends.

Workflow

The workflow begins with data loading and preprocessing, where essential libraries for data handling, modeling, evaluation, and visualization are imported. The dataset train_final.csv is loaded and passenger-level data is aggregated into ride-level features using the ride_id.

Feature engineering plays a crucial role in enhancing model performance. Time-based features such as hour, day, and month are extracted to capture temporal patterns. Route and slot identifiers are generated to represent travel segments, while interaction features such as fuel multiplied by distance are created to capture combined effects. Booking behavior is modeled using variables like urgency and lead time, and additional indicators such as weekends and holidays are incorporated.

Categorical variables are handled using label encoding, while K-Fold smoothed mean encoding is applied to capture historical demand patterns more effectively and reduce overfitting. Further feature enhancement is achieved by introducing interaction terms such as demand with time, fare with distance, and lead time with slot.

Model Training

A wide range of machine learning models are trained and evaluated to identify the best-performing approach. Linear models such as Linear Regression, Ridge, Lasso, ElasticNet, and Huber are used as baselines. Distance-based methods including K-Nearest Neighbors and Support Vector Regression are also explored.

Tree-based models such as Decision Trees provide non-linear modeling capabilities, while ensemble techniques including Random Forest, Bagging, and Extra Trees improve performance through aggregation. Boosting models such as Gradient Boosting Machine, AdaBoost, XGBoost, LightGBM, and CatBoost are employed to capture complex patterns and interactions in the data.

Model Evaluation

The models are evaluated using standard regression metrics including R² Score, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE). Additional evaluation techniques such as learning curves are used to analyze model performance over iterations, and staged predictions are applied particularly for boosting models to track improvements progressively.

Visualization

Various visualizations are generated to interpret model performance and data patterns effectively. These include predicted versus actual plots to assess accuracy, model comparison charts to rank models based on evaluation metrics, learning curves for ensemble and boosting techniques, and feature importance plots to identify the most influential variables.

Key Insights

The analysis reveals that passenger demand is highly dependent on time-based patterns, with consistent peaks observed during morning and evening hours, reflecting commuter behavior. Demand during weekends and holidays shows greater variability and is influenced more by leisure travel patterns.

Route-specific features such as travel origin, route identifiers, and slot encodings emerge as strong predictors, indicating that location plays a significant role in demand forecasting. Booking behavior variables, particularly urgency and lead time, significantly impact predictions, with shorter lead times leading to higher variability.

Ensemble and boosting models outperform simpler models, highlighting the presence of complex non-linear relationships in the data. Feature engineering, especially the use of interaction features, substantially improves model accuracy. Smoothed mean encoding effectively captures historical demand trends, further enhancing predictive performance. External factors such as fuel prices, weather conditions, and competition have some influence but are less significant compared to time and route-based features.

Conclusion

Passenger demand is influenced by a combination of temporal patterns, route characteristics, booking behavior, and seasonal effects. The findings indicate that demand is driven by complex interactions among multiple variables rather than a single dominant factor. The use of advanced machine learning models and feature engineering techniques enables accurate and reliable predictions.

Future Improvements

Future enhancements to this project include incorporating real-time data for dynamic predictions, exploring deep learning approaches such as LSTM models for time-series forecasting, deploying the system as an interactive web-based dashboard, and integrating pricing optimization strategies to further improve decision-making.

Tech Stack

The project is implemented using Python along with libraries such as Pandas and NumPy for data processing, Scikit-learn for machine learning, XGBoost, LightGBM, and CatBoost for advanced modeling, and Matplotlib and Seaborn for visualization.

Dataset

The dataset used in this project is train_final.csv, which contains aggregated ride-level information derived from passenger booking data.
