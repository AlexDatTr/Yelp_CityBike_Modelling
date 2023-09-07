## Final-Project-Statistical-Modelling-with-Python

### Project/Goals

- Request necessary data from Yelp and Foursquare. Join table to create new dataframe to store those informaiton. Then  create a database for the those data.
- Clean and validate data
- Build regression model to discover the relationship between restaurant information and the number of bikes

### Process
- Request API call from city bike API to retrieved stations data in Washington DC. Then parse the response and store the data in a dataframe. Here's a sample of the data received
|Latitude |	longitude|	number of bikes|	station id|
|---------|----------|-----------------|------------|
|38.890612	|-77.084801|	0.0|	1.0|
|38.986743	|-77.000035|	7.0|	2.0|
|38.865553	|-77.05003 |	8.0|	3.0|
|38.820064	|-77.057619|	7.0|	4.0|
- For each stations, use the latitude and longitude to call API request from Foursquare and Yelp API to retrieve the information of restaurant in the 1000m radius from the station cordinate. Data from Foursquare API is stored in foursquare_df dataframe, data from Yelp API is stored in yelp_df dataframe, the stations data's also added to both dataframes.
- Join two dataframe for Foursquare and Yelp to create joined_df dataframe.
- Calculated the average of number of review, average price, average rating, average distance to the station, number of restaurant using pandas group by function.
- Clean data from joined_df dataframe.
- Use heatmap and scatterplot to roughly explore the data.
- Evaluate data to build linear regression models. Improving the models to find the most fit.
- Evaluate the outcome.

### Results
- Many point of data is collected from the Foursquare and Yelp API. Yelp API provide more data point and provide an easier method to retrieved the data. With the same input 
- All different models tried in the project have low R square value and The built model suggests that the number of bike do not depend on any variables in the dataset

### Challenges 
- Local computer configuration doesn't allow more API call from Foursquare and Yelp API.
- The evaluated models is not strong, and no relationship is found from the any models
## Future Goals
- Retrieve more data from both API to check if there is any other element that can affect the number of bikes per station
