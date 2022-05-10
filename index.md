# Movies' Popularity and Vote Analysis Using Visualization

## Introduction 
The movies dataset from Kaggle containing 45,000 movies information was used as an original dataset. Using this dataset, this project focuses on three features, movies' popularity, their vote average and the number of vote, and seeks to identify whether there are connections between the three and how they differ over time if there are any connections. The analysis will reveal the tendencies of popularity and vote on over 40,000 movies (after removing all movies with missing observations) released over 140 years. 


## Description of Data
The original dataset, the movies dataset, from Kaggle contains information on 45,000 movies featured in the Full MovieLens dataset. Features include title, budget, revenue, genres, release dates, original languages, overview, production countries, and companies. 
The dataset was re-formatted for the part of original data used complicated JSON-like formats, and missing observations were largely removed. To analyze the tendencies of popularity, vote average, and vote counts by years, four columns indicated below were taken for the subset data. 

The columns being examined:
- popularity: each movie's popularity
- release_date: the date each movie was released in "YYYY-MM-DD" format
- vote_average: each movie's vote average in a scale of 0 to 10 in steps of 0.1
- vote_count: the number of vote that each movie obtained 


## Analysis Methodologies
All movies with zero vote counts were removed from the subset data. Then, all movie data of the dataframe was separated into seven subsets of 20-year span by extracting first four digits from the release_date column. 
Three types of visualization were created to analyze three correlations between popularity and vote average, vote count and vote average, and vote count and popularity. All seven two-decade span subset data was examined in each kind of visualization to compare the changes over time. Based on the results, two time periods, 1941-1960 and 2001-2020, were chosen for the graphs to be incorporated on this publication, as they depicted the trends and transition over time very well in two sufficiently different time periods. 
The popularity values were calculated in logarithm of 10 for the better visualization since the values vary over a wide range, from 0.000001 to 547.488298. 

The types of visualizations:
- **A hexbin plot of popularity in log10 vs vote_average**: the hexbin plot bins the individual movie points by where they fall on the plot, and shows areas of high density and resolves the data.
- **A strip plot of vote count vs vote average**: all movies were separated into three categories based on their vote average – low: 0≤x<4, middle: 4≤x<8, high: 8≤x≤10. Each movie is a plot point.   
  _(The plot scale of the vertical axis, vote count, is different between 1941-1960 plot and 2001-2020 plot for the sake of comparison.)_
- **A strip plot of vote count vs popularity**: all movies were separated into three categories based on their popularity – low: 0≤x<10, middle: 10≤x<15, high: 15≤x for 1941-1960, and low: 0≤x<20, middle: 20≤x<100, high: 100≤x for 2001-2020; the separations were adjusted for the better visualizations for the comparison purpose. Each movie is a plot point.   
  _(The plot scale of the vertical axis, vote count, is different between 1941-1960 plot and 2001-2020 plot for the sake of comparison.)_


## Results
The key charts demonstrating the results are shown below.

**Notes**: when that number is below 1, the logarithm of any positive number to any base is negative.   
**i.e., log10(100) = 2, log10(10) = 1, log10(1) = 0, log10(0.1) = -1, log10(0.01) = -2**   
_*Inside of the log10 parentheses are the actual values of popularity_

### Hexbin Plots of Popularity in log10 vs Vote Average in Different Timeframe:

![final_hexbin_1941-1960](https://user-images.githubusercontent.com/98488324/166302266-85eba58d-d398-4c41-a8fd-9e735df13c71.png)

![final_hexbin_2001-2020](https://user-images.githubusercontent.com/98488324/166256817-0d818d1d-c91b-4667-8996-cef63c50eda8.png)

#### <ins>Findings:</ins>
The hexbin plot allow us to have an effective visualization for the analysis of the correlation between popularity and vote average. By creating the same structured plots for seven two-decade span subset data, I found a trend that appeared in all charts with the movies over 140 years. The trend is that the area with high density of movies is around the vote average of 5 to 8 and the popularity around 1 (0 in log10). Specifically, 1941-1960 plot has its high density (60-80+ movies) between the popularity range of 0.3162 to 3.1623 (-0.5 to 0.5 in log10), and 2001-2020 plot has its high density (500-600+ movies) between the popularity range of 0.3162 to 10 (-0.5 to 1 in log10). This is interpreted as a tendency that the majority of movies share similar range of vote average and popularity, which does not change over 140 years. Although I expected the vote average to focus around 5 to 8 as its commonplace, it was surprising to see that even the popularity range remained similar over this long time of period. 


### Strip Plots of Vote Count vs Vote Average & Vote Count vs Popularity in 1941-1960:

![final_strip_1941-1960](https://user-images.githubusercontent.com/98488324/166092879-190df453-e46a-4303-a42c-048e6e513050.png)
![final_strip_pop_1941-1960](https://user-images.githubusercontent.com/98488324/166092884-f6fa5180-a8cf-425e-b6d8-fd960ef1a5a6.png)


### Strip Plots of Vote Count vs Vote Average & Vote Count vs Popularity in 2001-2020:

![final_strip_2001-2020](https://user-images.githubusercontent.com/98488324/166092882-cb0cc0d3-fafa-4cf8-b5f9-c30396a8ca45.png)
![final_strip_pop_2001-2020](https://user-images.githubusercontent.com/98488324/166130195-851ae83d-2267-4a9b-8242-eb81bf860732.png)


#### <ins>Findings:</ins>
The stripchart captures vote count efficiently since it spans a full range of values. There are also trends in these plots. With the larger number of movies in 2001-2020 plot, the tendencies appear to be exaggerated.

For the strip plots of vote count vs vote average, both 1941-1960 and 2001-2020's share a very similar tendency. Movies in low (0≤x<4) vote average have very few votes, movies in middle (4≤x<8) vote average spread wider than the low category's but narrower than high category's, and movies in high (8≤x≤10) vote average spread the widest in vote counts in the three categories. This means that the higher the vote average is, the larger the number of vote count is.

For another set of strip plots of vote count vs popularity, 1941-1960 and 2001-2020's appear to be slightly different. While overall spreads of plot points for three categories are similar for both time periods, the middle popularity movies in 1941-1960 plot spread their vote counts narrower than high popularity ones, and the middle popularity ones in 2001-2020 plot spread wider than high popularity ones.
This means that between 1941-1960 the higher popularity the movies have, the higher vote counts the movies obtain. The 2001-2020 plot can be interpreted in the same way, though it includes a movie with the highest vote counts but with middle popularity. 


## Conclusion
This research demonstrates the relationship between the movies' three features: popularity, vote average, and the number of vote. Each visualization was effective for this project, which allowed us to identify the features' trends and to gain insights into the dataset. 
From the results, I found that overall each correlation between popularity and vote average, vote count and vote average, and vote count and popularity shared very similar trends over 140 years. Although the number of movies published were significantly different from 1881 to 2020, it was surprising that the same trends appeared in all two-decade spans to some extent. I conclude that there were connections between movies' popularity, their vote average, and the number of vote. 


## Reference
Banik, R. (2017). The Movies Dataset, Version 7. Retrieved February 15, 2022 from [ https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset ](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset).


##### Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/r-fukutoku/Project2/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

##### Support or Contact
Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
