Analyzing trends of organ donor enrollment in Chicago state
================

| Name         | Uni    |
|--------------|--------|
| Minxiu Shi   | ms6358 |
| Shengzhi Luo | sl5009 |
| Yitian Zhang | yz4185 |
| Yiwen Zhao   | yz4187 |

## Introduction:

Gotham City, a city of sin that exists in comic and film works, is
wildly considered to be created based on New York. This is because from
a lexical history perspective, Gotham City is an alias for New York.
This alias first appeared in Washington Irving’s mocking periodical
“Salmagundi” in 1807. Frank Miller, the author of Batman’s Dark Knight
Revisited, also said, “Metropolis is New York by day; Gotham City is New
York by night.”

However, the longtimde author of Batman series Neal Adams thought Gotham
City was more like Chicago-based in the early comics. A city that
combines prosperity with high crime rates. From the towering skyscrapers
to the trash-strewn back alleys. Brilliant neon lights at night can’t
hide the darkness beneath the glitz. These characteristics of Chicago
set the tone for Gotham City, the shadowy capital of evil.

Due to a shooting case that happened in Chicago recently, the crime
rates in different areas of Chicago caught our attention. Violent
incidents in Chicago are of increasing concern over the last few years,
and we are interested in looking at what might be associated with
increased violence in Chicago. We are concerned about people’s living
safety in the city and motivated to find safer neighborhoods for living
in Chicago.

## Data

#### Data Source

5-year Chicago Crime data records are retrieved from Chicago’s official
public data [Chicago Data Portal](https://data.cityofchicago.org).

-   5-year Chicago crime data records (2017 - 2021):
    -   [2017](https://data.cityofchicago.org/Public-Safety/Crimes-2017/d62x-nvdr/data)
    -   [2018](https://data.cityofchicago.org/Public-Safety/Crimes-2018/3i3m-jwuy/data)
    -   [2019](https://data.cityofchicago.org/Public-Safety/Crimes-2019/w98m-zvie/data)
    -   [2020](https://data.cityofchicago.org/Public-Safety/Crimes-2020/qzdf-xmn8/data)
    -   [2021](https://data.cityofchicago.org/Public-Safety/Crimes-2021/dwme-t96c/data)

This dataset reflects reported incidents of crime (with the exception of
murders where data exists for each victim) that occurred in the City of
Chicago from 2006 to present, minus the most recent seven days. Data is
extracted from the Chicago Police Department’s CLEAR (Citizen Law
Enforcement Analysis and Reporting) system. In order to protect the
privacy of crime victims, addresses are shown at the block level only
and specific locations are not identified. Each record represents one
criminal case. This dataset contains approximately 2 million crime
records and details 22 variables such as ID, number, data, neighborhood,
IUCR, and primary type for each case.

#### Data Description

The resulting data file of `data_clean` contains 45498 criminal records
and 24 variables. The list below is the description of our interested
variables:

-   `data`. The date of occurrence of crime.
-   `block`. The block where the crime occurred.
-   `primary_type`. The primary description of crime.
-   `description`. Detail description to the crime.
-   `location decription`. Detail description about where the crime
    occurred.
-   `latitude`. The latitude of occurrence of crime.
-   `longitude`. The longitude of occurrence of crime.

## Motivation:

Due to the cases that happened in Chicago recently, the crime rates in
different areas of Chicago caught our attention. Violent incidents in
Chicago are of increasing concern over the last few years, and we are
interested in looking at what might be associated with increased
violence in Chicago. We are concerned about people’s living safety in
the city and motivated to find safer neighborhoods for living in
Chicago.

From news, an 18-year-old man was charged with robbing and murdering
Shaoxiong “Dennis” Zheng (right), 24, in the 900 block of East 54th
Place (left) Tuesday afternoon
</p>

Apart from that, news came that Zheng, a 24-year-old native of of
China’s Sichuan province, was shot and killed on November 9th during a
robbery in the 900 block of East 54th Place, which was in the vicinity
of University of Chicago’s campus. As his compatriots, we were all
overwhelmed by unbearable sorrow and loss. And such tragedies kept
occuring every now and then. Therefore, our concern towards the crimes
in Chicago grew.

## Study Questions:

-   **Question 1**: How does the crime amount change over these 6 years?
    Is there any significant change in the number of crimes? What are
    the possible reasons that cause the change?

-   **Question 2**: In what kind of location in Chicago does the most
    amount of crime happen? Which type of crime is most likely to occur
    in Chicago?

-   **Question 3**: According to the data analysis, what suggestions we
    can give on the security in Chicago?

## Exploratory Analysis:

-   **Figure1: Trends in Time - The Number of Crimes Monthly Trends Over
    5 Years**

This figure shows how the number of crime cases in Chicago changed
monthly over the years. According to this graph, 2017, 2018, and 2019
show a similar trend in the number of crimes. The number of crimes per
year is between 3,119 and 4,574 from 2017 to 2021. However, the graph
presents a significant trend difference in 2020 and 2021. The number of
crimes in 2020 stay in the same trend as previous years’ in January and
February but drop immediately in March. The number of crimes reached the
lowest point in April 2020, with only 1,119 crime cases this month. The
number of crimes in 2021 seems lower than in 2020 in this graph. Since
the crime case data of 2021 is only to the present, the database does
not include crimes that happened in December 2021. Considering the start
time of the COVID-19 pandemic coincide with the drop in the number of
crimes, the rapid decrease of crime cases from March 2020 is probably
associated with the prevalence of COVID-19.

-   **Figure2: Heat Map - The Monthly Density Trends of Crimes Over 5
    Years in Chicago**

This heat map gives a better visualization for the monthly density trend
of crimes from 2017 to 2021 in Chicago. It clearly shows that in 2017,
2018, 2019, and the first two months in 2020, there is a much higher
density of crimes happened during the year. The crime case density drops
rapidly in the middle of March in 2020 and reaches the lowest point in
April 2020. Comparing the density of crimes in 2017, 2018, and 2019, we
can see that crimes are more likely to happen in the middle of the year
(from May to September) and are less likely to happen at the beginning
and the end of the year. This graph also clearly shows that, generally,
Christmas Day has the lowest crime rate of the year.

-   **Figure3: Word Clouding - Word Clouding of Crime Types: The top
    number of crimes appeared in 5 years**

After reviewing the number trends and density of crime, our group also
want to dig further about the primary type of crime with high incidence
in Chicago. As a result, we decide to make a word clouding to give
greater prominence to crime type that appear more frequently. According
to this figure 3, the most frequently occurring type of crime in Chicago
from 2017 to 2021 is narcotics, followed by weapons violation, theft,
battery, assault, other offense, and criminal trespass etc.

-   **Figure4: Trends in Location - Top 10 Locations With High Criminal
    Incidence Over 5 Years**

In addition, our group also sorted and ranked the data, and compiled the
top 10 locations with high criminal incidence from 2017 to 2021 into a
dynamic bar graph to get a more in-depth understanding of the crime
situation. Through this motion chart, we can visually observe the names
of the crime areas, the number of crime incidents, and their changing
trends.It is clear that streets and sidewalks are the locations with
high crime rates during the five-year period. It is also interesting to
note that these two locations always reach a peak in January, July and
August, respectively, over the five-year period, and then drop extremely
quickly to a low in December. Meanwhile, crime rates in stores
(department stores, mall retail stores and food stores) and restaurants
can be relatively high in January and December. The number of cases in
stores and restaurants will be much higher in December and January,
while crime in apartments and residential areas will be more frequent at
other times.

-   **Map: Distribution of Crime Rate From 2017 to 2021 in Chicago**

As the map shown, we found that crimes is concentrated in the central
and south side of Chicago, with a gradual decrease outward. over 20,000
crimes have been accumulated over the 6 years. The amount of crimes in
north district was the least but still summed up to 5,000 in the last 5
years. Thus, it is fairly enough to conclude that the middle and south
districts are comparatively more dangerous while the north is safer
although its number of crimes still shocked.

From our perspective, Chicago’s persistently high crime rate is
inextricably linked to the density of gangs. Chicago is considered to be
the most gang-influenced city, with over 60 medium or large gangs, more
than 700 factions or branches, and over 100,000 active gang members.
Below is a detailed map of Chicago’s gang distribution which includes
the name of each gang and their frequently gathering areas, we can
clearly observe that gangs are concentrated in the central and southern
parts of the city. This characteristic coincides with our crime rate
distribution. As a result, it is reasonable for us to suspect that the
concentration of gangs is one of the reasons for the high level of
violence in Chicago.

## Results

According to our study, in 2017, 2018, 2019, and the first two months in
2020, there is a much higher density of crimes happened during the year.
The crime case density drops rapidly in the middle of March in 2020 and
reaches the lowest point in April 2020. The crime rate has a significant
increase in 2020, and the significant increase of crime in Chicago is
probably associated with the COVID-19 prevalence.

Meanwhile, we find the most frequently occurring type of crime in
Chicago from 2017 to 2021 is narcotics, followed by weapons violation,
theft, battery, assault, other offense, and criminal trespass etc. Also,
our animated bar graph shows that streets and sidewalks are the
locations with high crime rates during the five-year period.

To further explain the high crime rates, we do a regression to see if
there is an association with weather. Unfortunately, there is no
evidence to show there is a direct association between weather condition
and criminal incidence.

## Discussion:

Since we got the unexpectedly high crime rates , we want to dig in and
are curious about what causes these. According to some existed
researches and studies, we hypothesize that the weather may be related
to the number of criminal cases and start a further exploration.

## Suggestion:

Thus, in case of unexpected violence, here we provide some suggestions
to properly protect yourselevs. Firstly, stay home after sunset.
Secondly, stay away from crossroads, try to use the shelters around to
avoid being targeted. Be alert to the dark streets.
