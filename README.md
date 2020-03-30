## Airbnb Data Exploration -Portland, OR
Live website [here](https://bootcampe-project2.herokuapp.com/)

### Overview
Explored Airbnb data to perform price-trend and popularity analysis over time in Portland, OR. A Leaflet map was created to show clusters by neighborhood with number of reviews by neighborhood. 48 csv files (32.2 MB) were combined, cleaned and SQL database was created using python. D3.js was used to create impactful charts and a flask app was created to render html with the charts coming from d3.js. Webpage was built and deployed in Heroku. 

### File and Guideline
etl.ipynb consist of complete ETL process via SQL Alchemy. Created three SQL tables in a database called airbnb_db (rentals listings and airbnb) from Zillow and Data_World CSVs. 

- Raw data are in the Resources folder
- HTML pages are in the templates folder
- CSS and JS in the static folder

The flask app is airbnb_app.py. We are using it to render on landing2.html with the chart coming from rentals_listings_d3.js

### Limitations
Some of the primary limitations we found with our datasets were that the Airbnb, Home Listing Values and Rental Values had different amounts of neighborhood data. For example, the rental data had twice as many listed neighborhoods. In addition, some of the data was unavailable for some of the months listed and reflects as zero. It was also pointed out that reviewing this as a mean or median listing can be difficult given that each neighborhood has a different number of rentals and listings.

### After Action Review
One area to improve would be to clean or remove all the data which has a value of zero. 

The questions that we wanted to answer according to our proposal are
1. Is popularity of portland Airbnb increaseing with time, 2015 to 2019? 
For this, we used airbnb review trend over years. 
2. How is the average price of portland Airbnb changing over time?
To plot average price of portland Airbnb changing over time , to make the graph informative we had to find mean price in each year.
3. Compare prices of Airbnb and houselisting prices over time.
We used d3.js to plot all the graphs.Combining different persons codes to single .js file was also a challenge. 

Leaflet library is used to get the map on our web page.  Marker clusters were used to show density of listings for the most recent data we have available.  Neighborhood boundaries were included to be able to see visually which neighborhood a listing was in.  Pie charts were added to neighborhoods to show the distribution of room types available in that neighborhood.
