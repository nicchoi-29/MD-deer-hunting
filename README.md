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

2. I scraped additional data from these PDFs, specifically the "Maryland Reported Button Buck Harvest by County" tables: https://dnr.maryland.gov/wildlife/pages/hunt_trap/deer_annualreports.aspx. However, I didn't end up cleaning or using this data. 

3. I downloaded data on the incidence rate of tickborne diseases from the Johns Hopkins Lyme and Tickborne Diseases Dashboard: https://www.hopkinslymetracker.org/explorer/. There are 10 downloadable files under "Reported Case Data," and I downloaded the incidence rates fles for each disease. 

4. I contacted the Department of Natural Resources with some clarification questions, including inconsistencies in reported deer population estimates. The game data and research project leader explained that a different biologist likely rounded figures in earlier reports. He then sent me population estimates from 2015-2024 according to his latest models.

## Overview of Data Analysis Process 
1. **Identify percentages and trends in the number of harvested deer before re-establishment of Suburban Deer Management Zone (2020) and after**. I chose to look at data from a 10-year period that covered five years before the zone was re-established and five years after. Data from the 2014-2015 hunting season was included in the 2015-2016 report, so I chose to keep that in. 

2. **Identify percentages and trends in the number of female deer harvested during same time period.** After learning that encouraging the harvests of female deer was part of the state's population management strategy, I wanted to see if there was any trend or pattern in the number of female deer harvests over time.  

3. **Compare antlered to antlerless harvests by hunting regions over time period.** I initially compared these numbers based on county, but I ended up with a long dataset since there are 23 different counties. Because hunting is regulated across three regions and zones (Region A, Region B, and Suburban Deer Management Zone that's in Region B) I decided that those zone levels were the most useful for comparsion rather than granular county levels. 

4. **Calculate incidence rates per 1,000,000 people of tickborne diseases in Maryland during time period and compare to national average.** Though Though Lyme disease data is available through 2023, comparisons of Lyme incidence rates with other tickborne diseases are limited to 2022, since that is the most recent year for which data is available for the other diseases. 


## Skills Used 
1. Filtering and Querying 
2. Close Reading 
3. Removing duplicates, deciding what to drop, deciding what to combine, finding efficient ways to filter and drop rows (str.contains)
4. Aaron color 

## Key Learning Moments 
1. Question kept changing 
2. More specific questions 
2. .groupby and .pivot 
3. combining headers 
4. step-by-step problem solving 
5. using ai: color schemes, in dadition to color generator
6. knowing what to cut, including graphics and charts that i had spent time making and time filtering and reformatting the data for example: reporte ddeer harvests 
7. file hygeinge 
8. Record why certain time periods were chosen and keep track. REalizing as I wriete this everythign starts from 2014 except lyme incidence rate, which i began at 2015

## What I Wanted to Do 
1. home range map 
2. incidence rate by county on changing chorpleth map 
2. draw correlations that I think are hard to do in practice and actully rely on a lot of assumptions 
