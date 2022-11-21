---
layout: default
title: Customizing Properties 
nav_order: 2
parent: Build a Webmap
---


```<body>
    <div id='map' style='width: 700px; height: 600px; margin-left: 23%;'></div>
    <script>
        mapboxgl.accessToken = 'PASTE_YOUR_ACCESS_TOKEN_HERE'; //replace with your access token
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
```

### Container 

### Style 

(styles)[https://docs.mapbox.com/api/maps/styles/#mapbox-styles]

### Center


### Zoom 


### Projection

