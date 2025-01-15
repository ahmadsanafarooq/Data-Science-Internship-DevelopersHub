This task involves **data cleaning** and **exploratory data analysis (EDA)** on the Titanic dataset. The main steps are as follows:

1. **Missing Values Handling**:
   - The code identifies columns with missing values and fills them using appropriate methods:
     - **Age**: Missing values in the Age column are filled with the mean value of the column.
     - **Embarked**: Missing values in the Embarked column are filled with the mode (most frequent value).
     - **Cabin**: Missing values in the Cabin column are filled with the mode.

2. **Checking for Duplicates**:
   - The dataset is checked for duplicate rows to ensure that there are no repeated entries, which could skew analysis or modeling.

3. **Exploratory Data Analysis (EDA)**:
   - **Categorical Data**: The code generates bar plots for each categorical variable (like Embarked, Sex, etc.) to visualize the distribution of values in these columns.
   - **Numerical Data**: The distribution of numerical variables (like Age, Fare, etc.) is visualized using histograms with KDE curves to understand the distribution of data.
   - **Correlation Heatmap**: A heatmap is created to visualize the correlation between numerical variables. This helps identify potential relationships or patterns in the data (e.g., how Fare correlates with Pclass).


