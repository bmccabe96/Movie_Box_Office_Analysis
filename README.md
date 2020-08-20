# Movie_Box_Office_Analysis
For this project, we analyze movie data we gathered on the web to present to Microsoft with recommendations on certain metrics regarding the movie they intend to make.

## Table of Contents
1. Codes
1. Analysis and Recommendations
1. Conclusion
1. Disclaimers

## Codes
#### Box_Office_Mojo_Scrape.ipynb
* Gathers data from boxofficemojo.com for 2015-2020
* Compiles data into dataframe and cleans it up to the point that analysis can be done
* Creates a csv that can be used for analysis
#### Twitter Data Collection-Copy1.ipynb
* Utilizes "twint" twitter api to gather data
* Gets 50 popular tweets for every movie
* Stores data in jsons and creats a list of dataframes to then aggregate the data into a final csv
#### Reddit_API_Calls_and_Webscrape.ipynb
 * **TBD**
#### Mojo_and_Twitter_Analysis.ipynb
* Explores data gathered from boxofficemojo and twitter
* Asks questions and uses the data to formulate answers and inferences
* Creates and saves images created from data visualizations
#### TMDB_Watch_Mojo_db_Analysis.ipynb
* **TBD**
* **TBD**
#### Reddit_Data_Anaylsis.ipynb
* **TBD**
* **TBD**



## Analysis and Recommendations

### Budget Analysis
**TBDTBDTBDTBDTBD**
**TBDTBDTBDTBDTBD**


### Revenues and Theaters Correlation

![Image](Screenshots/Gross_Theaters_Heatmap.png?raw=true)

These are all correlated. Apart from the information we received from the prior two graphs (see analysis ipynb), there is one more piece of relevant information here. There is a very strong correlation between opening weekend gross revenue and overall gross revenue.

Our advice to Micosoft here is to focus hard on the opening weekend, regardless of the kind of movie they release. Spend money on ads and make sure to promote the movie ahead of time so that the opening weekend is as good as possible.

### Genres to Gross Revenue Analysis

![Image](Screenshots/Genres_vs_Gross.png?raw=true)

As we can see here from the past 5 years of movie data, adventure and sci fi movies are doing very well from a gross revenue standpoint. The numbers are almost certainly inflated from the regine of the Marvel movies, so that needs to be considered. Another point that needs to be considered is that sci fi movies likely have a higher cost of production, since the CGI and action scenes involve quite a lot of work. Though, that is not to say that an action movie can be low budget.

Our advice to Microsoft here would be to make a movie with a genre that falls within the better half from the graph above. Adventure, scifi, action, comedy, animation, etc. Our other advice is to not make an adult film...for a number of reasons.

### Runtime and Rating Analysis

![Image](Screenshots/Popularity_Rating_Length.png?raw=true)

The results above can be analyzed to help determine the length of the movie and the maturity level of the movie.

From both graphs, it is interesting to note that longer movies tend to do better both in terms of popularity and revenue when the movie is targeted at a more adult audience (PG13, PG, R). Howecver, for G rated movies, medium/shorter movies tend to do better. This could be due to the fact that many children that watch G rated movies likely have shorter attention spans than the average adult.

Our recommendation to Microsoft is to make a long movie for any adult genre. If Microsoft wishes to make a G rated movie, then we recommend shortening the runtime.

### Day of the Week Analysis
**TBDTBDTBDTBDTBD**
**TBDTBDTBDTBDTBD**

### Twitter Data Analysis

![Image](Screenshots/Twitter_Genre.png?raw=true)

After compiling a list of likes, retweets, and replies for top tweets for every movie, we then wanted to see how the numbers responded to grouping by movie category. From the data above, it appears that musicals get quite a lot of social media presence. This could be for a variety of reasons. (1) While musicals are not as common as action/adventure, when they are released, they are often released based on a world-famous broadway show such as Les Mis or on a world famous musician (Elton John - Rocketman), so they could amass quite a large following on social media. (2) People often times create cover-songs or even musical-parodies based off famous songs. Twitter would be a place for people to share these videos, and if one of them goes viral (either it is a very funny spoof or a really impressive work of musician-ship), it would amass a lot of likes/retweets/replies.

As far as recommendations to Microsoft, this data should be taken with a grain of salt. Data found on twitter should not be held in high standards, and certainly should not be used to make any decisions. These findings are more of a nice-to-have. Once Microsoft decides on a movie, they can check these charts, compare them with the movie genre they decided to make, and from that, can get a very rough idea of how much social media presence their movie can expect. This could help them decide on how much they should invest in social media advertizing for their movie.


## Conclusion

## Disclaimers
Because this is a public directory, we would like to note that we **are not** working with Microsoft in any capacity about movies. To the best of our knowledge, Microsoft **has no plans to make a movie**
