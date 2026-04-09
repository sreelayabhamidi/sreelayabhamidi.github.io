---
name: Vega Lite Example Project
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 5 Assignment


<vegachart schema-url="{{ site.baseurl }}/assets/json/shape_bars.json" style="width: 100%"></vegachart>

For this graph, I am visualizing the shape of the UFOs with the mean number of seconds that the UFOs were observed. I wanted to see the distribution of the mean observed time that the particular shape of the UFO was observed. I used a nominal coding type for the shape and a quantitative type for the duration in seconds. I used a symlog scale so that the bars can be visualized better. I also went with a color scheme since it was a bit hard to see how many seconds each bar representes using the log scale. I chose the blue purple color scheme because I thought it had a good contrast between the lowest number and the highest number of seconds. For this chart, I grouped the data by shape and only included the mean number of seconds that the UFOs were observed, and I resetted the index. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/country_dropdown.json" style="width: 100%"></vegachart>

For this chart, I am visualizing the duration of UFO in seconds by the year separated by country. I wanted to do this so that I can see a distribution of duration of UFO sightings by year and check for any differences in distribution between each country. I encoded the date as temporal, the duration in seconds as quantitative, and countries as nominal. I used the log scale so that the dots can be visualized better. I did not use a color scheme, but I did use the opacity value, setting it as 1 if the country is selected and 0 if the country is not selected. I colored all the dots in dark green because I thought that the color looked well on the graph. For this graph, I took a subset of the total dataframe consisting of the date, country, and duration in seconds. I made the interactivity selection on the country because I wanted to make the graph clearer. Without the selection, there were too many dots on the graph. After the selection, it became easier to visualize the distribution of the duration per year selected by country. 


## Search The Data & Methods

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/sreelayabhamidi/sreelayabhamidi.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

