# Final Project - Movie Data

## Introduction 
The movies dataset from Kaggle containing 45,000 movies information was used as an original dataset. This project focuses on movies' popularity, their vote average, and the number of the votes and seeks to identify the correlations between three measurements, popularity, vote average, and vote count, and how these differ over time by using the movies dataset. The analysis will expose the tendencies of popularity and vote of over 40,000 movies (after removing all movies with missing observations) released over 140 years. 


## Description of Data
The original dataset, the movies dataset, from Kaggle contains information on 45,000 movies featured in the Full MovieLens dataset. Features include title, budget, revenue, genres, release dates, original languages, overview, production countries, and companies. 
The dataset was re-formatted for the part of original data used complicated JSON-like formats, and missing observations were largely removed. To analyze the tendencies of popularity, vote average, and vote counts by years, four columns indicated below were taken for the subset data. 

The columns being examined:
- popularity: each movie's popularity
- release_date: the date each movie was released in "YYYY-MM-DD" format
- vote_average: each movie's vote average in a scale of 0 to 10 in steps of 0.1
- vote_count: the number of vote each movie obtained 


## Analysis Methodologies
All movies with zero vote counts were removed from the subset data. Then, all movie data of the dataframe was separated into seven subsets of 20-year span by extracting first four digits from the release_date column. 
Then, the visualizations were created to analyze three correlations between popularity and vote average, vote count and vote average, and vote count and popularity. The popularity values were calculated in logarithm of 10 for the better visualizations since the values vary over a wide range, from 0.000001 to 547.488298. 

The types of visualizations:
- **A hexbin plot of popularity in log10 vs vote_average**: the hexbin plot bins the individual movie points by where they fall on the plot, and shows areas of high density and resolves the data.
- **A strip plot of vote count vs vote average**: all movies were separated into three categories based on their vote average - low: 0≤x<4, middle: 4≤x<8, high: 8≤x≤10. Each movie is a plot point. (The size of plot regarding the vertical axis, vote count, is different between 1941-1960 plot and 2001-2020 plot to examine their trends).
- **A strip plot of vote count vs popularity**: all movies were separated into three categories based on their popularity - low: 0≤x<10, middle: 10≤x<15, high: 15≤x for 2001-2020, and low: 0≤x<20, middle: 20≤x<100, high: 100≤x for 2001-2020; the separations were adjusted for the better visualizations for the comparison purpose. Each movie is a plot point. (The size of plot regarding the vertical axis, vote count, is different between 1941-1960 plot and 2001-2020 plot to examine their trends).


## Results
The key charts demonstrating the results are shown below.

**Hexbin Plots of Popularity in log10 vs Vote Average in Different Timeframe:**

![final_hexbin_1941-1960](https://user-images.githubusercontent.com/98488324/166302266-85eba58d-d398-4c41-a8fd-9e735df13c71.png)

![final_hexbin_2001-2020](https://user-images.githubusercontent.com/98488324/166256817-0d818d1d-c91b-4667-8996-cef63c50eda8.png)


**Strip Plots of Vote Count vs Vote Average in Different Timeframe:**

![final_strip_1941-1960](https://user-images.githubusercontent.com/98488324/166092879-190df453-e46a-4303-a42c-048e6e513050.png)
![final_strip_2001-2020](https://user-images.githubusercontent.com/98488324/166092882-cb0cc0d3-fafa-4cf8-b5f9-c30396a8ca45.png)


**Strip Plots of Vote Count vs Popularity in Different Timeframe:**

![final_strip_pop_1941-1960](https://user-images.githubusercontent.com/98488324/166092884-f6fa5180-a8cf-425e-b6d8-fd960ef1a5a6.png)
![final_strip_pop_2001-2020](https://user-images.githubusercontent.com/98488324/166130195-851ae83d-2267-4a9b-8242-eb81bf860732.png)



## Findings from the Visualizations
The hexbin plot allowed us to have an effective visualization for the analysis of the corlleration between popularity and vote average. I created the same structured plots for seven two-decade span subset data to analyze the trends of population and vote average over time. I found a trend that appears in all charts with the movies over 140 years, which is that the areas of high density are around the vote average of 5 to 8 and the popularity range of -1 to 1 in log10. This is interpreted as a tendency that the mojority of movies share similar range of vote average and popularity which do not change over 140 years. I picked two plots, 1941-1960 and 2001-2020, as they indicate the trend well.

The stripchart captures vote count efficiently since it spans a full range of values. There are also trends in these plots. For the first two strip plots of vote count vs vote average, both 1941-1960 and 2001-2020's share very similar trend. Movies in low (0≤x<4) vote average have very few votes, movies in mediam (4≤x<8) vote average spread wider than the low category's but narrower than high category's, and movies in high (8≤x≤10) vote average spread the widest in vote count in the three categories. This means that the higher the vote average is, the larger the number of vote count is.

For the second two strip plots of vote count vs popularity, 1941-1960 and 2001-2020's appear to be very similar. With larger number of movies in 2001-2020 plot, the tendency is exaggerated. Low popularity movies have small vote counts, mediam popularity movies spread their vote counts wider than low popularity ones but wider than high popularity ones, and high popularity movies spread out widely and evenly from small to large vote counts. 


## Conclusion
From this analysis with three different types of visualizations, I found that the movies' population, vote average, and vote count share very similar trends over 140 years. Although the number of movies published are very different in 1881 and 2020, it was surprising that the trends appear in all two-decade span. I conclude that there were correlations between vote count and vote average, and vote count and popularity, while there was no relationship between vote average and popularity. 


## References
Banik, R. (2017). The Movies Dataset, Version 7. Retrieved February 15, 2022 from [ https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset ](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset).


##### Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/r-fukutoku/Project2/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

##### Support or Contact
Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
