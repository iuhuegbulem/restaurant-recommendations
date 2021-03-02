# restaurant-recommendations
<h2> INTRODUCTION AND BUSINESS PROBLEM </h2>

<h3> Introduction </h3>
 
The city of Lagos is the most populous state in Nigeria and one of the fastest growing cities in the world. It is divided into two main geographical areas – the island and the mainland. Victoria Island, the business and financial centre of Lagos is located on the island. It is also one of the most expensive and exclusive areas to reside in Lagos. Victoria Island is packed with offices, restaurants, hotels and night life. For people that are new to Lagos and staying in Victoria Island, it can be daunting to figure out what restaurants are worth going to and where they are. 
    
<h3> Business Problem </h3>

For this project, I am going to create a simple guide on where to eat based on Foursquare likes, restaurant category and geographic location data for restaurants in Victoria Island.  I will then cluster these restaurants based on their similarities so that a user can easily determine what type of restaurants are best to eat at based on Foursquare user feedback.


<h2> DATA REQUIREMENTS AND METHODOLOGY </h2>

<h3> Data Requirements </h3>
  
For this project, I will be utilizing the Foursquare API to pull the following location data on restaurants in Victoria Island:
<ul>
  <li> Venue Name </li>
  <li> Venue ID </li>
  <li> Venue Location </li>
  <li> Venue Category </li>
  <li> Count of Likes </li>
</ul>

<h3> Data Acquisition Approach </h3>

To acquire the data mentioned above, I will do the following:
•	Get geolocator latitude and longitude coordinates for Victoria Island, Lagos
•	Use Foursquare API to get a list of all venues in Victoria Island
o	Get venue name, venue ID, location, category, and likes

<h3> Methodology </h3>
  
The thought process behind this is that likes are a proxy for quality.  The more likes there are, the better the restaurant is.  This might be incorrect but API call issues (how many I can use for free) hold me back from getting price / rating data.  I will then bin this data into quality categorical variables so we can cluster appropriately.

I am also going to create new categorical variables for the restaurants to better group them based on type of cuisine. 

I will take the gathered data (see above in Data Acquisition Approach and Data Required sections) and will create a k-means clustering algorithm that groups restaurants into 4-5 clusters so that people looking to eat in Victoria Island can easily see which restaurants are the best to eat at, what cuisine is available and where they can look to eat.


<h2> RESULTS </h2>
  
Running my clustering algorithm, I was able to generate four clusters of restaurants.  These are as follows:

<h3> Cluster 1 </h3>
  
<ul>
  <li> Poor quality food </li>
  <li> Mostly asian food or other </li>
</ul>

<h3> Cluster 2 </h3>
  
<ul>
  <li> Below average quality food </li>
  <li> Mostly asian inspired food </li>
</ul>

<h3> Cluster 3 </h3>
  
<ul>
  <li> High quality food </li>
  <li> Mostly take out foods and fine dining restaurants </li>
 </ul>
  
<h3> Cluster 4 </h3>
  
<ul>
  <li> Above average quality food </li>
  <li> Mostly bars and fancy restaurants </li>
 </ul>


<h2> OBSERVATIONS </h2>
<ul>
  <li> There are more Mediterranean/Asian foods in Victoria Island, however, about 85% of them appear to have lesser likes amongst foursquare users </li>
  <li> Delis and fine dining restaurants are a favorite amongst foursquare users </li>
</ul>
