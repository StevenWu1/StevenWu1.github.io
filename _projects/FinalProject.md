---
name: Crime in DC Final Project
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/DC.png
description: An interactive data visualization article aimed to explore reported crime in Washington, DC. where Readers can explore crime by offense, ward, shift, and month.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Crime in Washington, DC: Patterns and Insights
**Authors:** Steven Wu

## Central Visualization: Crime map and Ward Offense Counts
The following plot was generated with a URL link to the data
<vegachart schema-url="{{ site.baseurl }}/assets/json/crime_map.json" style="width: 100%"></vegachart>

This main visualization shows reported crimes across DC. Each point represents a reported crime, colored by offense type. Users can filter by selecting a specific offense from the dropdown menu. The barchart attached also shows the number of offenses in each ward broken down by the shift when the crime was committed. This visualization allows readers to quickly see which areas experience more crime, what type of offenses are most common in each ward, and when the type of offense is generally committed.


## Contextual Visualization 1: Crime by Month and Offense Type
The following plot was generated with a URL link to the data
<vegachart schema-url="{{ site.baseurl }}/assets/json/crime_stacked_month_chart.json" style="width: 100%"></vegachart>

This stacked bar chart shows the number of crimes per month, broken down by offense type. Using tool tips, hovering over each bar also reveals the exact count. Readers can use this visualization to identify season trends and when specific crimes spike in occurance throughout the year, helping contextualize crime patterns over time.

## Contextual Visualization 2: Crime by Ward and Shift
The following plot was generated with a URL link to the data
<vegachart schema-url="{{ site.baseurl }}/assets/json/crime_dashboard.json" style="width: 100%"></vegachart>

The last visualization is a dashboard containing a heatmap of crime incidents by ward and police shift with a linked bar chart showing offense breakdown. Readers can click on the heatmap square to filter the bar chart, allowing exploration of which offenses occur most during different shifts in different wards. This provides more detailed break down compared to the map visualization.

## Data and Analysis
The visualizations were created from public data. Specifically, the data used contains every reported crime from 2024 reported in the District of Columbia.



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/crime-incidents-in-2024" text="The Data" %}
</div>


<div class="right">
{% include elements/button.html link="https://github.com/StevenWu1/StevenWu1.github.io/blob/main/python_notebooks/FinalPart31.ipynb" text="The Analysis" %}
</div>

