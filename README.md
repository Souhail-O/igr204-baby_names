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

In this mini-project, we will be working with a data set of baby names in France. It contains the list of all baby names registered in France, year by year, from 1900 through 2020. There are two data sets: one aggregated to the national level, and another with data by department. 

Our goal is to create 3 different visualizations around these data, each focused on answering different kinds of questions about the data.

## **Visualization 1**: 
This section is done on the Tableau visualization software, answering the most general questions to get a feeling of our data. The questions it aims to answer are : 
  - Are there trends in time?
  - How do baby names evolve over time? 
  - Are there names that have consistently remained popular or unpopular? 
  - Are there some that have were suddenly or briefly popular or unpopular? 

### Analysis
A global overview of the visualization is presented below. The interactive components are accessible through the Tableau Software.
(Tableau file attached at *Tableau/baby_names.twb*)

<p align="center">
  <img src="/Tableau/images/Tableau_Overview.png", height=500/>
</p>

#### Baby Names Evolution & Name popularity

The 3 graphs on the top of the dashboard are the part of the visualization that help us answer all the questions we have asked before.

The main problem we encountered was the quantity of information in the dataset. We know that clutter is an issue that comes from the visualization, and not from the data, so that is what we tried to tackle through our work.

We included interaction in our visualization through 2 filters. The year filter is connected to all graphs on the top of the visualization, and allows the user to explore the data through the time dimension. The "Prénom" filter is connected to the graph on the top-right of the visualization, and allows the user to focus on certain names.

The two *race bar charts* (on the top-left of the visualization) show the top 10 and bottom 10 names for the selected year. Filtering by year is our way, here, to reduce the amount of information displayed to the user at once so it is manageable. 
We can use this to visualise the evolution of the top 10 or bottom 10 over time, which allows us to see if names remained popular or unpopular on a national level over time, or if they were briefly popular or unpopular. 

One shortcoming of the visualization that should be pointed out is the fact that the computation for the bottom 10 is not theoretically correct.
For an honest representation of the data, we should filter by year first, then choose the 10 least given names that year. 
Tableau does the opposite as it ranks the names based on how many times they were given (all time across the country), and then filters on the year. This is the only way we have found to allow the interactivity of the year filter (on the right) with the Race Bar Charts.

The limits we saw to these *Race Bar Charts*  is that we can only see the data from names that are in the top 10 and bottom 10 for the given year (and not for any name that we might be interested in). Another limit is that we only see the data for a given year, which means we need to do some work mentally to represent the data over time.

That is why we incorporated the upper right chart, which shows us the evolution of names *starting with* the value of the "Prénom" filter (or all if the field is blank).
This helps us see the (un)popularity of the selected names over time. This solves the two previous issues by allowing to filter by names (i.e. letting the user select a name of his/her choice), and by showing the evolution over time directly (as time is encoded through the x-axis).
The legend of this figure rests on the right of the dashboard (*Prénom* : shows correspondance between the colors of the curves and the corresponding names).

The lower graph, on the other hand, illustrates the yearly evolution of top 10 attributed names of all time. The choice of the stacked graph here is justified by the *Pop-Out* effect it generates, as each name is encoded by a different color, allowing the viewer to immediately see how the popularity of names rises and falls.

## **Visualization 2**:
This segment uses Dash with Plotly, to try to answer these questions : 
 - Is there a regional effect in the data? 
 - Are some names more popular in some regions? 
 - Are popular names generally popular across the whole country?

The Dashboard includes : 
 - a choropleth map showing the distribution of names across departments ;
 - a stacked bar chart showing the 10 most frequent names.

One of these visualisations acts as 'input' and filters the second one, the 'output'. By default, the 'input' visualisation is the choropleth but the user can change it if he or she so wishes it.

 - If the choropleth map is the 'input', then by clicking on a department, the stacked bar chart will show the ten most frequent names in the chosen department. This is particularly useful to see regional effects and see the popularity of names within a region.
 - If the stacked bar chart is the 'input', then by clicking on a name, the choropleth map will show the distribution of the chosen name across all departments. 

As 'input', there exist two versions for the choropleth map :
 - 'Population' shows the number of births by department ;
 - 'Max names' shows the most frequent name by department. This graph is also useful to see regional effects across the country, on a glance.

There also exist multiple filters :
 - A filter by gender (girls, boys or both) ;
 - A filter by name : the user can choose only to keep names beginning with 'A' ;
 - A filter by years : the user choose a start and end year and only names between this interval shall be kept.

This visualisation allows the user to quickly see which names are the most popular in the country, their distribution as well as the presence in some departments (chosen by the user) of more 'unique' names.

For instance, the user can choose as 'input' the bar chart and filter the data by keeping only girls. If they click on 'Marie', it is shown that 'Marie' is mostly present in the western as well as northernmost and easternmost parts of France. Despite differences of population, there are 25K more 'Marie' in 'Finistère' than in 'Paris'. The same can be said of the name 'Anne'. Conversely for another popular name such as 'Catherine', the distribution is much more uniform.

<p align="center">
  <img src="/Dash/Dash_1.png", height=250/>
</p>

<p align="center">
  <img src="/Dash/Dash_2.png", height=250/>
</p>

If the user chooses as 'input' Map (Max names) and filters the data by keeping only boys, then we can see that there are only 4 unique names that are the most frequent names in a department with 'Jean' being clearly the most important. However, if we filter with years and keep only the decade 2010-2020, then we can see a far greater degree of diversity with 13 different names with some regional particularities : 'Jules' being mostly present in the eastern part of France.

<p align="center">
  <img src="/Dash/Dash_3.png", height=250/>
</p>

<p align="center">
  <img src="/Dash/Dash_4.png", height=250/>
</p>

The choropleth is the obvious choice for visualizing regional tendencies in data. 
We keep in mind, that it can lead to false interpretations if read too quickly (area should not be confounded with population).

**Addendum**: Due to some technical difficulties, the option to filter the barchat while using 'Max names' choropleth map is disabled. Moreover, filtering by name can take a bit of time.

## **Visualization 3**:
This segment uses Dash with Plotly, to try to answer these questions:
 - Are there gender effects in the data?
 - Does popularity of names given to both sexes evolve consistently?

The Dashboard includes :
 - a bar chart indicating the distribution of names across male and female gender;
 - a line chart showing the evolution of these names through time.

We use the following formula to define the distribution of a name across genders :
$1 - \frac{\|P(M) - P(F)\|}{max(P(M) - P(F))}$
 - where P(M) is the probability that the name is assigned to a boy
 - and P(F) the probability that it is assigned to a girl
The closer it is to 1 the more equally it is spread between boys and girls. When it equals 0, it is exclusively given to one gender.

In order to avoid too uncommon names, we only keep those with more than 500 occurences.

The user can choose the color scheme for the bar chart:
 - Show gender ratio: transforms the bar chart into a stacked bar chart with the distribution for boys in blue and girls in gold
 - Show total number: use a color scale showing the number of times a name was given

Furthermore, clicking on a name in the bar chart transforms the line chart into a stacked line chart showing the distribution across time for boys in blue and girls in gold.

Finally, we can filter the data in two ways :
 - Filter by names (e.g. only keep names starting with 'A')
 - Filter by dates
    
This visualisation allows the user to quickly see names that are popular for boys and girls as well as its evolution through time (as time passes, does it become a name more for boys or girls ?).

<p align="center">
  <img src="/Dash/Dash_5.png", height=250/>
</p>

For instance, we will see the distribution of names across genders between 1960 and 1970.

We can observe that names which are popular for both genders tend to only be popular for both during a short period of time (i.e. between 1940 and 1960) and there exist strong variations between each years which could indicate that there are few occurences of these names.

There are however two exceptions: Camille which remained fairly popular for both genders throughout the years and, to a lesser extend, Dominique.

<p align="center">
  <img src="/Dash/Dash_6.png", height=250/>
</p>

If we click on 'Camille', we can see its distribution through time. We can see that that before 1960, this name was mostly given to boys and after 1970, that it was mostly given to girls.
During the period 1960-1970, the name was not popular which explains the strong variations occuring during those years as well as the peak of 1963 shown in the previous image.

<p align="center">
  <img src="/Dash/Dash_7.png", height=250/>
</p>

If we click on 'Joan', we can observe that before 1960, the name was not popular and was almost exclusively given to girls. However starting from 1960, the name became increasingly popular but only with boys. During a short period of time, it was given almost equally to boys and girls thus explaining the distribution values during this period.
