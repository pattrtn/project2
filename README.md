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

#### Conclusions
* House prices can vary significantly depending on various factors like features and surrounding of the house, including location, property size and house condition but house that more convenience, price will be more expensive like more rooms and use of space or near station , shop and downtown.
*After considering all the above factors the model predicted value may not much accurate, due to incomplete Data , outlier and model complexity such as too many features or parameters.



---

#### Recommendations

For a homebuyer who have limit budget should consider create a list of features in a home that are in need to narrow down the choices and stay in the budget.
