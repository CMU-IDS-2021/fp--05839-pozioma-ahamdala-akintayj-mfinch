# Final Project Report

**Project URL**: TODO

This narrative work is an inquiry into the nature of income household and child income distributions in US tertiary institutions. Using five income classes, we explore the mean yearly household income distribution of different college tiers in the US. An exploration of the median yearly income showed a similar pattern as the mean yearly household income. We also explored income distribution by college through a drop-down menu that allowed the selection of each college. For each college, we plotted the probability of a parent falling within a particular income class with a barchart. Using the height of the bars, we showed the proportion of parents that actually fall within the income class. This was done for the children’s income too. Eventually, using the income classes, we showed income mobility of each of the income classes. Using a scatter plot, we looked at the direction of income mobility for colleges within each college tier. Our results show that people from lower income households are more likely to attend lower tier colleges and those from higher income households are more likely to attend higher tier colleges. We conclude with a recommendation on how we can improve students, colleges and governments can work together to improve upward income mobility for students from lower income households. 

## Introduction

Income mobility explores the upward or downward movement of people from one income class to another. Intergenerational income mobility explores income mobility across various generations of a family. Education is generally considered to be a driver of upward income mobility across generations. Even more importantly, the type of education children within a household receive can affect intergenerational income mobility. The high cost of attending high tier schools coupled with limited financial aid resources make it inaccessible for most students from lower income families. Top employers, however, are more likely to recruit students from these schools. More opportunities and exposure are also available to these students. Exploring the extent of this issue and presenting the results in an interactive visualization, in our opinion, is thus a worthwhile endeavor. This forms the basis of the data science problem for our project. We are setting out to investigate how household income affects the type of college attended and subsequently future income. We intend to follow the narrative track in solving this problem and produce an interactive article with insights gleaned from datasets on income distribution and college level characteristics from the Integrated Postsecondary Education Data System (IPEDS) and College Scoreboard. The goal of this data analysis project is to obtain in-depth understanding on how the household income in the US affects the types of colleges people attend. It would also shed light on questions relating to how different categories of colleges affect earning power and ultimately, how they affect income mobility.

## Related Work

[1, 2] have characterized social mobility resulting from colleges in the United States. Chetty et al’s results have been reported by the New York Times [3] and APM Report [4] articles where the reader is provided interactive infographic using the data presented in [1]. The reader of the New York Times article provides a college into the infographic which returns related information comparing the entered college to peer institutions while also providing a scatter plot of parent incomes to graduates’ income at age 34. The article by APM Report provides a mouse hover chart using data source form the Brooking Institute to show discrepancies in family income between income percentiles. In addition, the APM Report also provides an infographic of students admitted at various universities as a function of parents’ income over time.  

## Methods

We set about approaching this project empirically, collecting data from existing research. We identify 5 income classes based on the income quintile: Upper Class, Upper Middle Class, Lower Middle Class, Working Class and Middle Class.

We started with exploring mean yearly household income of students in the various university tiers. This was then further developed to show the proportion of parents that belonged to each income class. This was done with two linked charts. The first chart (a vertical histogram) showed the mean yearly income of parents within each university tier. A linked chart (a horizontal histogram) shows the proportion of parents within the selected tier that belong to each income class.

We took the mobility rate as a key parameter in this endeavor. We plotted the mobility rates of different universities in an interactive format where each school is the main view (schools are selected from a dropdown menu) at a given time with four different visualizations to this effect: 

A stacked bar chart that shows the forecasted probability of a parent from the school falling into a certain income class. Each bar further the proportion of parents within each income class that are actually within each income class
A stacked bar chart that shows the forecasted probability of a child from the school falling into a certain income class. Each bar further the proportion of children within each income class that are actually within each income class
Heatmap that shows intergenerational income mobility of children as a function of their household income
People chart to show the income distribution of parents from 1980 to date (dates can be selected vis a slider)

We also categorised the students into three groups:
Those that remain in the same income group as their parents - Staylites
Those that move into a higher income group than their parents - Upward Movers
Those that fall below their parents’ income group - Downward  Movers

To visualize these classes, we explore the data based on college tiers. We created a scatter plot and explored income mobility for schools within each income class. The plot allowed us to visualize college tier clusters (and subsequently mobility).
To further understand this grouping as well as more interactive inference, we decided to make a scatter plot  of parent income against children income  for the different universities while categorizing the schools based on their appeal and social perception e.g Ivy leagues, Community colleges etc. These categories then serve as clusters on the scatter plot that can be interacted with separately. Choosing any one of the clusters shows the scaled positions of the universities that belong to the group along with their average mobility rates. Below that chart is then a spectral horizontal chart that shows the different groups of students per university per income group. 

## Results

We have generated an interactive article that shows the relationships between incomes of parents and their wards after graduation from United States universities which can be assessed here: https://share.streamlit.io/cmu-ids-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/main/scs/python/app.py

We achieved a visualization of mean yearly income of households in each income tier. We found that higher tier colleges had more students from high income households while lower tier colleges tend to have more students from lower income households. 

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image7.png">
Figure 1: Household income class distribution of Ivy League Schools

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image10.png">
Figure 2: Household income class distribution of Two-Year for-Profit Schools

We also found that students from higher income households were more likely to even get an education.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image9.png">
Figure 3: Household Income Class Distribution for all schools in the US

We created a dropdown menu that allowed a deeper view of each college. Using Carnegie Mellon University as an example, we got a chart that showed the forecasted probability that a parent would belong to a particular income class as shown in the chart below:

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image12.png">
Figure 4: Parents’ Income Probability Distribution for Carnegie Mellon University.


Each bar shows the actual proportion of parents that fall within each income class given the forecast. 
The same is done for the children’s incomes

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image1.png">
Figure 5: Children’s Income Probability Distribution for Carnegie Mellon University.


We then proceed to draw a heat map that shows the intergenerational mobility for each income class. We represented the children’s income class on the y-axis and the parents’ income class on the x-axes. We found that students from upper income households tend to maintain their income class. There was some mobility from lower income classes into the higher income strata too. 

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image8.png">
Figure 6: Intergenerational Income Mobility Map for CMU.


We also created a people’s chart that shows the household income class distribution for each year.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image3.png">
Figure 7: Parents’ Income Probability Distribution for Carnegie Mellon University in 1982.


The same charts for a 2-year community college (Pioneer Pacific College) are shown below: 

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image11.png">
Figure 8:  Parents’ Income Probability Distribution for Pioneer Pacific College.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image4.png">
Figure 9: Children’s Income Probability Distribution for Pioneer Pacific College.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image5.png">
Figure 10: Intergenerational Income Mobility Map for Pioneer Pacific College.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image6.png">
Figure 11: Parents’ Income Probability Distribution for Pioneer Pacific College in 1982


We also generated a scatter plot of universities clustered by their tiers i.e Ivy Leagues etc. This plot is linked to a horizontal stacked chart that shows for each school, the percentage of students that attended that eventually ended up in the same income class as their parents, stayed in the same bracket or did poorly. Very interesting revelations from these charts as different positions of these schools on the plot meant a different behavior in income distribution as well as room for extreme/wide mobility gaps and eventual possibilities.

<img src= "https://github.com/CMU-IDS-2021/fp--05839-pozioma-ahamdala-akintayj-mfinch/blob/main/images/image2.png">
Figure 12: Income Mobility Direction for Some Elite Schools


## Discussion

This work hopefully is able to help policymakers and the general public understand how disparities in earning potential is fostered by the kinds of universities that people attend. The universities that people get to attend do not necessarily depend on their academic potential alone, it is also largely influenced by their household income as can be seen in the results above. We hope that stakeholders, including universities will be informed by our work and thus, seek ways to ensure that income mobility propensities are common across tertiary institutions. It is also our expectation that the general public will be better informed about how income mobility is defined by educational institutions through this work. This information can, thus, help them make the best decisions for their financial future. As our work not only analyses how household income and the universities attended affects future income, but also gives information about how other factors contribute to future income may not be contained therein. We make the following suggestions to allow for greater income mobility in lower income groups: 

[1] Colleges can consider extending student recruitment and information sessions to students from low income and disadvantaged communities.

[2] Top tier institutions can also consider need-based scholarships to well deserving students from low income and disadvantaged communities.

[3] The US government can also provide better comprehensive packages that enable students to attend the top-tier schools without exhausting student loan facilities to worry about when they are done.

[4] Employers also should consider equal opportunities for students from any school rather than just targeted recruiting.
Students from lower income households should also stay active and look out for the occasional opportunities for scholarships and fundings to attend the top tier institutions in the country.

## Future Work

It would also be enlightening to see how college debts in addition to household income affects intergenerational income mobility. It would also be interesting to see how target schools (for top employers) widen the income mobility spectra when compared with non-target schools.  

## References

[1] R. Chetty, J. Friedman, E. Saez, N. Turner, and D. Yagan, "Mobility report cards: the role of colleges in intergenerational mobility," National Bureau of Economic Research, vol. w23618, JUL 2017.

[2] R. Chetty, J. N. Friedman, E. Saez, N. Turner, and D. Yagan, "Income segregation and intergenerational mobility across colleges in the United States," The Quarterly Journal of Economics , vol. 135, no. 3, pp. 1567-1633, FEB 2020.

[3] G. Aisch, L. Buchanan, A. Cox, and K. Quealy, "Some colleges have more students from the top 1 percent than the bottom 60. Find yours.," The New York Times, Jan 2017.

[4] S. Aslanian and E. Hanford, "Changing class: colleges helping Americans move up?," APM Reports, AUG 2018.
