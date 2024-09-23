# ICO Success Prediction Using Machine Learning

## Overview
This project applies machine learning techniques to predict the success of Initial Coin Offerings (ICOs). Using historical ICO data, the models developed in this project aim to help investors and developers predict whether an ICO will successfully reach its fundraising goal. The analysis includes data preprocessing, feature engineering, and the evaluation of several classification algorithms to determine the best model for predicting ICO success.


## Dataset
The dataset consists of **2,767 ICO campaigns** with **16 variables** detailing various attributes of each fundraising project, such as:

- **priceUSD**: Coin price in USD
- **teamSize**: The size of the team behind the ICO
- **platform**: The blockchain platform the ICO is based on (e.g., Ethereum, NEO)
- **rating**: Rating of the ICO
- **success**: A binary indicator of whether the ICO succeeded in reaching its goal

## Models Evaluated
The following machine learning models were tested to predict ICO success:

- **Logistic Regression** (Best-performing model with hyperparameter tuning)
- **Random Forest**
- **Gradient Boosting**
- **Support Vector Machines (SVM)**
- **K-Nearest Neighbors (KNN)**
- **Decision Trees with AdaBoost**

## Best Model: Logistic Regression
After testing and tuning the models, **Logistic Regression** was selected as the best model for ICO success prediction due to its high accuracy and balanced performance between precision and recall.

### Model Performance

| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression   | 67.87%   | 0.56      | 0.43   | 0.49     |
| Random Forest         | 66.61%   | 0.54      | 0.40   | 0.46     |
| Gradient Boosting     | 66.97%   | 0.55      | 0.39   | 0.46     |
| SVM (Linear)          | 67.51%   | 0.53      | 0.37   | 0.44     |
| KNN                   | 60.46%   | 0.44      | 0.40   | 0.42     |
| Decision Trees (AdaBoost) | 63.54%   | 0.48      | 0.38   | 0.43     |

## How It Works

### Data Preprocessing
- Missing values were handled using median imputation for numerical columns like `teamSize` and `priceUSD`.
- Outliers were identified and handled via log transformations.
- New features like `campaignDuration` were engineered, and categorical variables like `platform` were label-encoded.

### Model Training and Evaluation
- The dataset was split into training and testing sets, with models trained on the training data and evaluated on the test data.
- `GridSearchCV` was used to perform hyperparameter tuning on certain models like Logistic Regression and Gradient Boosting to optimize performance.

### Results
- The Logistic Regression model achieved the highest accuracy of **67.87%**, with a balanced precision, recall, and F1-score, making it the best choice for predicting ICO success.

## Limitations and Future Work
- The model recall is less than 50%, meaning it may miss successful ICOs, which could mislead investors.
- The dataset consists of historical data and may not fully capture future market trends or changes in the blockchain ecosystem.
- A larger and more diverse dataset could improve the generalization of the model.

## Future Enhancements
- Increase dataset size and include more features related to market conditions.
- Explore more advanced machine learning models such as deep learning for better performance.
- Implement continuous model updates to adapt to market changes.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes or improvements.

