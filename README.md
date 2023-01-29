<p align="center"><img src="images/movie_reel.png" alt="movie reel"></p>

# Microsoft Enters Film Industry: Data Analysis and Recommendations

Team: Diego Fernandez, Rachael McCue, Parker DeShazo

[Slide Deck](https://docs.google.com/presentation/d/17G9n6wys8Iu3T0q2sCgcOy3Fa13mw6SsH-ouRQe6H10/edit?usp=sharing)


## Overview
Microsoft will be entering the film industry, and we were tasked with analzying some data sets to set them up for success on their first film. Using domain knowledge, and the datasets provided below, we drew insights about the movie industry, genres, creative talent, and release dates that have shown to be successful. 

Data is reviewed from:
  - IMDB database
  - The Numbers
  - The Movie Database
  
## Navigating this repository

| Folder Name | Contents    |
| ----------- | ----------- |
| notebooks   | Code & output file production  |
| images      | Plots & images     |
| zipped_data  | Raw zipped datasets |
| plotting_data  | Datasets created |


## Business Understanding
Microsoft, while a head honcho in many other facets, is the underdog in the film industry. They have the capital to produce a film, but perhaps not the experience. In order for Microsoft to insert themselves into the $209B industry, we studied what would be a successful safe-bet first movie. What genres are proven to be successful? What time of year should you release a film? Who should you hire to produce the film? 

We used total revenue to locate successful genres to tap into, as well as return on investment to see who to hire and when to release a film. 


## Data Understanding and Analysis

Our insights were retrieved by creating a master data set with the following parameters: 
- A budget of at least $10 million to rule out the small or independent filmmakers
- Dropped any data that did not have a worldwide gross income datapoint

The master dataset includes 1091 movies released between 2010-2020 with the following information:
  - Release Date
  - Movie Name 
  - Production Budget
  - Inflation Adjusted Production Budget
  - Domestic Gross 
  - Worldwide Gross
  - Worldwide Profit
  - ROI
  - Person Name
  - Movie Role
  - And boolean values for all of the genres:
  Action, Adult, Adventure, Animation, Biography, Comedy, Crime, Documentary, Drama, Family, Fantasy, Game-Show, History, Horror Music, Musical, Mystery,   News, Reality-TV, RomanceSci-Fi, Short, Sport, Talk-Show, Thriller, War, Western
 
 
Data Limitations:
- The raw data sets did not include information on all of the same movies. This implied that we lost information that could bias our analysis of the top genres, cast, and crew.
- Rotten Tomatoes data sets did not contain movie titles, therefore, we could not connect reviews and ratings to our dataset.
- The IMDB dataset included movies without listed genres, meaning the data could be skewed in favor of some genres.

While merging some individual datasets, we merged on Movie Name amd Release Date as keys so we knew we were referencing the correct movie. There were some duplicate movie names, such as Avatar. Did you know there is a Japanese horror film called Avatar? 
 
### Genre Recommendations

Based on worldwide gross, the following genres brought in the most revenue: Action, Adventure, and Comedy. These genres make up 28% of the market. These genres are the ideal initial investment.

<p align="center"><img src="images/gross_revenue_pie_chart.png" alt="genre pie chart"></p>


### Talent Recommendations

We also found that particular creative talent is a driver for return on investment. We analyzed directors, producers, writers, actors and actresses based off of their ROI. These people were all involved in at least 3 movies between 2010 and 2020. They were also involved in films where the inflation adjusted budget was at least $24 million -- this is the Q1 of budgets from the dataset. In addition to pulling the data, we did some research to ensure these people were relevant in the industry. We used their median ROI, as mean would be skewed towards outliers. The relevant plots can be located in the talent_recommendations notebook.

<p align="center"><img src="images/talent_table_names.png" alt="tables of talent recommendations"></p>


### Release Planning

Also using median ROI, we found the best time of year to release a movie. July is the optimal release month, followed by the winter holiday season.

<p align="center"><img src="images/release_month_roi.png" alt="bar graph of release months"></p>


## Conclusion

While there are many factors in creating a great movie, we decided on finances as the measure of success. 

These are the recommendations for Microsoft's entry into the film industry: 

- Lucrative genres include Action, Adventure, and Comedy. 

- Creative talent selection has the greatest correlation to return on investment. 

- The best time to release a film is in the summer (specifically July), followed by the winter holidays. 

