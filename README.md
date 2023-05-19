# Project-1-5
In our first project, we were asked to collaborate on an eploratory data analysis. In order to ensure effective communication, we created a Slack channel and ensures that the group knew each group member’s available working hours. We set up an agile project by using GitHub ProjectsLinks to an external site, so that our group can track tasks.

Before we started writing any code, our group outlines the scope and purpose of our project. This helped provide direction and safeguard against scope creep (the tendency for projects to become more complex after work begins).

The aim of our project was to uncover patterns in crime data from Chicago during 2020. We examine relationships between incidents and location, incident categories, incident descriptions, percentage of total incidents in each district over the course of the year, and other related relationships derived from the data.

Data Cleanup and Analysis
Once we picked our data, we were able to tackle development and analysis.
We broke our analysis into two broad phases: (1) exploration and cleanup, and (2) analysis.

We explored, cleaned, and reformated our data before we were able to answer our research questions. 
After we cleaned your data and were ready to start crunching numbers, we should tracked our work in a Jupyter notebook dedicated specifically to analysis. We created plots along the way which revealed insights and interesting trends in the data.

Data Analysis write up: Supplemental to our formal presentation

-------------------------During the Exploration and Analysis-------------------------

Initially, we wanted to compare the crime reports taht were recorded between 2020-2023. After extracting the null values, we created a list to represent the counts of incidents per year. When we did this, we found that in 2020, 8046 crimes were recorded; in 2021, 1519 crimes were reported; in 2022, 610 crimes were reported, and in 2023, 44 crimes had been reported on or before March of that year. 

Although we are aware of the effects of the pandemic on crime rates, we were hesitent when observing the data due to the vast separation in crime counts. Because of this, we consulted our project managers and decided our best option for accurate data analysis would be to focus on what we believed was the most reliable reporting year. We then went forward with collecting and analyzing data from the year 2020. We pivoteded our time centered questions to analyzing crime rates per month. Again, this resulted in questionable counts as we recieved the following information on crime counts per month: 
March        3199
August       2063
December     1076
July           55
November       53
February       48
January        23
April          11
June            9
October         9
May             8
September       1

Again, we considered the effect of the pandemic. However, the stark differences across each month with no reliable pattern caused us to question the reliability of the data. We conferred with our managers and were encouraged to redirect our analysis towards crime types since the data connected with the yearly and monthly rates were most likely unreliable. While exploring this data and facing obstacles in the reliabilityAfter this, we collaborated on analyzing the data in order to answer the following questions.

-------------------------------Question #1-----------------------------------
What trends do we see in violations?

Using the cleaned dataframe, Ryann created a new dataframe which grouped the data by Priamry Type of infraction. With this, she observed that the top three types of infractions were Battery, Theft, and Criminal Damage. 

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/Incidents_bar.png
 "Top Three Bar")

She then analyzed each of the results by creating speerate dataframes for each type of infraction so that they could be further analyzed based on the infraction's description. In doing so, she was able to present findings on the description of the Criminal Damage charges which were broken down into the following categories: Criminal Damage to State Supported Property, Criminal Damage to City of Chicago Property, Criminal Damage as Criminal Defacement, Criminal Damage to Vehicle, and Criminal Damage to Property. With this analysis, it was clear that most Criminal Damage charges are categorized under Criminal Damage to Property; this does not include the state or city's property, but rather private property. With this information, along with proceeding analysis from the other group members, the group could reason that investments in enhanced security measures on private properties would benefit the safety of the communities that reported higher than average crime rates.

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/CD_Pie.png
 "Pie Chart")

-------------------------------Question #2-----------------------------------
What is the correlation between location vs crime rate?

As Mario looked deeper into the Chicago crime data the question arose whether location and crime rate were correlated. There seemed to be an early indicator with an answer of yes with District 11 having the most crimes thus location and crime rate were related. District 11 was found to have a crime rate of 79.99 per 100k. This means for every 100k in this district there would be about 80 crimes committed. However, creating a scatter plot to compare the two it was found the r-value (or the correlation coefficient) was at a 0.21 making the correlation very weak with no merit. It was interesting to find the linear regression line had a negative indicating the possibility the further you head east the lower the crime rate.



Is this finding clear evidence certain areas don’t have more crimes committed that others? Well no. Our sample size was not indicative of Chicago’s full complete districts and our data was heavily skewed with plenty of missing data. Chicago has a total of 77 districts and our data set only contained 16 of them. In total only 6555 individual data points were used to evaluate the correlation coefficient. With a city as big as Chicago there definitely needs to be a larger sample size.

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/LinReg_CR.png
 "Line Regression")

-------------------------------Question #3-----------------------------------
What is the comparison between domestic vs. nondomestic infractions and what percentage of charges lead to arrests?

Laura's goal was to try to find a correlation between location and crime rates. A possible hypothesis was that certain areas of Chicago in 2020 were contributing the overall crime rates significantly for either social economic reasons or a possible involvement in organized crime. To begin, she calculated the value counts of non-domestic versus domestic crime and then organized this output into a pie chart. Both outputs demonstrated that Chicago’s crime is mostly non-domestic, meaning that most infractions are not occurring inside the family residence. More specifically, domestic crime is at 21.6% while non-domestic crime is at 78.4%. Still, there are still perspectives that need to be considered, such as: does this mean that domestic crime is less reported? Some conclusions that can be drawn are that the city of Chicago needs to (1) enhance security measures (2) increase patrols and police presence (3) organize meaningful community engagement (4) conduct education and awareness (5) share information and collaborate with businesses and community members, and (6) conduct more accurate data collection for more credible data analysis.

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/DvsND_Pie.png
 "Domestic VS NonDomestic")

Secondly, Laura sought to discover which districts experience more or less crime. After a value counts function, she organized the data onto a descending bar chart. The result revealed that District 11 experiences the most crime. She researched the commanding officer for this district to see if any efforts are currently being made to prevent these outcomes. Laura found that Officer Davina F. Ward is the commanding officer for this district. If she were a data scientist for this policing district, she would suggest the aforementioned solutions. In addition, she would highly recommend crime prevention through environmental design (CPTED), which involves using architectural design to an advantage in seeking less criminal activity. Most importantly, after finding that the given dataset was highly unreliable, we would highly recommend that the city of Chicago improves their system for data collection. 

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/District_bar.png
 "District Comparison Bar Graph")

-------------------------------Question #4-----------------------------------
Which district has the biggest percentage of crime?

Michaela wanted to find out what district had the highest percentage of crime from the dataset. She created a for loop for the district number list and had it pull every district and find the percentage for each. At first glance she decided to go with a pie chart for the visualization of the data. However, since the data isn’t far off from one another you can't see the true difference in each data on the visualization. A bar graph would’ve been better to show the percentage differences.

![alt text](https://github.com/msryannhawkins/Project-1-5/blob/main/Chicago%20Analysis/CRPercent_Pie.png
 "District Comparison Pie Chart")

---------------------------Conclusion and Next Steps-----------------------------
While we were able to answer the majority of our questions which drove our analysis, we were concerend with the data's reliablity. With this consideration, we would not feel comfortble using this data to support any consultation. If given more time and more reliable data, we would like to have explored and analyzed the crime rates as well as the local weather data. 