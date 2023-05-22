# Project 2: Ames Housing Data and Kaggle Challenge
Analysis by Charles Ramey for General Assembly Data Science Immersive Course - Project 2

### Problem Statement

For home sellers and their agents, setting the initial asking price for a home is often one of the most difficult stages of the selling process. There are several tools for establishing a market value for the home, and once it is established, sellers and their agent may choose to price the home above or below that market value for various reasons, often strategic. Choosing and implementing a pricing strategy that will maximize the value sellers get for their home begins by setting an accurate market value. This project aims to use machine learning and the comprehensive Ames housing dataset to create a general model for predicting the sale value of a home, and give home sellers and their agents a reasonable baseline for dictating the initial asking price.

---

### Datasets

- [`train.csv`](https://www.kaggle.com/competitions/221-ames-competition/data?select=test.csv): Ames housing data used to train the model.
- [`test.csv`](https://www.kaggle.com/competitions/221-ames-competition/data?select=test.csv): Ames housing data used to test the model's accuracy. In this project, this data will also represent potential home listing for a real estate agent.

---

### Data Dictionary

A complete data dictionary detailing the data used in this analysis can be found [here](https://www.kaggle.com/competitions/221-ames-competition/data).

---

### Summary

This projected used data from 2051 homes in Ames, IA to create various machine learning models designed to predict the sale price of future home listings. The sale price of homes used to train the data ranged from ``$130,000-612,000`, with an average sale price of ``$181,000`. Models created in this project include Linear Regression, Lasso, Ridge, and ElasticNet models. Each model was fit to three different refined dataframes: a simple dataframe consisting of 5 features (iteration 1), a complex dataframe consisting of 35 features (iteration 2), and a medium dataframe consisting of 25 features (iteration 3).

The Ridge models performed the best overall, striking a balance between bias and variance, and generalizing well to new data. The Lasso and ElasticNet models had a tendency to overfit the data, often having low error on the training dataset, but significant error on the testing data. The Linear Regression had moderate performance in the first iteration, but was not suited to the data in the second and third iterations. 

---

### Conclusion and Recommendations

The conclusion of this report is that a Ridge model would perform best when predicting housing sale prices based on the given characteristics; however, the models contained herein should not be used for determining an accurate market value for a potential home listing. With even the best model's error falling between $21,000-31,000, the model is likely to predict home values that deviate greater than 10-15% from the average home value. With such a large window of error, a market value established using the best Ridge model would likely mislead home sellers and their agents, causing them to potentially set the starting asking price too high or too low.

Using machine learning to help real estate agents accurately determine market value does have promise, and the benefit of being able to value a home that does not have comparable sales cannot be understated. Yet, greater refinement of the models would be necessary to achieve a confidence level high enough for real estate agents to deviate from the traditional CMA approach. Some recommendations to improve the models and the interpretation thereof include:
- Performing a deeper, more methodical cleaning of the available data to remove outliers and impute missing values where reasonable.
- Using a different k-value for cross-validation. This project used a k-value of 5 across the board to maintain consistency, though 10 is another common k-value for cross-validation.
- Collecting more data to train the model on, including more recent data as well as housing data outside of Ames, IA.
- Including sale date (month/season) in the model data. This project did not look seasonal relationships to sale price, though time of year is a commonly regarded factor that impacts the value of a home.

---

### Sources

1. [https://www.nar.realtor/research-and-statistics/quick-real-estate-statistics](https://www.nar.realtor/research-and-statistics/quick-real-estate-statistics)
2. [https://palermolistings.com/market-data/the-great-pyramid-of-real-estate](https://palermolistings.com/market-data/the-great-pyramid-of-real-estate)
3. [https://www.investopedia.com/terms/c/comparative-market-analysis](https://www.investopedia.com/terms/c/comparative-market-analysis.asp#:~:text=A%20comparative%20market%20analysis%20(CMA)%20is%20an%20estimate%20of%20a,for%20the%20property%20and%20comparables.)
4. [https://www.nar.realtor/nar-doj-settlement/multiple-listing-service-mls-what-is-it](https://www.nar.realtor/nar-doj-settlement/multiple-listing-service-mls-what-is-it)
5. [https://www.kaggle.com/competitions/221-ames-competition/data](https://www.kaggle.com/competitions/221-ames-competition/data)
6. [https://pandas.pydata.org/docs/reference/index.html](https://pandas.pydata.org/docs/reference/index.html)
7. [https://scikit-learn.org/stable/modules/classes.html](https://scikit-learn.org/stable/modules/classes.html)
8. [https://matplotlib.org/stable/api/index.html](https://matplotlib.org/stable/api/index.html)
9. [https://seaborn.pydata.org/api.html](https://seaborn.pydata.org/api.html)
10. [https://stackoverflow.com/questions](https://stackoverflow.com/questions)