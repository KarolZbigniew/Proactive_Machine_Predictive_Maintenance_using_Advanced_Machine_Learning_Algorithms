The primary goal of the project is to showcase the effectiveness and efficiency of implementing tools such as Pipeline transformers and Grid Search for training machine learning models. By applying these tools, the project aims to optimize the model creation process, enabling simultaneous management of various data processing stages and the search for optimal model hyperparameters. As a result, the project can provide valuable insights into effective practices in the field of predicting machine failures using advanced machine learning techniques.

The dataset consists of 10 000 data points stored as rows with 14 features in columns:
- UID: unique identifier ranging from 1 to 10000.
- Product ID: consisting of a letter L, M, or H for low (50% of all products), medium (30%), and high (20%) as product quality variants and a variant-specific serial number.
- Air temperature [K]: generated using a random walk process later normalized to a standard deviation of 2 K around 300 K.
- Process temperature [K]: generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K.
- Rotational speed [rpm]: calculated from powepower of 2860 W, overlaid with a normally distributed noise.
- Torque [Nm]: torque values are normally distributed around 40 Nm with an Ïƒ = 10 Nm and no negative values.
- Tool wear [min]: The quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.
- Target : Failure or Not.

The XGBoost model achieved a high accuracy of 97.5%, indicating generally accurate predictions. The highest ROC AUC score of 0.981 suggests that the XGBoost model has a strong ability to discriminate between classes, which is crucial in classification problems. Regarding the benefits of using GridSearch, this method allows for automatic exploration of the model's parameter space to find the optimal configuration. In the case of limited computational power, GridSearch enables defining a constrained parameter grid, facilitating the discovery of relatively optimal hyperparameters with lower computational cost. In presented case, training only 5 models, GridSearch helps in efficiently selecting parameters, potentially improving model performance under constrained computational resources.
