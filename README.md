Titanic Data Preprocessing – Step by Step

1. Importing and Exploring the Dataset

      The Titanic dataset is loaded for analysis.
      
      First, you check the first few rows to get a preview.
      
      Then, you inspect the data types (numerical, categorical, text) and see how many missing values each column has.
      
      This step helps you understand the structure of the dataset and where problems (like missing data) exist.

2. Handling Missing Values
  
      The Age column is often missing for many passengers. These gaps are filled using the median value, which is less sensitive to extreme values compared to the mean.
      
      The Embarked column (the port where passengers boarded) has a few missing values. These are filled with the most common port (the mode).
      
      The Cabin column usually has too many missing entries, so instead of trying to fill it, it’s completely removed.
      
      After this step, the dataset no longer has problematic missing values.

3. Encoding Categorical Variables

      Machine learning models can’t understand text, so categorical variables are converted into numbers.
      
      For example, Sex is converted into 0 (male) and 1 (female).
      
      The Embarked column is converted into dummy variables (one column per port), which allows the model to treat each embarkation point as a separate feature.

4. Normalizing Numerical Features

      Features like Age, Fare, number of siblings/spouses, and number of parents/children are on very different scales.
      
      These are standardized so they all have the same mean (0) and standard deviation (1).
      
      This prevents features with large values (like Fare) from dominating features with smaller values (like SibSp).

5. Detecting and Removing Outliers

      Boxplots are drawn for numerical features to visually check for extreme outliers.
      
      Then, an outlier detection method (the Interquartile Range method) is applied: values that fall far below or far above the typical range are removed.
      
      This ensures that extreme, unusual values don’t distort the model’s learning process.

6. Final Cleaned Dataset

      After cleaning, imputing, encoding, scaling, and outlier removal, the dataset is now consistent and ready to be used for machine learning.
      
      At this point, you can split the data into training and testing sets and apply models like Logistic Regression, Decision Trees, or Random Forests to predict survival.
