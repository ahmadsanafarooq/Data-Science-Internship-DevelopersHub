The task involves performing data preprocessing, model training, and evaluation. Here's a brief explanation:

1. **Data Preprocessing**:
   - **Missing Values**: The dataset is checked for missing values, and any missing values in the rm column (average number of rooms) are filled with the mean of the existing values.
   - **Normalization**: The numerical features of the dataset are normalized using **StandardScaler**. This ensures all features are on the same scale, improving model performance.
   - **Data Splitting**: The data is divided into two sets: one for training the model and another for testing it.

2. **Model Training**:
   - A **Linear Regression** model is trained using the training set to learn the relationship between the input features and the target variable (medv, median house value).

3. **Model Evaluation**:
   - The model’s performance is evaluated by predicting house values on the test set and calculating the **Root Mean Squared Error (RMSE)**. This metric measures how well the model's predictions match the actual values.

4. **Visualization**:
   - **Scatter Plot**: A scatter plot is used to compare actual vs. predicted values, with an ideal line showing perfect predictions.
   - **Residuals Plot**: A histogram of residuals (differences between actual and predicted values) is plotted to check for any patterns or biases in the errors.
   - **RMSE Bar Chart**: A bar chart displays the RMSE value, giving a quick overview of the model's error.
