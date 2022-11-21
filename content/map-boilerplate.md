---
layout: default
title: Boilerplate Code
nav_order: 1
parent: Build a Webmap
---

## Map Boilerplate
explain what this is - remix from leaflet tutorial


{: .label .label-green } To Do
DOWNLOAD FIRST 
Navigate into your "mapbox-intro" folder and locate the file ```boilerplate1.html```. Right click and open it with your preferred internet browser. You should see an interactive map like this:
     
<iframe src="./content/boilerplate1.html" style="width:100%; height:400px; border:none;"></iframe>
     
    
Now Let's look at what's powering this map. Navigate back to your "mapbox-intro" folder and right-click ```boilerplate1.html``` to open it with your source code editor. 
Your code will look like this: 

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
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN_HERE'; //replace with your access token
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

To Do 
{: .label .label-green } Replace ```PASTE_YOUR_ACCESS_TOKEN_HERE``` with your Mapbox Access Token generated earlier in this workshop. Then, save your HTML file and open it in your web browser. You may need to "right-click" and "open with" your browser of choice. You should see an interactive basemap centered on Vancouver, Canada. Use the controls to zoom in and out and pan around your web map.


## Making Sense of the Code
Let's look at what is making this file work using our code editor. The HTML document is split into two main sections: (1) the <code>head</code> and the (2) <code>body</code>. Each of these sections are contained within opening and closing tags.
```
<head> some stuff </head>
<body> some other stuff </body>
```

### Head
The stuff inside the <code>head</code> is the metadata for your browser about the document. Inside the <code>head</code> are things like the document’s title - in this case "Web Map" - so that it can used for things like being displayed in your browser's tab. Additionally, there are links to the source code for Mapbox's JavaScript and CSS rules:     
```html
 <script src='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.js'></script>
    <link href='https://api.mapbox.com/mapbox-gl-js/v2.10.0/mapbox-gl.css' rel='stylesheet' />
```

If you copy either one of those links and paste it in a new tab in your browser, you’ll see a lot of raw code. By linking to the source, we avoid having to carry this text into our own document, while also being assured that the code we're using is up-to-date.

### Body 
The <code>body</code> is the container for the what you see formatted in your browser. Here, you have an HTML container for your map. 
```
<div id='map' style='width: 700px; height: 600px; margin-left: 23%;'></div>
```
The access token you already know about.
   
Also included in the <code>body</code> is a script that loads the map to your page.  
```js
var map = new mapboxgl.Map({
            container: 'map', // container ID
            style: 'mapbox://styles/mapbox/streets-v11', // style URL try other styles from https://www.mapbox.com/gallery/
            center: [-123.11738086752482, 49.25090077610571], // starting position [lng, lat]
            zoom: 10, // starting zoom
            projection: 'globe' // display the map as a 3D globe
        });
        map.on('style.load', () => {
            map.setFog({}); // Set the default atmosphere style
        });
```

The first line is our map variable. A JavaScript variable is something that holds values, and our <code>map</code> variable holds values for the initial starting view location and zoom level of the loading map. Naming the <code>map</code> variable using the <code>const</code> declaration means that while the properties (eg  style, center, zoom, and zoom) can be changed, the variable map cannot be reassigned to another object??. It also means --> initiialized 

Next we will adjust our map's properties.



