---
layout: post
author: Jasmon 2049767T
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
Our group's chosen dataset is about the conversion of leads for an educational institute that is likely based in India. In total, there are 9,240 observations in the dataset, and the available variables for analysis ranged from demographic characteristics (country, city...etc), behavioural (time spent on website, number of page views), to information about the lead itself (Source, Quality...etc). Based on this chosen dataset, the overall objective of group is set to be improving the conversion rate as that seems to be the main purpose of the dataset as well. 

With this, I decided to choose another variable within the dataset to be the center of my individual objective. Eventually I settled on focusing on time spent on website, as I think that it is connected to conversion rate. The rationalte is that it is likely that if someone spends longer on the educational institute's website, he/she is more likely to have positive experiences on the website, as such he/she is more likely to be successfully converted. Rather than focusing on an abstract action of "successful conversion", perhaps it would be better to take a step backwards and focus on a measurable, incremental metric, which is time spent on website. As such, my objective is to find out what are the factors that can increase the time spent on the website.

## Work Accomplished


### Data Preparation
To prepare the data, I first chose the variables that I want to include in my model. The first stage is to understand what does each variable mean, and whether on the surface level, does it make sense to be included in my model. Then I analyzed the number of missing observations for the variables that makes sense to be added, and also analyzed the distribution. Some of the variables, however, like those that hear about us through different channels (Newspapers, Magazines...etc) are too skewed (e.g. 99.9% No, 0.1% yes), and those are discarded as well.

I ended up with 10 independent variables chosen, namely the city, lead quality, lead source, country, education specialization, occupation, number of visits to website, page views, activity score and profile score. 

Then, further data preparation steps are performed. For example for the country variable, I simplified the variable from 38 different countries to just 2 categories (India vs Not India), effectively changing it to a binary variable. Such data preparation steps are also performed on the other variables, reducing all the categorical variables with many categories essentially to around 2-4 categories so that the model can be simplified. The continuous variables were left as is. 

Then in terms of handling missing data, I observed that all of my chosen independent variables had some missing data, ranging from 1% missing to around 50% missing. Mean/Mode imputation is not as feasible as there are quite a number of variables with a percentage of missing data. Eventually, I decided to go with listwise deletion. Around 1,506 observations had no missing data in among the dependent variable and all the other independent. As such, the total sample size for the dataset is reduced to 1,506 observations, which I assessed is still large enough for analysis.

### Modelling
The two models that were chosen is random forest and linear regression. The aim is to find the factors that affects time spent on website the most. With the dependent variable set as time spent on website, and independent variable being the rest of the variables in the model as listed in the preivous section, I built the Random Forest model. I used a test size of 25%, and I also adjusted the n_estimators, choosing n_estimators to be 500 as the mean-squared error started to plateau around there.  On the feature importance, the top three most important features using the Random Forest model is number of visits to website, number of page views, and profile score, while the three least important features are country, lead quality, and occupation.

The other model that I have built is linear regression. The dependent variable, independent variables, and test size are kept the same as the Random Forest model. The results this time showed that the only three independent variables that are statistically significant (95% CI) are only lead quality, occupation, and activity score. Better lead quality leads to more time spent on the website, working (instead of not working) leads to more time spent on the website, and a higher activity score is also correlated with more time spent on the website.


### Evaluation
Overall, the Random Forest had a mean-squared error of 306,374, while the Linear Regression model had a mean-squared error of 271,660. As the mean-squared error of the Linear Regression model is lower, the linear regression is evaluated to be the better model.


## Recommendation and Analysis
Based on the Linear Regression Model, the most important variables are lead quality, occupation, and activity score. On the other hand, certain demographic variables, such as the city or country, was not significantly correlated, which was in a way, surprising. On the finding for occupation, it would probably be better for the company to re-design its website such that it is more catered to those that are already working. Additionally, perhaps its course offerings could also try to reflect that, to have something that is more relevant to industries, which could then improve time spent on website and conversion rate. On lead quality, this suggests that the educational institute should invest in more resources to improve its lead information. This is because the variables on lead information tends to also have a larger proportion of missing values. Doing so may therefore improve the performance of future models. Lastly, the model can also improve if it can also capture more basic variables, such as age and gender for analysis.

## AI Ethics
One issue related to AI ethics in this project is privacy. In terms of privacy, there were no explicit information on whether consent had obtained for the respondents that are included in this dataset. However, at the very least, the dataset itself does not contain any identifiable data, and hence, using it in that sense, any model training will not infringe on personal privacy in this regards.

On Fairness, using this data will also not lead to any significant discriminatory on unfairness, precisely because the data itself actually does not have any pertinent demographic information. As such, it is unlikely to lead to bias towards or against any vulnerable groups. 

On Accuracy, it is difficult to ascertain the exact accuracy of the dataset as there are no other ways to triangulate it. The ethical issue at play for accuracy is that if the data is of poor quality, especially in terms of accuracy it may lead to unfair outcomes. In terms of data quality, there are quite a number of missing variables in the data, which ideally should be mitigated further to reduce biasedness. The model that I built relies on listwise deletion, which if the missing variables are not missing completely at random (MCAR), could potentially introduce bias into my model. I have tested it before, and the missing values are indeed not MCAR. As such, there are some bias introduced into the model on my decision to use listwise deletion. That being said, as the dataset did not really have any variables that are more sensitive to vulnerable groups, it is unlikely that the poorer quality and the decision to use listwise deletion (which introduced additional bias) would lead to any ethical or discriminatory outcomes that are unfavourable to certain vulnerable groups.

On Accountability, the idea is that if there are something wrong with the AI model, it should be possible to accuractely assign liability for different parties. For this project, we are all very clear on the individual parts that we are taking, and the models that we have built. Each of our group members have their own research questions, and as such, i beleive it is possible to for us to be accountable if there are indeed something wrong with our models that lead to unfavourable outcomes, but again as I have mentioned, this risk is very low because of the type of data available in the dataset.

On Transparency, 

Discuss the potential data science ethics issues (privacy, fairness, accuracy, accountability, transparency) in your project. 


## Source Codes and Datasets
Upload your model files and dataset into a GitHub repo and add the link here. 
https://github.com/nyp2049767t/itd214_project
