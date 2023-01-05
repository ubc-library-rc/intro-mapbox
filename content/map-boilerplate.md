---
layout: default
title: Boilerplate Code
nav_order: 1
parent: Build a Webmap
---

## Basemap 
explain 'basemap.' explain boilerplate code concept.


To Do
{: .label .label-green } 
Navigate into your "intro-mapbox" folder and locate the file ```boilerplate.html```. Replace ```PASTE_YOUR_ACCESS_TOKEN_HERE``` with your Mapbox Access Token generated earlier in this workshop. Then, save your HTML file and open it in your web browser. You may need to "right-click" and "open with" your browser of choice. You should see an interactive basemap centered on Vancouver, Canada. Use the controls to zoom in and out and pan around your web map.

     
## Basemap Code 
Now Let's look at what's powering this map. Navigate back to your "intro-mapbox" folder and right-click ```boilerplate.html``` to open it with your source code editor. Your code will look like this: 

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
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN'; //replace with your access token
        const map = new mapboxgl.Map({
            container: 'map', // container ID
            style: 'mapbox://styles/mapbox/streets-v11', // style URL try other styles from https://www.mapbox.com/gallery/
            center: [-123.11738086752482, 49.25090077610571], // starting position [lng, lat]
            zoom: 10, // starting zoom
            projection: 'globe' // display the map as a 3D globe
        });

    </script>
</body>

</html>

```


<br>
The HTML document is split into two main sections: the <code>head</code> and the <code>body</code>. Each of these sections are contained within opening < tags > and closing </ tags >. Notice that because the document is in HTML format, everything is contained within the html tag.     


```html
<html>
    <head> 
        The stuff inside the head is the metadata for your browser about the document.    
        Inside the head are things like the document’s title - in this case “Web Map” -     
        so that it can used for things like being displayed in your browser’s tab.    
        Additionally, there are links to the source code for Mapbox’s JavaScript and CSS rules.    
        If you copy either one of those links and paste it in a new tab in your browser,    
        you’ll see a lot of raw code. By linking to the source, we avoid having to carry this text     
        into our own document, while also being assured that the code we’re using is up-to-date.
    </head>

    <body>  
        The body contains what you see formatted in your browser. In the code above, the body     
        contains a directions for rendering and displaying an interactive map centered on Vancouver.    

        <div> This element states how tall and how wide the map should be on the screen. </div>    

        <script> 
        //Included in the body is a block of JavaScript that loads the map on the screen.    
        //Continue to the next section for a better understanding of this script... 
        </script>

    </body>
</html>
```
