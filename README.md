# Movie_Box_Office_Analysis
For this project, we analyze movie data we gathered on the web to present to Microsoft with recommendations on certain metrics regarding the movie they intend to make.

## Table of Contents
1. Codes
1. Analysis and Recommendations
1. Conclusion
1. Future Analysis
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
* Collects urls from Reddit using API calls
* Collects Data from urls using Selenium Library
* Cleans and organizes Data in prepration to be exported to a final csv
* Stores clean dataset in a final csv file
#### Watch_Mojo_dataset_merged_with_TMDB_dataset.ipynb
* Short notebook, simply merges our TMDB and Mojo datasets into one large dataframe
* Exports as csv
#### Mojo_and_Twitter_Analysis.ipynb
* Explores data gathered from boxofficemojo and twitter
* Asks questions and uses the data to formulate answers and inferences
* Creates and saves images created from data visualizations
#### TMDB_Watch_Mojo_db_Analysis.ipynb
* Explores data using the TMDB and Watch Mojo Datasets
* Asks the Question "how does the day of the week influences opening weekend sales?"
* Creates visulazations and computes metrics to determine the best day to release a movie
#### Mojo_TMDB_Monthly_Analysis
* Explores data using the TMDB and WatchMojo datasets
* Asks the Question "does the time of year matter?", specifically the month of the year.
* Creates visualizations and computes metrics to determine which month or range of months will bring the most box office success
#### Reddit_Data_Anaylsis.ipynb
* Explores the Reddit dataset that we obtained through webscraping 
* Explores the relationship between budget and box office sales 
* Through data visualizations and computing metrics, insights about the ideal budget are shown.


## Analysis and Recommendations

### Budget and Value Analysis
![Image](Screenshots/Values%20for%20the%2010%20Highest%20Budgeted%20Movies.png?raw=true)

![Image](Screenshots/Values%20for%20the%2010%20Lowest%20Budgeted%20Movies.png?raw=true)

Value,in this context,is a ratio of Worldwide Box Office Sales to a Movie's budget. So we are essentially measuring how much money did a movie generate
vs how much did it cost to produce. The plots themselves are very telling in this case. As for the 10 most expensive movies, Only two movies actually had a value north of 5 (highest was 7). While in the case of the 10 least expensive movies, 4 movies had a value of 9 or greater (3 of those were greater than 10).
Also, from a metrics standpoint. The median Value for the least 10 expensive movies was 2.9 while for the 10 Most Expensive it was only 1.7.
Clearly,if you just want to maximize profits, having a super high budget is not the best way to do so.

![Image](Screenshots/Box_Office_Budget_Scatterplot.png?raw=True)

As you can see in the graph,There is a strong linear relationship between Budget and worldwide sales. So you can expect about $3.5 in worldwide revenue for 
every dollar spent on budget. 
Thus,our advice to Microsoft is to maximize profit and select a budget of around 50 million.(average budget of 10 most valuable films)
Microsoft should follow our advice because almost all of the movies from the most valuable list have a budget between 20-50 million.
This way Microsoft will be able to maximize their value and also maximizing profit. (since worldwide sales increases linearly with budget). 
Our estimation says they would generate $175 million in gross worldwide revenue, thus a net profit of $125 million. Not too shabby. 


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

### Week and Month Analysis
**Week Analysis**
![Image](Screenshots/Day%20of%20the%20Week%20vs%20Opening%20Weekend%20Sales.png?raw=true)
This graph is looking at day of the week vs opening weekend sales because opening weekend sales is very important to a movie's success.
In fact, on average 28% of a Movie's revenue comes from opening day weekend.
As you can see, Friday is the best day to maximize opening weekend sales. 
However, our recommendation to Microsoft would be to pick a Wednesday for a release date. There are two main reasons as to why.
One, Wednesday had the second best numbers out of all of the days of the week and only 8% of new releases in our dataset were released on a Wednesday.
Compared to Friday, which contains 81% of the movies in our dataset.
That is a lot less competition.
Also, by releasing the movie on a wednesday, Microsoft can essentially create a "5-day weekend" and really try to get as many people in the seats as possible.

**Month Analysis**
![Image](Screenshots/2015-2020%20Monthly%20Median%20Gross%20Box%20Officw%20Sales.png?raw=true)
As can be seen above, December is the best month to release a movie. In 4 out of the last 6 years, December had the most Box office sales.
Due to the holiday season, this is expected.
However, These graphs show that Febraury and November also do very well.
Since November is right before december, this is not too surprising.
However, February was a surprise.
Thus, our we suggestestion to Microsoft would be to release a movie in Febraury where they will have the least competition from big blockbuster films.
The numbers aren't strong enough to merit a recommendation But we believe february should certainly be  considered.
### Twitter Data Analysis

![Image](Screenshots/Twitter_Genre_Averages.png?raw=true)

After compiling a list of likes, retweets, and replies for top tweets for every movie, we then wanted to see how the numbers responded to grouping by movie category. From the data above, it appears that the genres that get the most traction on social media more or less aline with the genres that generated the most revenue. Genres like action and adventure get quite a lot of hype it seems. This makes sense, since the past 5 years had a lot of Marvel movies, and they have dominated the industry to some extent.

From the data above, it appears that musicals get quite a lot of social media presence. This could be for a variety of reasons. (1) While musicals are not as common as action/adventure, when they are released, they are often released based on a world-famous broadway show such as Les Mis or on a world famous musician (Elton John - Rocketman), so they could amass quite a large following on social media. (2) People often times create cover-songs or even musical-parodies based off famous songs. Twitter would be a place for people to share these videos, and if one of them goes viral (either it is a very funny spoof or a really impressive work of musician-ship), it would amass a lot of likes/retweets/replies.

As far as recommendations to Microsoft, this data should be taken with a grain of salt. Data found on twitter should not be held in high standards, and certainly should not be used to make any decisions. These findings are more of a nice-to-have. Once Microsoft decides on a movie, they can check these charts, compare them with the movie genre they decided to make, and from that, can get a very rough idea of how much social media presence their movie can expect. This could help them decide on how much they should invest in social media advertizing for their movie.


## Conclusion

From our analysis, we have come to three final recommendations for Microsoft. We believe our other recommendations should still be considered and noted, but the following should be weighed more heavily:
1. Microsoft should create a budget of $50 million for this film. We believe that any budget between $20-50 million should be capable of maximizing a movie's Value.However, the $50 million number is the sweet spot in that range since profits goes up linearly with budget. This allows microsoft to maximize Value and Profit as much as possible.
1. Microsoft should create a long movie if they are targeting an adult audience, and a shorter movie if they are targeting a child audience. From our data, this long insinuates a movies of at least 109 minutes, and short insinuates a movie no longer than 96 minutes.
1. Microsoft should release the movie on a Wednesday. By releasing on wednesday, they can generate a lot of profit from the "5-day Weekend effect" and also will have a lot less competition. 

## Future Analysis
1. One area we would like to explore data from online streaming services such as Netflix,Amazon Prime Video,HBO,hulu, and etc... We would be particularly interested in viewer data such as number of downloads/purchases of movies as well as view counts.
1. One other area we could research further is how the global pandemic is affecting the movie industry. Maybe certain genres will do better amidst the pandemic. Additionally, with theaters closed, we would need to research the best platform to release our movie.
1. One last area of interest would be the correlation between critic reviews and general population reviews. We would acquire this data through sites such as Rotten Tomatoes and IMDB.

## Disclaimers
Because this is a public directory, we would like to note that we **are not** working with Microsoft in any capacity about movies. To the best of our knowledge, Microsoft **has no plans to make a movie**

