# IGR204-Visualisation 

### Groupe 0 - Alann Goerke, Nicolas Esdras, Urian Millard, Rayan El Halabi

###### *All the instructions can be found on the following link: https://perso.telecom-paristech.fr/eagan/new/class/igr204/baby-names*

In this mini-project, we will be working with a data set of baby names in France. It contains the list of all baby names registered in France, year by year, from 1900 through 2019. There are two data sets: one aggregated to the national level, and another with data by department. We will answer the above questions with an interactive visualization made with Tableau. 

Here is the general aspect of our dashboard : 

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/visualisation_globale.png)

### Part 1:

- How do baby names evolve over time?
- Are there names that have consistently remained popular or unpopular? 
- Are there some that have were suddenly or briefly popular or unpopular? 
- Are there trends in time? 

By moving the mouse over this bubble graph, you can see the top 3 years in which a name has been given more. 

<img src="https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_1.1.png" width="700" height="450">

By clicking on the name John, the graph below shows us the general tendency given to this name. We can see that it is in 1946 that this name has been given the most. Names evolve over time.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_1.2.png)

Taking the window 2000-2020, several names have become unpopular, the first name Jean seen before has been replaced in the early 2000s by Louis, however Marie remains in the Top 3 of the most given names in 2020 with Jeanne. 

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_1.3.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_1.4.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_1.5.png)

We can deduce that Marie remains a name very loved by the French, even if it tends to be replaced. 


### Part 2:

- Is there a regional effect in the data? 
- Are some names more popular in some regions? 
- Are popular names generally popular across the whole country?

First, the orange gradient shows visually that the departments are not equal in the given names.

While the first names Marie and Jean remain very popular in particular in Finistère, it is interesting to see that in Seine-saint-denis the Top 3 names are : 
- Mohamed
- Nicolas
- Stephane

History has something to do with it. Indeed, many Maghreb countries were colonized by the French. After the 2nd world war, there was a migration of the countries of the south towards the north and it is particular in the department of the seine-saint-denis that these people ce are installed. A wave of births followed, hence the name Mohamed became very popular.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_2.3.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Question_2.2.png)

However, it should not be forgotten that the history of Seine-Saint-Denis is that of a young department in administrative terms, since it was created on January 1, 1968, in application of the law of July 10, 1964, from the northeastern part of the former department of Seine (24 towns) and a small portion of that of Seine-et-Oise (16 towns).

It inherited the postal code "93", formerly assigned to the department of Constantine.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/2.4.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/2.5.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/2.6.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/2.7.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/2.8.png)

The top 5 French departments with the largest areas show that the names Marie and Jean remain very popular. We can deduce that by taking this small sample of departments that the top 2 most popular names are found across the whole country.


### Part 3 (bonus):

- Are there gender effects in the data? 
- Does popularity of names given to both sexes evolve consistently? (Note: this data set treats sex as binary; this is a simplification that carries into this assignment but does not generally hold.)

We can see that in general the gender of the names is quite balanced, with a majority for male names. We can deduce that the number of births in both sexes remains balanced by assuming that a female name was given to a girl and a male name was given to a boy. 

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/3.1.png)
![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/3.2.png)

This graph below shows us that the evolution of names according to gender is similar, it follows the same trend.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/3.3.png)

Let's focus on the two major wars, the 1st and the 2nd World War (we place the time window between 1910 and 1950). We notice two distinct stages. Indeed, the wars had impacts on the births and we notice that the number of female names is higher than the male ones. The post-war periods show a will of the 

French to repopulate the country (1919-1920 and 1945-1946).  
During these two periods, there was an increase in births of nearly 60%. And it's after 1946 that the male names are well above the female ones.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/3.4.png)

We also tried to work with Altair to find another visualisation. But before using Altair, we had to do some manipulations on the data set because there too much data for our laptops. Therefore, we reduced the size of the dataset by only keeping lines where names had been given to both genders. First we separated the Data Frame in 2, one for each gender. Then, we created a third DataFrame my merging the Male DataFrame and the Female DataFrame by chosing the feature "name" as the commun element. At the end, we managed to solve the big size issue by getting a DataFrame which contains data of people where their names had been given to both genders.

With Altair, we build the following histogram which represents the evolution of names given to both genders, blue for Male and orange for female.

![image](https://github.com/N-dras/IGR204-Visualisation/blob/main/Images/Altair_Question3.png)

There are two things we discovered by studying this graph :
- If a name can be given to both genders, it does not mean that there is an equal distribution between male nad female. For example, the name "Camille" is given to both genders, but it is more likely given to a girl then a boy. In the grap, we can see it by taking a look on the data from 1919 to 1950 : we can easily see that blue bars are higer than orange bars. It means that a lot of names, given to both genders, have been given way more to boys than to girls.

- The second surprising discover can seen if we take a look on the recent years : it can clearly see that there are much few names given to boys and girls. Probably, because parents want original names ...
