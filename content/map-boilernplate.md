---
layout: default
title: Map Boilerplate 
nav_order: 1
parent: Hands On
---

## Boiler plate code
explain what this is - remix from leaflet tutorial

```html
<html>
<head>
    <title>Boiler Plate Code</title>
    <script src='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.js'></script>
    <link href='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.css' rel='stylesheet' />
</head>

<body>
    <div id='map' style='width: 700px; height: 600px; margin-left: 23%;'></div>
    <script>
        mapboxgl.accessToken = 'pk.eyJ1IjoibGNyYW5kYWxsb3JhIiwiYSI6ImNraGM2d2EwYjA2MXEzMnBocmdscmwzb2YifQ.qLzdLjST_taS3roJDpdDjg'; //replace with your access token
        const map = new mapboxgl.Map({
            container: 'map', // container ID
            style: 'mapbox://styles/mapbox/streets-v11', // style URL try other styles from https://www.mapbox.com/gallery/
            center: [-123.11738086752482, 49.25090077610571], // starting position [lng, lat]
            zoom: 10, // starting zoom
            projection: 'globe' // display the map as a 3D globe
        });
        map.on('style.load', () => {
            map.setFog({}); // Set the default atmosphere style
        });
    </script>
</body>
</html> 

```