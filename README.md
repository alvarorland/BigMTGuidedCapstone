Purpose

The purpose of this data science project is to come up with a pricing model for ski resort tickets in our market segment. Big Mountain suspects it may not be maximizing its returns, relative to its position in the market. It also does not have a strong sense of what facilities matter most to visitors, particularly which ones they're most likely to pay more for. This project aims to build a predictive model for ticket price based on a number of facilities, or properties, boasted by resorts (at the resorts). This model will be used to provide guidance for Big Mountain's pricing and future facility investment plans. The goal is to create a new data-based pricing strategy for Big Mountain Resort to increase revenue and cover their operating expenses.

Method

Using a correlation heatmap to determine which features are most correlated with ticket price.

![image](https://user-images.githubusercontent.com/72377927/121642621-624ace80-ca56-11eb-87b3-60cb6fb34088.png)

AdultWeekend ticket price correlations:

-fastQuads

-Runs

-Snow Making_ac. 

-resort_night_skiing_state_ratio

-total_chairs

-vertical drop

Modeling

I used two models for this project.

Linear Regression:

-Imputed with mean and median values

-Using the Mean Absolute Error of this model gave an estimate of $9 or so of the real price

Random Forest:

-Built a pipeline using the median as an imputer, a standard scaler, and cross-validation

-Also used GridSearchCV, leveraging one of the hyperparameters that can be explored using RF

-The random forest model had a lower cross-validation mean absolute error by almost $1 

-Verifying performance on the test set produced performance consistent with the cross-validation results

-This was the model used to determine the final ticket price for the resort

BMR could save on operation costs by closing a specific number of runs as shown below.

![image](https://user-images.githubusercontent.com/72377927/121643766-d174f280-ca57-11eb-943a-5f995c14c41f.png)

Conclusion

Big Mountain Resort's modelled price is $95.87$, actual price is $81.00$. Even with the expected mean absolute error of $10.39$, this suggests there is room for an increase. The additional operating cost of the new the 2 new lifts and the extra 2 acres of snow coverage would be covered under scenario 3, with enough revenue to profit from the season. I'd recommend going with scenario 3, the new features at the resort justifies the increase in ticket price in a market where adult tickets are undervalued.
