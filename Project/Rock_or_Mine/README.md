# Goal: Use logistic model to classify rock and mine.
---
## Purpose and Audience:
- This project aims to classify rock and mine by using logistic model.
- To minimize undetected mine, since it is explosive -> maximize recall while balancing precision

*This project is only for self-pratice purpose

## Data Preprocessing:
- Replace "R" to 0, and "M" to 1 for better model interpretation
- Scale the data using StandardScaler

## Model:
- The pipeline includes StandardScaler and LogisticRegression

## Model Performance:
              precision    recall  f1-score   support

           0       0.71      0.50      0.59        20
           1       0.64      0.82      0.72        22

    accuracy                           0.67        42
   macro avg       0.68      0.66      0.65        42
weighted avg       0.68      0.67      0.66        42

- The positive recall is high (less undetected mine)
- The precision is quite low

## Issues:
- High negative recall, and low positive precision -> Lots of rock may be misclassified as mine

## Need Improvements:
- Add hyperparameter tuning may end up better
- Add more data
