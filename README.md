<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/fr/d/d9/Logo_T%C3%A9l%C3%A9com_ParisTech.svg", height=200/>
</p>

<p align="center">
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
The graph below shows summary analysis of the evolution of births over the last decade by gender :

<p align="center">
  <img src="/Tableau/images/BirthsEvolution.png", height=500/>
</p>

This quick analysis allows us to clearly detect certain patterns. For example we can see how during the First and Second World Wars, the population went from a strong growing trend to a notable decline in births over the war periods. 

What is interesting is we can also see that right after the 2nd World War, there was a strong surge in natalities in france, going from an average of 630k births/year in the 1930s France to a whopping 860k births/year in the 1950s (a 25% increase).

Another trend this visualization reveals is the end of the "30 Glorieuses" during the mid 1970s, a post-war development boom, characterized by a strong economic growth.

The last insight from this chart that we'll focus on is the predictions for the 2020-2030 period as estimated by Tableau's in-built algorithm. We can clearly see the population decline in France has been ongoing for the past decade, and trends estimate that it will continue for the following decade.

#### Names Evolution

<p align="center">
  <img src="/Tableau/images/Top10Evolution.gif"/>
</p>


## **Visualization 2**: 
This section is realized using Dash, Dash which is an application that give a point-&-click interface to models written in the Python progamming language, vastly expanding the notion of what's possible in a traditional "dashboard." In this segment, we will be answering :
  - Is there a regional effect in the data?  
  - Are some names more popular in some regions? 
  - Are popular names generally popular across the whole country?

## **Visualization 3**: 
Are there gender effects in the data? Does popularity of names given to both sexes evolve consistently? (Note: this data set treats sex as binary; this is a simplification that carries into this assignment but does not generally hold.)


