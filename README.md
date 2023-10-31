# Project-2
#### Problem Statement:
House buyers want to estimate the affordability of a property and make informed choices about where to live.

#### Background: 
House buyers have a budget in mind when searching for a new home so they want to narrow down their options and identify properties that fall within their budgetary constraints.

#### Objectives:
Understand the expected costs of house owner and whether they are making a sound financial investment.

---

#### Datasets:

**Datasets corresponding to rainfall information:**

* [`train.json`](./Data/train.json): the training set with target value price
* [`test.json`](./Data/test.json): the test set without target value price
* [`bangkok_district.csv`](./Data/bangkok_district.csv): supplemental data

---

#### Data Import & Cleaning:
* Step 1 : Import data by using Pandas
* Step 2 : Check for missing values , datatype and any obvious issues
* Step 3 : Fixing and cleaning data
  - replace missing value in subdistrict columns
  - replace null value with 0
  - Get dummy for categories columns

---
#### Modelling
Model 1 : 
- Features : bedrooms + baths + floor area + nearby stations / shops / supermarkets
- Linear score : 0.40956
- Linear RMSE : 1675002.69
- Ridge score : 0.40956
- Ridge RMSE : 1675003.68
- Lasso score : 0.40641
- Lasso RMSE : 1679468.46

Model 2 :
- Features : Model 1 + property type + province
- Linear score : 0.49413
- Linear RMSE : 1550404.40
- Ridge score : 0.49413
- Ridge RMSE : 1550408.49
- Lasso score : 0.48068
- Lasso RMSE : 1570887.61

Model 3 : 
- Features : Model 1 + property type + District
- Linear score : 0.62237
- Linear RMSE : 1339545.66
- Ridge score : 0.62218
- Ridge RMSE : 1339883.93
- Lasso score : 0.47939
- Lasso RMSE : 1572834.70

Model 4 : SELECTED FOR BEST MODEL
- Features : Model 3 + land area + longitude + floor level + year built
- Linear score : 0.63301
- Linear RMSE : 1320539.22
- Linear Cross val score(mean) : 0.62544
- Ridge score : 0.63295
- Ridge RMSE : 1320660.29
- Ridge Cross val score(mean) : 0.62546
- Lasso score : 1645355.5710681996
- Lasso RMSE : 104789.77
- Lasso Cross val score(mean) : 0.42421

## Chose Model 4 features with Ridge score for the best prediction
---

#### Conclusions
* House prices can vary significantly depending on various factors like features and surrounding of the house, including location, property size and house condition but house that more convenience, price will be more expensive like more rooms and use of space or near station , shop and downtown.
*After considering all the above factors the model predicted value may not much accurate, due to incomplete Data , outlier and model complexity such as too many features or parameters.



---

#### Recommendations

For a homebuyer who have limit budget should consider create a list of features in a home that are in need to narrow down the choices and stay in the budget.
