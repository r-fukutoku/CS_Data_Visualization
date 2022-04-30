# Final Project - Movie Data

## Introduction 
The movies dataset from Keggle containing 45,000 movies information was used as an original dataset. This project focuses on the movies' popularity, their vote average, and the number of the votes and seeks to identify how popularity of movies correlates with vote average, and how this differs over time by using the movies dataset. The analysis will expose the tendencies of popularity and vote of over 40,000 movies (after removing all movies with missing observations) released over 140 years. 


## Description of Data
The original dataset, the movies dataset, from Keggle contains information on 45,000 movies featured in the Full MovieLens dataset. Features include title, budget, revenue, genres, release dates, original languages, overview, production countries, and companies. 
The dataset was re-formatted for the part of original data used complicated JSON-like formats, and missing observations were largely removed. To analyze the tendencies of popularity, vote average, and vote counts by years, four columns indicated below were taken for the subset data. 

The columns being examined:
- popularity: each movie's popularity
- release_date: the date each movie was released in "YYYY-MM-DD" format
- vote_average: each movie's vote average in a scale of 0 to 10 in steps of 0.1
- vote_count: the number of vote each movie obtained 


## Analysis Methodologies
All movies with zero vote counts were removed from the subset data, and all movie data of the dataframe was separated into seven subsets of 20-year span by extracting first four digits from the release_date column. 
Then, the visualizations were created to analyze three correlations between popularity and vote average, vote count and vote average, and vote count and popularity. The popularity values were calculated in logarithm of 10 for the better visualizations since the values vary over a wide range, from 0.000001 to 547.488298. 

The types of visualizations:
- A hexbin plot of popularity in log10 vs vote_average - the hexbin plot bins the individual movie points by where they fall on the plot, and shows areas of high density and resolves the data.
- A strip plot of vote count vs vote average: all movies were separated into three categories based on their vote average - low: 0≤x<4, middle: 4≤x<8, high: 8≤x≤10. Each movie is a plot point. 
- A strip plot of vote count vs popularity - all movies were separated into three categories based on their popularity - low: 0≤x<10, middle: 10≤x<15, high: 15≤x for 2001-2020, and low: 0≤x<30, middle: 30≤x<100, high: 100≤x for 2001-2020; the separations were adjusted for the better visualizations for the comparison purpose. Each movie is a plot point.


## Results
The key charts demonstrating the results are shown below.

**Hexbin Plots of Popularity in log10 vs Vote Average in Different Timeframe:**

![final_hexbin_1941-1960](https://user-images.githubusercontent.com/98488324/165655712-c06e7db2-5a98-4960-a04a-30f506d780a5.png)

![final_hexbin_2001-2020](https://user-images.githubusercontent.com/98488324/165655720-d5a716b3-3d0a-4083-8f52-4f00ada2201b.png)


**Strip Plots of Vote Count vs Vote Average in Different Timeframe:**

![final_strip_1941-1960](https://user-images.githubusercontent.com/98488324/166092879-190df453-e46a-4303-a42c-048e6e513050.png)
![final_strip_2001-2020](https://user-images.githubusercontent.com/98488324/166092882-cb0cc0d3-fafa-4cf8-b5f9-c30396a8ca45.png)


**Strip Plots of Vote Count vs Popularity in Different Timeframe:**

![final_strip_pop_1941-1960](https://user-images.githubusercontent.com/98488324/166092884-f6fa5180-a8cf-425e-b6d8-fd960ef1a5a6.png)
![final_strip_pop_2001-2020](https://user-images.githubusercontent.com/98488324/166092886-16e23e83-df32-4b96-884a-d6c020e2acf4.png)



## Findings from the Visualizations
The hexbin plot allowed us to have an effective visualization for the analysis of the corlleration between popularity and vote average. I created the same structured plots for seven two-decade span subset data to analyze the trends of population and vote average over time. Surprisingly, I found that there are two trends that appear in all charts with the movies over 140 years. The first one is that the plot points focus on the vote average of 5 to 8 and the popularityof 0 in log10. The second trend is that the plots showed in different colors than purple are focus on very similar place on the charts, the vote average of 6 to 8 and the popularity of 1 in log10. This is interpreted as a tendency that the popular movies tend to have relatively high votes with many vote counts. I picked two plots of 1941-1960 and 2001-2020 as they indicate the trends well and clearly. 

The stripchart captures vote count efficiently since it spans a full range of values.


## Conclusion



## References
Banik, R. (2017). The Movies Dataset, Version 7. Retrieved February 15, 2022 from [ https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset ](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset).


##### Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/r-fukutoku/Project2/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

##### Support or Contact
Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
