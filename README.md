# House Price AI

House Price Prediction AI by Neil G. and Daniel D.

[![License](https://img.shields.io/github/license/RandomKiddo/HousePriceAI)](https://www.gnu.org/licenses/agpl-3.0.en.html)
[![Size](https://img.shields.io/github/languages/code-size/RandomKiddo/HousePriceAI)](https://github.com/RandomKiddo/HousePriceAI/blob/master/Project.ipynb)
___

### Goal

As part of a club project starting in August 2022, we sought to collaborate to create a model that predicts house prices in a certain area based on many factors like square feet, amount of bedrooms, and more. Using knowledge we gained from said club meetings and our own personal programming skills, we were able to create a highly accurate and successful model given the data set. All acknowledged libraries and sources are located in the Jupyter Notebook file, however, we would still like to credit the original dataset at: [Kaggle - House Data](https://www.kaggle.com/datasets/shree1992/housedata).

Additionally, we would like to thank all officers of AI Club: Fall 2022 for supporting us in this journey with their helpful workshops. 

___

### CRISP-DM

#### Business understanding - What does the business need?

The real estate business that needs to set house prices would need a way to automatically determine the prices of a house based on certain characteristics. This model could also be used to help predict house prices as the house changes (i.e. gets renovated, other house prices change, etc.).

#### Data understanding - What data do we have / need? Is it clean?

The data we have is taken from Kaggle. It has various sqft information, amount of rooms, condition information, and positional data (i.e. location).

#### Data preparation - How do we organize the data for modeling?

The plan for cleaning this data was to drop data that didn't have a price attached to it. For missing values, we filled the gaps with the median since there were so few. Then we dropped any duplicate data values.

#### Modeling - What modeling techniques should we apply?

With the prepared data set, we decided on a regression technique, due to a price being a predicted value, rather then us classifying houses. From there, we chose a `KNeighborsRegressor` model, since our data had a lot of values, and was rather complicated, so we could not assume a linear model. A radius regression technique was not chosen, in order to conserve time, and to reduce the risk of no points falling in a given radius, due to the amount of variables we were testing with.  

#### Evaluation - Which model best meets the business objectives?

Our model with 3 nearest neighbors out-performed the other models. The KNN regression technique was superior, due to similar houses having similar prices in the real world. Although not shown in our project files, linear regression models tended to have a much worse performance and r<sup>2</sup> value (with many far below `.50` in the `.20` to `.40` range). Therefore, to reach the business model, our best performing AI should be selected.

#### Deployment - How do stakeholders access the results?

This notebook, the results, and the model will be posted on Github. 

___

### Final Thoughts

The main purpose of this project was to learn how to build an AI model, and hopefully build a successful one. With an r<sup>2</sup> of `0.9999968`, it is safe to say that we succeeded in creating a highly accurate model (with the sample data). Of course, this data has not been tested for rigidity in comparison to other data sets, so we cannot say that this model is accurate for all housing markets. 

The model functioned very accurately, which is a definite positive of the project. One downside of our model is that it factors in location-based data values. However, some of these data values are rather arbitrary, such as zip code or street name (streed id). This decreases the ruggedness of our model, and we could've created a more applicable model by dropping arbitrary data values. 

We learned, through this project, how to prepare a data set, and eventually create an AI model through the data. From this, we can work on creating more advanced and applicable AI models, and expand our horizons past regression models and onto classification models.

___

[Back to Top](#house-price-ai)

<sub>This page was last edited on 11.28.2022</sub>


