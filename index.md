# Final Project - Movie Data

## Introduction
This project focuses on the movies' popularity, their vote average, and the number of the votes. I examine how popularity of movies correlates with vote 
average, and how this differs over time by using the movies dataset. This will expose the tendencies of popularity and vote of over 40,000 movies released over 140 years. 



## Description of Data:
To analyze this relationship, the popularity, release_date, vote_average, and vote_count columns were taken for the subset data. 



## Analysis Methodologies:
I removed all movie data with zero vote, extracted first four digits indicating year from the release_date column, and separated all movie data into seven subsets of 20-year span. 
Then, I created visualizations of popularity and vote average correlation with the color differentiations based on the vote counts. The popularity values were calculated in log10 for the better visualizations since the values vary over a wide range, from 0.000001 to 547.488298. 

- A hexbin plot just of log(popularity) vs vote_average, The hexbin plot bins the individual points by where they fall on the plot, and will show areas of high density and will better resolve the data.

- A stripchart - separate the movies into two categories - more popular (maybe > 8) and less popular (or three categories) and then plot the vote count for those. That will also capture vote count better since it is spans a full range of values and not just those shown by the specific colors used in the plot you have now.



## Results:
The key charts demonstrating the results are shown below.

**Hexbin Plots for log10 of Popularity vs Vote Average in Different Timeframe:**

![final_hexbin_1941-1960](https://user-images.githubusercontent.com/98488324/165655712-c06e7db2-5a98-4960-a04a-30f506d780a5.png)

![final_hexbin_2001-2020](https://user-images.githubusercontent.com/98488324/165655720-d5a716b3-3d0a-4083-8f52-4f00ada2201b.png)


**Strip Plots for Vote Count vs Vote Average in Different Timeframe:**

![final_strip_1941-1960](https://user-images.githubusercontent.com/98488324/165883458-22ecf989-5d68-4e6b-bad3-0f97602995f0.png)
![final_strip_2001-2020](https://user-images.githubusercontent.com/98488324/165883270-004867b3-ecff-446a-b8d2-753f38bb9ff2.png)

**Strip Plots for Vote Count vs Popularity in Different Timeframe:**

![final_strip_pop_1941-1960](https://user-images.githubusercontent.com/98488324/165883324-630ad352-05f6-4fa9-822b-215cd43fec57.png)
![final_strip_pop_2001-2020](https://user-images.githubusercontent.com/98488324/165883306-c8218dfb-f3f3-41a5-9304-ccf080ba69d0.png)



## Discussion/Inference of the Visualization:
The hexbin plot bins the individual points by where they fall on the plot, and will show areas of high density and will better resolve the data.

The stripchart - you could separate the movies into two categories - more popular (maybe > 8) and less popular (or three categories) and then plot the vote count for those. That will also capture vote count better since it is spans a full range of values and not just those shown by the specific colors used in the plot you have now.



The scatter plots allowed us to have the most effective visualization for this analysis, with the vote average on x-axis, popularity in log10 in y-axis, and each movie is a plot point with the different colors that differentiate vote counts. I created the same structured scatter plots for seven two-decade span subset data to analyze the trends of population and vote average over time. 
Surprisingly, I found that there are two trends that appear in all charts with the movies over 140 years. The first one is that the plot points focus on the vote average of 5 to 8 and the popularityof 0 in log10. The second trend is that the plots showed in different colors than purple are focus 
on very similar place on the charts, the vote average of 6 to 8 and the popularity of 1 in log10. This is interpreted as a tendency that the popular movies tend to have relatively high votes with many vote counts. I picked two plots of 1941-1960 and 2001-2020 as they indicate the trends well and clearly. 




## References
Brownlee, J. (August 17, 2016). A Gentle Introduction to XGBoost for Applied Machine Learning. [_Machine Learning Mastery_](https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/). (https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/)

Chugh, A. (Dec 8, 2020). MAE, MSE, RMSE, Coefficient of Determination, Adjusted R Squared — Which Metric is Better? [_Medium_](https://medium.com/analytics-vidhya/mae-mse-rmse-coefficient-of-determination-adjusted-r-squared-which-metric-is-better-cd0326a5697e). (https://medium.com/analytics-vidhya/mae-mse-rmse-coefficient-of-determination-adjusted-r-squared-which-metric-is-better-cd0326a5697e)

Li, C. A Gentle Introduction to Gradient Boosting. [gradient_boosting.pdf](https://github.com/r-fukutoku/Project3/files/8154698/gradient_boosting.pdf)

Vega, R. D. V. and Rai, A. G. Multivariate Regression. [ Brilliant.org ](https://brilliant.org/wiki/multivariate-regression/). (https://brilliant.org/wiki/multivariate-regression/)



##### Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/r-fukutoku/Project2/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

##### Support or Contact
Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
