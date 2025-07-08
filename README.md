# CaliforniaHousing
California Housing Price Prediction Report
This project aimed to develop a regression model capable of predicting median housing prices
in California using data from the California Housing Dataset. The analysis focused on
understanding key drivers of housing value, ensuring model performance above an R² of 0.75
on a hold-out test set, and extracting insights relevant to policy or real estate planning.
The exploratory data analysis revealed that the dataset contained no missing values. Several
features, such as average rooms and population, exhibited skewed distributions and significant
outliers. Feature–target correlation analysis identified median income (MedInc) as the most
predictive feature for housing value. Additionally, an engineered feature,
rooms_per_household (calculated as average rooms divided by house age plus one), was
introduced to capture the density of living space per household in a way that adjusted for
neighborhood maturity.
The data was split into an 80% training set and 20% test set. All features were standardized
using StandardScaler to improve model convergence and comparability. A baseline model
using linear regression was trained first, achieving an R² of approximately 0.61 on the test set.
While interpretable, the linear model lacked the capacity to capture complex, nonlinear
relationships in the data.
To address this, a Random Forest Regressor was trained and tuned using GridSearchCV with
five-fold cross-validation. The final model achieved an R² of approximately 0.80 on the test set,
surpassing the target benchmark. Evaluation metrics showed a mean absolute error of around
0.33 and a root mean squared error of about 0.45, indicating strong predictive performance.
Feature importance analysis confirmed MedInc as the most significant predictor of housing
prices. Other relevant features included average occupancy (AveOccup) and the engineered
rooms_per_household, supporting the idea that both income levels and space distribution
play crucial roles in housing value.
From a real-world perspective, the model suggests that areas with higher median income and
more optimal room-to-household ratios tend to have higher home values. This could inform
developers, urban planners, and policy analysts when identifying zones for investment,
expansion, or intervention. Moreover, the model can serve as a foundation for future projects
involving geographic clustering or time-series forecasting of housing trends.
The project meets its success criteria: strong model performance (R² > 0.75), clear and
repeatable code structure, and interpretable results with business relevance. All modeling
choices were made with practical applications in mind, ensuring that the results are not only
statistically robust but also actionable in real-world scenarios.
