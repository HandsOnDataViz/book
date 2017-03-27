# Normalize Data to Create Meaningful Polygon Maps
*By [Jack Dougherty](../../introduction/who.md), last updated March 26, 2017*

** TO DO **

Raw data - absolute values

(example: number of unemployed people in US States), hard to compare across regions of different size (FIND example of two states with similar geographic area but very diff populations)

Normalized data -- represented on a standard scale (aka standardized data), often in one of two ways:
- normalized by total (example: income per capita)
- normalized by area (example: population per square mile)
  - as “per capita” or “percent of total”
examples:
- percent unemployed in US by state  (= unemployed/population of state)
- percent of total US unemployed by state(= unemployed in each state / total unemployed in US)

Normalized data makes for easier comparisons across regions of different size, but may hide very low raw data (example: high unemployment rate in small area may be based on small population)

Your data table looks like this:
State	Population	Square Miles
A
B
C
…
Total

What are TWO meaningful ways to normalize this data?

CORRECT
Normalized by area: Population per square mile by state (calculate = pop / square miles)
Normalized by total: Percent of total US population by state (calculate = state pop / total US pop)
