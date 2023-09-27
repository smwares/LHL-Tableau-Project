# Final-Project-Tableau

# Table of Contents
1. [Project/Goals](#projectgoals)
2. [Process](#process)
3. [Results](#results)
4. [Challenges](#challenges)
5. [Future Goals](#future-goals)
6. [References](#references)

## Project/Goals
Project focuses on the Canadian housing market and looking at past trends. The main goal is to answer a set of questions that are relevant to finding important trends and observations.

## Process
1. Review each file that was provided
2. Parse through the JSON file (weekly_earnings.json) and create a CSV file as Tableau has a more difficult time handling data in JSON format (weekly_earnings.ipynb)
3. Import each of the data sets as data sources into Tableau
4. Format the data types as required to ensure proper categorization and for analytical purposes
5. Link the data sets together (housing price index table was chosen as the primary table)
6. Create visualizations on sheets that are relevant to each question that is being asked
7. Create calculated fields, parameters, filters (static and/or interactive), animations, etc as required for each visualization
8. Combine visualizations, filters, etc on dashboards, one dashboard per question
9. Create a single story containing all the dashboards

## Results
### Option 1 - Housing Price Trends

- Show the trend of house prices across Canada in the last 40 years (table housing_price_index). (D1)
    - 2 line graphs (S1)
        - housing price index vs time
        - % difference in index value vs time
    - filter for date level
    - colored to show above and below 0%

- Compare the trend after 2005 with actual benchmark prices in table real_estate_prices to see if there are any differences. (D2)
    - 2 line graphs (S2.1)
        - housing price index vs time
        - real estate benchhmark prices vs time
    - 2 line graphs (S2.2)
        - % difference in housing price index vs time
        - % difference in real estate benchhmark prices vs time
    - filter for date level

- Compare this trend with the trend of office prices. Which one is getting more expensive, faster? (D3)
    - 1 multi-line graph (S3.1)
        - housing and office price index vs time
    - 2 line graphs on one sheet (S3.2)
        - % difference in housing price index vs time
        - % difference in office price index vs time
        - filter for date level

- Create a heatmap of Canada with current house prices for each available district. (D4)
    - filtered to show September 2020 average
    - 1 heat map with squares of varying sizes and colours (D4.1)
    - 1 symbol map with circles of varying sizes and colours (D4.2)
    - 1 packed bubble chart showing top 5 most expensive locations (D4.3)
    - 1 packed bubble chart showing top 5 least expensive locations (D4.4)

- Are the price differences between different districts increasing? (D5)
    - 2 line graphs (S5)
        - standard deviation of house prices vs time
        - % difference in house prices vs time
    - filter for date level
    - colored to show above and below 0%

- Compare the trend of house prices with earnings. \*In case you want to plot monthly salary, be aware that the earnings value is per week. (D6)
    - 1 multi-line graph (S6.1)
        - house prices and earnings vs time
    - 2 line graphs (S6.2)
        - % difference in house prices vs time
        - % difference in weekly earnings vs time
        - filter for date level

- Did people spend more of their earnings in 2014 than they did in 2001? (D7)
    - 1 bar graph (S7)
    	- CPI vs time
    	- 2001 and 2014 CPI labeled

- There were several economic crises in the world in the last 40 years, including these four: Black Monday (1987), Recession (early 1990s), dot com bubble (2000 - 2002), Financial crisis (2007 - 2009). Show the effect of these crises on earnings, house prices, office prices, house constructions and consumer index. (D8)
	- 5 line graphs (S8.1)
	    - weekly earnings vs time
	    - house prices vs time
	    - office prices vs time
	    - number of house construction completions vs time
	    - consumer index vs time
	- 5 line graphs (S8.2)
	    - % difference in weekly earnings vs time
	    - % difference in house prices vs time
	    - % difference in office prices vs time
	    - % difference in number of house construction completions vs time
	    - % difference in consumer index vs time
	- filter for date level

- Plot consumer_index together with housing_price_index and fit the regression line between them. Can we predict consumer_index from the housing_price_index? (D9)
    - 1 scatter plot (S9)
    	- HPI vs CPI
    	- linear regression line with 95% confidence interval bands

- Try to find an interesting pattern, trend, outlier, etc. from the data used in the above questions. (D10) HINT : Double check all units in the table before any comparison.
	- investigate housing prices rates for the most expensive cities after 2015
	- 1 bar graph (S10.1)
		- average home price for each region
		- filtered by date (each graph is a monthly average)
		- colour graded based on price (red is higher, blue is lower)
	- 1 bar graph (S10.2)
		- % change in average home price for each region
		- filtered by date (each graph is a change in the monthly average)
		- colour graded based on price criteria from graph on sheet S10.1
	- 5 area charts (S10.3)
		- % change in average home price for each region vs time

## Challenges
- Challenge of dealing with a JSON file:
	- JSON file was imported into Tableau at first
	- Due to unconventional formatting of the file (i.e. combination of lists in dicts and vice versa) led to complexities
	- Issue was resolved by using Python to create a CSV file containing relevant information from the JSON file

- Challenge of selecting appropriate visualizations for each question
	- Choose base line visualization type based on the question asked
	- Modify visualizations in ways that would help in answering the question better
	- Modify visualizations further in ways that would help the audience understand better as well
		- Since this is subjective, it boils down to trial and error in several instances where different settings, graph types, colours, etc are modified until it "looks good"

- Challenege of creating calculated fields and parameters
	- Re-review course material and visit other resources that would assist in building parameters relevant to the project
	- Thoroughly examine available calculations in Tableau prior to creating a custom one (this is to avoid re-inventing the wheel essentially)

- Challenge of incorporating updated housing_price_index file into the project part-way through
	- Initial file provided was a duplicate of the consumer index one
	- Using updated file broke many associations and therefore visualizations
	- After attempting to remedy the broken associations, started a new Tableau file altogether as the software was not willing to co-operate

## Future Goals
- Expand on data sets that were provided. For instance, the weekly earnings did not cover earnings statistics before 2001, even though Statistics Canada has this information available for use.
- Use data sets that were outside the scope of this project. Some additional data sets that may be relevant in understanding housing price trends would be population growth rates, immigration/emigration rates, employment/unemployment rates and crime statistics.
- Focus specifically on a few cities (such at Toronto and Vancouver) as these are some of the largest metropolitan areas in the country.
- Build predictive models based on additional and expanded datasets

## References
3d-house-plans_1048-4704.avif - 3D House, Plans - <a href="https://www.freepik.com/free-photo/3d-house-plans_1020519.htm">Image by kjpargeter</a> on Freepik