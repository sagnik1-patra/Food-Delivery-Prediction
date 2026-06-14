
# Food Delivery Fast vs Delayed Classification Report

## Objective

The objective of this project is to predict whether a food delivery will be Fast or Delayed using features such as customer location, restaurant location, distance, weather conditions, traffic conditions, vehicle type, ratings, order cost, and other delivery-related features.

This is a binary classification problem where:

- 0 = Fast Delivery
- 1 = Delayed Delivery

## Dataset

Input Dataset:

C:\Users\NXTWAVE\Downloads\Food Delivery Prediction\Food_Delivery_Time_Prediction.csv

Total Records After Cleaning:

200

Total Features Used:

16

## Target Creation

The delivery status was created using the median delivery time.

Median Delivery Time Threshold:

72.775

Deliveries greater than this threshold were marked as Delayed, while deliveries less than or equal to this threshold were marked as Fast.

## Models Used

Three classification models were trained and evaluated:

1. Gaussian Naive Bayes
2. K-Nearest Neighbors
3. Decision Tree Classifier

## Model Performance

        Model  Accuracy  Precision  Recall  F1_Score
  Naive Bayes      0.45     0.4375    0.35  0.388889
          KNN      0.60     0.6000    0.60  0.600000
Decision Tree      0.45     0.4500    0.45  0.450000

## Best Model

The best model based on F1-score is:

KNN

## Insights

### Naive Bayes

Naive Bayes is simple and fast. It performs well when features are conditionally independent, but it may not capture complex non-linear relationships.

### KNN

KNN can perform well when similar deliveries have similar outcomes. However, it is sensitive to scaling and may become slower on larger datasets.

Best KNN Parameters:

{'metric': 'euclidean', 'n_neighbors': 5, 'weights': 'uniform'}

### Decision Tree

Decision Tree is highly interpretable and can capture non-linear patterns. It also helps identify important features affecting delayed deliveries.

Best Decision Tree Parameters:

{'criterion': 'gini', 'max_depth': 4, 'min_samples_leaf': 2, 'min_samples_split': 15}

## Recommendation

The recommended classifier is KNN, as it achieved the best F1-score among all models.

If interpretability is important, Decision Tree is preferred because it explains which features contribute most to delay prediction.

## Generated Files

- preprocessed_scaled_food_delivery_data.csv
- model_comparison_results.csv
- food_delivery_predictions.csv
- decision_tree_feature_importance.csv
- naive_bayes_model.pkl
- knn_model.pkl
- decision_tree_model.pkl
- standard_scaler.pkl
- label_encoders.pkl
- confusion matrix graphs
- ROC curve graphs
- model comparison graph
- decision tree visualization
