# Customer Propensity Modeling

## Project Description
<p align="justify">
The goal of this project is to build a customer propensity model to estimate the propensity (or likelihood) of a customer at an e-commerce website to make a purchase. We are thus modeling customer behavior, since the higher the propensity, the more likely it is for the visitor to complete a transaction. A typical propensity model looks at customer demographics, psychographic factors, engagement patterns, and user behavior. In our analysis, we shall be focusing on the user behavior aspect.
</p>

We have chosen a Kaggle dataset to work on, found at this link [Customer Propensity to Purchase Dataset](https://www.kaggle.com/benpowis/customer-propensity-to-purchase-data).

<p align="justify">
As a first step, we perform exploratory data analysis (EDA) to gain a better understanding of our selected dataset and to clean and pre-process our data (including checking for multi-collinearity and correlation). Next, we move on to feature selection by eliminating multi-collinear features present within the dataset. Finally, we build five different models – Logistic Regression, Naïve Bayes, Support Vector Machine, Random Forest, and XGBoost; and compare their results to select the one with the best performance using relevant evaluation metrics.</p>
  
 
| Model  | Precision | Recall  | Accuracy |
| ------------- | ------------- | ------------- | ------------- |
| Logistic Regression  | 0.8727	|0.8566|	0.8690|
|Random Forest|	0.8581	|0.89|	0.899|
|XGBoost	|0.852|	0.901|	0.901|
|Naïve Bayes	|0.7992	|0.802|	0.850|
|SupportVector Classifier|	0.8921|	0.8962	|0.8982|

  
  
All the models have similar performance on test data. However, maximum recall values are observed for XGBoost, which is the metric of choice (because of the lost revenue due to a false negative).

<p align="justify">
For customers having high propensity, we see that the users who ended up purchasing the product have clicked on the basket and it makes sense. Those in high propensity who did not purchase are just window shoppers and we might roll out some discount offers to lure them to make a purchase. Also, we see that among users who have more propensity to purchase, returning users are more than first time users. This tells us that the returning ones are loyal to our website and we should not lose them. Finally, looking at the users with low propensity, we see that vast majority of them did not click on the basket. So, these are just exploring the product and not actually interested in buying.</p>
