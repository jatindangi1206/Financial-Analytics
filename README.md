# Financial-Analytics
contains various models like cedit card fraud detection, financial modelling, etc



**Overview:**
This code is a simple implementation of a binary classification neural network using the Keras library in Python. The dataset used is related to churn modeling, where the goal is likely predicting customer churn (whether a customer will leave or not). The neural network is trained on features like credit score, age, tenure, balance, etc., and the target variable is whether the customer exited (1) or not (0).

**Code Explanation:**
1. **Data Loading:** The dataset is loaded using pandas from a CSV file named "Churn_Modelling_2.csv".

2. **Data Preprocessing:** The target variable `y` is extracted, and the input features `x` are obtained by excluding the target variable.

3. **Data Splitting:** The dataset is split into training and testing sets using `train_test_split` from sklearn.

4. **Standardization:** The input features are standardized using `StandardScaler` from sklearn.

5. **Neural Network Model Creation:**
   - The neural network is created using Keras, with a sequential model.
   - It has an input layer with 7 input dimensions (features) and two hidden layers with 4 units each, using the ReLU activation function.
   - The output layer has 1 unit with a sigmoid activation function since it's a binary classification problem.
   - The model is compiled using the Adam optimizer and binary cross-entropy loss function.

6. **Model Training:** The neural network is trained on the training set with 100 epochs and a batch size of 10.

7. **Model Evaluation:** The model accuracy and confusion matrix are evaluated on the test set.

8. **Cutoff Analysis:** A range of cutoff values (thresholds) are used to classify the predicted probabilities into binary outcomes (0 or 1). Accuracy is computed for each cutoff, and the results are stored in the `accuracy` list.

**Results:**
- The model is trained and achieves an accuracy of approximately 79.75% on the test set.
- The cutoff analysis shows the accuracy at different probability cutoffs, indicating how the model's performance varies with different classification thresholds. The accuracy remains constant at 79.75% for the cutoff values tested.

**Note:**
- The model training output (epoch-wise loss and accuracy) is displayed during training.
- The choice of cutoff value depends on the specific requirements of the application, and it's crucial to consider the trade-off between false positives and false negatives based on the problem context.
