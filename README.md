# WindTurbine_Failure_Prediction_EnsembleMethods_HyperparamterTuning

## Summary
<p align="justify"> This project presents a ML based solution to a renewable energy resource company that is looking to reduce its cost for repairing generators on wind turbines. Sensors fitted across different machines involved in the wind energy generation collect various environmental and machinery data that has been provided to predict machine failure ahead of time. The main goal was to predict machine failure ahead of time as replacement costs after failure are significantly more expensive compared to inspection and repair cost before failure. </p>

<p align="justify"> Dataset had several missing values which were imputed using median values. Given the problem, the goal was to maximize the recall metric to minimize false negatives as maintenance costs are highest for replacement where machine failure despite the model predicting no failure. Due to signficant class imbalance, ML models were built with oversampled minority class and undersampled majority class along with models built on original data. </p>

<p align="justify"> A number of classification based ML models were employed including Random Forest Classifier, Gradient Boosting classifier and XG Boost classifier amongst other tree-based, bagging and boosting models. Because of highly time intensive model executions, a number of models with high cross validation scores and generalizable performance were selected for hyperparameter tuning. RandomizedSearchCV were employed compared to GridSearch to save computation time. XGBoost Classifier model trained on the original data was selected as the final model with emphasis given on recall, generalizability in terms of performance metrics such as recall, F1 score as well as total computation time. A pipeline was built for the final selected model to help automate the predictions for further use.</p>

## Context 
<p align="justify"> Renewable energy sources play an increasingly important role in the global energy mix, as the effort to reduce the environmental impact of energy production increases. Out of all the renewable energy alternatives, wind energy is one of the most developed technologies worldwide. The U.S Department of Energy has put together a guide to achieving operational efficiency using predictive maintenance practices.</p>

<p align="justify"> Predictive maintenance uses sensor information and analysis methods to measure and predict degradation and future component capability. The idea behind predictive maintenance is that failure patterns are predictable and if component failure can be predicted accurately and the component is replaced before it fails, the costs of operation and maintenance will be much lower.The sensors fitted across different machines involved in the process of energy generation collect data related to various environmental factors (temperature, humidity, wind speed, etc.) and additional features related to various parts of the wind turbine (gearbox, tower, blades, break, etc.).</p>



## Objective
A company working on improving the machinery/processes involved in the production of wind energy using machine learning and has collected data of generator failure of wind turbines using sensors. They have shared a ciphered version of the data, as the data collected through sensors is confidential (the type of data collected varies with companies). Data has 40 predictors, 40000 observations in the training set and 10000 in the test set.

The objective is to build various classification models, tune them, and find the best one that will help identify failures so that the generator could be repaired before failing/breaking to reduce the maintenance cost. The different costs associated with maintenance are as follows:

- `Replacement cost = $40,000`
- `Repair cost = $15,000`
- `Inspection cost = $5,000`

“1” in the target variables should be considered as “failure” and “0” will represent “No failure”.

## Data Description
- The data provided is a transformed version of original data which was collected using sensors.
- Train.csv - To be used for training and tuning of models. 
- Test.csv - To be used only for testing the performance of the final best model.
- Both the datasets consist of 40 predictor variables and 1 target variable
