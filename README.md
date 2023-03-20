# WindTurbine_Failure_Prediction_EnsembleMethods_HyperparamterTuning

## Summary
<p align="justify"> This project presents a ML based solution to a renewable energy resource company that is looking to reduce its cost for repairing generators on wind turbines. Sensors fitted across different machines involved in the wind energy generation collect various environmental and machinery data that has been provided to predict machine failure ahead of time. The main goal was to predict machine failure ahead of time as replacement costs after failure are significantly more expensive compared to inspection and repair cost before failure. </p>

<p align="justify"> Dataset had several missing values which were imputed using median values. Given the problem, the goal was to maximize the recall metric to minimize false negatives as maintenance costs are highest for replacement where machine failure despite the model predicting no failure. Due to signficant class imbalance, ML models were built with oversampled minority class and undersampled majority class along with models built on original data. </p>

<p align="justify"> A number of classification based ML models were employed including Random Forest Classifier, Gradient Boosting classifier and XG Boost classifier amongst other tree-based, bagging and boosting models. Because of highly time intensive model executions, a number of models with high cross validation scores and generalizable performance were selected for hyperparameter tuning. RandomizedSearchCV were employed compared to GridSearch to save computation time. XGBoost Classifier model trained on the original data was selected as the final model with emphasis given on recall, generalizability in terms of performance metrics such as recall, F1 score as well as total computation time. A pipeline was built for the final selected model to help automate the predictions for further use.</p>



