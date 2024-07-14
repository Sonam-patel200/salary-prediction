# Salary Prediction
   - An end-to-end data science project I made as a machine learning intern @ Mentorness.
   - This project predicts employee salaries using advanced regression techniques and thorough data preprocessing. We compare multiple machine learning models to select the best-performing one, which is then integrated into a pipeline. This pipeline includes all necessary preprocessing steps, ensuring accurate predictions and easy deployment.

Steps performed: 
## 1. Exploratory Data Analysis
   - Gender Distribution: More females than males.
   - Unit Distribution: Most employees are in the `IT` department.
   - Designation Distribution: A significantly large population of analysts.
   - Age Trend: Older employees tend to have higher salaries.
   - Experience Trend: Higher experience correlates with higher salaries.
## 2. Data Preprocessing
   - **Encoding**: Ordinal Encoding for ordered categories and Label Encoding for unordered categories.
   - Dropped duplicates.
   - Checked for null values.
   - Imputed `DOJ`, `AGE`, and `RATINGS` columns with mode.
   - Imputed `LEAVES USED`, `LEAVES REMAINING` columns with median.
   - Dropped `FIRST NAME`, `LAST NAME` columns.
 ## 3. **Feature Engineering**
   - Converted DOJ and CURRENT DATE columns to datetime datatype.
   - Created a new feature: years_experience.
   - Dropped date columns.
## 4. **Feature Selection**:
   - Used SelectKBest to select best features.
   - Extracted selected feature names: `SEX`, `DESIGNATION`, `AGE`, `UNIT`, `PAST EXP`, `years_experience`.
   - Reassigned selected features to training and test datasets.
   - Conducted correlation study and dropped columns with correlation exceeding [-0.8, 0.8].
## 5. **Model Training and Evaluation**
   - **Trained models**: Linear Regression, Ridge, Lasso, Gradient Boosting, XGBoost, SVR, and KNN Regression. 
   - **Metrics**: Evaluated using MAE, MSE, RMSE, and R² score.
   - **Visualization**: Plotted metrics for comparison.
