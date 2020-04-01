# House Data Exploration

## Dataset


## Dataset

The data contains information regarding 1460 houses, including sale price, 
overall quality, year built, above ground living area, neighborhood, zoning,
and other house qualities.

For the purposes of this project I will be working with a slightly modified 
version of the original dataset, this is available through Kaggle 
[here](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). 
The corresponding data dictionary is also available at the same link.

This dataset was originally compiled by [Dean De Cock](http://www.truman.edu/faculty-staff/decock/) 
for the primary purpose of having a high quality dataset for regression, as 
an alternative to the Boston Housing Data Set. You can read more about his 
process and motivation [here](https://doi.org/10.1080/10691898.2011.11889627) 
and download the original dataset [here](https://dsserver-prod-resources-1.s3.amazonaws.com/235/AmesHousing.txt). 
The original data dictionary can be found [here](http://www.amstat.org/publications/jse/v19n3/decock/DataDocumentation.txt).


## Summary of Findings

In the exploration, I found that there was a strong relationship between the
price of a house and its above ground liveable area, overall quality, and year 
built, with modifying effects from the neighborhood and zoning features.
The relationship is approximately linear between sale price and above ground 
liveable area when both features are transformed to be on a logarithmic scale. 
I found a similar linear relationship between sale price and overall quality.
With regards to year built, for this dataset the large majority of the houses 
were built post-WWII. The data is somewhat less linear when considering sale 
price by year built, although the trend is for newer houses to have higher prices. 
Above ground liveable area and overall quality show that generally larger houses 
will have higher quality levels. I found that these house features are somewhat 
interdependent. Looking at sale price with respect to neighborhoods my findings 
were that there are specific neighborhoods where the sales prices are higher. 
When comparing year built by neighborhood I found some pattern of development for 
specific areas, always keeping in mind that the data represents a subset of the 
houses and there were missing years for which data could not be readily imputed. 
I also looked at the interaction between sale price, year built, and overall quality. 
Here again the findings were dependent on the available data points, however it was
apparent that the most recent houses in the dataset were achieving substantially 
higher quality ratings while prices also rose substantially. 

Outside of the main variables of interest, I verified the relationship between
house neighborhood and zoning. For the dataset given, zoning does not play such 
an important role in being a possible predictor for sale price since the majority 
of the houses are designated as Residential Low Density. 


## Key Insights for Presentation

For the presentation, I focus on just the influence of the above ground living area,
overall quality, year built, neighborhood, and zoning, setting aside the other numerous 
features. I start by introducing the sale price variable, followed by the pattern in 
above ground living area distribution, then plot the transformed scatterplot. I proceed 
with the distribution of overall quality and then use a categorical swarm plot to visualize 
the relationship between sale price and overall quality, and also above ground living area 
and overall quality. Next, I look at the distribution of year built. I use a scatter plot 
for sale price versus year built.

Afterwards, I introduce the categorical variables one by one. To start, I use an ANOVA
test to show that neighborhood has significant disparity in predicting sale price. I 
then use a bar plot to show the distribution of houses by neighborhood for the dataset.
A swarm plot of sale price by neighborhood helps to visualize house prices across these
neighborhoods. I employ a heatmap to show development trends in neighborhoods, limiting
the data to houses built from 1950 onwards. I then use a bar plot to show the different 
zones, and then using the same color-coding with a categorical swarm plot to show the 
possible relationship between sale price, neighborhood, and zoning. Finally I employ a
categorical swarm plot to visualize sale price, year built, and overall quality. 

I asked for and received valuable feedback on this project. For the categorical swarm 
plots I had originally planned to use violin plots however due to the size of the features
the visualization was rather poor. I then tried reducing the number of neighborhoods, and 
the year built however felt that it was not a good choice to leave out the bigger picture.
One colleague made suggestions about using the categorical swarm plot and I think that for 
this particular case it provides valuable insight. Another colleague made suggestions about
the color choices used in the plots, especially where insights into particular variables
are used from one plot to the next.

