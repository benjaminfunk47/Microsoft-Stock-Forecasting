# Introduction
This is a personal project. The main goal of this project was to sharpen my skills with Power BI visualizations, AWS tools, and predictive forecasting. In this project I created visualizations of the dataset using Power BI to gather insights. I then used AWS Sagemaker Studio Lab to create an XGBoost Model that could forecast the Microsoft Stock Price for the next 6 months. Lastly, I compared my forecast with the real stock price for those 6 months to see how well my model performed.

To refine my skills, I included the following in the personal project:
- Power BI Visualizations
- Feature engineering
- Data analysis
- Model creation, evaluation, and visualization
- Predictive Forecasting using XGBoost
- Metrics evaluation and visualizations
- AWS tools

The technologies and libraries used for this project are:
- Power BI
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Holidays (Python library for getting holiday dates)
- XGBoost
- AWS Sagemaker Studio Lab

# Kaggle Datasets
- The first step I took was to find a public dataset to use for training. I found a [Microsoft Stock Kaggle Dataset](https://www.kaggle.com/datasets/vijayvvenkitesh/microsoft-stock-time-series-analysis) which has stock price data for April 2015 - April 2021. As the stock market is closed on weekends, Saturdays and Sundays are not included in the dates. With these days excluded, there are only 1,511 rows in the dataset.

![Kaggle Preview](images/kaggle.JPG)
![Kaggle Preview](images/kaggle2.JPG)

- There are 6 features included in the dataset. These features are:
  - Date: M/D/YYYY H:M:S, all hours are set at 4 P.M. (no data across each day)
  - Open: opening price of the day
  - High: highest value of the day
  - Low: lowest value of the day
  - Close: closing price of the day
  - Volume: number of shares traded that day


- The target variable is going to be stock price for each day. As there are 4 columns related to stock price, I chose to create a column called "Average" later in the project to serve as the target variable. This column is created from averaging the "High" and "Low" columns to get the average value of the stock for each day.

- I decided to find another dataset that includes data for the 6 months after the first dataset ended (April 2021 - October 2021). I could use this dataset to evaluate how well my model performed in its predictive forecast of 6 months. I found another [Microsoft Stock Kaggle Dataset](https://www.kaggle.com/datasets/berkayalan/microsoft-stock-data-between-2015-and-2022/data). This one had the "High" and "Low" columns that I needed to create the "Average" column like with the first dataset.

![Kaggle Preview](images/kaggle3.JPG)
![Kaggle Preview](images/kaggle4.JPG)


