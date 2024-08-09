# Health Insurance Premium Predictor

## Goal: 

Given a dataset containing client information of Age, Sex, BMI, # of Children, Smoker status, Region; we want to be able to predict their health insurance charges. This is beneficial to insurance companies as it allows them to assess the risk of taking this client on and better proceed on a course of action.

### Summary Statistics

![image](https://github.com/cam-leo/HealthPredict/blob/main/Assets/Dashboard%201.png)

Age: The age of individuals in the dataset ranges from 18 to 64 years.

Children: The number of children covered under the insurance policy ranges from 0 to 5.

BMI: The most common BMI is 28-30

Sex: The distribution seems to be around 54% male, 46% female

Charges: Most common charge amount is ~ 5k

### Model Predictions

|   Original Values |   Predicted (Initial) |   Predicted (GridSearchCV) |   Predicted (RandomizedSearchCV) |
|------------------:|----------------------:|---------------------------:|---------------------------------:|
|           9095.07 |               9101.46 |                   10306.1  |                         10263.4  |
|           5272.18 |               5568.86 |                    5833.43 |                          5796.24 |
|          29331    |              27929.1  |                   27360.6  |                         27294.6  |
|           9301.89 |              12174.8  |                   10208.6  |                         10538.8  |
|          33750.3  |              35036.5  |                   34799    |                         34834.2  |

### Model Evaluations

| Model                                    |   Mean Squared Error |   R-squared |
|:-----------------------------------------|---------------------:|------------:|
| Initial RandomForestRegressor            |          2.47379e+07 |    0.840656 |
| GridSearchCV RandomForestRegressor       |          2.08331e+07 |    0.865808 |
| RandomizedSearchCV RandomForestRegressor |          2.0245e+07  |    0.869596 |


![image](https://github.com/user-attachments/assets/720b5c15-6bd2-4f20-895a-bf616cfa75c7)


### Synthetic Data Generation Model Predictions

|   Original Values (Synthetic) |   Predicted (Initial) |   Predicted (GridSearchCV) |   Predicted (RandomizedSearchCV) |
|------------------------------:|----------------------:|---------------------------:|---------------------------------:|
|                      36219.4  |              36463    |                   36353.9  |                         36335.3  |
|                      13831.1  |              13976.8  |                   13816.2  |                         13834.6  |
|                       9964.06 |               9964.06 |                    9964.06 |                          9964.06 |
|                       7742.11 |               7742.11 |                    7769.73 |                          7822.11 |
|                      18223.5  |              18189.3  |                   18223.5  |                         18221.7  |

| Model                                                |   Mean Squared Error |   R-squared |
|:-----------------------------------------------------|---------------------:|------------:|
| Initial RandomForestRegressor (Synthetic)            |               793657 |    0.994514 |
| GridSearchCV RandomForestRegressor (Synthetic)       |               781592 |    0.994598 |
| RandomizedSearchCV RandomForestRegressor (Synthetic) |               775881 |    0.994637 |

![image](https://github.com/user-attachments/assets/06dede5c-9ec0-4160-b951-c99258c485cc)
