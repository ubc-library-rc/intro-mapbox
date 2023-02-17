---
layout: default
title: Mapbox GL JS
nav_order: 2
parent: Introduction
---

# "Mapbox GL JS is a JavaScript library for vector maps on the Web."

Like Leaflet, [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/guides/) is a collection of JavaScript code that builds customizable maps for web display. What makes Mapbox GL JS so advantageous for web mapping is its use of vector graphics rather than sets of static tile layers. Vectors are graphics composed of points, lines, and polygons. Vector layers are constructed with JavaScript while CSS is responsible for their styling. Mapbox provides vector layer basemaps already styled, but if you're feeling creative you can always make a [custom style](https://docs.mapbox.com/help/tutorials/create-a-custom-style/).

## Tile vs. Vector Layer Maps 
Compared to tile layers, vector layers render on the fly, meaning they load much faster and require less storage capacity. Additionally, web maps utilizing vector graphics are freed from discreet zoom levels since vector layers have no set scales at which they can be rendered. Try zooming slowly in and out of the following two maps. The first is powered by Leaflet and uses tile layers, the second is powered by Mapbox and uses vector graphic layers. Notice how it takes a moment for the tiles to load as you zoom between scales.

 <iframe src="./content/tile-example.html" style="margin-right: 10%; width:110%; height:450px; border:none;"></iframe>
 <br>   
 <iframe src="./content/vector-example.html" style="margin-right: 10%; width:100%; height:450px; border:none;"></iframe>

In the next section we will look more closely at some code and learn what each statement does and how different languages work together to design and execute a map for display in a web browser. To do that, we must first set up a developer environment. 

