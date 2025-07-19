# Wine Quality Prediction 

This project focuses on building a machine learning model to predict the quality of red wine based on various physicochemical features. Using the **Random Forest Classifier**, we aim to classify wines into *good* or *bad* categories based on their attributes.

## Dataset

The dataset used is `winequality-red.csv`, which contains 1599 samples and 12 columns:

- **Features**:
  - fixed acidity
  - volatile acidity
  - citric acid
  - residual sugar
  - chlorides
  - free sulfur dioxide
  - total sulfur dioxide
  - density
  - pH
  - sulphates
  - alcohol
- **Target**: `quality` (integer score from 0–10)

##  Workflow

### 1. **Data Collection & Preprocessing**
- Loaded the dataset using `pandas`
- Checked for null values (none were found)
- Performed exploratory data analysis (EDA) using `matplotlib` and `seaborn`
- Analyzed feature distributions and correlations with wine quality
- Applied label encoding to the `quality` column:  
  - Quality ≥ 6 → `1` (Good Quality)  
  - Quality < 6 → `0` (Bad Quality)

### 2. **Exploratory Data Analysis**
- Bar plots to understand the impact of `citric acid` and `volatile acidity` on wine quality
- Heatmap of feature correlations

### 3. **Model Training**
- Split the data into training and testing sets (80%-20%)
- Trained a **RandomForestClassifier** from scikit-learn

### 4. **Evaluation**
- **Training Accuracy**: 100%
- **Testing Accuracy**: 82.19%
- The model slightly overfits the training data but still performs well on the test set.

### 5. **Prediction System**
- Built an input interface for custom predictions using manually entered wine properties
- Example inputs are reshaped and passed to the model for quality classification

##  Key Findings

- Higher citric acid levels are associated with better quality
- Lower volatile acidity corresponds to higher quality
- Alcohol and sulphates also have a positive correlation with wine quality

##  Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (RandomForestClassifier, train_test_split, accuracy_score)


##  Conclusion

This project successfully demonstrates a simple yet effective machine learning pipeline to predict wine quality. With further optimization and feature engineering, this model can be expanded for more granular multi-class classification and deployment.
