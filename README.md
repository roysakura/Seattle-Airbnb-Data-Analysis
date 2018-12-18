# Seattle Airbnb Data Analysis

In this project, I use Data Science methodology to analyse the Open Data of Airbnb.

We will see how good it is to start up this kind of business in Seattle by reviewing the Open Data of Airbnb in Seattle from Kaggle platform. 

In this project, there is one Ipython notebook for data anylitics, you can open this notebook and go through my data analytics journey steps by steps.

## How to use

Install the necessary libries for this project.

`pip install pandas`

`pip install seaborn`

`pip install wordloud`

`pip install nltk`

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

Next, let’s check out the top 10 most profitable properties in town, and try to find out the reason for that.

We can find out that the top 1 profitable property can earn around 188,763 annually.

![](https://cdn-images-1.medium.com/max/1600/1*LBahKFOc-7_5juolRmt2vA.png)

By merging it with reviews, I try to find out what’s the key features for their success.

![](https://cdn-images-1.medium.com/max/1600/1*zI3vUc_Cphbb0lB1rXJBYw.png)

Apparently the big house with amazing view would attract people to book for living.

Next we will try to find out the fact and prove it by using data analytic model.

Here we will use RandomForrest (RF)Model for that purpose. Since there are different categorical data in the dataset, Decision Tree modelling are very good at those data types and can easily split out the data for getting more inforamtion.

First let’s try to predict the price by using the features in the listings.csv. After applying the RF Regression model on the dataset we find out the feature importances as following:

![](https://cdn-images-1.medium.com/max/1600/1*qKDYhv9NThJikBET6RQgww.png)

We can find out that the price of property is basically determined by the accommodation and size, the bigger the place is, the more higher the price is, the more accommodates it can provide, the higher the price it is.

Next we will try to predict the revenue by using the same dataset features to find out the key facts. After applying the modelling on the dataset, we can find out that

![](https://cdn-images-1.medium.com/max/1600/1*LSb-GUxC_G1aCgd9Dy0BFw.png)

We can find out that location and reveiws contribute to the revenue. For deeper understanding, I also use correlation graph for detail understanding.

![](https://cdn-images-1.medium.com/max/1600/1*d-WD0pRgRzYGCrygctDbQA.png)

We can see that accommodates and bedrooms number take significant effect on the total revenue to the property, while reviews take negative effects on the total revenue that less reviews generate more revenue.

In conclusion, there are three insights that generated from the Data itselfe.

Average price of Airbnb property in Seattle is around 150, the maximum revenue during one year is around 188,000.
It would have more advantages that you have bigger property that can provide more accommodates to guests in getting more profit.
More reviews can’t really help you get more clients, but a nice view can.

