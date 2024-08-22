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

I ended up with 10 independent variables that I chose, namely the city, lead quality, lead source, country, education specialization, occupation, number of visits to website, page views, activity score and profile score. 

Then, further data preparation steps are performed. For example for the country variable, I simplified the variable from 38 different countries to just 2 categories (India vs Not India), effectively changing it to a binary variable. Other data preparation steps are also performed, reducing all the categorical variables with many categories essentially to around 2-4 categories so that the model can be simplified. The continuous variables are left as is. 

Then in terms of handling missing data, I observed that all of my chosen independent variables had some missing data, ranging from 1% missing to around 50% missing. Mode imputation is not as feasible as there are quite a number of variables with a percentage of missing data. Eventually, I decided to go with listwise deletion. Around 1,506 observations had no missing data in among the dependent variable and all the other independent. As such, the total sample size for the dataset is reduced to 1,506 observations, which arguably is still large enough for analysis.

### Modelling
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

### Evaluation
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

## Recommendation and Analysis
Explain the analysis and recommendations

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

## AI Ethics
Discuss the potential data science ethics issues (privacy, fairness, accuracy, accountability, transparency) in your project. 

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit. Proin convallis mi ac felis pharetra aliquam. Curabitur dignissim accumsan rutrum. In arcu magna, aliquet vel pretium et, molestie et arcu. Mauris lobortis nulla et felis ullamcorper bibendum. Phasellus et hendrerit mauris. Proin eget nibh a massa vestibulum pretium. Suspendisse eu nisl a ante aliquet bibendum quis a nunc. Praesent varius interdum vehicula. Aenean risus libero, placerat at vestibulum eget, ultricies eu enim. Praesent nulla tortor, malesuada adipiscing adipiscing sollicitudin, adipiscing eget est.

## Source Codes and Datasets
Upload your model files and dataset into a GitHub repo and add the link here. 
https://github.com/nyp2049767t/itd214_project
