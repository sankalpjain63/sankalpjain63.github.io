---
name: Lights, Camera, Action
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: An interactive analysis of shooting locations in New York City.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## Light, Camera, Location aanndd….Action!!
The art of filmmaking is exciting and challenging. From saying the four (in our case five) magical words to assembling costumes, locations, script, acting, directing and everything that lies in between it takes decades if not years to master. In our analysis today, we will be looking at one aspect mainly the shoot location and some formal permissions and procedures that lie in this realm. Our dataset is collected and maintained by the New York State Department’s Mayor’s Office of Media and Entertainment (MOME). Our dataset is in the public domain and has 10.8 downloads, 13.6K rows, and 14 columns where each row is a film permit giving us information about the location, borough, date and time of the permit, etc. We have created our graphs for both the main as well as the contextual visualizations.

##### This project displays the usage of Python+altair+vegalite to your GitHub repository.
##### In this Visualization 1 is a generic one and for Visualization 2 a dropdown is added for interactivity so that the user can change the city according to their preference.

# Visualization 1 
##### Using a line chart, visualize the average square footage of buildings constructed from 1800 to 2022
This visualization aims to examine the changes in the average size of buildings over time, as the reduction of open spaces has resulted in smaller buildings. 
To achieve this, we utilized temporal encoding for the X-axis to map the year values and calculated the average square footage for the Y-axis from the data frame. 
We removed rows with empty values in the year constructed and square footage fields and filtered the data to only include buildings constructed between 1800 and 2022. 
We utilized the ".properties" trait in Altair to encode the width and height of the chart. The original color of the line chart is blue. There is no plot overlap from homework 9.
<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz1.json" style="width: 100%"></vegachart>


# Visualization 2
##### Interactive bar chart shows the total building square footage by status for each city in the dataset. Users can filter for specific cities.
The objective of this visualization is to gain insight into the utilization of building space in various cities of Illinois, as measured in square footage. 
We utilized ordinal encoding on the X-axis to map building status and calculated the sum of square footage for the chosen city on the Y-axis. 
We discovered an alternative plotting method using Altair's chart function, which allowed us to incorporate interactivity using the ".from_dict" trait (source citation provided). 
However, we encountered difficulty displaying empty building status categories on the X-axis for cities with only one type of building status-related data. 
Additionally, due to Altair's limitations on interactivity for datasets with more than 5000 rows, we created a subset of the original data frame. 
To validate interactivity, we created a pivot table using pandas to confirm the total square footage values for each city and building status type. 
Ultimately, this visualization may be useful to the real estate industry in creating city blueprints. There is no plot overlap from homework 9.
<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz2.json" style="width: 100%"></vegachart>

# Challenges
While plotting the graphs and uploading to GitHub we faced numerous challenges as the file size was larger than supported. Hence we have included specific code like alt.data_transformers.enable(‘default’, max_rows=None) and also made use of nbviewer for viewing the data uploaded in Git Hub. This allows us to view data. At the same time working with Altair was challenging as there is minimal support and the library is basic. Interactivity is hard to achieve but it is interesting to work with.

# Conclusion
Overall, the use of data from the Film Permits dataset has allowed us to build powerful visualizations that make it easier to explore and understand trends in the film industry in New York City.

## Search The Data & Methods


<!-- these are written in a combo of html and liquid --> 
 
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sankalpjain63/sankalpjain63.github.io/blob/main/python_notebooks/ASSIGNMENT10.ipynb" text="The Analysis" %}
</div>
