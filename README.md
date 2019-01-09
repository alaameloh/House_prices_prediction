# House_prices_prediction

This Python Notebook was developed for a Kaggle challenge: [House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) as part of lab in the Algorithmic Machine Learning course

## Project overview
### Purpose 
The goal of this challenge was to learn how to analyse and process data in order to perform a regression: although it was a didactical experience, we were asked to do everything autonomously as if it was a real-life complex problem we had to face.

The topic of the notebook is predicting apartments' selling prices. The dataset provided is not huge (so, for the moment there is no need to use distributed frameworks like Spark) and it is a set of apartments described by 81 features. These features can be both qualitative or quantitative and present incongruencies (such as NaN values).

The first section of the notebook is dedicated to data analysis: dataset is loaded into memory and its content is decribed using tables and plots. Then, an integrity control is performed in order to spot (and eventually correct) those records whose values are not compliant with the documentation provided.

In the second section of the notebook, we check that the assumptions to build a Multiple Linear Regression model are met. This analysis is quite long, but effective: after every step, the model performances increase. Examples of analysis run in this section are selecting the best features to use, or highlighting outliers and leverage points.

Then, the model is built. What we do in the final section is to consider alternative models from the scikit-learn library and create an ensemble keeping the most performant ones. Model parametrization is done performing cross-validation: it takes time, so we decided to parallelize the computation over our cluster, using Spark.

This final ensemble model is the one used to predict SalePrice values over the test set provided for the challenge.


## Technical details

### Data Science Python libraries
We have decided to use some of the most famous available Python libraries:
- Pandas and Numpy: dataset processing and analysis
- Matplotlib and Seaborn: data visualization
- SciKit-learn: used to generate the regression models we have explored and tried to implement
