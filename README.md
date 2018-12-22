# Seattle Airbnb Data Analysis

In this project, I use Data Science methodology to analyse the Open Data of Airbnb.

We will see how good it is to start up this kind of business in Seattle by reviewing the Open Data of Airbnb in Seattle from Kaggle platform. 

In this project, there is one Ipython notebook for data anylitics, you can open this notebook and go through my data analytics journey steps by steps.

## How to use

Install the necessary libries for this project.

`pip install jupyter`

`pip install -r requirements.txt`

## What are included

Data for analysing and one Ipython notebook are included in this repository. You can download the whole project and run jupyter notebook for reviewing my analysing procedure. 


## Steps by steps

Let’s first take a look at the data that we have. There are three datasets, calendar.csv which records the daily price and availability for properties on Airbnb from 2016 January to 2017 January, listings.csv records 3818 different properties detailed information, and last but not least reviews.csv records reviews from different customers for different properties from 2009 to 2016.

![](https://cdn-images-1.medium.com/max/1600/1*gD7ulBcmhEpTRG3OefEfiw.png)

After reviewing the calendar.csv, we found some missing values and different data type, we will do some data preprocessing jobs first. Change the data type as it stands and fill out the missing value as mean of the same group of property. After transforming, the data is now easier to handle.

![](https://cdn-images-1.medium.com/max/1600/1*-bmzDIx0nbXzY7tu4y_-FQ.png)

I had added one more column “revenue” by multiplying price and availability in calendar dataset for later analysing.

Let’s see how’s the business going on during 2016 by visualising the dataset.

![](https://cdn-images-1.medium.com/max/1600/1*piGbW9vM5ukZSxXh8yBkdw.png)

We can find that the fully book situation at 2016 is like that the book rate is high at the start of year, and getting low along the way with some raises during Apr and Jul.

![](https://cdn-images-1.medium.com/max/1600/1*4jPbMqWVcvBwZ6MQB65Ypg.png)

We can find that the price of property goes up along the year.

Next, we will merge two datasets together for digging out more information about the fact of booking.

The dataset we will use for merging is the listings.csv which records properties detailed information. The listings.csv contains 3818 rows and 93 columns data, with fruitful of features describing each property informaion.

Before merging them together, I will do the same data preprocessing by transforming object data to categorical data and appropriate data type as needed.

After merging two datasets, let’s see if any district differences in pricing or booking situation.

![](https://cdn-images-1.medium.com/max/1600/1*feR7p7j8nitejDU5QbrXWg.png)

From above figure, we can find out the fact that most of the porperties aside in the center of Seattle, and the booking rate is also a little higher than other areas. But generally, the book rate in Seattle is not high.

And from the average price figure, we can also conclude that the average price of property in Seattle is around 150 per night.

You can find more by running in my notebook.

