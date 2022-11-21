---
layout: default
title:  Map Properties 
nav_order: 2
parent: Build a Webmap
---
## A closer look at the script
```html
    <script>
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN_HERE'; 
        const map = new mapboxgl.Map({
            container: 'map', 
            style: 'mapbox://styles/mapbox/streets-v11', 
            center: [-123.11738086752482, 49.25090077610571], 
            zoom: 10, 
            projection: 'globe' 
        });
        map.on('style.load', () => {
            map.setFog({}); // Set the default atmosphere style
        });
    </script>

```

break down each element - one by one explain and change (explain how to save and load/refresh now)


### Container 

### Style 
// style URL try other styles from https://www.mapbox.com/gallery/
[styles](https://docs.mapbox.com/api/maps/styles/#mapbox-styles)

### Center
// starting position [lng, lat]


### Zoom 
// starting zoom

### Projection
// display the map as a 3D globe


### initialize 
// Set the default atmosphere style

