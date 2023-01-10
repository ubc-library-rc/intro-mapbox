---
layout: default
title: Clustering
nav_order: 5
parent: Build a Webmap
---
# Build a Cluster Map of Vancouver Parks

Now that you are familiar with the boilerplate code and how it works, the next step is adding and styling data of our own. Below is a preview of the web map we will create using the boilerplate as a basemap. (Zoom in on the iframe for map to appear)

<iframe src="./cluster-map.html" style="width:950px; height:440px; border:none;"></iframe>
<!-- https://github.com/ubc-library-rc/intro-mapbox/blob/5b582ed327ce2fb6a4a04db4e26ddb6baa819271/content/cluster-map.html -->
    

   <br> 
*1*{: .circle .circle-purple}
Open `boilerplate.html` in your code editor. Replace YOUR_ACCESS_TOKEN_HERE with your access token. We will be adding to the `< script>` block using javascript.
```html
<html>

<head>
    <title>Boiler Plate Code</title>
   <link href="https://api.mapbox.com/mapbox-gl-js/v2.12.0/mapbox-gl.css" rel="stylesheet">
    <script src="https://api.mapbox.com/mapbox-gl-js/v2.12.0/mapbox-gl.js"></script>
</head>

<body>
    <div id='map' style='width: 700px; height: 600px; margin-left: 23%;'></div>
    <script>
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN_HERE'; //replace with your access token
        const map = new mapboxgl.Map({
            container: 'map', // container ID
            style: 'mapbox://styles/mapbox/streets-v12', // style URL try other styles from https://www.mapbox.com/gallery/
            center: [-123.11738086752482, 49.25090077610571], // starting position [lng, lat]
            zoom: 10, // starting zoom
            projection: 'globe' // display the map as a 3D globe
        });
        
        //Navigation Controls
        map.addControl(new mapboxgl.NavigationControl());
    </script>
</body>

</html>
```
If you installed the Live Server extension to Visual Studio Code, in the blue ribbon at the bottom of your code editor there should be an option to "Go Live." Click "Go Live" to open the boilerplate basemap in a web browser. 

<!--- ![Go Live](./images/go-live_20220109.png) --->
<br>
*2*{: .circle .circle-purple} Below Navigation Controls add map.on('load', () => { 


        });

```html
<html>
<head>
    <title>Boiler Plate Code</title>
    <link href="https://api.mapbox.com/mapbox-gl-js/v2.12.0/mapbox-gl.css" rel="stylesheet">
    <script src="https://api.mapbox.com/mapbox-gl-js/v2.12.0/mapbox-gl.js"></script>
</head>

<body>
    <div id='map' style='width: 700px; height: 600px; margin-left: 23%;'></div>
    <script>
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN_HERE'; //replace with your access token
        const map = new mapboxgl.Map({
            container: 'map', // container ID
            style: 'mapbox://styles/mapbox/streets-v12', // style URL try other styles from https://www.mapbox.com/gallery/
            center: [-123.11738086752482, 49.25090077610571], // starting position [lng, lat]
            zoom: 10, // starting zoom
            projection: 'globe' // display the map as a 3D globe
        });
        
        map.addControl(new mapboxgl.NavigationControl());

        //
        map.on('load', () => { 


        });

    </script>
</body>

</html>
```




map onload function --> everything inside this function will render. 1) add source 2) add layers

add source (right now only works when source is local)

explain cluster option and zooms

add circle layer; explain steps -- copy paste this one
for symbology - participants can pick hex code for color 

add point count to cluster


display unclustered points when zoomed in sufficiently

add pop ups to unclustered points on click with properties, such as name etc. 
