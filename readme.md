# Ford Go Bike bike sharing Analysis

## Introduction

This project focuses on data vizualisation. In the first part vizualisations are used to get a sens of data and  clean it by noticing outliers from plots of single variables to plots of multiple variables. The second part focuses on sharing insights and producing a short presentation that illustrates interesting properties, trends, and relationships discovered in the dataset. The aim is to get a grasp of the use of the use of "exploratory data visualization" vs "explanatory data visualization" in the data analysis process.

## Files

- 201902-fordgobike-tripdata --> dataset
- 201902-fordgobike-tripdata_clean --> cleaned dataset
- exploration_template_filled --> code in .ipynb and .html
- slide_deck_template --> code to share findings in a html presentation format (slide_deck_template.slides.html)


## Dataset

The dataset consists of 183412 bike riding records on which 16 informations were collected.
    
In this analysis, we will investigate three questions :
    - What is the distribution of the distance traveled by users ?
    - Is there a difference in terms usage duration between customers and subscribers ?
    - Should the bike seat be more ergonomic or design (style) oriented ?
    
To calculate distance from start ot end station based on longitude and latitude coordinates, this source was used :
https://www.movable-type.co.uk/scripts/latlong.html


## Summary of Findings

Distribution of distance traveled by users :
    We can notice that, as expected, the distribution is right skewed. The longest trips are around 8 km (very few over this value). The majority of trips lay around 0 and 3 km. Not much trips are under 0.5 km as biking is probably not the way to go for users who could use other transporation ways (maybe walking ?). Mixed with the number of users per year, this information could be used in many ways :
    - Know how far needs to be the closest end station from the start one.
    - Designing the next generation of Ford Go Bike in terms of sizing of mechanical components.
    - Establish a maintenance strategy based on the expected wear of this coponents.

Difference in terms usage duration between customers and subscribers :
    The mean duration of a customer usage is higher than the mean duration of a subscriber. I was personnally expecting the opposite, but this sheds lights on another possibility : that subscribers use more often the bikes for shorter trip and that customers would rent only if the duration is higher. Before drawing any conclusions, we need to investigate if other parameters have an impact on duration, this can leed afterwards to some thiking about how to charge surbscribers vs customers.
    
Ergonomic or design (style) oriented for the next gen bike seat ?
    When the first generation was launched, the media criticized the bikes for their dull design. For the next generation, Ford are thinking about a new bike seat style. However to make it look sleek, they want to make it more narrow. Women have on average wider hips then men. In terms of comfort for long rides over 30 min (specially for 40+ women) a wider bike seat is better for them. So ford would like to investigate if on the first generation, in the 40+ which on the genders uses the bikes for longer periods.
    We can notice that plots look kind of similar but that there is higher usage over longer durations for men specially over 30 min. This means we can probably orientate the design towards style without big impact over the biking experience of female 40+.


## Key Insights for Presentation

For this presentation, I focused on :
Three categorcial variables :
    - Gender (Male, Female, Other)
    - User type (Customer or Subscriber)
    - If the bike share represented the whole trip (Yes or No)
Three numerical variables :
    - Distance from start to end station (in km)
    - Duration of the bik usage (in min)
    - User age
    
For each on of the numerical variables, I started by checking (through boxplots) outliers. This helped afterwards to set the axis limits.
I focused on the distribution of one of them (distance). I then had a look at a numerical value that distinguished subscribers and customers. Afterwards, I tried to set for myself a business oreinted question with the design of the bike seat using multivariate exploration (two numerical, one categorical variables) : duration vs age by gender.
