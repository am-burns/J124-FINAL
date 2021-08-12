# Kindergarten Vaccine Rates Project

Between 2000 and 2013, 86.21% of California counties saw a decrease in the percent of kindergarten students who had received a measles, mumps, and rubella (MMR) vaccine. In both 2000 and in 2013, the northern part of the state, covering counties including Lassen, Trinity, and Nevada, had the lowest rates of MMR-vaccinated kindergarteners. For this project, 2013 was the most recent year I used because there was incomplete data in all subsequent years.

This story would look at why this specific region has been so vaccine-averse. I would look at COVID-19 vaccine data to see whether adults also are experiencing low rates, to try to understand if this is an issue of general distrust in vaccines. I would also look into how California's [2015 vaccine law](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=201520160SB277) that eliminated personal beliefs exemptions (PBE) has changed the percentage of students vaccinated, and see if any policy lessons could be learned from that for current vaccination issues, in particular low COVID-19 vaccination rates.

### Contacts

#### Jennifer Reich, PhD <br>
*Professor of Sociology at the University of Colorado, Denver* <br>
jennifer.reich@ucdenver.edu

Reich studies why families interact in different ways with healthcare and welfare-related issues. I think she could help explain the sociology of why entire communities become under-vaccinated, and why overall vaccine rates are dropping.
#### Daniel Salmon, PhD <br>
*Professor of International Health and Health, Behavior and Society; Director of the Institute for Vaccine Safety at Johns Hopkins Bloomberg School of Public Health*
<br>443-803-7754
<br>dsalmon1@jhu.edu

Salmon is an expert specializing in research concerning epidemiology and public health policy. He could help describe the potential impacts and dangers of low vaccine rates.

### Additional Sources
**[COVID-19 Vaccines Administered by Zip Code](https://data.ca.gov/dataset/covid-19-vaccine-progress-dashboard-data-by-zip-code/resource/15702a90-aa5d-49bc-8621-a8129630725a)  from the California Department of Public Health**

Looking at this COVID-19 vaccination data would be a way to see whether the areas with low vaccine rates in 2013 are still choosing to not vaccinate when a vaccine is optional. It would also be helpful, because all vaccine-eligible people are over the age of 12, to see whether this is an entire community issue, or whether people are more hesitant to vaccinate very young children compared to older children/adults.

**[Getting Personal: How Childhood Vaccination Policies Shape the Landscape of Vaccine Exemptions](https://academic.oup.com/ofid/article/7/3/ofaa088/5805242) from *Open Forum Infectious Diseases***

This peer-reviewed paper analyzes the impact of non-medical exemptions (NME), in California called PBEs, on vaccine rates, as well as the effect of restricting NMEs. Understanding how NME restrictions have changed California's kindergarten vaccination rates could provide guidance on how to deal with other low vaccine rates.

### Data Visualization
[![Kindergarten MMR Vaccines in 2000](/fixed-mmr-2000.png)](https://datawrapper.dwcdn.net/9paZC/1/)
[![Kindergarten MMR Vaccines in 2013](/mmr-2013.png)](https://datawrapper.dwcdn.net/Jc9tr/1/)

### Analysis

1.  What percent of counties have had personal belief exemption rates increase between 2000-2013?
    1.  Create a pivot table with counties as rows, years as columns, and the sum of nPBE, and the sum of n (number of kindergarteners) as values. Apply a filter so the only years shown are 2000 and 2013.
        ![PBE Pivot Table for 2000 and 2013](/PBE_PIVOT.png)
    3.  Copy and paste data into an empty sheet
    4.  Calculate the percent of students with a PBE in 2000 and 2013
    5.  Some counties had zero PBEs initially, so it is messy to calculate the percent change — **since what we only care about is whether there was an increase or not, instead just check if each counties percent of students with PBEs is greater in 2013 than 2000**
    6.  Take the number of counties that did have an increase and divide that by the total number of counties to find the percent of counties that increased
        ![PBE Sheet and Calculations](/PBE_C&Y.png)
    8.  ***We find that 93.10% of counties had an increase in PBE rates***
3.  What percent of counties have had MMR vaccine rates decrease between 2000-2013?
    1.    Create a pivot table with counties as rows, years as columns, and the sum of nMMR and the sum of n as values. Apply a filter so the only years shown are 2000 and 2013.
        ![MMR Pivot Table for 2000 and 2013](/MMR_PIVOT.png)
    3.   Copy and paste data into an empty sheet
    4.   Calculate the percent of students vaccinated against MMR in 2000 and 2013
    5.   Calculate the percent change for each county's MMR vaccination rate from 2000 to 2013. Use the formula *(New - Old)/Old*
    6.   A negative percent change means the vaccination rate decreased in that county. Divide the number of counties that had a decrease by the total number of counties.
        ![MMR Sheet and Calculations](/MMR_C&Y.png)
    8.   ***We find that 86.21% of counties had a decrease in MMR vaccination rates***
5.  Which counties had the lowest MMR rates in 2000?
    1.  Take the sheet we created to answer the last question
    2.  Apply a filter, and sort the **PCT_2000** column in ascending order
        ![MMR Sheet Filter 2000](/MMR_FILTER_2000.png)
    4.  The three counties with the lowest rates are ***Sierra, Tuolumne, and Nevada***
7.  Which counties had the lowest MMR rates in 2013?
    1.  Take the MMR vaccine rate sheet
    2.  Apply a filter, and sort the **PCT_2013** column in ascending order
        ![MMR Sheet Filter 2013](/MMR_FILTER_2013.png)
    4.  The three counties with the lowest rates are ***Nevada, Trinity, and Humboldt***
9.  Were rates lower for some vaccines than for others between 2000-2013?
    1.  Create a pivot table with years as rows and sum of nMMR, nDTP, nPolio, and n as the values.
        ![Vaccine Rates Pivot](/VAX_PIVOT.png)
    3.  Copy and paste data into an empty sheet
    4.  Calculate the percent of students vaccinated for each vaccine and year.
    5.  Compare the different percentages for each vaccine, and find which one had the lowest rate each year.
        ![Vaccine Rates 2000-2013](/VAX_Y.png)
    7.  ***We find that DTP had the lowest rate every year but 2010, when Polio had the lowest rate***
