#Lab 06: Web Mapping with D3.js

##Part I. D3.js Mapping

**Option #1** 6.5pts.

Follow the lesson instructions and submit either a proportional symbol map or choropleth map using the provided data.

**Option #2** 7.5pts.

Experiment with a new geography and map a new or different dataset. Note that for projecting specific countries or US states you'll need to change the projection parameters. Specifically, there are two additional D3 methods you'll need to use. Consider these examples:

To center your map on the state of Colorado:

```javascript
var projection = d3.geo.albers()
        .center([0, 39.07])  // centering the project with lat value
        .rotate([105.42,0])  // rotating the earth to lon value
        .scale(7000)
        .translate([width / 2, height / 2]);
```

There are also standard parallels you can use within an Albers projection. To center your map on France:

```javascript
var projection = d3.geo.albers()
        .center([0, 46.2])
        .rotate([-2, 0])
        .parallels([43, 62])
        .scale(2500)
        .translate([width / 2, height / 2]);
```

Getting the projection parameters right for various projections can be a challenge. This stack overflow question, [d3js - how to set Albers projection properly?](http://stackoverflow.com/questions/13303371/d3js-how-to-set-albers-projection-properly), may help. Consult examples and ask me for help!

Also, consider remaking a map previously made with a different web mapping technology (QGIS, Leaflet) with D3.js instead. The bi-variate power plant data from MAP672 would work well!

Or consult examples referenced within the lesson and see if you can get one working within your local development environment.

## Part II. Your final project's topic, objectives, and data (2.5pts)

It's time to start thinking deeply about your final map project for MAP673. Using the process covered in Module 05, the deliverable for this week will include three pieces:

1. the **map topic** and/or geographic phenomena your map will explore
2. an articulation of the **map's objectives** and **user needs**
3. your **data source** and (at least a sample of) the data required to meet the map's objectives

Write thorough descriptions/answers to the following within some text-based format of your choice, and submit through your GitHub account.

### Topic and/or geographic phenomena your map will explore

What are you mapping? Briefly describe the topic and the geography the map intends to represent. Also, provide a tentative title (and possibly a subtitle) for you map. Remember that good titles, while being provocative and potentially fun, also tell a user three things: 1. what is being mapped, 2. where it's being mapped, and 3. when the phenomena occurred.

### Map objectives and user needs

* Begin by answer the question,  "Why are you making this map?"
* Consider your own positionality with respect to the map and tell us why you are making it and what you want to get out of it.
* Create a brief user persona and tell us what this persona(s) will get out of the map. Why are they using it? How would you characterize this user in terms of their expertise and motivation (i.e., novice/public, average, expert/domain-specific)
* Imagine a scenario about how the user may use the map. It need not cover all potential use case scenarios, but it should describe some potential action the user will engage in to meet their objective (i.e., filtering the data, searching for an address, changing the attribute through a dropdown menu)

## Data source

This one is really important. Sometimes we have great goals and ideas for a map. But if we can't (somewhat easily) get the data ... the map is going nowhere. I need to see that you have access to the data, or at least some ugly data that we can consider strategies for refining and cleaning up.

Provide me with 1. your anticipated data source (URL, etc) and 2. a small sample of the data (e.g., CSV, GeoJSON, Shapefile, or within a database)

## Part III. Anticipating your technology stack

While your answer to this question need not be definite at this point, briefly describe the "technology stack" you anticipate using for your final map. This should include:

* data and information processing tools, web-based or desktop (i.e., QGIS, [MapShaper](http://www.mapshaper.org/))
* the format you'll use to store your data (i.e., flat files such as CSV or GeoJSON, database technology such as CartoDB)
* the JS libraries you anticipate using or need (include any relevant plugins)
* other relevant web technologies you'll be using (i.e., HTML, CSS)
* the hosting platform you intend to use to host your map (i.e., GitHub pages, your own web server)

Note: This is a draft of the information we'll want to include in your final map writeup. While informative to curious users of your map, it also looks good to employers and clients in terms of demonstrating your expertise in the world of open source web mapping!
