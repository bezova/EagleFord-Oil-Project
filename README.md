### Group 3: David Hickman, Austin Coleman, Sal Marino, Darya Rudych, Mauricio Gonzalez

# Project Title: Analysis of Eagle Ford Oil&Gas Production

## Goal Statement
We're a burgeoning exploration company seeking funding for an Eagle Ford Shale asset. Investing in a quality area is our primary concern. We define a quality area as an area that is primarily oil and has high production values. Costs are important and are prohibitive at exorbitant levels. We will perform an analysis of sub-Plays to define areas (sub-plays) of biggest opportunity (think, zip codes for the O&G). Furthermore, sub-plays of high well and operator activity are not only indicative of geologically sound areas, but also have more data on drilling and completion costs   and methods. Once we narrow down to two sub-plays we will look at minimum and maximum potential costs for drilling and completing.

## Data
The dataset we are using has been obtained from an aggregating company Wood Mackenzie. The dataset contains basic information on all the wells drilled and being operated in Eagle Ford play and spans from 2007 to 2017. Specifically, the dataset includes information on:
1. Operators (The companies that have drilled the wells and are now producing oil from them)
2. Geographical information (Where is the well located, latitudes, longitudes etc, county, state, sub-play etc.)
3. Important Well Lifecycle dates (permit, drilling, completion, first production etc.)
3. Important well development costs (capex spent in developing the well and getting it ready for production - rig cost, casing cost, water cost, proppant cost etc.)
4. Information on operational parameters (lateral length, proppant used, water used, fracking stages etc.)
5. Information on initial production (How many BOE was reported on Day 1, first 30 days, first 60 days first 90 days first 180 days and so on.

## Project Objectives Breakdown:
1.	Determine areas with oil as a primary commodity
2.	Identify sub-plays with highest activity (operators, well count)
3.	Identify most profitable sub-plays (i.e. High Total Production (EUR (boe)
4.	Compare sub-plays by Average Drilling Costs and Average Completions Costs
5.	Once top two sub-plays are established, analyze competitor data to get potential minimum and maximum drilling and completion costs.

## Analysis Outline:

## STEP 1: DATA CLEANING 
![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/Code%20snippet.png)

## STEP 2: VISUALIZING THE GEOGRAPHIC & TEMPORAL EXTENT OF THE DATA

### The extent of each sub-play in Eagle Ford
![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/EagleFordSubPlays.png)

### Eagle Ford map by commodity type
![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/EagleFordWells.png)

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/ProdByYear.png)

**Takeaways from visualizations:**
- most of wells in Eagle Ford produce oil
- Black Oil and Karnes Trough are largest sub-plays in Eagle Ford Play
- The production of oil&gas peaked by 2015. In October 2015 the price of crude oil has dropped significantly resulting in the major short-term drop in investment and downward trend in production reflected by the graph. The industry has recovered in 2017. However, the incomplete data for 2017 does not allow us to see whether the production has actually returned to the levels of 2015.

## STEP 3: VISUALIZING ACTIVITY & PRODUCTION BY SUB-PLAY

### Well & Operator count by Sub-play 
![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/ActivityBySubPlay.png)

* Here we can see that **Black Oil**, **Karnes Trough**, and **Edwards Condensate** have the most activity both in terms of number of operators and the number of drills.  Areas with lower wells and activity 

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/EURbySubPlay.png)

* However, Southeast Gas, Southwest Gas, and Maverisck Condensate, that have the lowest well count, have a higher average BOE production. This, in turn, suggest the need for further analysis where the average EUR needs to be normalized by the well count.

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/ProdBySubPlay.png)

* Yet, Southeast and Southwest Gas appear to be rich in gas assets rather than oil assets. As we are interested primarily in oil, the chart suggest we should further focus on Karnes Trough, Edwards Condensate, and Black Oil which have highest average oil production respectively. 

* Since investors usually prefer quicker producing areas, and since Karnes Trough and Edwards Condensate have roughly similar average oil production, we also want to look which of the sub-plays produce more during the first year of production. 

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/AvgFirstYearProd.png)

* This chart suggest that Edwards Condensate and Karnes Trough produce more in the first year, while Black Oil has one of the lowest oil production levels during the first year.

**Takeaway from activity analysis:**
- Edwards Condensate and Karnes Trough sub-plays are more rich in oil assets and are faster to produce high volumes of oil. 
- Now, that we have identified Edwards Condensate and Karnes Trough as the highest producing sub-plays, let's compare the costs across sub-plays to determine what sub-plays will have the higher rate of return on investment. 

## STEP 4: COMPARING THE COSTS BY SUB-PLAY
* Let's first look at the Total Well Cost average by Sub-Play

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/AvgWellCostBySubPlay.png)

* The **Karnes Trough** (purple) and **Edwards Condensate** (green) have roughly same average production costs, sitting around $7.2m and $7.5m respectively.

* Break them out one step further into Drilling and Completions

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/AvgDrilling%26Completions.png)

* Here are the different cost categories and how they contribute to average total well cost. 

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/pareto.png)

* Let's break the costs down further to see differences in all cost categories.

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/CostBreakdown.png)

* Looking at **Edwards Condensate** and **Karnes Trough**, they appear to have relatively same development costs. Karnes Trough has slightly higher "Other Cost", though. (*Dataframe sorted by ***Other Cost***). Southeast Gas has very low proppant and low water, indicating a smaller completion method.

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/Drilling%20Cost%20Per%20Foot.png)

* In terms of drilling costs (other costs and rig costs combined) Maverick sub-play overall looks to be the most expensive area which could be due to the specifics of geological formation it belongs to.  Other Eagle Ford could be wildcats and other areas not benefitting from development mode cost reductions. The Karnes adn Edwards are one of the cheapest places to drill.

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/Completion%20Cost%20Per%20Foot.png)
* Completion costs (water, proppant, and pumping costs) are indicative of completion methods. Historically, completions have increased with time. Our target Sub-Plays are a little above average, but not prohibitively high. Average lateral lengths range from 4,500' to 11,500 ft.
* Overall, the Maverick Oil sub-play is the most expensive area on average. Steering clear of that area is advised.

## STEP 5: ANALYZING ROI RATES BY SUB-PLAY

![alt text](https://github.com/DaryaRudych/EagleFord-Oil-Project/blob/master/CostPerBOE.png)

* When we normalize the costs by production volume, Edwards Condensate is nearly 30,000 (USD) per 1,000 barrels of oil equivalent, while Karnes Trough is almost 50,000 (USD) per 1,000 barrels of oil equivalent.

* This, again, proves that while Edwards and Karnes have similar costs, your dollar goes further in the Edwards.

## Conclusion: (to be edited)
We chose to target the Karnes Trough and Edwards Condensate sub-plays. We anticipate our overall individual well costs to have a minimum of ____ and a maximum of ____. Our drilling cost min and max are respectively ___ and ____. Completions ____ and ____. Our area is significantly derisked not only by the activity in the area, but also our ML model variables contributing to a successful payout.
### Key Limitations/Uncertainities

TBD
