# Health Insurance Premium Predictor

## Goal: 

Given a dataset containing client information of Age, Sex, BMI, # of Children, Smoker status, Region; we want to be able to predict their health insurance charges. This is beneficial to insurance companies as it allows them to assess the risk of taking this client on and better proceed on a course of action.

### Summary Statistics

![image](https://github.com/cam-leo/HealthPredict/blob/main/Assets/Dashboard%201.png)

Age: The age of individuals in the dataset ranges from 18 to 64 years.

Children: The number of children covered under the insurance policy ranges from 0 to 5.


### Forest Regressor Model

|   Original Values |   Predicted Values (Initial) |
|------------------:|-----------------------------:|
|           9095.07 |                      9474.09 |
|           5272.18 |                      5723.26 |
|          29331    |                     28266.1  |
|           9301.89 |                     11309    |
|          33750.3  |                     34744.8  |

### Grid Search

|   Original Values |   Predicted Values (GridSearchCV) |
|------------------:|----------------------------------:|
|           9095.07 |                          10043.3  |
|           5272.18 |                           5790.37 |
|          29331    |                          27123    |
|           9301.89 |                          10382    |
|          33750.3  |                          34715.2  |

### Randomized Search

|   Original Values |   Predicted Values (RandomizedSearchCV) |
|------------------:|----------------------------------------:|
|           9095.07 |                                10117.1  |
|           5272.18 |                                 5819.87 |
|          29331    |                                27185.9  |
|           9301.89 |                                10196.2  |
|          33750.3  |                                34831.8  |

### Model Evaluations

| Model                                    |   Mean Squared Error |   R-squared |
|:-----------------------------------------|---------------------:|------------:|
| Initial RandomForestRegressor            |          2.40173e+07 |    0.845298 |
| GridSearchCV RandomForestRegressor       |          2.09626e+07 |    0.864974 |
| RandomizedSearchCV RandomForestRegressor |          2.01338e+07 |    0.870313 |


![image](https://github.com/user-attachments/assets/720b5c15-6bd2-4f20-895a-bf616cfa75c7)
