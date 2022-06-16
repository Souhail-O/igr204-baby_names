<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/fr/d/d9/Logo_T%C3%A9l%C3%A9com_ParisTech.svg", height=200/>
</p>

<p align="center">
  <b>Post Masters' Degree in Artificial Intelligence - 2021/2022</b><br>
  <b>IGR204 - Data Visualization</b><br>
  <i>Pr. James EAGAN</i><br>
  Lab4 - Baby Names
</p>

<p align="center">
  <b> Authors :</b><br>
  - Souhail OUMAMA<br>
  - Alexandre ROULEAU<br>
  - Charles-Elie SIMON<br>
  - Roland SCHWARTZ<br>
  - Florian TORROBA<br>
</p>

In this mini-project, we will be working with a data set of baby names in France. It contains the list of all baby names registered in France, year by year, from 1900 through 2019. There are two data sets: one aggregated to the national level, and another with data by department. 

Our goal is to create 3 different visualizations around these data, each focussed on answering different kinds of questions about the data:

## **Visualization 1**: 
This section is done on the Tableau visualization sotfware, answering the most general questions to get a feeling of our data. The questions it aims to anwser are : 
  - How do baby names evolve over time? 
  - Are there names that have consistently remained popular or unpopular? 
  - Are there some that have were suddenly or briefly popular or unpopular? 
  - Are there trends in time?

### Analysis
#### Births Evolution
A global overview of the visualization is presented below. The interactive components are accessible through the Tableau Software.

<p align="center">
  <img src="/Tableau/images/Overview.png", height=500/>
</p>

A quick analysis of the lowest graphs (evolution of births over the last century by gender) allows us to clearly detect certain patterns. For example we can see how during the First and Second World Wars, the population went from a strong growing trend to a notable decline in births over the war periods. 

What is interesting is we can also see that right after the 2nd World War, there was a strong surge in natalities in france, going from an average of 630k births/year in the 1930s France to a whopping 860k births/year in the 1950s (a 25% increase).

Another trend this visualization reveals is the end of the "30 Glorieuses" during the mid 1970s, a post-war development boom, characterized by a strong economic growth.

The last insight from this chart that we'll focus on is the predictions for the 2020-2030 period as estimated by Tableau's in-built algorithm. We can clearly see the population decline in France has been ongoing for the past decade, and trends estimate that it will continue for the following decade.

#### Names Evolution

<p align="center">
  <img src="/Tableau/images/Top10Evolution.gif"/>
</p>

This visualization allows us to examine how names evolved over time, mainly for the top 10 given names by year. 

As we can observe, things have changed over the course of the 20th century, and much of the trends we described earlier manifest their effects on each name, of course with subtle differences as each lived its own cycle.

Let us now examine how some names evolved over time : 
- **Marie** : Peaked at the beginning of the century and has been on a constant decline for over 100 years.
- **Jean** : Already the most common name in the early 1900s, this name has reached its peak in 1946 before fading away as well. The popularity of the name during the early 40s might have to do with Jean Moulin, the famous French resistant after the end of the Second World War.
- **Philippe** This name has been riding low on the radar until the 1950s where it started tracting popularity among newborns, until it peaked in 1964, all before fading away as well
- **Uncommon Names** : Starting in the mid-40s, newer names were given to babies more and more often, until 1974 where the newcomers dominated the game, as in 2020, they represent more than 90% of the overall newborns. This doesn't mean that the previously mentioned names have disappeard all together, but their numbers have been dilluted into all their variants.

## **Visualization 2**: 
This section is realized using Dash, Dash which is an application that give a point-&-click interface to models written in the Python progamming language, vastly expanding the notion of what's possible in a traditional "dashboard." In this segment, we will be answering :
  - Is there a regional effect in the data?  
  - Are some names more popular in some regions? 
  - Are popular names generally popular across the whole country?

This visualisation is composed of two main representations :
 - a choropleth map showing the distribution of names across departments ;
 - a stacked bar chart showing the 10 most frequent names.

One of these visualisations acts as 'input' and filters the second one, the 'output' By default, the 'input' visualisation is the choropleth but the user can change it if he or she so wishes it.
 - If the choropleth map is the 'input', then by clicking on a department, the stacked bar chart will show the ten most frequent names in the chosen department ;
 - If the stacked bar chart is the 'input', then by clicking on a name, the choropleth map will show the distribution of the chosen name across all departments.

There also exist multiple filters :
 - A filter by gender (girls, boys or both) ;
 - A filter by name : the user can choose only to keep names beginning with 'A' ;
 - A filter by years : the user choose a start and end year and only names between this interval shall be kept.

This visualisation allows the user to quickly see which names are the most popular in the country, their distribution as well as the presence in some departments (chosen by the user) of more 'unique' names.

## **Visualization 3**: 
Are there gender effects in the data? Does popularity of names given to both sexes evolve consistently? (Note: this data set treats sex as binary; this is a simplification that carries into this assignment but does not generally hold.)


