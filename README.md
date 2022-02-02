# airbnb-analysis-capstone-project
# EDA-Capstone-Project

EDA capstone project on 

AIRBNB BOOKING ANALYSIS

Technical Documentation by-

Ranjan kumar sahoo



Abstract-

Airbnb is an online booking system for rental rooms available in New York. They are providing different types of rental rooms in the New York region. The information has been provided in the given data set.
 
Our analysis helps to understand various aspects of room booking activity in New York City. In this Data analysis, we are using different data visualization techniques which help us to determine trends followed in bookings.

Keywords- Data analysis, data visualization etc

Problem Statement-
Since 2008, guests and hosts have used Airbnb to expand their travelling possibilities and present a more unique, personalized way of experiencing the world. Today, Airbnb became one of a kind service that is used and recognized by the whole world. Data analysis on millions of listings provided through Airbnb is a crucial factor for the company. This data can be analyzed and used for security; business decisions, understanding of customer’s and host’s behaviour and performance on the platform, guiding marketing initiatives, implementation of innovative additional services and much more. 
id- It contains the respective id of the owner on the listings.
name- It contains the name of the owner.
host_id- Having respective id’s of a host on the listings.
host_name- It contains the names of the host.
neighbourhood_group - It contains various neighbourhood groups available in New York.
neighbourhood - neighbourhood  resides inside the neighbourhood groups.
latitude - showing geographical coordinates for latitude.
longitude - showing geographical coordinates for longitude.
room_type- available room types on the listings.
Price -prices for rooms on the listings.
minimum_nights -minimum number of nights of stay required to book the room.
number_of_reviews -reviews obtained for each type of room 
reviews_per_month - reviews obtained for each type of room per month
calculated_host_listings_count -host listings on the listings
availability_365 - availability of rooms for the number of days throughout the year.
 
 
Introduction -
 Airbnb hosts price their properties to maximize profits what approach do they use to price their properties expensively to get higher profit margins, or should they be more competitive to generate more sales? Many Airbnb hosts struggle with this pricing problem: they don’t know if they’re undercutting potential profits through low pricing.
The goal of this data exploration is to understand the significance related to the Airbnb dataset, we got to know different hosts having different kinds of properties for rent. Prices of rooms depending upon location and facilities provided and with a minimum number of nights of stay required, also check various aspects related to price, room type, availability 365, reviews per month etc.

Exploratory Data Analysis-

For Exploratory Data Analysis it is important to import libraries because these are necessary for data exploration.

Import NumPy -NumPy can be used to perform a wide variety of mathematical operations on arrays. It adds powerful data structures to Python and it supplies an enormous library of high-level mathematical functions that operate on these arrays and matrices.

Import pandas- Pandas is a Python library for data analysis. Pandas is built on top of two core Python libraries—matplotlib for data visualization and NumPy for mathematical operations.

Import seaborn- Seaborn is an open-source Python library built on top of matplotlib. It is used for data visualization and exploratory data analysis. Seaborn works easily with data frames and the Pandas library. The graphs created can also be customized easily.

Import matplotlib.pyplot - Matplotlib is a cross-platform, data visualization and graphical plotting library for Python and its numerical extension NumPy.
%matplotlib inline -sets the backend of matplotlib to the 'inline' backend, with this backend, the output of plotting commands is displayed inline within frontends.

Handling Null values-
Data Cleaning is the process of finding and correcting the inaccurate data that are present in the dataset. Our dataset contains a large number of null values which might tend to disturb our understanding hence we dropped them at the beginning to get better insights. Replacing null values in the column reviews_per_month with 0 in the dataset. Name and hostname are not the main aspects of our analysis, that's why replaced them with some characters. Dropping the column the last review having a large number of data points contains null values.

seaborn.countplot-
Show the counts of observations in each categorical bin using bars.
A count plot can be thought of as a histogram across a categorical, instead of a quantitative, variable.
For finding popular neighbourhood groups among neighbourhood groups we are using a count plot. Count plot showing count for different values of neighbourhood groups. from the dataset, we are plotting categorical values like neighbourhood_groups, neighbourhoods, room_types with respective counts.
seaborn.boxplot-
A box plot (or box-and-whisker plot) shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels of a categorical variable. The box shows the quartiles of the dataset while the whiskers extend to show the rest of the distribution, except for points that are determined to be “outliers” using a method that is a function of the inter-quartile range.
In our data exploration, we are using neighbourhood_groups and price,room_type and average price which helps us explore this data.

Bar plot-
A bar plot is a plot that presents categorical data with rectangular bars with lengths proportional to the values that they represent. A bar plot shows comparisons among discrete categories. One axis of the plot shows the specific categories being compared, and the other axis represents a measured value.
Plotting neighbourhood_groups and availability_365 gives insights on the data in the particular neighbourhood_groups values or which is most preferred in the neighbourhood_gropus.

seaborn.jointplot-
Draw a plot of two variables with bivariate and univariate graphs. Plotting availability_365 and price gives a favourable price range with the availability of rooms. Plotting room_type and number_of_reviews gives a preferred type of room.

Pair plot-
Plot pair wise relationships in a dataset.
By default, this function will create a grid of Axes such that each numeric variable in data will be shared across the y-axes across a single row and the x-axes across a single column. The diagonal plots are treated differently: a univariate distribution plot is drawn to show the marginal distribution of the data in each column.
It is also possible to show a subset of variables or plot different variables on the rows and columns.
Plotting price, latitude and availability_365 gives valuable information on the features concerning each other.

seaborn.displot-
This function provides access to several approaches for visualizing the univariate or bivariate distribution of data, including subsets of data defined by semantic mapping and faceting across multiple subplots. 
availability_365 plotted with the number of counts which shows availability over the year and most preferred days for booking.

seaborn.scatterplot-
Draw a scatter plot with the possibility of several semantic groupings.
Longitude, latitude and neighbourhood_group showing it grouping of 
Neighbourhood groups across Longitude and latitude in a different colour.
Longitude, latitude and room_type showing it presence of rooms across Longitude and latitude in a different colour.
 
seaborn. Heatmap-
Plot rectangular data as a colour-encoded matrix.
Plotting all features for checking correlation with each other. Not showing significant relevance or correlation with each other.




Pivot Table -
Create a spreadsheet-style pivot table as a Data Frame.
The levels in the pivot table will be stored in MultiIndex objects (hierarchical indexes) on the index and columns of the result Data Frame.
Pivot table makes us easy to understand values or counts for different features in the form of a data frame.
From the Pivot table, we are getting information about the following features
1. Price among the neighbourhood groups
2. Price among the neighbourhood
3.Price among the neighbourhood and neighbourhood groups.
4. Price among the room types
5. Host id and Number of reviews
5. Latitude and longitude with price
6. Availability with price
 
Conclusion -

We can conclude this analytical study by starting with loading the data so far we have done EDA, null values treatment. The insights about the most preferred room type on the listing are also taken into consideration. Neighbourhood groups were analysed in detail with respect to the most preferred booking, top favourable neighbourhoods, a most preferred price range, hosts id’s having a maximum number on listings, availability of rooms for 365 days, and the number of reviews for respective rooms. 


References-

Geeks for Geeks

Analytics Vidhya

https://pandas.pydata.org

https://numpy.org

https://seaborn.pydata.org

https://matplotlib.org



Summary

Overview:
Airbnb is an online marketplace that connects people who want to rent out their homes with people looking for accommodations in that locale. NYC is the most populous city in the United States, and one of the most popular tourism and business places globally. Airbnb would like to understand customers and provider’s behavior and performance on the platform, marketing initiatives, implementation of innovative additional services etc.

Data Structure:
The first step was to load the data set with the proper libraries required for executing operations to be performed on the dataset. After loading and reading the data set, basic information was checked. The dataset included about 49000 rows and 16 columns. Dataset having categorical and numerical features contains null values in it. All null values and unwanted columns were removed which were of less importance.

Data Analysis:
Airbnb NYC dataset contains variables like price, room_type, neighborhood_group, neighborhood, host_id, availability_365 etc. The dataset values will help in the EDA visualization by giving an idea about price in a particular neighborhood, neighborhood groups, room types, 365 availability of rooms, and preferred room types in a particular area, criteria to select a room, reviews, minimum stay by customers etc.
Pivot tables would help to get the top 5 or 10 values or data points with the selected set of features. In addition, plots like scatter plots, joint plots, pair plots will provide insights on the data dataset and heat maps will show how the data points of variables correlate with each other.

Recommendation:

●	Manhattan and Brooklyn are the most preferred neighborhoods.

●	Home apartment rooms are the most popular room types.

●	75% of the prices is below US$200.
