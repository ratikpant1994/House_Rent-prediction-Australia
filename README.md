🏡 House Rent Prediction - Suburban Australia
This repository contains the code, models, and report for a machine learning project predicting weekly house rental prices across suburbs in Australia. The project was commissioned by Brick Over Brick, a real estate firm aiming to enhance pricing strategies using predictive analytics.

🧠 Business Problem
Brick Over Brick sought a robust forecasting system to predict weekly rental prices based on property features. Accurate rent prediction would:

Help landlords price competitively.

Provide transparency and fairness to tenants.

Guide investors to target high-rent areas.

📊 Dataset
The dataset consisted of rental listings including:

Suburb

Number of bedrooms and bathrooms

Floor area (sq ft)

Furnishing status

Advertised month

🔧 Data Preprocessing
Steps included:

Outlier removal: Based on IQR, removing extreme rent and floor area values.

Missing value imputation: Mean imputation grouped by suburb.

Encoding: One-hot encoding of categorical variables (e.g. suburb, month).

Feature engineering:

AvgRent_Bath_Bed: Avg rent for bath-bedroom combos.

Level: Separated into current and total levels.

Seasonal effects from months.

Scaling: StandardScaler applied for KNN and distance-based models.

🧪 Models and Evaluation
We built and compared the following models:

Model	Validation RMSE	Test RMSE	Month 7 RMSE
Linear Regression (Base)	26.14	30.69	463.00
ElasticNet (α=0.09, L1=0.45)	27.14	40.17	76.00
KNN (k=5, p=1)	22.10	35.50	70.00
✅ Final Model: KNN (k=5, Manhattan Distance)
Best generalization on unseen data (Month 7).

84.78% improvement over baseline RMSE (from 463 → 70).

Handled non-linear relationships and local data distributions effectively.
