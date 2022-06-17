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
  - Are there trends in time?
  - How do baby names evolve over time? 
  - Are there names that have consistently remained popular or unpopular? 
  - Are there some that have were suddenly or briefly popular or unpopular? 

### Analysis
A global overview of the visualization is presented below. The interactive components are accessible through the Tableau Software.

<p align="center">
  <img src="/Tableau/images/Tableau_Overview.png", height=500/>
</p>

#### Baby Names Evolution
A quick analysis of 2 graphs at the bottom of the visualization (evolution of births over the last century by gender) allows us to clearly detect certain patterns. For example we can see how during the First and Second World Wars, the population went from a strong growing trend to a notable decline in births over the war periods. 

What is interesting is we can also see that right after the 2nd World War, there was a strong surge in natalities in france, going from an average of 630k births/year in the 1930s France to a whopping 860k births/year in the 1950s (a 25% increase).

Another trend this visualization reveals is the end of the "30 Glorieuses" during the mid 1970s, a post-war development boom, characterized by a strong economic growth.

The last insight from this chart that we'll focus on is the predictions for the 2020-2030 period as estimated by Tableau's in-built algorithm. We can clearly see the population decline in France has been ongoing for the past decade, and trends estimate that it will continue for the following decade.

The data we have is binary (Male and Female). Therefore to be able to visualize the total number of births per year, we chose to use a stacked graph. 

#### Name popularity

The 2 graphs on the top of the dashboard are the part of the visualization that help us answer these questions : 
  - Are there names that have consistently remained popular or unpopular? 
  - Are there some that have were suddenly or briefly popular or unpopular? 

The graph on the top left dynamically shows the top 10 attributed names for the considered year.
It is useful as it reflects which names have remained in the ranking and for how long, depicting trends of names that remained popular over decades, such as "Marie" or "Pierre". It also allows us to see spikes (i.e. names whose popularity was brief, for example "Philippe"). 

The graph on the top right shows us the evolution of names *starting with* the value of the "Prénom" filter (or all if the field is blank).
This helps us see the (un)popularity of the selected names over time.

The center graph, on the other hand, illustrates the yearly evolution of top 10 attributed names of all time. The choice of the stacked graph here is justified by the *Pop-Out* effect it generates, as each name is encoded by a different color, allowing the viewer to immediately see how the popularity of names rises and falls. 

## **Visualization 2**: 
 - a choropleth map showing the distribution of names across departments ;
 - a stacked bar chart showing the 10 most frequent names.

One of these visualisations acts as 'input' and filters the second one, the 'output' By default, the 'input' visualisation is the choropleth but the user can change it if he or she so wishes it.

 - If the choropleth map is the 'input', then by clicking on a department, the stacked bar chart will show the ten most frequent names in the chosen department ;
 - If the stacked bar chart is the 'input', then by clicking on a name, the choropleth map will show the distribution of the chosen name across all departments.
 
As 'input', there exist two versions for the choropleth map :
 - 'Population' shows the number of births by department ;
 - 'Max names' shows the most frequent name by department. 

There also exist multiple filters :
 - A filter by gender (girls, boys or both) ;
 - A filter by name : the user can choose only to keep names beginning with 'A' ;
 - A filter by years : the user choose a start and end year and only names between this interval shall be kept.

This visualisation allows the user to quickly see which names are the most popular in the country, their distribution as well as the presence in some departments (chosen by the user) of more 'unique' names.

For instance, the user can choose as 'input' the bar chart and filter the data by keeping only girls. If he clicks on 'Marie', it is shown that 'Marie' is mostly present in the western as well as northernmost and easternmost parts of France. Despite differences of population, there are 25K more 'Marie' in 'Finistère' than in 'Paris'. The same can be said of the name 'Anne'. Conversely for another popular name such as 'Catherine', the distribution is much more uniform.

<p align="center">
  <img src="/Dash/Dash_1.png", height=250/>
</p>

<p align="center">
  <img src="/Dash/Dash_2.png", height=250/>
</p>

If the user chooses as 'input' Map (Max names) and filters the data by keeping only boys, then we can see that there are only 4 unique names that are the most frequent names in a department with 'Jean' being crealy the most important. However, if we filter with years and keep only the decade 2010-2020, then we can see a far greater degree of diversity with 13 different names with some regional particularities : 'Jules' being mostly present in the eastern part of France.

<p align="center">
  <img src="/Dash/Dash_3.png", height=250/>
</p>

<p align="center">
  <img src="/Dash/Dash_4.png", height=250/>
</p>

**Addendum**: Due to some technical difficulties, the option to filter the barchat while using 'Max names' choropleth map is disabled. Moreover, filtering by name can take a bit of time.

## **Visualization 3**: 
Are there gender effects in the data? Does popularity of names given to both sexes evolve consistently? (Note: this data set treats sex as binary; this is a simplification that carries into this assignment but does not generally hold.)


