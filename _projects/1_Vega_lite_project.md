---
name: IS 445 DATA VIZUALIZATION
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework - 10, Group - 5
## Team Members: 
#### Aatmic Tiwari
#### Sankalp Jain


##### This assignment displays usage of Python+altair+vegalite to your github repository.
##### In this assignment there are 2 visualizations. This assignment is NOT a continutaion of Homework 9. Visualization 1 is a generic one and for Visualization 2, we have added a dropdown as an interactivity so that the user can change the city according to their preference.

# Visualization 1 
##### Using a line chart, visualize the average square footage of buildings constructed from 1800 to 2022
The goal of this visualization is to examine the changes in the average size of buildings over time, as the reduction of open spaces has resulted in smaller buildings. 
To achieve this, we utilized temporal encoding for the X-axis to map the year values and calculated the average square footage for the Y-axis from the dataframe. 
We removed rows with empty values in the year constructed and square footage fields and filtered the data to only include buildings constructed between 1800 and 2022. 
We utilized the ".properties" trait in Altair to encode the width and height of the chart. The original color of the line chart is blue. There is no plot overlap from homework 9.
<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz1.json" style="width: 100%"></vegachart>



# Visualization 2
##### Interactive bar chart shows total building square footage by status for each city in dataset. Users can filter for specific city.
The objective of this visualization is to gain insight into the utilization of building space in various cities of Illinois, as measured in square footage. 
We utilized ordinal encoding on the X-axis to map building status and calculated the sum of square footage for the chosen city on the Y-axis. 
We discovered an alternative plotting method using Altair's chart function, which allowed us to incorporate interactivity using the ".from_dict" trait (source citation provided). 
However, we encountered difficulty displaying empty building status categories on the X-axis for cities with only one type of building status-related data. 
Additionally, due to Altair's limitations on interactivity for datasets with more than 5000 rows, we created a subset of the original dataframe. 
To validate interactivity, we created a pivot table using pandas to confirm the total square footage values for each city and building status type. 
Ultimately, this visualization may be useful to the real estate industry in creating city blueprints. There is no plot overlap from homework 9.
<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz2.json" style="width: 100%"></vegachart>


## Search The Data & Methods


<!-- these are written in a combo of html and liquid --> 
 
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sankalpjain63/sankalpjain63.github.io/blob/main/python_notebooks/ASSIGNMENT10.ipynb" text="The Analysis" %}
</div>
