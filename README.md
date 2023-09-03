## Final-Project-Statistical-Modelling-with-Python

### Project/Goals

- Request necessary data from Yelp and Foursquare. Join table to create new dataframe to store those informaiton. Then  create a database for the those data.
- Clean and validate data
- Build regression model to discover the relationship between restaurant information and the number of bikes

### Process
- Request API call from city bike API to retrieved stations data in Washington DC. Then parse the response and store the data in a dataframe.
- For each stations, use the latitude and longitude to call API request from Foursquare and Yelp API to retrieve the information of restaurant in the 1000m radius from the station cordinate. Data from Foursquare API is stored in foursquare_df dataframe, data from Yelp API is stored in yelp_df dataframe, the stations data's also added to both dataframes.
- Join two dataframe for Foursquare and Yelp to create joined_df dataframe.
- Calculated the average of number of review, average price, average rating, average distance to the station, number of restaurant using pandas group by function.
- Clean data from joined_df dataframe.
- Use heatmap and scatterplot to roughly explore the data.
- Evaluate data to build linear regression models. Improving the models to find the most fit.
- Evaluate the outcome.

### Results
- Many point of data is collected from the Foursquare and Yelp API. Yelp API provide more data point and provide an easier method to retrieved the data 
- The built model suggests that the number of bike depend on the average rating of restaurant in the area.

### Challenges 
- Local computer confid doesn't allow more API call from Foursquare and Yelp API.
- The evaluated model is not completely strong
## Future Goals
- Retrieve more data from both API to check if there is any other element that can affect the number of bikes per station
