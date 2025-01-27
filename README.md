# Churn_Prediction

## Project Overview
This project focuses on analyzing and predicting customer churn for a telecommunications company. By utilizing customer demographic information, service subscriptions, and account details, we aim to uncover key patterns related to churn and build predictive models to assist in proactive customer retention strategies.

## Dataset Description
The dataset contains detailed information about telecom customers and their behaviors, including:
- **Demographic Information**: Gender, partner status, dependents, etc.
- **Service Subscriptions**: Phone services, internet services, multiple lines, etc.
- **Account Details**: Contract type, payment method, tenure, monthly charges, paperless billing, etc.
- **Churn Indicator**: A binary column indicating whether the customer churned (`Yes`/`No`).

### Key Insights from Data Analysis:
- **Churn Patterns**:
  - Higher churn rates among customers with:
    - **Month-to-month contracts**
    - **Electronic check payment methods**
    - **Paperless billing**
  - Gender does not significantly affect churn.
- A significant proportion of customers in the dataset have churned, leading to an **imbalanced dataset** where churned customers represent a smaller proportion. 

### Data Preprocessing:
1. **Binary Columns**: Converted to numerical values (0 and 1) for analysis.
2. **Categorical Columns**: Transformed into dummy variables for compatibility with machine learning models.
3. **Data Splitting**: Dataset split into:
   - **Training Set**: 64%
   - **Validation Set**: 16%
   - **Test Set**: 20%

## Model Development
Three models were trained to predict customer churn:
- **Loss Function**: Binary Cross-Entropy Loss, chosen for its suitability in binary classification tasks.
- **Evaluation Metrics**: Models were evaluated based on accuracy, precision, recall, and AUC-ROC to ensure robust performance.

## Future Improvements
- **Addressing Data Imbalance**: Since the dataset is imbalanced with a higher proportion of non-churned customers, future work should focus on using techniques to balance the dataset. Potential approaches include:
  - **Oversampling**: Using methods like SMOTE (Synthetic Minority Oversampling Technique) to generate synthetic examples for the minority class.
  - **Undersampling**: Reducing the size of the majority class to create a balanced dataset.
  - **Class Weights**: Assigning higher weights to the minority class during model training to emphasize its importance.
  - **Hybrid Methods**: Combining oversampling and undersampling for better results.

