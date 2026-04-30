Project Overview

This project focuses on building a regression-based machine learning system to forecast the number of seats likely to be sold per ride. The system is designed to help transportation providers make informed decisions regarding capacity planning, pricing, and scheduling.

Objectives
Optimize fleet and seat allocation
Reduce overbooking and underutilization
Improve operational efficiency
Enable data-driven transport planning
Visualize demand patterns for better insights
Workflow
Data Loading and Preprocessing
Imported required libraries for data processing, modeling, evaluation, and visualization
Loaded dataset: train_final.csv
Aggregated passenger-level data into ride-level features using ride_id
Feature Engineering
Created time-based features (hour, day, month)
Generated route and slot identifiers
Built interaction features such as fuel × distance
Added booking behavior metrics like urgency and lead time
Incorporated weekend and holiday indicators
Encoding Techniques
Applied label encoding for categorical variables
Implemented K-Fold smoothed mean encoding to capture historical demand patterns and reduce overfitting
Feature Enhancement
Created additional interaction features:
demand × time
fare × distance
lead time × slot
Model Training
Linear Models
Linear Regression
Ridge
Lasso
ElasticNet
Huber
Distance-Based Models
K-Nearest Neighbors (KNN)
Support Vector Regression (SVR)
Tree-Based Models
Decision Tree
Ensemble Models
Random Forest
Bagging
Extra Trees
Boosting Models
Gradient Boosting Machine (GBM)
AdaBoost
XGBoost
LightGBM
CatBoost
Model Evaluation

Models were evaluated using:

R² Score
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)

Additional evaluation included:

Learning curves for boosting and ensemble models
Iterative performance tracking using staged predictions
Visualization

The following visualizations were generated:

Predicted vs Actual plots
Model comparison charts (R², MAE, RMSE, ranking)
Learning curves for ensemble and boosting models
Feature importance dashboards
Key Insights
Time-Based Demand Patterns

Passenger demand varies significantly with hour, day of the week, and month. Peak demand is consistently observed during morning and evening hours, indicating strong commuter patterns.

Impact of Weekends and Holidays

Features such as is_weekend, is_holiday, and is_school_hol show noticeable variations in demand during non-working days. Weekend demand is less predictable and often reflects leisure travel behavior.

Route and Location Importance

Encoded features such as route, travel_from, and slot-based encodings are among the most important predictors. This highlights the importance of location-specific travel behavior.

Booking Behavior Influence

Variables such as booking urgency, ticket lead time, and lead spread significantly impact demand predictions. Shorter booking lead times are associated with higher demand variability.

Model Performance

Ensemble and boosting models such as XGBoost, LightGBM, Random Forest, and CatBoost outperform linear and distance-based models, indicating strong non-linear relationships in the data.

Importance of Feature Engineering

Interaction features (e.g., fuel × distance, slot × week, lead × holiday) significantly improve model performance, showing that demand is influenced by combined feature effects.

Effectiveness of Mean Encoding

Smoothed target encoding features such as slot_mean, route_mean, and origin_mean effectively capture historical demand patterns and improve prediction accuracy.

External Factors

Variables such as fuel price, weather conditions, distance, and competition have some influence on demand, though less significant than time and route-based factors.

Model Consistency

Top-performing models produce consistent predictions, indicating stable patterns and reliable learning.

Conclusion:
Passenger demand is influenced by a combination of time-based patterns, route characteristics, booking behavior, and seasonal effects. Demand is not driven by a single factor but by complex interactions between multiple variables.

Future Improvements:
Incorporate real-time data
Explore deep learning approaches such as LSTM for time-series forecasting
Deploy as a web-based dashboard
Integrate pricing optimization strategies
