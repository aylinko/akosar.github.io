---
layout: post
title: Imprisonment & Corruption vs. Government Type 
permalink: /stories/
---

## Background

Does the number of people imprisoned, number of penal institutions, and amount of corruption have anything to do with the type of government a country has?

When we look at the world we live in today, I always wondered if corruption and/or the type of government itself was the root of the problem with the number of penal institutions being built and the amount of people being incarcerated. I was inspired by the number of stories I would always hear of people going to a different country and going to prison. Most of the time it was some people going to North Korea or usually a different country with strict laws that these individuals would get in trouble and go to prison for a crime they did not know was a crime to begin with. Then many of the media sources would rant on how terrible this country is and how the leader is a dictator or how the people in the country are suffering from the government abusing its power over them. 

The data was created from scratch. The prison data was collected from The World Prison Brief and the corruption data was collected from Transparency International. The population data and government data was collected from Wikipedia and other sources. Originally, I wanted to collect more data on the amount of money spent building penal institutions and putting a person in jail, the type of crimes and ethnic group the imprisoned individual might have committed and came from. However, that sort of data was nonexistent for many countries since their government does not provide such data. 

If I were to predict, I would assume that countries labeled as Authoritarian and/or Dictatorship are more likely to be highly corrupted and have higher amount of penal institutions and incarcerated people while countries who are opposite, are more likely to have less incarcerated people and less penal institutions.
 
## Data

The data set consisted 209 observations and 10 variables. The following variables are Country, Population, Prison Population, Foreign (%), Female (%), Incarceration Rate (Per 100,000 of national population), Pretrial Detainees (%), Number of Penal Institutions, Government, Descriptive Form of Government, and Levels of Corruption. To note, **Country** was included the name of each country and fifteen unrecognized countries listed with the addition to Bosnia & Herzegovina split into two (Federation of Bosnia and Herzegovina and Republika Srpska), Hong Kong & Macao added under China, and the United Kingdom divided into England, Wales, Scotland, and Northern Ireland. **Government** was the type of government each destination was categorized as while **Descriptive Form of Government** was the further description of what type of government the country had. **Levels of Corruption** there was originally a division within this category with the subcategories **Rank** and **Score**. **Rank** described where the countries stand out from each other, i.e., 1 out 180 meant the country was rated as the top country with no corruption while 180 out 180 meant it was one of the bottom countries and heavily corrupted. **Score** described the score given by the Transparency International on how corrupted the country was. A score of 1 meant it was a very clean country (no corruption) and the highest score, 100, meant it was a heavily corrupted. The **score** and **Government** were mostly used along with the variables **Country**, **Prison Population**, **Incarceration Rate**, and **Number of Penal Institutions**. The data had some missing values for some of the countries and the variables used. The data set was split into three, one data set was the cleaned data set with no missing values, the other data set had the missing values and remained the same as the original, and the last, had the names changed from categorical variables to dummy variables.
 
## Analysis


Originally, Tableau and Weka were used to do the data analysis however this time R was used to do the data analysis as well as Tableau. 
There were various techniques that I have done. The most useful was the Regression method. I wanted to see if there were any other variables that would affect the question. First, all variables were chosen to see which would be significant and then a stepwise regression model was done afterwards to confirm the original results that were taken. The best model was 

       f6 = lm(Corruption.Score ~ Pretrial.Detainees + Number.Penal.Institutions + Government, data = icg)


with a p- value of 3.146e-05. This means there is a correlation between how corrupted a country is and the number of people being held in jail before their trial, number of penal institutions, and the type of government. 





## Conclusion
