# Analysis of 2016 United States Presidential Election

This project analyzes the demographical roles and voter behavior in 2016 United States Presidential Election via **machine learning** methods including PCA, decision tree, random forest, boosting, logistic regression, support vector machine and exploratory data analysis methods. 

## Dataset

It uses the dataset election.raw(18345 observations and 5 variables) and census(74001 observations and 36 variables).

election.raw:
* state
* county 
* candidate (president candidates, 32 in total)
* votes (number of votes received)

census
* Men (Number of men)
* Women (Number of women)
* White (percent of population that is white)
* Citizen (Number of citizens)
* Unemployment (percent of population that is unemployed)
* Poverty (percent of population that is under poverty level)
* Drive (percent of population that is commuting alone in a car, van, or truck) • Employed (Number of employees)
* ...

## Some Results
### Exploratory Data Analysis
It indicates even though the winner of the election was Donald Trump, Hillary Clinton got more votes in total. From the county-level map, Donald Trump won in 2607 counties, and Hillary Clinton won in 462 counties. So even though Hillary got more votes in total, Trump won in more electoral districts. 

<img width="500" alt="Screenshot 2023-05-26 at 15 18 22" src="https://github.com/MeiyuLiT/Analysis-of-2016-United-States-Presidential-Election/assets/75913591/a8cb8d2a-b8a3-42ce-8a54-55e014850e15">
<img width="417" alt="Screenshot 2023-05-26 at 15 19 06" src="https://github.com/MeiyuLiT/Analysis-of-2016-United-States-Presidential-Election/assets/75913591/ab319442-9461-40c5-8d3c-b0dc66316860">

### Principal Component Analysis
The Principal Component Analysis(PC) was conducted on both county and sub-county level data. Regarding that the variables included in each data have different ranges of value, scaling and centering option was enabled in the PCA. Please see detailed analysis in the report.

### Classification
This section uses decision tree, Random Forest, Logistic Regression, etc. In Decision Tree, we pruned tree to minimize the misclassification error and use folds defined in the handout for cross-validation. In Random Forest, we decorrelate the trees, and plot confusion matrix as well as the accuracy and Gini for each census variable to see which one has higher impact on voting decision. In Logistic Regression, we interpret some coefficients in terms of a unit change in the variables. In result, we found the significant variables are proverty, childPoverty, transit, selfEmployed, etc., and the best model we decided is random forest in our scenario. Please see detailed analysis in the report.
<img width="417" alt="Screenshot 2023-05-26 at 15 14 48" src="https://github.com/MeiyuLiT/Analysis-of-2016-United-States-Presidential-Election/assets/75913591/4253793e-0198-4425-adce-34ad92806223">



