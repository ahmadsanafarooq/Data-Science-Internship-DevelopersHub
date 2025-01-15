### 1. **Loading and Exploring the Dataset:**
   - The dataset is loaded from a CSV file using pandas. The read_csv() function is used to read the dataset, which is then stored in a DataFrame called data.
   - The head() method displays the first few rows of the dataset for inspection.
   - The value_counts() function is used to count how many "positive" and "negative" labels are present in the sentiment column.

### 2. **Mapping Sentiment Labels:**
   - The sentiment labels ("positive" and "negative") are mapped to numerical values. "positive" is converted to 0, and "negative" is converted to 1. This step is necessary for machine learning algorithms, as they typically work with numerical data.

### 3. **Text Preprocessing:**
   - **Lowercasing**: A function is defined to convert all text in the review column to lowercase. This ensures that the model treats words like "Good" and "good" as the same.
   - **Removing Stopwords**: Using the nltk library, a list of common English stopwords (such as "the", "is", "in") is retrieved. A function is applied to the review column that splits the text into words, filters out any stopwords, and then joins the words back into a cleaned-up sentence.
   - **Removing Special Characters**: A custom function is written to remove any non-alphanumeric characters from the review text. It loops through each character and keeps only the alphanumeric ones.
   - **Removing HTML Tags**: The re (regular expressions) library is used to remove any HTML tags from the review text (such as <br>, <p>, etc.). This ensures the text is clean for further processing.

### 4. **Text Vectorization:**
   - The CountVectorizer from sklearn is used to convert the text data into a matrix of token counts. This is a form of **text vectorization**, where each word in the review is represented as a feature in the model. The fit_transform() method is applied to the review column, transforming the text into numerical features.

### 5. **Train-Test Split:**
   - The dataset is split into training and testing sets using train_test_split() from sklearn. Typically, 80% of the data is used for training and 20% for testing. This ensures that the model is trained on one subset of the data and evaluated on a separate, unseen subset.

### 6. **Model Training and Prediction:**
   - A **Logistic Regression** model is created and trained using the fit() method on the training data. This model is used for binary classification (positive vs. negative).
   - After training, the model is tested by making predictions on a sample input ("movie is excellent") to see how well it performs on new data.
   - The model's performance is evaluated using model.score(), which calculates the accuracy on the test data.

### 7. **Performance Evaluation:**
   - **Accuracy**: The accuracy score is calculated using accuracy_score() from sklearn, which compares the predicted labels with the actual labels in the test set.
   - **Precision and Recall**: The precision_score() and recall_score() functions are used to calculate precision and recall. These metrics are useful for understanding how well the model handles false positives and false negatives.
     - **Precision**: Measures how many of the predicted positive reviews are actually positive.
     - **Recall**: Measures how many of the actual positive reviews the model successfully identified.

### 8. **Visualization:**
   - A bar chart is generated using matplotlib to visualize the model's performance metrics: accuracy, precision, and recall. Each metric is displayed on the y-axis, and the corresponding score is shown for easy comparison.
   - The bar chart helps to visually assess how well the model is performing in terms of its key metrics.
