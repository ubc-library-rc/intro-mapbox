---
layout: default
title:  Parameters 
nav_order: 2
parent: Build a Webmap
---
## A closer look at the script: Map Parameters
<br>
This section will break down the javascript responsible for containing, styling, and making your map interactive. We will modify parameters of the boilerplate's script to explore how customizable even the basemap can be. The definitions that follow are drawn from Mapbox's [API reference](https://docs.mapbox.com/mapbox-gl-js/api/), which offers a comprehensive description of map properties and options.    

Return to the boilerplate basemap open in your web-browser. Because we will be working back and forth between the browser page the code editor it's helpful to arrange your computer screen(s) in a way where you can either see both windows at once or are able to toggle between the two. This way, every time you modify the html code you can see the changes by refreshing the browser page. You'll also want to have this workshop page accessible. 


    
```html
    <script>
        mapboxgl.accessToken = 'YOUR_ACCESS_TOKEN_HERE'; 
        const map = new mapboxgl.Map({
            container: 'map', 
            style: 'mapbox://styles/mapbox/streets-v12', 
            center: [-123.11738086752482, 49.25090077610571], 
            zoom: 10, 
            projection: 'globe' 
        });
        map.addControl(new mapboxgl.NavigationControl());
    </script>
```
<br>




### Map Object  
```js
const map = new mapboxgl.Map({

});
```
Below your access token is the map object. Contained within the ```map``` object are various methods and properties such as container, style, center, zoom, and projection. Mapbox GL JS takes the values you set for these options and renders the map object as specified on your screen. 
<br>    
<br>     

### Container 
```js
container: 'map'
```
The ```container``` option specifies an the HTML element within which the map will be rendered.
<br>    
<br>   

### Style 
```js
style: 'mapbox://styles/mapbox/streets-v12'
```
The ```style``` option indicates the style of your basemap. While you can create your own map styles in Mapbox Studio, there are an array of Mapbox styles available for you to choose from. Look through the [gallery](https://www.mapbox.com/gallery/) for visual reference. Then replace the style in your boilerplate code with a [style URL](https://docs.mapbox.com/api/maps/styles/#mapbox-styles). Save your code and refresh your browser page. The map should now render with your chosen style. 
<br>  
<br>  

### Center
```js
center: [-123.11738086752482, 49.25090077610571]
```
The ```center``` option specifies the geographic centerpoint of the map when it first loads. The parameter is in decimal degrees in the format [longitude, latitude]. Go to [Google Maps](https://www.google.com/maps/@41.3294462,57.6083804,3z) and navigate to any location in the world. Right click to copy the coordinates to your clipboard. Paste them into your boilerplate code. Make sure to switch the positions of latitude and longitude to match the input format noted above. Save your code and refresh your browser page. The map should now be centered on a new location. 
<br>
<br>

### Zoom 
```js
zoom: 10
```
While your map can interactively zoom between discreet levels, the ```zoom``` option specifies the initial scale of your map. Mapbox zoom levels go from 0 to 22, with 22 being the most zoomed in or largest scale. Try changing the zoom level. Save your code and refresh your browser page to see your changes. 
<br>
<br>
### Projection

```js
projection: 'globe'
```
The ```projection``` option sets the projection your map will be rendered in. The boilerplate projection will display the map as a 3D globe if you zoom out enough. Take a look at the [supported projections](https://docs.mapbox.com/mapbox-gl-js/style-spec/projection/) and try a few out. 
<br>
<br>

### Navigation Controls    
```js
map.addControl(new mapboxgl.NavigationControl());
```
The ```addControl()``` function adds buttons for zooming in and out. You can also zoom using your fingers on a track pad or the scroll wheel of a mouse. Note that this function is outside the map object and not required for your map to load or be interactive. 

Now that we are familiar with the script that builds a basemap it's time to add our own data to it. 



