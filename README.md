# Can Deer Harvest Numbers Help Explain Lyme Disease in Maryland?

## What I hoped to accomplish
I was interested in trying to answer this question: If deer can put ticks in contact with more humans, and those ticks can transmit diseases like Lyme to those humans, could increased hunting of deer, including in suburban neighborhoods, lower the incidence rates of Lyme?

## Findings 
I was unable to find correlations between deer harvest numbers and Lyme disease incidence rates. This was for a few reasons:
* While current cases could serve as a baseline, I was unable to identify clear correlations between deer harvest numbers and Lyme incidence rates because Lyme disease cases are underreported and underdiagnosed. 
* Many factors could contribute to the spread of ticks, not just deer population and movement.
* Hunting regulations are not designed solely to reduce tickborne disease cases or achieve any single outcome. They're used to help manage a broader set of conflicts that arise as deer and human populations increasingly overlap in shared spaces. 

## Data Collection Process 
1. I scraped annual harvest tables published by Maryland's Department of Natural Resources. There was no one table, so I scraped 10 from 10 separate websites. I Googled each year from 2015-2025. Here's an example of one such report: https://news.maryland.gov/dnr/2026/02/12/maryland-hunters-harvest-71649-deer-for-2025-2026-season/. 

2. I scraped additional data from these PDFs, specifically the "Maryland Reported Button Buck Harvest by County" tables: https://dnr.maryland.gov/wildlife/pages/hunt_trap/deer_annualreports.aspx. Though I cleaned it, I didn't end up using this data. 

3. I downloaded data on the incidence rate of tickborne diseases from the Johns Hopkins Lyme and Tickborne Diseases Dashboard: https://www.hopkinslymetracker.org/explorer/. There are 10 downloadable files under "Reported Case Data," and I downloaded the incidence rates fles for each disease. 

4. I contacted the Department of Natural Resources with some clarification questions, including inconsistencies in reported deer population estimates. The game data and research project leader explained that a different biologist likely rounded figures in earlier reports. He then sent me population estimates from 2015-2024 according to his latest models.

## Overview of Data Analysis Process 
1. **Identify percentages and trends in the number of harvested deer before re-establishment of Suburban Deer Management Zone (2020) and after**. I chose to look at data from a 10-year period that covered five years before the zone was re-established and five years after. Data from the 2014-2015 hunting season was included in the 2015-2016 report, so I chose to keep that in. 

2. **Identify percentages and trends in the number of female deer harvested during same time period.** After learning that encouraging the harvests of female deer was part of the state's population management strategy, I wanted to see if there was any trend or pattern in the number of female deer harvests over time.  

3. **Compare antlered to antlerless harvests by hunting regions over time period.** I initially compared these numbers based on county, but I ended up with a long dataset since there are 23 different counties. Because hunting is regulated across three regions and zones (Region A, Region B, and Suburban Deer Management Zone that's in Region B) I decided that those zone levels were the most useful for comparsion rather than granular county levels. 

4. **Calculate incidence rates per 1,000,000 people of tickborne diseases in Maryland during time period and compare to national average.** Though Though Lyme disease data is available through 2023, comparisons of Lyme incidence rates with other tickborne diseases are limited to 2022, since that is the most recent year for which data is available for the other diseases. 

5. **Calculate incidence rates per 1,000,000 people of tickborne diseases in Maryland counties grouped by regulated hunting areas: Region A, Region B, and Suburban Deer Management Zone.** 2023 is the year for which the most recent data is available for Lyme from the Centers for Disease Control and Prevention (used in Hopkins dashboard). Because the Suburban Deer Managemnt Zone was re-established in 2020, I thought it would still be worthwhile to see if any patterns could be detected in Lyme disease incidence rates before and after the re-establishment of this zone, even though hunting harvest data is provided up to the 2025-2025 hunting season. 

## Skills Used and Key Learning Moments
1. **Cleaning and reshaping**: I admittedly was more dependent on AI that I would've liked to have been for the .groupby and .pivot functions. I am, however, starting to slowly understand the differences between .groupby and pivoting after watching more tutorials. Also, a few times I thought my data was clean until I tried extracting certain values or manipulating the shape. For instance, it took me a while to realize that a column like "Harvest_Total_2015_16" was esentially joining two values instead of keeping years and harvest totals in separate columns. 
2. **Scraping**: I learned about user agent libraries that generate random user agent IDs for you. I also used Natural PDF to scrape tables from reports. 
3. **Chart selection and design**: I iniitally didn't realize I would have to reshape my data in order for certain charts to look the way I wanted them to. It also took me several iterations to decide which charts felt useful and which ones felt like just a dump of information. I changed my charts and tables several times while drafting. In terms of design, I was mostly focused on color for this project and used color generators, as well as AI to generate complementary hex codes. 

## Key Learning Moments 
1. Drawing correlations is difficult! It felt kind of frustrating to realize that I wouldn't be able to answer the question I wanted to answer with the data I had.  
2. I felt limited in my ability to analyze because I don't have sufficient understanding of core functions like .groupby, .pivot, and .pivot_table. 
3. I realized that I am a very messy and shotgun problem solver. I do leave a lot of comments for myself (I do this a lot when drafting while writing), which helped me a lot when I had to revisit earlier parts of my code. I also appreciated Sandhya's advice to keep a data diary. But there were several moments when I would've solved a problem more quickly by pausing to read documentation and watch more tutorials. 
4. File hygiene, file naming, and variable naming felt overwhelming. But again, I appreciated Sandhya's advice to keep raw copies, processed copies, and to follow naming conventions.  

## What I Wanted to Do 
1. I read a study that measured the home range of deer in a suburban neighborhood, and I would've liked to try to map that home range. I already felt overwhelmed with data scraping and cleaning though, and I didn't have the mental energy to practice using the mapping software that Aaron had introduced to us. 
2. Related, I was interested in showing the change in Lyme incidence rates by county in Maryland on a changing map. I didn't want to make 10 maps though and put them into an animation, and I had difficulty getting my incidence rate values to show up on a choropleth map while also displaying county names in Datawrapper. I think I would've had to use a different base map, which would've created a longer and more involved workflow.   
---Update July 1, 2026---
3. I ended up making the choropleth maps, but I didn't find them to be helpful given the sheer amount. I also didn't want to do an animation because I didn't want the values to quickly disappear after each frame/map. So, after grouping Maryland counties by the regulated hunting areas, I created a heatmap table for incidence rates from 2014-2023, as 2023 is the year for which the most recent data on Lyme is available from the CDC. 