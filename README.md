# Restaurant Quality and Co-location in Toronto

## Research Question
  This study aims to determine if restaurants in Toronto tend to locate near similar quality restaurants and businesses. Knowing if quality determines co-location for restaurants is important because high-quality businesses attract productive workers. These productive workers in turn increase the economic standards (Couture 2012). Moreover, understanding the spillover effects of quality of businesses in urban areas can help determine why some neighbourhoods are more desirable than others. 


## Data 
  This study asks if restaurants in Toronto locate near similar quality restaurants and non-restaurant businesses. To examine this question, Yelp’s Academic Dataset is used. Yelp’s dataset contains information for 156,639 businesses in 12 major metropolitan areas in North America, including Toronto. 
  
  For each business, the dataset provides the name and type of business it is along with a unique business ID number. Every business has an attributes column that states characteristics such as free Wi-Fi and parking, associated with that business. The dataset also states the latitude and longitude, city and the neighborhood each business is in. Further, postal code and an address for businesses are also included as separate columns. Business hours are provided alongside a separate column that states if the business is open at the current time of retrieving the dataset. A column called stars stores the average ratings received by each business so far while another column gives a count of the number of reviews received so far.  

  The independent variables that are used throughout the research include the categories variable as it stores information regarding the business type. The study requires isolating all restaurant businesses from non-restaurant businesses, that can be done with the help of categories variable. Further, this study requires knowing how every restaurant is affected by the quality of its surrounding restaurants and businesses. Thus, for each restaurant, its surrounding restaurants and businesses need to be identified first. The surrounding area for each restaurant is defined to be covered by a radius of 1 kilometer around that restaurant. Then, all the restaurants falling in that radius are considered to be the surrounding restaurants. Therefore, in order to determine the surrounding restaurants, the latitude and longitude variables are used. These latitude and longitude values are converted to kilometers first using the Haversine formula that specifically accounts for distances over the spherical surface of the Earth (Van Brummelen and Robert 2013). As the study focuses on all businesses in Toronto, the city variable is used to filter down on businesses in Toronto. Neighborhood and hours of service are included as control variables. Finally, the stars variable shows the average stars the business has received so far. This average rating will be used to represent quality in this study.


## Model and Research Methodology
  In Ohlin’s (1933) theory of agglomeration, he proposed that firms co-located to take advantage of the benefits of agglomeration. Fischer and Harrington (1996) used Ohlin’s theory of agglomeration and argued that benefits of co-location were not just limited to resource and knowledge spillovers. Co-location gave service-based firms access to additional customers due to the agglomeration of several competitive firms. High-quality service-based firms preferred to stay away from similar quality firms while low-quality firms co-located near high-quality firms (Fischer and Harrington 1996). Based on this reasoning, this study hypothesizes that high-quality restaurants in Toronto locate away from similar quality restaurants and non-restaurant businesses. Also, low-quality restaurants co-locate with high-quality restaurants and non-restaurant businesses.
 
  This study breaks down this hypothesis into two cases. First, this study checks if restaurants in Toronto prefer to co-locate with similar quality restaurants. Second, it checks if restaurants also prefer to locate near similar quality non-restaurant businesses. The hypothesis is separated into two cases to see if the type of a surrounding business plays a role in influencing the quality of restaurants and where they chose to locate. To test the above two cases, Yelp Academic Dataset is used because it contains information about businesses in Toronto. Businesses are separated into restaurant and non-restaurant business based on their category type. For the first case, a single restaurant is isolated and then restaurants surrounding this restaurant are located. The mean rating of all these surrounding restaurants is calculated and compared against the restaurant’s rating. This process is repeated for all restaurants in Toronto to obtain the ratings of every restaurant against the mean rating of the restaurants surrounding them. For the second case, this entire process is repeated to get the ratings of every restaurant against the mean rating of the non-restaurant businesses surrounding them.
  
  Apart from the mean quality of surrounding restaurants, certain other factors can affect the quality of the restaurants and so need to be controlled. Neighborhoods (&#947;) and Hours of service (&#963;) are both controls in this study.
  

For the first case, the linear equation is defined to examine the relationship between restaurant quality and the mean surrounding restaurant quality :
  
   Qir =  &#945; + &#956;&#946;Qir + &#947; + &#963;          where  i &#1013; (0, 13456)                            (1)

Similarly, for the second case, the equation is also used to see the relationship between restaurant quality and mean quality of surrounding non-restaurant businesses ().

  Qir =  &#945; + &#956;&#946;Qib + &#947; + &#963;           where  i &#1013; (0, 13456)                             (2)

 
## Results
  
  ![Table 2](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Table%202.png)
  ![Table 3](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Table%203.png)

Ordinary Least Squares (OLS) is used to understand the extent to which restaurant ratings depend on the mean ratings of surrounding restaurants. In the first case, Table 4 shows a standard error of 0.09. This indicates that the accuracy with which the sample represents the population is very high. A 0.79 regression coefficient means that an increase in the rating of a restaurant by 1 increases the mean surrounding rating of restaurants by 0.79. Finally, to see the relationship between ratings of restaurants (Y) and the mean rating of surrounding restaurants (X), a “Y and Fitted vs. X” graph is used, as seen in Figure 1. The direct relationship in the graph along with the correlation coefficient of 0.3 tells that restaurant rating and mean rating of surrounding restaurants are positively associated. 
  
  ![Figure 1](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%201.png)
  
For the second case, OLS in Table 4 is used to examining the relationship between restaurant ratings and mean rating of surrounding non-restaurant businesses. The regression coefficient shows that an increase in the rating of the restaurant by 1 increases the mean surrounding rating of non-restaurant businesses by 0.79 as well. A “Y and Fitted vs. X” graph in Figure 2 also indicates a direct, linear relationship between restaurant rating (Y) and mean rating of surrounding non-restaurant businesses (X). But the very low positive correlation of 0.07 indicates that this positive relationship is weak. 

![Figure 2](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%202.png)

Once the relationship between restaurant quality and co-location is determined, this study examines if quality of the restaurants is affected by the number of restaurants they co-locate with. Specifically, the study examines if competition affects restaurants quality. Here, competition is considered to be the number of restaurants or non-restaurant businesses. The regression line in both Figure 3 and Figure 4 shows that there is no significant relationship between restaurant quality and the number of surrounding restaurants and non-restaurant businesses. So, competition does not seem to be a factor that restaurants consider when choosing a location. 

![Figure 3](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%203.png)
![Figure 4](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%204.png)

Restaurants are also separated into good and poor-quality restaurants to see if the type of the restaurant quality determines if they choose to co-locate with a lot of other restaurants. Good-quality restaurants are defined by a rating of 3.5 and higher while poor-quality restaurants are defined by a rating of 2.5 and lower. Figure 5 shows the negative relationship between good-quality restaurants and number of surrounding restaurants. So, good-quality restaurants do not seem to locate themselves near a lot of restaurants.


![Figure 5](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%205.png)

Meanwhile, in Figure 6 it is seen that poor-quality restaurants do prefer to locate near a lot of other restaurants. On examining the nature of these low-quality restaurants, it is observed that 86% of these low-quality restaurants are fast-food restaurants. 

![Figure 6](https://github.com/shrutirao94/Yelp-Data-Analysis-for-Urban-Density/blob/master/Figure%206.png)


## Conclusions
  This study aims to understand if restaurants co-locate with similar quality restaurants and non-restaurant businesses. Analysis shows that restaurants prefer to locate near similar quality restaurants and to a lesser extent, non-restaurant businesses. Competition has no effect on quality of restaurants. However, it is seen that good-quality restaurants with a rating of 3.5 and higher seem to locate themselves away from restaurant clusters. Poor-quality restaurants with a rating of less than 2.5, seem to prefer clustering together. 

 
