---
layout: page
title: Homework 5
permalink: /hw5/
---
## Building Inventory Visualizations

**[Link to the Dataset](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)**
**[Link to my Python Notebook](https://github.com/jacobbirger/jacobbirger.github.io/blob/main/hw5analysis.ipynb)**

### Plot 1: Total Square Footage by Building Status

<vegachart schema-url="./plot1.json" style="width: 100%"></vegachart>

In this first plot I am visualizing the total aggregated square feet acroos the different building statuses. The x-axis is using a nominal encoding for the building status. The y-axis is using a quantitative encoding to represent the total square feet. I chose the set2 categorical color scheme for the bars as a way to cleary differentiate the nominal categories but without creating or implying any sequential hierarchy. I also performed data transformations using Pandas before the ploting by first filtering out the invalid entries in the 'Year Acquired" column and then grouping the entire dataframe by 'Bldg Status' to easily calculate the total square feet in each category.

### Plot 2: Square Footage vs. Year Acquired

<vegachart schema-url="./plot2.json" style="width: 100%"></vegachart>

For the second plot, I am visualizing the relationship between the acquistion year for a building and it's square footage. For both the x-axis which was "Year Acquired" and the y-axis which was "Square Footage" I used quantitative encodings by passing the raw CSV URL into Altair and then restricting the domain for the x-axis from 1750 to 202. To make the plot interactive, I added an interval selection brush with tooltips. The brush makes it so the user can click and drack as a way to select specific clusters of buildings which retain their set2 coloring while making all the other point gray which helps make the visualization clearer since it allows the user to isolate the data points they want in a highly dense area of the scatter plot. The tooltips are able to provide the exact info when hovering without actually cluttering the entire graph with text.