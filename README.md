# 1. Age 📅
The "Age" column tells us how old each person is, ranging from 18 to 72 years in the cleaned data. Age influences health insurance costs, as older people may require more medical care.

# 2. Gender 👨‍👩‍👧‍👦
This column shows if a person is "Male" or "Female." Gender affects insurance premiums since men and women may have different health risks.

# 3. Region 🌍
The "Region" column indicates where a person lives: "Southeast," "Northeast," "Southwest," or "Northwest." Healthcare costs vary by region, impacting insurance premiums.

# 4. Marital Status 💍
This field shows whether someone is "Married" or "Unmarried." Married individuals might receive discounts or different rates due to shared policies or varied health risks.

# 5. Physical Activity 🏃‍♂️
The "Physical Activity" column rates activity levels as "Low," "Medium," or "High." Active people tend to have lower premiums since they are often healthier.

# 6. Stress Level 😰
Stress levels are categorized as "Low," "Medium," or "High." High stress can lead to more health problems, potentially increasing insurance costs.

# 7. Number of Dependents 👶
This column indicates how many dependents (children or elderly parents) an individual supports. More dependents can affect insurance choices and premiums.

# 8. BMI Category 🏋️‍♀️
Body Mass Index (BMI) categories include "Normal," "Overweight," "Obesity," and "Underweight." A "Normal" BMI often results in lower premiums, as it suggests better health.

# 9. Smoking Status 🚬
This shows if someone is a "No Smoking," "Occasional," or "Regular" smoker. Smokers usually face higher premiums due to the health risks linked to smoking.

# 10. Employment Status 💼
This field shows if someone is "Self-Employed," a "Freelancer," or "Salaried." Employment status impacts income stability, which may influence insurance coverage choices.

# 11. Income Level and Income in Lakhs 💰
Income levels are categorized as "<10L," "10L - 25L," "25L - 40L," and ">40L" (1 lakh = 100,000). Income affects what insurance plans individuals can afford.

# 12. Medical History 🏥
This includes any health conditions like "High blood pressure," "Thyroid," "Diabetes," or "No Disease." Medical history helps insurers assess health risks and set premiums.

# 13. Insurance Plan 📋
Insurance plans are categorized as "Bronze," "Silver," or "Gold." Bronze plans have lower premiums but higher out-of-pocket costs, while Gold plans offer better coverage with higher premiums.

# 14. Annual Premium Amount 💵
This is the yearly cost a person pays for their insurance plan. The premium depends on factors like age, health, and plan type.

# 15. Data Cleaning and Handling Missing Values 🧹
Missing data (e.g., smoking status or employment status) was handled by filling in with the most common value (mode) to ensure complete records.

# Feature Engineering 🛠️
# 16. Encoding Categorical Variables 🧬
Categorical variables like "gender," "region," and "BMI category" were converted to numerical values for machine learning models.

Methods:

One-Hot Encoding: Used for variables without inherent order (e.g., "region" becomes "region_Southeast," "region_Northeast," etc.).
Label Encoding: Used for ordinal variables (e.g., "insurance plan" is encoded as Bronze = 1, Silver = 2, Gold = 3).
# 17. Creating a Risk Score from Medical History ⚕️
A risk score was created based on a person’s medical history by assigning scores to different diseases (e.g., Diabetes = 6, Heart Disease = 8). The total score was normalized to a range of 0 to 1.

# 18. Transforming Numerical Features 📉
Numerical features like "age," "income in lakhs," and "number of dependents" were normalized using a MinMaxScaler to improve model performance.

# 19. Combining Features to Create Interaction Terms 🔄
Interaction terms were created by combining features, like "stress level" and "physical activity," to capture the relationships between them.

# 20. Binning Continuous Variables 📊
Continuous variables like "age" were grouped into categories (e.g., Young = 18-30, Middle-aged = 31-50, Senior = 51+), which helps reduce the effect of outliers.

# 21. Handling Multi-Collinearity with Variance Inflation Factor (VIF) 📉
VIF was used to detect and remove features that were highly correlated with others, improving model performance.

# 22. Feature Selection for Model Training 🎯
After feature engineering, techniques like Recursive Feature Elimination (RFE) were used to identify the most important features for training the model.

 # Model Training and Predictions 🤖
Various models like Linear Regression, Ridge Regression, and XGBoost were used to predict annual premium amounts.

 # Error Analysis 🔍
Error analysis helped identify where the model made accurate or inaccurate predictions, providing insights for improving the model.
